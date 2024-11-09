<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241108`](#odoo160-20241108)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241108`](#odoo170-20241108)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241108`](#odoo180-20241108)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:7e05c6101bf41f56210d29138cf18fc86da7670fe5173d3ca00b35b112bf70b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:db19636c29eab488aba105500824ea2d8afb95d06687629720e7bfa9fc6665c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588490203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4f441875297c0ec2a967b49173679afa599af71e253d102a1d61c5d20c2c31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3debe5503c9c852161c15d7d751083b9c60af9aa437565d402ff8eba39baa5`  
		Last Modified: Fri, 08 Nov 2024 22:02:06 GMT  
		Size: 223.6 MB (223576785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11adc5c286096faeb74ae0d4f96df7e9600a908bd76abeb98cf5c8ec36204ce2`  
		Last Modified: Fri, 08 Nov 2024 22:01:58 GMT  
		Size: 2.5 MB (2494352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897dcd9121b2909bba8661d89fff856bae0bb06a92c03f1904c863792717aa03`  
		Last Modified: Fri, 08 Nov 2024 22:01:58 GMT  
		Size: 468.9 KB (468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb7aa2509151d095324336eb754d38549772216f95d094ac57bc2dcbcbb3ac5`  
		Last Modified: Fri, 08 Nov 2024 22:02:09 GMT  
		Size: 330.5 MB (330518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9c8396630a7f616cb548c893817e8470992a98d69a5bc96aeeec762e05e669`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63da9aa4e752a6795833f2de769df468b68a75d4e230446c73b37e937ffac1d`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21cd94a439fa6c6a7b9deb60c143147b98dc796b69fdb6d756a3ad8020a2e3`  
		Last Modified: Fri, 08 Nov 2024 22:02:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700426ba44e8a8c3b0f8af151e7f5ddec5968e0a7fa698fd28d747ac78691fd9`  
		Last Modified: Fri, 08 Nov 2024 22:02:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:86b6dcf5bf28f7774ce0e85894af8c71026b82388a681c40ed9c9c2cfc23ffe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38882314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0325bad04fa8acefa9d9be1848b89fde527f8fa695abc02cde6e7e66e705fc`

```dockerfile
```

-	Layers:
	-	`sha256:d2883100dfb43cd67f4945fc699f67dca18fb73ec3f7729e173d66219ee32c58`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 38.9 MB (38855738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d0c671759cd020c8139a0e5ece08cdc7027c3cc984f02adf6521ce3eae5070`  
		Last Modified: Fri, 08 Nov 2024 22:01:57 GMT  
		Size: 26.6 KB (26576 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b27820766eac5ea2f1e3de660529b1361b5ec82353e7b0e969fc3eced648c030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583918824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e266d2fd28e27aafa7a5f5369a9412093c23b1ed3062ddc0995b549cfa520edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c34a395203d46f3a8438f67c8cd7665c25a82da3950fb3bf31986dfe41a540`  
		Last Modified: Fri, 08 Nov 2024 23:27:40 GMT  
		Size: 220.7 MB (220693856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614610f6a56531bde8e444698314f25e68a42d662d9e0e88c3b98ed6d324a868`  
		Last Modified: Fri, 08 Nov 2024 23:27:36 GMT  
		Size: 2.5 MB (2504367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b1c3cf05b181f2fbf3600277ae6121e71ee794f5c1d41bd447f1163fdd4a27`  
		Last Modified: Fri, 08 Nov 2024 23:27:36 GMT  
		Size: 468.9 KB (468869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1edf7d494dba932bdc0bfc0cfa37e94e210e4d5d91ffdf29f67ce8aaf93951`  
		Last Modified: Fri, 08 Nov 2024 23:27:43 GMT  
		Size: 330.2 MB (330173537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768643374d2798e1167ea74d669c0c72e5feaad9514bca84db8734e05c8f9cb`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93012cc9c4656e55b9b467f7b6452d1cdb52086e81d74e97b37959afe49f4125`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f6589aff2013468264d34a36584974c957d2fa21c24095dbb69c70ada6bd98`  
		Last Modified: Fri, 08 Nov 2024 23:27:38 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3827ac2f669b176cf5ad76ee8d9a76b2eb8f7cfdf628c4efccce9728c2a0c`  
		Last Modified: Fri, 08 Nov 2024 23:27:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:69c30309a0a70dc3f56975d267fa16983a20800580996a80bc01dd1f6db75fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38888931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf480f2d9a48015167cd2a53faa85eaad4ac89bc49972e18dd191541fadab391`

```dockerfile
```

-	Layers:
	-	`sha256:71cd7233d0f64e4df6f79405df66e6a4ff8f7a3440ad8ed2b4b897c1b0b564f7`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 38.9 MB (38862210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fcd66b3ac5cf2f10d74bd418d055bc7eec76c7757f520320a3bab800412380`  
		Last Modified: Fri, 08 Nov 2024 23:27:35 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:7e05c6101bf41f56210d29138cf18fc86da7670fe5173d3ca00b35b112bf70b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:db19636c29eab488aba105500824ea2d8afb95d06687629720e7bfa9fc6665c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588490203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4f441875297c0ec2a967b49173679afa599af71e253d102a1d61c5d20c2c31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3debe5503c9c852161c15d7d751083b9c60af9aa437565d402ff8eba39baa5`  
		Last Modified: Fri, 08 Nov 2024 22:02:06 GMT  
		Size: 223.6 MB (223576785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11adc5c286096faeb74ae0d4f96df7e9600a908bd76abeb98cf5c8ec36204ce2`  
		Last Modified: Fri, 08 Nov 2024 22:01:58 GMT  
		Size: 2.5 MB (2494352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897dcd9121b2909bba8661d89fff856bae0bb06a92c03f1904c863792717aa03`  
		Last Modified: Fri, 08 Nov 2024 22:01:58 GMT  
		Size: 468.9 KB (468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb7aa2509151d095324336eb754d38549772216f95d094ac57bc2dcbcbb3ac5`  
		Last Modified: Fri, 08 Nov 2024 22:02:09 GMT  
		Size: 330.5 MB (330518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9c8396630a7f616cb548c893817e8470992a98d69a5bc96aeeec762e05e669`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63da9aa4e752a6795833f2de769df468b68a75d4e230446c73b37e937ffac1d`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21cd94a439fa6c6a7b9deb60c143147b98dc796b69fdb6d756a3ad8020a2e3`  
		Last Modified: Fri, 08 Nov 2024 22:02:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700426ba44e8a8c3b0f8af151e7f5ddec5968e0a7fa698fd28d747ac78691fd9`  
		Last Modified: Fri, 08 Nov 2024 22:02:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:86b6dcf5bf28f7774ce0e85894af8c71026b82388a681c40ed9c9c2cfc23ffe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38882314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0325bad04fa8acefa9d9be1848b89fde527f8fa695abc02cde6e7e66e705fc`

```dockerfile
```

-	Layers:
	-	`sha256:d2883100dfb43cd67f4945fc699f67dca18fb73ec3f7729e173d66219ee32c58`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 38.9 MB (38855738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d0c671759cd020c8139a0e5ece08cdc7027c3cc984f02adf6521ce3eae5070`  
		Last Modified: Fri, 08 Nov 2024 22:01:57 GMT  
		Size: 26.6 KB (26576 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b27820766eac5ea2f1e3de660529b1361b5ec82353e7b0e969fc3eced648c030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583918824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e266d2fd28e27aafa7a5f5369a9412093c23b1ed3062ddc0995b549cfa520edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c34a395203d46f3a8438f67c8cd7665c25a82da3950fb3bf31986dfe41a540`  
		Last Modified: Fri, 08 Nov 2024 23:27:40 GMT  
		Size: 220.7 MB (220693856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614610f6a56531bde8e444698314f25e68a42d662d9e0e88c3b98ed6d324a868`  
		Last Modified: Fri, 08 Nov 2024 23:27:36 GMT  
		Size: 2.5 MB (2504367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b1c3cf05b181f2fbf3600277ae6121e71ee794f5c1d41bd447f1163fdd4a27`  
		Last Modified: Fri, 08 Nov 2024 23:27:36 GMT  
		Size: 468.9 KB (468869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1edf7d494dba932bdc0bfc0cfa37e94e210e4d5d91ffdf29f67ce8aaf93951`  
		Last Modified: Fri, 08 Nov 2024 23:27:43 GMT  
		Size: 330.2 MB (330173537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768643374d2798e1167ea74d669c0c72e5feaad9514bca84db8734e05c8f9cb`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93012cc9c4656e55b9b467f7b6452d1cdb52086e81d74e97b37959afe49f4125`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f6589aff2013468264d34a36584974c957d2fa21c24095dbb69c70ada6bd98`  
		Last Modified: Fri, 08 Nov 2024 23:27:38 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3827ac2f669b176cf5ad76ee8d9a76b2eb8f7cfdf628c4efccce9728c2a0c`  
		Last Modified: Fri, 08 Nov 2024 23:27:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:69c30309a0a70dc3f56975d267fa16983a20800580996a80bc01dd1f6db75fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38888931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf480f2d9a48015167cd2a53faa85eaad4ac89bc49972e18dd191541fadab391`

```dockerfile
```

-	Layers:
	-	`sha256:71cd7233d0f64e4df6f79405df66e6a4ff8f7a3440ad8ed2b4b897c1b0b564f7`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 38.9 MB (38862210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fcd66b3ac5cf2f10d74bd418d055bc7eec76c7757f520320a3bab800412380`  
		Last Modified: Fri, 08 Nov 2024 23:27:35 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241108`

```console
$ docker pull odoo@sha256:7e05c6101bf41f56210d29138cf18fc86da7670fe5173d3ca00b35b112bf70b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20241108` - linux; amd64

```console
$ docker pull odoo@sha256:db19636c29eab488aba105500824ea2d8afb95d06687629720e7bfa9fc6665c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.5 MB (588490203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4f441875297c0ec2a967b49173679afa599af71e253d102a1d61c5d20c2c31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3debe5503c9c852161c15d7d751083b9c60af9aa437565d402ff8eba39baa5`  
		Last Modified: Fri, 08 Nov 2024 22:02:06 GMT  
		Size: 223.6 MB (223576785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11adc5c286096faeb74ae0d4f96df7e9600a908bd76abeb98cf5c8ec36204ce2`  
		Last Modified: Fri, 08 Nov 2024 22:01:58 GMT  
		Size: 2.5 MB (2494352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897dcd9121b2909bba8661d89fff856bae0bb06a92c03f1904c863792717aa03`  
		Last Modified: Fri, 08 Nov 2024 22:01:58 GMT  
		Size: 468.9 KB (468948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb7aa2509151d095324336eb754d38549772216f95d094ac57bc2dcbcbb3ac5`  
		Last Modified: Fri, 08 Nov 2024 22:02:09 GMT  
		Size: 330.5 MB (330518887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9c8396630a7f616cb548c893817e8470992a98d69a5bc96aeeec762e05e669`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63da9aa4e752a6795833f2de769df468b68a75d4e230446c73b37e937ffac1d`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21cd94a439fa6c6a7b9deb60c143147b98dc796b69fdb6d756a3ad8020a2e3`  
		Last Modified: Fri, 08 Nov 2024 22:02:00 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700426ba44e8a8c3b0f8af151e7f5ddec5968e0a7fa698fd28d747ac78691fd9`  
		Last Modified: Fri, 08 Nov 2024 22:02:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:86b6dcf5bf28f7774ce0e85894af8c71026b82388a681c40ed9c9c2cfc23ffe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38882314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0325bad04fa8acefa9d9be1848b89fde527f8fa695abc02cde6e7e66e705fc`

```dockerfile
```

-	Layers:
	-	`sha256:d2883100dfb43cd67f4945fc699f67dca18fb73ec3f7729e173d66219ee32c58`  
		Last Modified: Fri, 08 Nov 2024 22:01:59 GMT  
		Size: 38.9 MB (38855738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96d0c671759cd020c8139a0e5ece08cdc7027c3cc984f02adf6521ce3eae5070`  
		Last Modified: Fri, 08 Nov 2024 22:01:57 GMT  
		Size: 26.6 KB (26576 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20241108` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b27820766eac5ea2f1e3de660529b1361b5ec82353e7b0e969fc3eced648c030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583918824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e266d2fd28e27aafa7a5f5369a9412093c23b1ed3062ddc0995b549cfa520edf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=16.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=0ac65f3a2ec8787626c4e472694461e31ae109d5
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c34a395203d46f3a8438f67c8cd7665c25a82da3950fb3bf31986dfe41a540`  
		Last Modified: Fri, 08 Nov 2024 23:27:40 GMT  
		Size: 220.7 MB (220693856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614610f6a56531bde8e444698314f25e68a42d662d9e0e88c3b98ed6d324a868`  
		Last Modified: Fri, 08 Nov 2024 23:27:36 GMT  
		Size: 2.5 MB (2504367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b1c3cf05b181f2fbf3600277ae6121e71ee794f5c1d41bd447f1163fdd4a27`  
		Last Modified: Fri, 08 Nov 2024 23:27:36 GMT  
		Size: 468.9 KB (468869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1edf7d494dba932bdc0bfc0cfa37e94e210e4d5d91ffdf29f67ce8aaf93951`  
		Last Modified: Fri, 08 Nov 2024 23:27:43 GMT  
		Size: 330.2 MB (330173537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768643374d2798e1167ea74d669c0c72e5feaad9514bca84db8734e05c8f9cb`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93012cc9c4656e55b9b467f7b6452d1cdb52086e81d74e97b37959afe49f4125`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f6589aff2013468264d34a36584974c957d2fa21c24095dbb69c70ada6bd98`  
		Last Modified: Fri, 08 Nov 2024 23:27:38 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f3827ac2f669b176cf5ad76ee8d9a76b2eb8f7cfdf628c4efccce9728c2a0c`  
		Last Modified: Fri, 08 Nov 2024 23:27:38 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:69c30309a0a70dc3f56975d267fa16983a20800580996a80bc01dd1f6db75fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38888931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf480f2d9a48015167cd2a53faa85eaad4ac89bc49972e18dd191541fadab391`

```dockerfile
```

-	Layers:
	-	`sha256:71cd7233d0f64e4df6f79405df66e6a4ff8f7a3440ad8ed2b4b897c1b0b564f7`  
		Last Modified: Fri, 08 Nov 2024 23:27:37 GMT  
		Size: 38.9 MB (38862210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fcd66b3ac5cf2f10d74bd418d055bc7eec76c7757f520320a3bab800412380`  
		Last Modified: Fri, 08 Nov 2024 23:27:35 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:6a907c932b4edc88371416b6f55d0b8989887763059d74a62500420a53ebb0d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:c84993758bd8473f448cddc67b40da54a3683dda62bdf909e650a2b1041ccc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.2 MB (598217963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e18b05eb364ef3e9481dbeaaf75f006b01b6c553d512e2ae70bff625572db3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091aa3a70cdc091317f0ac78ead4aede39a11ba82451157780cbb1081915aaf4`  
		Last Modified: Fri, 08 Nov 2024 22:01:48 GMT  
		Size: 233.8 MB (233764900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bf42213b9acdf2863a6cef2646ec64b2098700d644d1e2508c8e23b4660a6c`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 2.4 MB (2405376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1160e9a9f625fe88959ca8464fde747a7f777dff22ddd5146a77ca2cbe1934`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 469.9 KB (469920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bd1a94bc69317877d1adb9cf894af560802199b24c6ec329d84f9922b9f652`  
		Last Modified: Fri, 08 Nov 2024 22:01:49 GMT  
		Size: 332.0 MB (332039639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bda7c84ba833a0500bd603d5f749227b1c5f5c4a960b32d83564e3c1f8c3a51`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d97a8dac2c82efd3ce94c2ca4c9435c28997f96061b32287a64723243433e0`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82967e4840e7b8dde09b35e06a57b473b01cd5b021cde48f6dfea257ff3e7bb7`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dfe830b6f17043abe173d7c55e374d119b937bac9dc85bbdb6fbb46295c468`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:9146c332e93ee4b2f6d3eaa27586a70a8f255c3ffcc1187940dd11d38ca17dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39617634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4950df6264755fcdd3f673e36b7bbe0be40cbcd15a34f1ecda90181b59f215`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb0ebd35e940c60d4e4c7bf925098839fc6e35162f3a972bafff21eb64da89`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 39.6 MB (39590800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b95f0b8b8d26fb8413dba53935c66e5a5fd63f3ec8ddbe2fc83e01025fea444`  
		Last Modified: Fri, 08 Nov 2024 22:01:44 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e1e74d9fcaec6e68f381c25e7c628bb29662e2b1e432b3a2582bbd163ae91181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.0 MB (593041310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5648e13330456bc51072c3a787069906c956029c3a643932029458f31c8d7286`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f8b0686bd6532cdda7a65424b2393e76bf37894b9b2c7ace657bb901aa9a6`  
		Last Modified: Fri, 08 Nov 2024 23:23:41 GMT  
		Size: 231.2 MB (231159525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a5341e72179a2664567bd72bbf2ffc3f2c2fac8adf0eaecc22b42880d85ef`  
		Last Modified: Fri, 08 Nov 2024 23:23:35 GMT  
		Size: 2.4 MB (2398322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8aa4f0b08707099defee3740c1f9b6ea1afdb621ff2835182b93b09309704b`  
		Last Modified: Fri, 08 Nov 2024 23:23:35 GMT  
		Size: 469.8 KB (469844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01434c337f6b1bc241acb2763d1e501c4d56a8d76fb13aec5a89d556ac31ce5`  
		Last Modified: Fri, 08 Nov 2024 23:23:42 GMT  
		Size: 331.7 MB (331652851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5c3af3797c98d5c90f76995820539ca6d5745407ac6f55bb7e27c5dba9f1ef`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c499d219855e1ef7888b2252afa972e599bc4ae63af0f0a94cb32a9e052a8c1`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9be0537758218da965fb5118912e8200f0469278c17e1a00ab8a3ca83db04f`  
		Last Modified: Fri, 08 Nov 2024 23:23:37 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b3c442527e996de1b26126802784dbf2bdff46f5e4d613582645f010fbac9`  
		Last Modified: Fri, 08 Nov 2024 23:23:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:2e76480b442d42432d408a695c496848125f94b2227cc2f592522f334c17cc96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39624300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b31245efcd839bb12152d8e2791483b155e5117efc177225520f0c44789cfaf`

```dockerfile
```

-	Layers:
	-	`sha256:1c79b6c7b7cffb3a341ac15cd5d2a4df727aab5afd532cc783f9398f88a4c2d5`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 39.6 MB (39597313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890f06d71a65d504e708454ab7cd8767d1b04f1b8b9d5166a156d9fb3c9de1f7`  
		Last Modified: Fri, 08 Nov 2024 23:23:34 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:e71c88462bcde2837da71553d43a22edd5351f824bb8af46c9773dfb1f3a8b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614681339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023424a3e4fb58a3d6ba427be88520c119662be8d086f971c6c1dad232609b04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb24c7d470fc45c29a851561d281016df8f8caf37ee0b788f211955a003125d`  
		Last Modified: Fri, 08 Nov 2024 23:44:21 GMT  
		Size: 243.3 MB (243296698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7b29df9bc9facc009f995251e6f6b4c8f29d8658ba6df185d5a0b26c87eb9`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 2.7 MB (2708491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e436d14cb20b9e94d971a6c72ce8bf56a6c8d3fc91e103979bd4b058ec904d`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 469.9 KB (469859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787453aca0858398fac2807e56cddd2e6953d525b20bc5591b11f2d727221e5d`  
		Last Modified: Fri, 08 Nov 2024 23:44:24 GMT  
		Size: 333.8 MB (333755604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de0e4e3c2ec1606e5508e2403c9e36de2616dee3a732a224d5e9055c869409`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec7226883c6f7aee991281b8982fc66c8de1ca8fab6fcecdd1225377e9587c`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0fe525e8bf98c9b835463c548f852b6308c99732774d808ae1758b2d89c9bd`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb3f640220aff27fd34df564b4bbc24552c2d6a18c968dd243749c290d1f046`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d3ad6bf2ba1cdbbd423332b35a409960b83bfbf75ea1dd3d175603547f8e1fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39625997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e95bc618fbff69d6d5c41afc695e8fbed5475b69963625ab8480b3a189cc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:1c5d5594c17001bc579117a8fc3838a57c5ef60c4b6773311a1d97c5bfc16265`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 39.6 MB (39599107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9a709dfa62d34ba86a3f8983fe3e679396a74dec8b0cb070809259afa62cec`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:6a907c932b4edc88371416b6f55d0b8989887763059d74a62500420a53ebb0d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:c84993758bd8473f448cddc67b40da54a3683dda62bdf909e650a2b1041ccc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.2 MB (598217963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e18b05eb364ef3e9481dbeaaf75f006b01b6c553d512e2ae70bff625572db3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091aa3a70cdc091317f0ac78ead4aede39a11ba82451157780cbb1081915aaf4`  
		Last Modified: Fri, 08 Nov 2024 22:01:48 GMT  
		Size: 233.8 MB (233764900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bf42213b9acdf2863a6cef2646ec64b2098700d644d1e2508c8e23b4660a6c`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 2.4 MB (2405376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1160e9a9f625fe88959ca8464fde747a7f777dff22ddd5146a77ca2cbe1934`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 469.9 KB (469920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bd1a94bc69317877d1adb9cf894af560802199b24c6ec329d84f9922b9f652`  
		Last Modified: Fri, 08 Nov 2024 22:01:49 GMT  
		Size: 332.0 MB (332039639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bda7c84ba833a0500bd603d5f749227b1c5f5c4a960b32d83564e3c1f8c3a51`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d97a8dac2c82efd3ce94c2ca4c9435c28997f96061b32287a64723243433e0`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82967e4840e7b8dde09b35e06a57b473b01cd5b021cde48f6dfea257ff3e7bb7`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dfe830b6f17043abe173d7c55e374d119b937bac9dc85bbdb6fbb46295c468`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9146c332e93ee4b2f6d3eaa27586a70a8f255c3ffcc1187940dd11d38ca17dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39617634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4950df6264755fcdd3f673e36b7bbe0be40cbcd15a34f1ecda90181b59f215`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb0ebd35e940c60d4e4c7bf925098839fc6e35162f3a972bafff21eb64da89`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 39.6 MB (39590800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b95f0b8b8d26fb8413dba53935c66e5a5fd63f3ec8ddbe2fc83e01025fea444`  
		Last Modified: Fri, 08 Nov 2024 22:01:44 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e1e74d9fcaec6e68f381c25e7c628bb29662e2b1e432b3a2582bbd163ae91181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.0 MB (593041310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5648e13330456bc51072c3a787069906c956029c3a643932029458f31c8d7286`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f8b0686bd6532cdda7a65424b2393e76bf37894b9b2c7ace657bb901aa9a6`  
		Last Modified: Fri, 08 Nov 2024 23:23:41 GMT  
		Size: 231.2 MB (231159525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a5341e72179a2664567bd72bbf2ffc3f2c2fac8adf0eaecc22b42880d85ef`  
		Last Modified: Fri, 08 Nov 2024 23:23:35 GMT  
		Size: 2.4 MB (2398322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8aa4f0b08707099defee3740c1f9b6ea1afdb621ff2835182b93b09309704b`  
		Last Modified: Fri, 08 Nov 2024 23:23:35 GMT  
		Size: 469.8 KB (469844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01434c337f6b1bc241acb2763d1e501c4d56a8d76fb13aec5a89d556ac31ce5`  
		Last Modified: Fri, 08 Nov 2024 23:23:42 GMT  
		Size: 331.7 MB (331652851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5c3af3797c98d5c90f76995820539ca6d5745407ac6f55bb7e27c5dba9f1ef`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c499d219855e1ef7888b2252afa972e599bc4ae63af0f0a94cb32a9e052a8c1`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9be0537758218da965fb5118912e8200f0469278c17e1a00ab8a3ca83db04f`  
		Last Modified: Fri, 08 Nov 2024 23:23:37 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b3c442527e996de1b26126802784dbf2bdff46f5e4d613582645f010fbac9`  
		Last Modified: Fri, 08 Nov 2024 23:23:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2e76480b442d42432d408a695c496848125f94b2227cc2f592522f334c17cc96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39624300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b31245efcd839bb12152d8e2791483b155e5117efc177225520f0c44789cfaf`

```dockerfile
```

-	Layers:
	-	`sha256:1c79b6c7b7cffb3a341ac15cd5d2a4df727aab5afd532cc783f9398f88a4c2d5`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 39.6 MB (39597313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890f06d71a65d504e708454ab7cd8767d1b04f1b8b9d5166a156d9fb3c9de1f7`  
		Last Modified: Fri, 08 Nov 2024 23:23:34 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e71c88462bcde2837da71553d43a22edd5351f824bb8af46c9773dfb1f3a8b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614681339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023424a3e4fb58a3d6ba427be88520c119662be8d086f971c6c1dad232609b04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb24c7d470fc45c29a851561d281016df8f8caf37ee0b788f211955a003125d`  
		Last Modified: Fri, 08 Nov 2024 23:44:21 GMT  
		Size: 243.3 MB (243296698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7b29df9bc9facc009f995251e6f6b4c8f29d8658ba6df185d5a0b26c87eb9`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 2.7 MB (2708491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e436d14cb20b9e94d971a6c72ce8bf56a6c8d3fc91e103979bd4b058ec904d`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 469.9 KB (469859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787453aca0858398fac2807e56cddd2e6953d525b20bc5591b11f2d727221e5d`  
		Last Modified: Fri, 08 Nov 2024 23:44:24 GMT  
		Size: 333.8 MB (333755604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de0e4e3c2ec1606e5508e2403c9e36de2616dee3a732a224d5e9055c869409`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec7226883c6f7aee991281b8982fc66c8de1ca8fab6fcecdd1225377e9587c`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0fe525e8bf98c9b835463c548f852b6308c99732774d808ae1758b2d89c9bd`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb3f640220aff27fd34df564b4bbc24552c2d6a18c968dd243749c290d1f046`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d3ad6bf2ba1cdbbd423332b35a409960b83bfbf75ea1dd3d175603547f8e1fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39625997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e95bc618fbff69d6d5c41afc695e8fbed5475b69963625ab8480b3a189cc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:1c5d5594c17001bc579117a8fc3838a57c5ef60c4b6773311a1d97c5bfc16265`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 39.6 MB (39599107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9a709dfa62d34ba86a3f8983fe3e679396a74dec8b0cb070809259afa62cec`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241108`

```console
$ docker pull odoo@sha256:6a907c932b4edc88371416b6f55d0b8989887763059d74a62500420a53ebb0d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241108` - linux; amd64

```console
$ docker pull odoo@sha256:c84993758bd8473f448cddc67b40da54a3683dda62bdf909e650a2b1041ccc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.2 MB (598217963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e18b05eb364ef3e9481dbeaaf75f006b01b6c553d512e2ae70bff625572db3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091aa3a70cdc091317f0ac78ead4aede39a11ba82451157780cbb1081915aaf4`  
		Last Modified: Fri, 08 Nov 2024 22:01:48 GMT  
		Size: 233.8 MB (233764900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bf42213b9acdf2863a6cef2646ec64b2098700d644d1e2508c8e23b4660a6c`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 2.4 MB (2405376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1160e9a9f625fe88959ca8464fde747a7f777dff22ddd5146a77ca2cbe1934`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 469.9 KB (469920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bd1a94bc69317877d1adb9cf894af560802199b24c6ec329d84f9922b9f652`  
		Last Modified: Fri, 08 Nov 2024 22:01:49 GMT  
		Size: 332.0 MB (332039639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bda7c84ba833a0500bd603d5f749227b1c5f5c4a960b32d83564e3c1f8c3a51`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d97a8dac2c82efd3ce94c2ca4c9435c28997f96061b32287a64723243433e0`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82967e4840e7b8dde09b35e06a57b473b01cd5b021cde48f6dfea257ff3e7bb7`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55dfe830b6f17043abe173d7c55e374d119b937bac9dc85bbdb6fbb46295c468`  
		Last Modified: Fri, 08 Nov 2024 22:01:46 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:9146c332e93ee4b2f6d3eaa27586a70a8f255c3ffcc1187940dd11d38ca17dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39617634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4950df6264755fcdd3f673e36b7bbe0be40cbcd15a34f1ecda90181b59f215`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb0ebd35e940c60d4e4c7bf925098839fc6e35162f3a972bafff21eb64da89`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 39.6 MB (39590800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b95f0b8b8d26fb8413dba53935c66e5a5fd63f3ec8ddbe2fc83e01025fea444`  
		Last Modified: Fri, 08 Nov 2024 22:01:44 GMT  
		Size: 26.8 KB (26834 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241108` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e1e74d9fcaec6e68f381c25e7c628bb29662e2b1e432b3a2582bbd163ae91181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.0 MB (593041310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5648e13330456bc51072c3a787069906c956029c3a643932029458f31c8d7286`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f8b0686bd6532cdda7a65424b2393e76bf37894b9b2c7ace657bb901aa9a6`  
		Last Modified: Fri, 08 Nov 2024 23:23:41 GMT  
		Size: 231.2 MB (231159525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a5341e72179a2664567bd72bbf2ffc3f2c2fac8adf0eaecc22b42880d85ef`  
		Last Modified: Fri, 08 Nov 2024 23:23:35 GMT  
		Size: 2.4 MB (2398322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8aa4f0b08707099defee3740c1f9b6ea1afdb621ff2835182b93b09309704b`  
		Last Modified: Fri, 08 Nov 2024 23:23:35 GMT  
		Size: 469.8 KB (469844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01434c337f6b1bc241acb2763d1e501c4d56a8d76fb13aec5a89d556ac31ce5`  
		Last Modified: Fri, 08 Nov 2024 23:23:42 GMT  
		Size: 331.7 MB (331652851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5c3af3797c98d5c90f76995820539ca6d5745407ac6f55bb7e27c5dba9f1ef`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c499d219855e1ef7888b2252afa972e599bc4ae63af0f0a94cb32a9e052a8c1`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9be0537758218da965fb5118912e8200f0469278c17e1a00ab8a3ca83db04f`  
		Last Modified: Fri, 08 Nov 2024 23:23:37 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b3c442527e996de1b26126802784dbf2bdff46f5e4d613582645f010fbac9`  
		Last Modified: Fri, 08 Nov 2024 23:23:37 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:2e76480b442d42432d408a695c496848125f94b2227cc2f592522f334c17cc96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39624300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b31245efcd839bb12152d8e2791483b155e5117efc177225520f0c44789cfaf`

```dockerfile
```

-	Layers:
	-	`sha256:1c79b6c7b7cffb3a341ac15cd5d2a4df727aab5afd532cc783f9398f88a4c2d5`  
		Last Modified: Fri, 08 Nov 2024 23:23:36 GMT  
		Size: 39.6 MB (39597313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890f06d71a65d504e708454ab7cd8767d1b04f1b8b9d5166a156d9fb3c9de1f7`  
		Last Modified: Fri, 08 Nov 2024 23:23:34 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241108` - linux; ppc64le

```console
$ docker pull odoo@sha256:e71c88462bcde2837da71553d43a22edd5351f824bb8af46c9773dfb1f3a8b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.7 MB (614681339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023424a3e4fb58a3d6ba427be88520c119662be8d086f971c6c1dad232609b04`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
ENV ODOO_VERSION=17.0
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_RELEASE=20241108
# Fri, 08 Nov 2024 10:31:04 GMT
ARG ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241108 ODOO_SHA=b49bcf72c9e57e444483c84323fbd2fe878f7651
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb24c7d470fc45c29a851561d281016df8f8caf37ee0b788f211955a003125d`  
		Last Modified: Fri, 08 Nov 2024 23:44:21 GMT  
		Size: 243.3 MB (243296698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7b29df9bc9facc009f995251e6f6b4c8f29d8658ba6df185d5a0b26c87eb9`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 2.7 MB (2708491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e436d14cb20b9e94d971a6c72ce8bf56a6c8d3fc91e103979bd4b058ec904d`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 469.9 KB (469859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787453aca0858398fac2807e56cddd2e6953d525b20bc5591b11f2d727221e5d`  
		Last Modified: Fri, 08 Nov 2024 23:44:24 GMT  
		Size: 333.8 MB (333755604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de0e4e3c2ec1606e5508e2403c9e36de2616dee3a732a224d5e9055c869409`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec7226883c6f7aee991281b8982fc66c8de1ca8fab6fcecdd1225377e9587c`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0fe525e8bf98c9b835463c548f852b6308c99732774d808ae1758b2d89c9bd`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb3f640220aff27fd34df564b4bbc24552c2d6a18c968dd243749c290d1f046`  
		Last Modified: Fri, 08 Nov 2024 23:44:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:d3ad6bf2ba1cdbbd423332b35a409960b83bfbf75ea1dd3d175603547f8e1fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39625997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e95bc618fbff69d6d5c41afc695e8fbed5475b69963625ab8480b3a189cc5fb`

```dockerfile
```

-	Layers:
	-	`sha256:1c5d5594c17001bc579117a8fc3838a57c5ef60c4b6773311a1d97c5bfc16265`  
		Last Modified: Fri, 08 Nov 2024 23:44:00 GMT  
		Size: 39.6 MB (39599107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9a709dfa62d34ba86a3f8983fe3e679396a74dec8b0cb070809259afa62cec`  
		Last Modified: Fri, 08 Nov 2024 23:43:59 GMT  
		Size: 26.9 KB (26890 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:f919e5ccf3c0d6971d713f5ce669ef9bdbe6fa87d30e2105bbbd508a5a5cc1f5
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
$ docker pull odoo@sha256:f81ece8dc140fba1701c80ccc49816810653751f09574bbca7fcfa916168162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658184855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b179ad6ddb4e44a0bfb096fe60407226f73e2aac675b46db11a45ea86729993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fc4e527e79e99befa35005401137c01bfbe0e191eb76563f4a8804e6d84551`  
		Last Modified: Fri, 08 Nov 2024 22:02:32 GMT  
		Size: 255.6 MB (255642280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e51fcc93bd9ca9c044c17308143f23bd1fc372575fce23fe807ea684ca4ec02`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 14.1 MB (14142415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2628834877a3eac4e027e516861b575814bf5f4bbf0ae3de1ad49cc1b209931`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 469.6 KB (469607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770366cbb36b23674a54d6bf041818ebb0dc74805f4a03b768ae824228a828f4`  
		Last Modified: Fri, 08 Nov 2024 22:02:34 GMT  
		Size: 358.2 MB (358177754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bda7c84ba833a0500bd603d5f749227b1c5f5c4a960b32d83564e3c1f8c3a51`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987fbb35471bf4df0260eb29c3ecb72bcba27e98a3cbde68dee46beeb7f5b7f`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ff4c46982d34facdaad250a9fc691b848473382ac4c316387ebd9ed2d9bdce`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec019d588cb9b5df05b4d2e8066a69ce65c5b0991d04aee05fda7bc94b4afd`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7eba9a1a5cc8e9a3b3f48aff49a3e72de60de7254946e0720c91d50935c869f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56223613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bdd5b1be9a423e3b72c71e0e7c1469053a671b34db956d6eb2be867658826b`

```dockerfile
```

-	Layers:
	-	`sha256:19fb9b50a593490c66f4ea606225d4045eb825f5c5780f32e15a96233944c668`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 56.2 MB (56196477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e31a96fd4bd9922f1138ac4afea0d860074d64d983ee7b9c74b5c454ef7c59`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a8adc4fb018a90c25c43b1d8055292014e9f7a33ac4ce85ba314e24c04b2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.5 MB (654502601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f2f1cda8c3380de42204a158796182cdcd56fa039a66fbc5cc5436001e8c7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b256dd78da704c0e392e7f41c1e562b2078d1dd6077ec3f63f235c1bd801f558`  
		Last Modified: Fri, 08 Nov 2024 23:17:04 GMT  
		Size: 253.0 MB (252998737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02171ccd35a530c539fa58e8ba735d2e4b12ded8a6929e6eba5b4473b9d4c49`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 14.1 MB (14115479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365fa69c021688334226aa7de66bbb73b8dd3d7eeb7163ebbc36f1818a56728`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 469.7 KB (469660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5017223533bbab820ecac13a366c0a52b4aa0f74ee756acf63f52052810ca59e`  
		Last Modified: Fri, 08 Nov 2024 23:17:07 GMT  
		Size: 358.0 MB (358030442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b70ec4b530131b883dd073224f04690d6da58c49bb340f5628ec795f917739`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ac167ee87cd60259c73f80fe4a1e16b88b62dedfb6559589515cd0948f0469`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738ea22ed548457804d679c5430f97f5ba43ddf8aedd5db3468bbe9194ec416d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2b74bf531fb0833f4527429727796c63c50213e7ee79420d33899e105ceb6d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:92118c2727e755a33efd0994e0fa8c7ce3660dfbcbb36cad181550d1a127c6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce5ff8746407de30e3f186239510c64776c3b13c33aa54d2baa7a0048d165e6`

```dockerfile
```

-	Layers:
	-	`sha256:52e36b19fd2a60c1372592f0b6bab02118fbc0059f9a43ef824eeb25e037be50`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 56.2 MB (56203771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814031fbcc6e20794b52b019497fcdec30b5563e239bd2052302afb969aa9feb`  
		Last Modified: Fri, 08 Nov 2024 23:16:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:adfb65412f33f6401cb76eee6774246d0144a8ce505b9b325ce447185de961be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 MB (674679380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd9f225e9037687e046af6dd4508177bc4a405c31dd8053136c670a04329eab`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945cad33a894b3838b385b7f86e8c9a7f09d9f28b08d1662aed37ee9120e0900`  
		Last Modified: Fri, 08 Nov 2024 23:33:37 GMT  
		Size: 266.4 MB (266405180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b880cc4226ec4a472884359dc4fe60fe31f2d16f4415d4196ab64c3043aaa9a`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 14.7 MB (14686214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16abe6c780d1671b85d7292ecb4c904c41621e779127970c78bd72e363789a78`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 469.7 KB (469685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd6609548b3779d46e24cb945478511657c8a3d68b7eccf5d8f3b531bbdd84`  
		Last Modified: Fri, 08 Nov 2024 23:33:41 GMT  
		Size: 358.7 MB (358726895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0048d47977e0aaf532f0843ebba114f247910e75a9f491b89e6f77fcb48caf`  
		Last Modified: Fri, 08 Nov 2024 23:33:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fc06c08cc93340016dd3c08de6a9c9f73822f459742c56aaea8ee6ed4b22ce`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776a8ca243735cf3bfff3fdbce132628b8f7b4525256061d313385c78f6912e`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b185034b6b4f267ede93929d110f1a7cab2ca24220cf82287264037cccf83de0`  
		Last Modified: Fri, 08 Nov 2024 23:33:21 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7da1777b5db83d247555f0e741e04ab897658fdee811e598c1c72b4f0133432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ca32c79d0d91ebcb64e755d28af5b7136c8287ac0df532fdd678a2d038c5e8`

```dockerfile
```

-	Layers:
	-	`sha256:bd219396a131da5a4c1f8e0cca42dbbc93a7b7c5a5940d8c2f8d4686f3485506`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 56.2 MB (56204620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a50d6444ad0a4e709b8af43eaf656c4e34468450466e866ee18f69e53baf0e`  
		Last Modified: Fri, 08 Nov 2024 23:33:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:f919e5ccf3c0d6971d713f5ce669ef9bdbe6fa87d30e2105bbbd508a5a5cc1f5
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
$ docker pull odoo@sha256:f81ece8dc140fba1701c80ccc49816810653751f09574bbca7fcfa916168162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658184855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b179ad6ddb4e44a0bfb096fe60407226f73e2aac675b46db11a45ea86729993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fc4e527e79e99befa35005401137c01bfbe0e191eb76563f4a8804e6d84551`  
		Last Modified: Fri, 08 Nov 2024 22:02:32 GMT  
		Size: 255.6 MB (255642280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e51fcc93bd9ca9c044c17308143f23bd1fc372575fce23fe807ea684ca4ec02`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 14.1 MB (14142415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2628834877a3eac4e027e516861b575814bf5f4bbf0ae3de1ad49cc1b209931`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 469.6 KB (469607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770366cbb36b23674a54d6bf041818ebb0dc74805f4a03b768ae824228a828f4`  
		Last Modified: Fri, 08 Nov 2024 22:02:34 GMT  
		Size: 358.2 MB (358177754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bda7c84ba833a0500bd603d5f749227b1c5f5c4a960b32d83564e3c1f8c3a51`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987fbb35471bf4df0260eb29c3ecb72bcba27e98a3cbde68dee46beeb7f5b7f`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ff4c46982d34facdaad250a9fc691b848473382ac4c316387ebd9ed2d9bdce`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec019d588cb9b5df05b4d2e8066a69ce65c5b0991d04aee05fda7bc94b4afd`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7eba9a1a5cc8e9a3b3f48aff49a3e72de60de7254946e0720c91d50935c869f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56223613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bdd5b1be9a423e3b72c71e0e7c1469053a671b34db956d6eb2be867658826b`

```dockerfile
```

-	Layers:
	-	`sha256:19fb9b50a593490c66f4ea606225d4045eb825f5c5780f32e15a96233944c668`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 56.2 MB (56196477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e31a96fd4bd9922f1138ac4afea0d860074d64d983ee7b9c74b5c454ef7c59`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a8adc4fb018a90c25c43b1d8055292014e9f7a33ac4ce85ba314e24c04b2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.5 MB (654502601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f2f1cda8c3380de42204a158796182cdcd56fa039a66fbc5cc5436001e8c7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b256dd78da704c0e392e7f41c1e562b2078d1dd6077ec3f63f235c1bd801f558`  
		Last Modified: Fri, 08 Nov 2024 23:17:04 GMT  
		Size: 253.0 MB (252998737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02171ccd35a530c539fa58e8ba735d2e4b12ded8a6929e6eba5b4473b9d4c49`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 14.1 MB (14115479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365fa69c021688334226aa7de66bbb73b8dd3d7eeb7163ebbc36f1818a56728`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 469.7 KB (469660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5017223533bbab820ecac13a366c0a52b4aa0f74ee756acf63f52052810ca59e`  
		Last Modified: Fri, 08 Nov 2024 23:17:07 GMT  
		Size: 358.0 MB (358030442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b70ec4b530131b883dd073224f04690d6da58c49bb340f5628ec795f917739`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ac167ee87cd60259c73f80fe4a1e16b88b62dedfb6559589515cd0948f0469`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738ea22ed548457804d679c5430f97f5ba43ddf8aedd5db3468bbe9194ec416d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2b74bf531fb0833f4527429727796c63c50213e7ee79420d33899e105ceb6d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:92118c2727e755a33efd0994e0fa8c7ce3660dfbcbb36cad181550d1a127c6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce5ff8746407de30e3f186239510c64776c3b13c33aa54d2baa7a0048d165e6`

```dockerfile
```

-	Layers:
	-	`sha256:52e36b19fd2a60c1372592f0b6bab02118fbc0059f9a43ef824eeb25e037be50`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 56.2 MB (56203771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814031fbcc6e20794b52b019497fcdec30b5563e239bd2052302afb969aa9feb`  
		Last Modified: Fri, 08 Nov 2024 23:16:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:adfb65412f33f6401cb76eee6774246d0144a8ce505b9b325ce447185de961be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 MB (674679380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd9f225e9037687e046af6dd4508177bc4a405c31dd8053136c670a04329eab`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945cad33a894b3838b385b7f86e8c9a7f09d9f28b08d1662aed37ee9120e0900`  
		Last Modified: Fri, 08 Nov 2024 23:33:37 GMT  
		Size: 266.4 MB (266405180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b880cc4226ec4a472884359dc4fe60fe31f2d16f4415d4196ab64c3043aaa9a`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 14.7 MB (14686214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16abe6c780d1671b85d7292ecb4c904c41621e779127970c78bd72e363789a78`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 469.7 KB (469685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd6609548b3779d46e24cb945478511657c8a3d68b7eccf5d8f3b531bbdd84`  
		Last Modified: Fri, 08 Nov 2024 23:33:41 GMT  
		Size: 358.7 MB (358726895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0048d47977e0aaf532f0843ebba114f247910e75a9f491b89e6f77fcb48caf`  
		Last Modified: Fri, 08 Nov 2024 23:33:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fc06c08cc93340016dd3c08de6a9c9f73822f459742c56aaea8ee6ed4b22ce`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776a8ca243735cf3bfff3fdbce132628b8f7b4525256061d313385c78f6912e`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b185034b6b4f267ede93929d110f1a7cab2ca24220cf82287264037cccf83de0`  
		Last Modified: Fri, 08 Nov 2024 23:33:21 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7da1777b5db83d247555f0e741e04ab897658fdee811e598c1c72b4f0133432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ca32c79d0d91ebcb64e755d28af5b7136c8287ac0df532fdd678a2d038c5e8`

```dockerfile
```

-	Layers:
	-	`sha256:bd219396a131da5a4c1f8e0cca42dbbc93a7b7c5a5940d8c2f8d4686f3485506`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 56.2 MB (56204620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a50d6444ad0a4e709b8af43eaf656c4e34468450466e866ee18f69e53baf0e`  
		Last Modified: Fri, 08 Nov 2024 23:33:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241108`

```console
$ docker pull odoo@sha256:f919e5ccf3c0d6971d713f5ce669ef9bdbe6fa87d30e2105bbbd508a5a5cc1f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241108` - linux; amd64

```console
$ docker pull odoo@sha256:f81ece8dc140fba1701c80ccc49816810653751f09574bbca7fcfa916168162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658184855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b179ad6ddb4e44a0bfb096fe60407226f73e2aac675b46db11a45ea86729993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fc4e527e79e99befa35005401137c01bfbe0e191eb76563f4a8804e6d84551`  
		Last Modified: Fri, 08 Nov 2024 22:02:32 GMT  
		Size: 255.6 MB (255642280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e51fcc93bd9ca9c044c17308143f23bd1fc372575fce23fe807ea684ca4ec02`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 14.1 MB (14142415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2628834877a3eac4e027e516861b575814bf5f4bbf0ae3de1ad49cc1b209931`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 469.6 KB (469607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770366cbb36b23674a54d6bf041818ebb0dc74805f4a03b768ae824228a828f4`  
		Last Modified: Fri, 08 Nov 2024 22:02:34 GMT  
		Size: 358.2 MB (358177754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bda7c84ba833a0500bd603d5f749227b1c5f5c4a960b32d83564e3c1f8c3a51`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987fbb35471bf4df0260eb29c3ecb72bcba27e98a3cbde68dee46beeb7f5b7f`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ff4c46982d34facdaad250a9fc691b848473382ac4c316387ebd9ed2d9bdce`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec019d588cb9b5df05b4d2e8066a69ce65c5b0991d04aee05fda7bc94b4afd`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:7eba9a1a5cc8e9a3b3f48aff49a3e72de60de7254946e0720c91d50935c869f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56223613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bdd5b1be9a423e3b72c71e0e7c1469053a671b34db956d6eb2be867658826b`

```dockerfile
```

-	Layers:
	-	`sha256:19fb9b50a593490c66f4ea606225d4045eb825f5c5780f32e15a96233944c668`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 56.2 MB (56196477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e31a96fd4bd9922f1138ac4afea0d860074d64d983ee7b9c74b5c454ef7c59`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241108` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a8adc4fb018a90c25c43b1d8055292014e9f7a33ac4ce85ba314e24c04b2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.5 MB (654502601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f2f1cda8c3380de42204a158796182cdcd56fa039a66fbc5cc5436001e8c7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b256dd78da704c0e392e7f41c1e562b2078d1dd6077ec3f63f235c1bd801f558`  
		Last Modified: Fri, 08 Nov 2024 23:17:04 GMT  
		Size: 253.0 MB (252998737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02171ccd35a530c539fa58e8ba735d2e4b12ded8a6929e6eba5b4473b9d4c49`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 14.1 MB (14115479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365fa69c021688334226aa7de66bbb73b8dd3d7eeb7163ebbc36f1818a56728`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 469.7 KB (469660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5017223533bbab820ecac13a366c0a52b4aa0f74ee756acf63f52052810ca59e`  
		Last Modified: Fri, 08 Nov 2024 23:17:07 GMT  
		Size: 358.0 MB (358030442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b70ec4b530131b883dd073224f04690d6da58c49bb340f5628ec795f917739`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ac167ee87cd60259c73f80fe4a1e16b88b62dedfb6559589515cd0948f0469`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738ea22ed548457804d679c5430f97f5ba43ddf8aedd5db3468bbe9194ec416d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2b74bf531fb0833f4527429727796c63c50213e7ee79420d33899e105ceb6d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:92118c2727e755a33efd0994e0fa8c7ce3660dfbcbb36cad181550d1a127c6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce5ff8746407de30e3f186239510c64776c3b13c33aa54d2baa7a0048d165e6`

```dockerfile
```

-	Layers:
	-	`sha256:52e36b19fd2a60c1372592f0b6bab02118fbc0059f9a43ef824eeb25e037be50`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 56.2 MB (56203771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814031fbcc6e20794b52b019497fcdec30b5563e239bd2052302afb969aa9feb`  
		Last Modified: Fri, 08 Nov 2024 23:16:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241108` - linux; ppc64le

```console
$ docker pull odoo@sha256:adfb65412f33f6401cb76eee6774246d0144a8ce505b9b325ce447185de961be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 MB (674679380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd9f225e9037687e046af6dd4508177bc4a405c31dd8053136c670a04329eab`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945cad33a894b3838b385b7f86e8c9a7f09d9f28b08d1662aed37ee9120e0900`  
		Last Modified: Fri, 08 Nov 2024 23:33:37 GMT  
		Size: 266.4 MB (266405180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b880cc4226ec4a472884359dc4fe60fe31f2d16f4415d4196ab64c3043aaa9a`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 14.7 MB (14686214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16abe6c780d1671b85d7292ecb4c904c41621e779127970c78bd72e363789a78`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 469.7 KB (469685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd6609548b3779d46e24cb945478511657c8a3d68b7eccf5d8f3b531bbdd84`  
		Last Modified: Fri, 08 Nov 2024 23:33:41 GMT  
		Size: 358.7 MB (358726895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0048d47977e0aaf532f0843ebba114f247910e75a9f491b89e6f77fcb48caf`  
		Last Modified: Fri, 08 Nov 2024 23:33:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fc06c08cc93340016dd3c08de6a9c9f73822f459742c56aaea8ee6ed4b22ce`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776a8ca243735cf3bfff3fdbce132628b8f7b4525256061d313385c78f6912e`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b185034b6b4f267ede93929d110f1a7cab2ca24220cf82287264037cccf83de0`  
		Last Modified: Fri, 08 Nov 2024 23:33:21 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241108` - unknown; unknown

```console
$ docker pull odoo@sha256:7da1777b5db83d247555f0e741e04ab897658fdee811e598c1c72b4f0133432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ca32c79d0d91ebcb64e755d28af5b7136c8287ac0df532fdd678a2d038c5e8`

```dockerfile
```

-	Layers:
	-	`sha256:bd219396a131da5a4c1f8e0cca42dbbc93a7b7c5a5940d8c2f8d4686f3485506`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 56.2 MB (56204620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a50d6444ad0a4e709b8af43eaf656c4e34468450466e866ee18f69e53baf0e`  
		Last Modified: Fri, 08 Nov 2024 23:33:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:f919e5ccf3c0d6971d713f5ce669ef9bdbe6fa87d30e2105bbbd508a5a5cc1f5
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
$ docker pull odoo@sha256:f81ece8dc140fba1701c80ccc49816810653751f09574bbca7fcfa916168162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658184855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b179ad6ddb4e44a0bfb096fe60407226f73e2aac675b46db11a45ea86729993`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fc4e527e79e99befa35005401137c01bfbe0e191eb76563f4a8804e6d84551`  
		Last Modified: Fri, 08 Nov 2024 22:02:32 GMT  
		Size: 255.6 MB (255642280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e51fcc93bd9ca9c044c17308143f23bd1fc372575fce23fe807ea684ca4ec02`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 14.1 MB (14142415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2628834877a3eac4e027e516861b575814bf5f4bbf0ae3de1ad49cc1b209931`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 469.6 KB (469607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770366cbb36b23674a54d6bf041818ebb0dc74805f4a03b768ae824228a828f4`  
		Last Modified: Fri, 08 Nov 2024 22:02:34 GMT  
		Size: 358.2 MB (358177754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bda7c84ba833a0500bd603d5f749227b1c5f5c4a960b32d83564e3c1f8c3a51`  
		Last Modified: Fri, 08 Nov 2024 22:01:45 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987fbb35471bf4df0260eb29c3ecb72bcba27e98a3cbde68dee46beeb7f5b7f`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ff4c46982d34facdaad250a9fc691b848473382ac4c316387ebd9ed2d9bdce`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ec019d588cb9b5df05b4d2e8066a69ce65c5b0991d04aee05fda7bc94b4afd`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7eba9a1a5cc8e9a3b3f48aff49a3e72de60de7254946e0720c91d50935c869f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56223613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bdd5b1be9a423e3b72c71e0e7c1469053a671b34db956d6eb2be867658826b`

```dockerfile
```

-	Layers:
	-	`sha256:19fb9b50a593490c66f4ea606225d4045eb825f5c5780f32e15a96233944c668`  
		Last Modified: Fri, 08 Nov 2024 22:02:30 GMT  
		Size: 56.2 MB (56196477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e31a96fd4bd9922f1138ac4afea0d860074d64d983ee7b9c74b5c454ef7c59`  
		Last Modified: Fri, 08 Nov 2024 22:02:29 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1a8adc4fb018a90c25c43b1d8055292014e9f7a33ac4ce85ba314e24c04b2137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.5 MB (654502601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f2f1cda8c3380de42204a158796182cdcd56fa039a66fbc5cc5436001e8c7c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b256dd78da704c0e392e7f41c1e562b2078d1dd6077ec3f63f235c1bd801f558`  
		Last Modified: Fri, 08 Nov 2024 23:17:04 GMT  
		Size: 253.0 MB (252998737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02171ccd35a530c539fa58e8ba735d2e4b12ded8a6929e6eba5b4473b9d4c49`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 14.1 MB (14115479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365fa69c021688334226aa7de66bbb73b8dd3d7eeb7163ebbc36f1818a56728`  
		Last Modified: Fri, 08 Nov 2024 23:16:59 GMT  
		Size: 469.7 KB (469660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5017223533bbab820ecac13a366c0a52b4aa0f74ee756acf63f52052810ca59e`  
		Last Modified: Fri, 08 Nov 2024 23:17:07 GMT  
		Size: 358.0 MB (358030442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b70ec4b530131b883dd073224f04690d6da58c49bb340f5628ec795f917739`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ac167ee87cd60259c73f80fe4a1e16b88b62dedfb6559589515cd0948f0469`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738ea22ed548457804d679c5430f97f5ba43ddf8aedd5db3468bbe9194ec416d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2b74bf531fb0833f4527429727796c63c50213e7ee79420d33899e105ceb6d`  
		Last Modified: Fri, 08 Nov 2024 23:17:01 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:92118c2727e755a33efd0994e0fa8c7ce3660dfbcbb36cad181550d1a127c6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce5ff8746407de30e3f186239510c64776c3b13c33aa54d2baa7a0048d165e6`

```dockerfile
```

-	Layers:
	-	`sha256:52e36b19fd2a60c1372592f0b6bab02118fbc0059f9a43ef824eeb25e037be50`  
		Last Modified: Fri, 08 Nov 2024 23:17:00 GMT  
		Size: 56.2 MB (56203771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814031fbcc6e20794b52b019497fcdec30b5563e239bd2052302afb969aa9feb`  
		Last Modified: Fri, 08 Nov 2024 23:16:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:adfb65412f33f6401cb76eee6774246d0144a8ce505b9b325ce447185de961be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 MB (674679380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd9f225e9037687e046af6dd4508177bc4a405c31dd8053136c670a04329eab`
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
# Fri, 08 Nov 2024 10:31:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 08 Nov 2024 10:31:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 08 Nov 2024 10:31:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Nov 2024 10:31:04 GMT
ARG TARGETARCH
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
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945cad33a894b3838b385b7f86e8c9a7f09d9f28b08d1662aed37ee9120e0900`  
		Last Modified: Fri, 08 Nov 2024 23:33:37 GMT  
		Size: 266.4 MB (266405180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b880cc4226ec4a472884359dc4fe60fe31f2d16f4415d4196ab64c3043aaa9a`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 14.7 MB (14686214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16abe6c780d1671b85d7292ecb4c904c41621e779127970c78bd72e363789a78`  
		Last Modified: Fri, 08 Nov 2024 23:33:18 GMT  
		Size: 469.7 KB (469685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd6609548b3779d46e24cb945478511657c8a3d68b7eccf5d8f3b531bbdd84`  
		Last Modified: Fri, 08 Nov 2024 23:33:41 GMT  
		Size: 358.7 MB (358726895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0048d47977e0aaf532f0843ebba114f247910e75a9f491b89e6f77fcb48caf`  
		Last Modified: Fri, 08 Nov 2024 23:33:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fc06c08cc93340016dd3c08de6a9c9f73822f459742c56aaea8ee6ed4b22ce`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776a8ca243735cf3bfff3fdbce132628b8f7b4525256061d313385c78f6912e`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b185034b6b4f267ede93929d110f1a7cab2ca24220cf82287264037cccf83de0`  
		Last Modified: Fri, 08 Nov 2024 23:33:21 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7da1777b5db83d247555f0e741e04ab897658fdee811e598c1c72b4f0133432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56231818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ca32c79d0d91ebcb64e755d28af5b7136c8287ac0df532fdd678a2d038c5e8`

```dockerfile
```

-	Layers:
	-	`sha256:bd219396a131da5a4c1f8e0cca42dbbc93a7b7c5a5940d8c2f8d4686f3485506`  
		Last Modified: Fri, 08 Nov 2024 23:33:20 GMT  
		Size: 56.2 MB (56204620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3a50d6444ad0a4e709b8af43eaf656c4e34468450466e866ee18f69e53baf0e`  
		Last Modified: Fri, 08 Nov 2024 23:33:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
