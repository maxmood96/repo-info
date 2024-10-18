<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241017`](#odoo160-20241017)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241017`](#odoo170-20241017)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241017`](#odoo180-20241017)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:f625316664baf656a05d3440cb2321ce0ebebc7ef616f3aa54c0829248e7587e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:4cb5be16504b43b0324704e496c76a48b82728a4a05d566e575e05f828267b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584403289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ffe57da1e37c85fcf88dd88935609deb41bffa3b29abe1604cd379764325f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c61e8834d1b8af69711bff624e33205dd5e149c29a0b4807378675824952b`  
		Last Modified: Thu, 17 Oct 2024 21:00:28 GMT  
		Size: 219.6 MB (219599568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9989b58f198b588e5e3aabdaefba2cac592f6256995f169f0766bf39b56c3b`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 2.5 MB (2493896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8972b3593fcceac418ba41eaca0cc4f276767d7157e1012e56dc70243361b02`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 468.5 KB (468461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0772af6591af6a3d54c9712e2e707f5b787d7e6ee71ee046bc1bc2f4df690d2`  
		Last Modified: Thu, 17 Oct 2024 21:00:30 GMT  
		Size: 330.4 MB (330410131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b38647d3dc8f778d0f2d0a677c09bbf02b10c512fa80008fd4349abc9115dd`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a3290b992f5232a12393e3d2db8590dd4921eaefdd864a2f913366da542747`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be181ed56fb6ce4d90fc53f13f613e3624faadb8ffe095d6c674246f67d698f8`  
		Last Modified: Thu, 17 Oct 2024 21:00:28 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:bcce24d35fdcb52fecd0a790f9d5de1555576ac05f4de30f9b3919e0046acfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38803784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a946ccfa4fb479da4d19e1d7d23516f935704e2367be184b6f86dcd8432e277c`

```dockerfile
```

-	Layers:
	-	`sha256:8be10d810a01a1061b90e1d2bed0243a7fa71f93057a31ed224ae6915891efa8`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 38.8 MB (38777204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f75cf5f75bea40c984024daada4f372539d5bc66b02b05e14c9c99b61a0435`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 26.6 KB (26580 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e73a4cedb75b42d3c41ed7c26b5d8f833b696c65c73f25e7080f2a8329da7ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580010232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d26c574f47633ac699b35bca28190c78cb80e588b768553633ce36fa37f013b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a1761ed27ad16aeb90badfaa34b9045d894381b474db7888873410718dcefb`  
		Last Modified: Thu, 17 Oct 2024 13:54:58 GMT  
		Size: 216.9 MB (216899251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956a8c79264ec242cbe31005d9e87fa8e4cacb514332ded2d74db229e6517569`  
		Last Modified: Thu, 17 Oct 2024 13:54:54 GMT  
		Size: 2.5 MB (2504023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda6cf348b966d9cbcb1db85cfae1d84c2db2c0671439d966d0d73f1ca63253a`  
		Last Modified: Thu, 17 Oct 2024 13:54:54 GMT  
		Size: 468.5 KB (468476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677a3e6319c32a1eebeb6d3dd18f45ed829ddc6b2197038a9cac8dae5443e61a`  
		Last Modified: Fri, 18 Oct 2024 00:20:43 GMT  
		Size: 330.1 MB (330060293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae3077c96004ba439f36f057c0bd2a48f96c47782e82de6a842ffc7e88cb71b`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa848d0aab279f7e7d60661bc305f7faa16166f783eb121ca39852780e78707`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54008d32c8a33dc246b9727401c3472798759120346da3d54907a4e9a51ed0a2`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab649811be03299c1ff1361c336f51f29e07ba48e86b25f1a2e32ffab1ec5f11`  
		Last Modified: Fri, 18 Oct 2024 00:20:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:15790619e25be4f52f008577f22a269e96aea742f5d9c6df7452dfde0e85696f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38810401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c532e28b26924a5b3f8ab31a13f92f4f6bba56a88f347a0633a65dc5a85679e`

```dockerfile
```

-	Layers:
	-	`sha256:bc64675d67d015a1cafb56c0c8ecd1a2cc983ffae2933d87d369aee17683538b`  
		Last Modified: Fri, 18 Oct 2024 00:20:37 GMT  
		Size: 38.8 MB (38783676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e916f992abd603c8b18f06ff512997b8e1a5dbc7e5a581e7959292bf4985f6af`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 26.7 KB (26725 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:f625316664baf656a05d3440cb2321ce0ebebc7ef616f3aa54c0829248e7587e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:4cb5be16504b43b0324704e496c76a48b82728a4a05d566e575e05f828267b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584403289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ffe57da1e37c85fcf88dd88935609deb41bffa3b29abe1604cd379764325f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c61e8834d1b8af69711bff624e33205dd5e149c29a0b4807378675824952b`  
		Last Modified: Thu, 17 Oct 2024 21:00:28 GMT  
		Size: 219.6 MB (219599568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9989b58f198b588e5e3aabdaefba2cac592f6256995f169f0766bf39b56c3b`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 2.5 MB (2493896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8972b3593fcceac418ba41eaca0cc4f276767d7157e1012e56dc70243361b02`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 468.5 KB (468461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0772af6591af6a3d54c9712e2e707f5b787d7e6ee71ee046bc1bc2f4df690d2`  
		Last Modified: Thu, 17 Oct 2024 21:00:30 GMT  
		Size: 330.4 MB (330410131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b38647d3dc8f778d0f2d0a677c09bbf02b10c512fa80008fd4349abc9115dd`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a3290b992f5232a12393e3d2db8590dd4921eaefdd864a2f913366da542747`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be181ed56fb6ce4d90fc53f13f613e3624faadb8ffe095d6c674246f67d698f8`  
		Last Modified: Thu, 17 Oct 2024 21:00:28 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:bcce24d35fdcb52fecd0a790f9d5de1555576ac05f4de30f9b3919e0046acfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38803784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a946ccfa4fb479da4d19e1d7d23516f935704e2367be184b6f86dcd8432e277c`

```dockerfile
```

-	Layers:
	-	`sha256:8be10d810a01a1061b90e1d2bed0243a7fa71f93057a31ed224ae6915891efa8`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 38.8 MB (38777204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f75cf5f75bea40c984024daada4f372539d5bc66b02b05e14c9c99b61a0435`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 26.6 KB (26580 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e73a4cedb75b42d3c41ed7c26b5d8f833b696c65c73f25e7080f2a8329da7ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580010232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d26c574f47633ac699b35bca28190c78cb80e588b768553633ce36fa37f013b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a1761ed27ad16aeb90badfaa34b9045d894381b474db7888873410718dcefb`  
		Last Modified: Thu, 17 Oct 2024 13:54:58 GMT  
		Size: 216.9 MB (216899251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956a8c79264ec242cbe31005d9e87fa8e4cacb514332ded2d74db229e6517569`  
		Last Modified: Thu, 17 Oct 2024 13:54:54 GMT  
		Size: 2.5 MB (2504023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda6cf348b966d9cbcb1db85cfae1d84c2db2c0671439d966d0d73f1ca63253a`  
		Last Modified: Thu, 17 Oct 2024 13:54:54 GMT  
		Size: 468.5 KB (468476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677a3e6319c32a1eebeb6d3dd18f45ed829ddc6b2197038a9cac8dae5443e61a`  
		Last Modified: Fri, 18 Oct 2024 00:20:43 GMT  
		Size: 330.1 MB (330060293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae3077c96004ba439f36f057c0bd2a48f96c47782e82de6a842ffc7e88cb71b`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa848d0aab279f7e7d60661bc305f7faa16166f783eb121ca39852780e78707`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54008d32c8a33dc246b9727401c3472798759120346da3d54907a4e9a51ed0a2`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab649811be03299c1ff1361c336f51f29e07ba48e86b25f1a2e32ffab1ec5f11`  
		Last Modified: Fri, 18 Oct 2024 00:20:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:15790619e25be4f52f008577f22a269e96aea742f5d9c6df7452dfde0e85696f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38810401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c532e28b26924a5b3f8ab31a13f92f4f6bba56a88f347a0633a65dc5a85679e`

```dockerfile
```

-	Layers:
	-	`sha256:bc64675d67d015a1cafb56c0c8ecd1a2cc983ffae2933d87d369aee17683538b`  
		Last Modified: Fri, 18 Oct 2024 00:20:37 GMT  
		Size: 38.8 MB (38783676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e916f992abd603c8b18f06ff512997b8e1a5dbc7e5a581e7959292bf4985f6af`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 26.7 KB (26725 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241017`

```console
$ docker pull odoo@sha256:f625316664baf656a05d3440cb2321ce0ebebc7ef616f3aa54c0829248e7587e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20241017` - linux; amd64

```console
$ docker pull odoo@sha256:4cb5be16504b43b0324704e496c76a48b82728a4a05d566e575e05f828267b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584403289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ffe57da1e37c85fcf88dd88935609deb41bffa3b29abe1604cd379764325f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c61e8834d1b8af69711bff624e33205dd5e149c29a0b4807378675824952b`  
		Last Modified: Thu, 17 Oct 2024 21:00:28 GMT  
		Size: 219.6 MB (219599568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9989b58f198b588e5e3aabdaefba2cac592f6256995f169f0766bf39b56c3b`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 2.5 MB (2493896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8972b3593fcceac418ba41eaca0cc4f276767d7157e1012e56dc70243361b02`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 468.5 KB (468461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0772af6591af6a3d54c9712e2e707f5b787d7e6ee71ee046bc1bc2f4df690d2`  
		Last Modified: Thu, 17 Oct 2024 21:00:30 GMT  
		Size: 330.4 MB (330410131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b38647d3dc8f778d0f2d0a677c09bbf02b10c512fa80008fd4349abc9115dd`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a3290b992f5232a12393e3d2db8590dd4921eaefdd864a2f913366da542747`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be181ed56fb6ce4d90fc53f13f613e3624faadb8ffe095d6c674246f67d698f8`  
		Last Modified: Thu, 17 Oct 2024 21:00:28 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241017` - unknown; unknown

```console
$ docker pull odoo@sha256:bcce24d35fdcb52fecd0a790f9d5de1555576ac05f4de30f9b3919e0046acfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38803784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a946ccfa4fb479da4d19e1d7d23516f935704e2367be184b6f86dcd8432e277c`

```dockerfile
```

-	Layers:
	-	`sha256:8be10d810a01a1061b90e1d2bed0243a7fa71f93057a31ed224ae6915891efa8`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 38.8 MB (38777204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f75cf5f75bea40c984024daada4f372539d5bc66b02b05e14c9c99b61a0435`  
		Last Modified: Thu, 17 Oct 2024 21:00:26 GMT  
		Size: 26.6 KB (26580 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20241017` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e73a4cedb75b42d3c41ed7c26b5d8f833b696c65c73f25e7080f2a8329da7ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (580010232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d26c574f47633ac699b35bca28190c78cb80e588b768553633ce36fa37f013b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=16.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=7223ab5d65a42a6d189cdfb5397716a51ef512f9
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a1761ed27ad16aeb90badfaa34b9045d894381b474db7888873410718dcefb`  
		Last Modified: Thu, 17 Oct 2024 13:54:58 GMT  
		Size: 216.9 MB (216899251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956a8c79264ec242cbe31005d9e87fa8e4cacb514332ded2d74db229e6517569`  
		Last Modified: Thu, 17 Oct 2024 13:54:54 GMT  
		Size: 2.5 MB (2504023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda6cf348b966d9cbcb1db85cfae1d84c2db2c0671439d966d0d73f1ca63253a`  
		Last Modified: Thu, 17 Oct 2024 13:54:54 GMT  
		Size: 468.5 KB (468476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677a3e6319c32a1eebeb6d3dd18f45ed829ddc6b2197038a9cac8dae5443e61a`  
		Last Modified: Fri, 18 Oct 2024 00:20:43 GMT  
		Size: 330.1 MB (330060293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae3077c96004ba439f36f057c0bd2a48f96c47782e82de6a842ffc7e88cb71b`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa848d0aab279f7e7d60661bc305f7faa16166f783eb121ca39852780e78707`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54008d32c8a33dc246b9727401c3472798759120346da3d54907a4e9a51ed0a2`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab649811be03299c1ff1361c336f51f29e07ba48e86b25f1a2e32ffab1ec5f11`  
		Last Modified: Fri, 18 Oct 2024 00:20:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241017` - unknown; unknown

```console
$ docker pull odoo@sha256:15790619e25be4f52f008577f22a269e96aea742f5d9c6df7452dfde0e85696f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38810401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c532e28b26924a5b3f8ab31a13f92f4f6bba56a88f347a0633a65dc5a85679e`

```dockerfile
```

-	Layers:
	-	`sha256:bc64675d67d015a1cafb56c0c8ecd1a2cc983ffae2933d87d369aee17683538b`  
		Last Modified: Fri, 18 Oct 2024 00:20:37 GMT  
		Size: 38.8 MB (38783676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e916f992abd603c8b18f06ff512997b8e1a5dbc7e5a581e7959292bf4985f6af`  
		Last Modified: Fri, 18 Oct 2024 00:20:36 GMT  
		Size: 26.7 KB (26725 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:3a54d048673fe009d7bd4da5a2191eb64c3d440eb7bd6e3f9f1efc46dc919499
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
$ docker pull odoo@sha256:95982961c21dad4adcea881427452cbd2427f72282fe159f05bf14620f3bc60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597936877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa75845f2615463df0bc994e845735c3830c673a663be9f2bc3b1ea98235bd4`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2f98e4445ffdab55a32d5496ce1922e1076bbadeb2c764f59f3ca1369b7d36`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 233.8 MB (233763342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708306bb4ac0f79ad89334a1c3050862182d6ef78993aa15f57c2d14fb4ff70a`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 2.4 MB (2405457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3d6f4c9a80dd7f541e17dc2c34a4437c4f66addd105866661314747cd6440`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 469.6 KB (469588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b526e7532304e643d7c1ac498601ebe4ab969eb1f8be3073179601a4b26c0`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 331.8 MB (331760363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af318c2629b92b3852975eeb4ebcc2e47fdda0cbf23f454fc273a991e52be3b`  
		Last Modified: Thu, 17 Oct 2024 21:00:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724842868eeaceb9c444d298e01a61ae05ceac6682e3b5f95c9d26879d827f4`  
		Last Modified: Thu, 17 Oct 2024 21:00:42 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3008e7da099aed23f77c322e13ce77d1298652b0e30298f031bbaededc78519f`  
		Last Modified: Thu, 17 Oct 2024 21:00:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:ccfb2cc9c1ac8bef5f657378899612bae3da8056a2ad82502ab89c83318c1d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39526961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb91f3f7895efe96d1dfdde6632618109834928d12d9a7ef3e4131ee83f62ed`

```dockerfile
```

-	Layers:
	-	`sha256:1604d9b9884ad05431dd53ca40c0b351374d190075fe94527a119e8ee15c7848`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 39.5 MB (39500342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a1768106de7d4fa42ce93084d2857a25517955b86186f30b97de196148461a`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 26.6 KB (26619 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2501a6c0c3b1b8e93a1ae8210144703ee5357cb67872cd632e342ffd444b976f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 MB (592758789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8319e86d2131b2a68c3abae136dfa5b7d6201673408b7ee05b4d8cd9c3394038`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ba2f4275bb3ac7ce58f6f9def22f6fe4169fb446542cadf90cf2eb10afa810`  
		Last Modified: Fri, 18 Oct 2024 00:17:47 GMT  
		Size: 231.2 MB (231157733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b204c8a7d15072279753edccf6ddf17419fbfa3e487e2cd811f6e8193487515`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 2.4 MB (2398299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6fa600f23da413627ff8b7554ba34c744999ae857bd0334a353ba38aee150`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 469.4 KB (469428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c47ce1b554166ab3cc36f36c82b4924da6547ba10e014499e983baaadc3fd1`  
		Last Modified: Fri, 18 Oct 2024 00:17:49 GMT  
		Size: 331.4 MB (331372561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd20aa377bbd6eb55c02f60cb6ae1fabda2ae334eebe800492ead8defa8f1fd`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cad9b7629e4ddfa99b4c2170b212c4601900fa603864afcde942b7fbfa389e`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ce592813654f7c795072e581ab20edb28b29512d548bda6f9ad2696333819`  
		Last Modified: Fri, 18 Oct 2024 00:17:44 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca432e409124316f4dd10442bdd6b507002477aa63c816fa859536a033cb64d7`  
		Last Modified: Fri, 18 Oct 2024 00:17:44 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a287a4c50d3491c92ca3f4f55a02233101e84695c911e234c7f66b7b74f4b956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39533620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbb0b9d85db0d1139c72ab17064629f52ca9806b0c6105ffb911e624b13daf`

```dockerfile
```

-	Layers:
	-	`sha256:fd28bf4a16ebc2323cc7aeb5aee36ed4a76987b4b028c9e90fc76161b6af7ec4`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 39.5 MB (39506855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc4989ac657e419a5a75e589b923184e7c58d48d8e6f67db91dde922917cf9a`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 26.8 KB (26765 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:fc4d5a6096e61910e8b07dabd3e8cdd4028ce8c9758be4b5d0ab6cc23909040a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.4 MB (614404351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075e19eaebf46be549ed8c6bc8cb0654dde85df21d77414590a3b9533fa2e061`
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941509acb92b3b73cb31b92f1454ff27fbb1e63d0f729b870ba762b03a7a28c9`  
		Last Modified: Thu, 17 Oct 2024 21:18:40 GMT  
		Size: 243.3 MB (243293381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c13b4dab18005b95dd0a0696ea4de8679e1baec5024826d53015a0aaae8a66b`  
		Last Modified: Thu, 17 Oct 2024 21:18:25 GMT  
		Size: 2.7 MB (2708324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5c53871087752d8edc9f7e81d0a36698f361eabe34dc07b1e4685bb99c194`  
		Last Modified: Thu, 17 Oct 2024 21:18:25 GMT  
		Size: 469.5 KB (469454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df58e996580397a8986197ec0b71be38c71d7b3dbc2c8a087ae733a57abc6b2`  
		Last Modified: Thu, 17 Oct 2024 21:18:48 GMT  
		Size: 333.5 MB (333482507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848a460c0e0cb1b53df3c421a6d68dc90012ccb6132b7cabf22d0865baca9716`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eedbb0a067e5ccd282438f7b89a24296e530cbe495e84a9363bc8012bdc21e`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3d27bde6dbd950ef7241bd992e7474ba774df27f362694e1f73c2e641e8c3d`  
		Last Modified: Thu, 17 Oct 2024 21:18:27 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e10ebf52830d0e713f61acb2ad5e70ae2b77e7a96774486c4b58b7001a8ccfc`  
		Last Modified: Thu, 17 Oct 2024 21:18:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:317188900b70ec0052343ecc72cc358055fa35b2764559d95459eef2eba27bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39535318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af04a2a9cdf583b37f35ec5054b078246327f205317f71e7d21f4a48c0f3aa9d`

```dockerfile
```

-	Layers:
	-	`sha256:0da024bb25122a51b607af93198fcffe855be019ef16946ec4f3d79268871b55`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 39.5 MB (39508649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd20e8d8a176f932e74e46dbdca414b49dba8fa89b5b0821924f55d2716f506`  
		Last Modified: Thu, 17 Oct 2024 21:18:24 GMT  
		Size: 26.7 KB (26669 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:3a54d048673fe009d7bd4da5a2191eb64c3d440eb7bd6e3f9f1efc46dc919499
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
$ docker pull odoo@sha256:95982961c21dad4adcea881427452cbd2427f72282fe159f05bf14620f3bc60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597936877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa75845f2615463df0bc994e845735c3830c673a663be9f2bc3b1ea98235bd4`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2f98e4445ffdab55a32d5496ce1922e1076bbadeb2c764f59f3ca1369b7d36`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 233.8 MB (233763342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708306bb4ac0f79ad89334a1c3050862182d6ef78993aa15f57c2d14fb4ff70a`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 2.4 MB (2405457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3d6f4c9a80dd7f541e17dc2c34a4437c4f66addd105866661314747cd6440`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 469.6 KB (469588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b526e7532304e643d7c1ac498601ebe4ab969eb1f8be3073179601a4b26c0`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 331.8 MB (331760363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af318c2629b92b3852975eeb4ebcc2e47fdda0cbf23f454fc273a991e52be3b`  
		Last Modified: Thu, 17 Oct 2024 21:00:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724842868eeaceb9c444d298e01a61ae05ceac6682e3b5f95c9d26879d827f4`  
		Last Modified: Thu, 17 Oct 2024 21:00:42 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3008e7da099aed23f77c322e13ce77d1298652b0e30298f031bbaededc78519f`  
		Last Modified: Thu, 17 Oct 2024 21:00:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ccfb2cc9c1ac8bef5f657378899612bae3da8056a2ad82502ab89c83318c1d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39526961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb91f3f7895efe96d1dfdde6632618109834928d12d9a7ef3e4131ee83f62ed`

```dockerfile
```

-	Layers:
	-	`sha256:1604d9b9884ad05431dd53ca40c0b351374d190075fe94527a119e8ee15c7848`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 39.5 MB (39500342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a1768106de7d4fa42ce93084d2857a25517955b86186f30b97de196148461a`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 26.6 KB (26619 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2501a6c0c3b1b8e93a1ae8210144703ee5357cb67872cd632e342ffd444b976f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 MB (592758789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8319e86d2131b2a68c3abae136dfa5b7d6201673408b7ee05b4d8cd9c3394038`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ba2f4275bb3ac7ce58f6f9def22f6fe4169fb446542cadf90cf2eb10afa810`  
		Last Modified: Fri, 18 Oct 2024 00:17:47 GMT  
		Size: 231.2 MB (231157733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b204c8a7d15072279753edccf6ddf17419fbfa3e487e2cd811f6e8193487515`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 2.4 MB (2398299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6fa600f23da413627ff8b7554ba34c744999ae857bd0334a353ba38aee150`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 469.4 KB (469428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c47ce1b554166ab3cc36f36c82b4924da6547ba10e014499e983baaadc3fd1`  
		Last Modified: Fri, 18 Oct 2024 00:17:49 GMT  
		Size: 331.4 MB (331372561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd20aa377bbd6eb55c02f60cb6ae1fabda2ae334eebe800492ead8defa8f1fd`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cad9b7629e4ddfa99b4c2170b212c4601900fa603864afcde942b7fbfa389e`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ce592813654f7c795072e581ab20edb28b29512d548bda6f9ad2696333819`  
		Last Modified: Fri, 18 Oct 2024 00:17:44 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca432e409124316f4dd10442bdd6b507002477aa63c816fa859536a033cb64d7`  
		Last Modified: Fri, 18 Oct 2024 00:17:44 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a287a4c50d3491c92ca3f4f55a02233101e84695c911e234c7f66b7b74f4b956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39533620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbb0b9d85db0d1139c72ab17064629f52ca9806b0c6105ffb911e624b13daf`

```dockerfile
```

-	Layers:
	-	`sha256:fd28bf4a16ebc2323cc7aeb5aee36ed4a76987b4b028c9e90fc76161b6af7ec4`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 39.5 MB (39506855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc4989ac657e419a5a75e589b923184e7c58d48d8e6f67db91dde922917cf9a`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 26.8 KB (26765 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:fc4d5a6096e61910e8b07dabd3e8cdd4028ce8c9758be4b5d0ab6cc23909040a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.4 MB (614404351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075e19eaebf46be549ed8c6bc8cb0654dde85df21d77414590a3b9533fa2e061`
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941509acb92b3b73cb31b92f1454ff27fbb1e63d0f729b870ba762b03a7a28c9`  
		Last Modified: Thu, 17 Oct 2024 21:18:40 GMT  
		Size: 243.3 MB (243293381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c13b4dab18005b95dd0a0696ea4de8679e1baec5024826d53015a0aaae8a66b`  
		Last Modified: Thu, 17 Oct 2024 21:18:25 GMT  
		Size: 2.7 MB (2708324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5c53871087752d8edc9f7e81d0a36698f361eabe34dc07b1e4685bb99c194`  
		Last Modified: Thu, 17 Oct 2024 21:18:25 GMT  
		Size: 469.5 KB (469454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df58e996580397a8986197ec0b71be38c71d7b3dbc2c8a087ae733a57abc6b2`  
		Last Modified: Thu, 17 Oct 2024 21:18:48 GMT  
		Size: 333.5 MB (333482507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848a460c0e0cb1b53df3c421a6d68dc90012ccb6132b7cabf22d0865baca9716`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eedbb0a067e5ccd282438f7b89a24296e530cbe495e84a9363bc8012bdc21e`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3d27bde6dbd950ef7241bd992e7474ba774df27f362694e1f73c2e641e8c3d`  
		Last Modified: Thu, 17 Oct 2024 21:18:27 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e10ebf52830d0e713f61acb2ad5e70ae2b77e7a96774486c4b58b7001a8ccfc`  
		Last Modified: Thu, 17 Oct 2024 21:18:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:317188900b70ec0052343ecc72cc358055fa35b2764559d95459eef2eba27bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39535318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af04a2a9cdf583b37f35ec5054b078246327f205317f71e7d21f4a48c0f3aa9d`

```dockerfile
```

-	Layers:
	-	`sha256:0da024bb25122a51b607af93198fcffe855be019ef16946ec4f3d79268871b55`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 39.5 MB (39508649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd20e8d8a176f932e74e46dbdca414b49dba8fa89b5b0821924f55d2716f506`  
		Last Modified: Thu, 17 Oct 2024 21:18:24 GMT  
		Size: 26.7 KB (26669 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241017`

```console
$ docker pull odoo@sha256:3a54d048673fe009d7bd4da5a2191eb64c3d440eb7bd6e3f9f1efc46dc919499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241017` - linux; amd64

```console
$ docker pull odoo@sha256:95982961c21dad4adcea881427452cbd2427f72282fe159f05bf14620f3bc60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597936877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa75845f2615463df0bc994e845735c3830c673a663be9f2bc3b1ea98235bd4`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2f98e4445ffdab55a32d5496ce1922e1076bbadeb2c764f59f3ca1369b7d36`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 233.8 MB (233763342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708306bb4ac0f79ad89334a1c3050862182d6ef78993aa15f57c2d14fb4ff70a`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 2.4 MB (2405457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3d6f4c9a80dd7f541e17dc2c34a4437c4f66addd105866661314747cd6440`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 469.6 KB (469588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26b526e7532304e643d7c1ac498601ebe4ab969eb1f8be3073179601a4b26c0`  
		Last Modified: Thu, 17 Oct 2024 21:00:45 GMT  
		Size: 331.8 MB (331760363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af318c2629b92b3852975eeb4ebcc2e47fdda0cbf23f454fc273a991e52be3b`  
		Last Modified: Thu, 17 Oct 2024 21:00:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724842868eeaceb9c444d298e01a61ae05ceac6682e3b5f95c9d26879d827f4`  
		Last Modified: Thu, 17 Oct 2024 21:00:42 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3008e7da099aed23f77c322e13ce77d1298652b0e30298f031bbaededc78519f`  
		Last Modified: Thu, 17 Oct 2024 21:00:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241017` - unknown; unknown

```console
$ docker pull odoo@sha256:ccfb2cc9c1ac8bef5f657378899612bae3da8056a2ad82502ab89c83318c1d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39526961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb91f3f7895efe96d1dfdde6632618109834928d12d9a7ef3e4131ee83f62ed`

```dockerfile
```

-	Layers:
	-	`sha256:1604d9b9884ad05431dd53ca40c0b351374d190075fe94527a119e8ee15c7848`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 39.5 MB (39500342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a1768106de7d4fa42ce93084d2857a25517955b86186f30b97de196148461a`  
		Last Modified: Thu, 17 Oct 2024 21:00:41 GMT  
		Size: 26.6 KB (26619 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241017` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:2501a6c0c3b1b8e93a1ae8210144703ee5357cb67872cd632e342ffd444b976f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 MB (592758789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8319e86d2131b2a68c3abae136dfa5b7d6201673408b7ee05b4d8cd9c3394038`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ba2f4275bb3ac7ce58f6f9def22f6fe4169fb446542cadf90cf2eb10afa810`  
		Last Modified: Fri, 18 Oct 2024 00:17:47 GMT  
		Size: 231.2 MB (231157733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b204c8a7d15072279753edccf6ddf17419fbfa3e487e2cd811f6e8193487515`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 2.4 MB (2398299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6fa600f23da413627ff8b7554ba34c744999ae857bd0334a353ba38aee150`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 469.4 KB (469428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c47ce1b554166ab3cc36f36c82b4924da6547ba10e014499e983baaadc3fd1`  
		Last Modified: Fri, 18 Oct 2024 00:17:49 GMT  
		Size: 331.4 MB (331372561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd20aa377bbd6eb55c02f60cb6ae1fabda2ae334eebe800492ead8defa8f1fd`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cad9b7629e4ddfa99b4c2170b212c4601900fa603864afcde942b7fbfa389e`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ce592813654f7c795072e581ab20edb28b29512d548bda6f9ad2696333819`  
		Last Modified: Fri, 18 Oct 2024 00:17:44 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca432e409124316f4dd10442bdd6b507002477aa63c816fa859536a033cb64d7`  
		Last Modified: Fri, 18 Oct 2024 00:17:44 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241017` - unknown; unknown

```console
$ docker pull odoo@sha256:a287a4c50d3491c92ca3f4f55a02233101e84695c911e234c7f66b7b74f4b956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39533620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bbb0b9d85db0d1139c72ab17064629f52ca9806b0c6105ffb911e624b13daf`

```dockerfile
```

-	Layers:
	-	`sha256:fd28bf4a16ebc2323cc7aeb5aee36ed4a76987b4b028c9e90fc76161b6af7ec4`  
		Last Modified: Fri, 18 Oct 2024 00:17:43 GMT  
		Size: 39.5 MB (39506855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc4989ac657e419a5a75e589b923184e7c58d48d8e6f67db91dde922917cf9a`  
		Last Modified: Fri, 18 Oct 2024 00:17:42 GMT  
		Size: 26.8 KB (26765 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241017` - linux; ppc64le

```console
$ docker pull odoo@sha256:fc4d5a6096e61910e8b07dabd3e8cdd4028ce8c9758be4b5d0ab6cc23909040a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.4 MB (614404351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075e19eaebf46be549ed8c6bc8cb0654dde85df21d77414590a3b9533fa2e061`
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=17.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241017 ODOO_SHA=e5d7e6c6d011698cb6589e2a9b717caaac69df35
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
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941509acb92b3b73cb31b92f1454ff27fbb1e63d0f729b870ba762b03a7a28c9`  
		Last Modified: Thu, 17 Oct 2024 21:18:40 GMT  
		Size: 243.3 MB (243293381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c13b4dab18005b95dd0a0696ea4de8679e1baec5024826d53015a0aaae8a66b`  
		Last Modified: Thu, 17 Oct 2024 21:18:25 GMT  
		Size: 2.7 MB (2708324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5c53871087752d8edc9f7e81d0a36698f361eabe34dc07b1e4685bb99c194`  
		Last Modified: Thu, 17 Oct 2024 21:18:25 GMT  
		Size: 469.5 KB (469454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df58e996580397a8986197ec0b71be38c71d7b3dbc2c8a087ae733a57abc6b2`  
		Last Modified: Thu, 17 Oct 2024 21:18:48 GMT  
		Size: 333.5 MB (333482507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848a460c0e0cb1b53df3c421a6d68dc90012ccb6132b7cabf22d0865baca9716`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82eedbb0a067e5ccd282438f7b89a24296e530cbe495e84a9363bc8012bdc21e`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3d27bde6dbd950ef7241bd992e7474ba774df27f362694e1f73c2e641e8c3d`  
		Last Modified: Thu, 17 Oct 2024 21:18:27 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e10ebf52830d0e713f61acb2ad5e70ae2b77e7a96774486c4b58b7001a8ccfc`  
		Last Modified: Thu, 17 Oct 2024 21:18:27 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241017` - unknown; unknown

```console
$ docker pull odoo@sha256:317188900b70ec0052343ecc72cc358055fa35b2764559d95459eef2eba27bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39535318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af04a2a9cdf583b37f35ec5054b078246327f205317f71e7d21f4a48c0f3aa9d`

```dockerfile
```

-	Layers:
	-	`sha256:0da024bb25122a51b607af93198fcffe855be019ef16946ec4f3d79268871b55`  
		Last Modified: Thu, 17 Oct 2024 21:18:26 GMT  
		Size: 39.5 MB (39508649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd20e8d8a176f932e74e46dbdca414b49dba8fa89b5b0821924f55d2716f506`  
		Last Modified: Thu, 17 Oct 2024 21:18:24 GMT  
		Size: 26.7 KB (26669 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:6691ff61b15ce8817efe27273fcfe71e3e5b7d33a52ecf66d5c48ce7f9ddb254
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
$ docker pull odoo@sha256:ef0d31df078d09ddb797a72df6eab78e50887d6e1de214347cde205e550f57f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.3 MB (654326132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9872023cb8afd49eb858caa038e42064d529f4a166726c9f3bdcbe462a054e54`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc86e2d02e7fe1e2d279ac93fbb548747f0b603130d965ceb6e77f21b9d2b1`  
		Last Modified: Thu, 17 Oct 2024 21:01:15 GMT  
		Size: 255.6 MB (255640631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bc0a33b7ac3a3eb7427e248c83deca6ff00c1039d982894a6871e0f1710578`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 14.1 MB (14142285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10f2415553b172f4bc15ab4b6093cd34bdecf0729b30c4fcaa77d500bd8151`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 469.2 KB (469184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2bc153b51bc7ed997e3e4b5b50f5f73c7c0ec7f503094e738f1d1aa9b9be3`  
		Last Modified: Thu, 17 Oct 2024 21:01:17 GMT  
		Size: 354.3 MB (354321225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec48f6088b329208bc687bb52713fc9cf7e10accc74cfb2896b5be32a63151e`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06cd21e7d7c8189413af58167022ed3f8411f5408fe973e4e85e547e965ef6d`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eae684dedf6619026fc7df36c63e3ceda0f7915f720d810df2258b5ff7a94`  
		Last Modified: Thu, 17 Oct 2024 21:01:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7e619817d1eb977478e39bd7436df86e81d6cfba03c5aa16bd5dcab85a6c1102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55502298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acba12b5723fa2b5190d24a3f344fc3afa46b2805324b45c482bc2660c45827b`

```dockerfile
```

-	Layers:
	-	`sha256:e40d36202e0d2e121c7c70c79fa8368588cbbf64acacad8b7f67374bbf137219`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 55.5 MB (55475378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d87ae6f6c03f3113c8b6282ccb58389a5055440e24ef9e77a75190c60a2a24`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 26.9 KB (26920 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:28773f71d88334362048623ff48db7140f6b7c6041862d2f36da61ca965b1581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650660425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094289930a8330466b7d1076eb0f5b522723ebeaf93d5aa38a94340cb1cfa62f`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:44603eeaa0a2caa90bff30ffeb0a9a9633a7fc80d248661090778b787551c286`  
		Last Modified: Fri, 18 Oct 2024 00:10:27 GMT  
		Size: 354.2 MB (354184033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb82f0e37b31ff9016c2ab5df73102768fb715c4ef93b8dc8c26888587f373d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e495fd24ea24052955c43e027b43897e78c83beb045b0aacaab5f6585551e4d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa82569752d7a87bae0a2c281a2a72166a0b48ce4eeeac2f2c8cb7037f83f3`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9515b3ced336fc58165c976ef1f74316af5672543e6c7af6c656f24fe84640c6`  
		Last Modified: Fri, 18 Oct 2024 00:10:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:a0233f1f712a6388ac1d70a3e4940ac871b66edb6dec32cae901e33b4248b08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55509750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4005bee07146b63612ed221daecd0c650f570c6218a0bad39aa905f3e48219`

```dockerfile
```

-	Layers:
	-	`sha256:fa945b99afed7745375c767a324d1cda2d5e4a897d027c07173577a94a3053ce`  
		Last Modified: Fri, 18 Oct 2024 00:10:21 GMT  
		Size: 55.5 MB (55482672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8606da8b322173f7d303d2e6f4c9b5600b3e30b084655bf72dabe50fdd4bb4ac`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

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

### `odoo:18` - unknown; unknown

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

## `odoo:18.0`

```console
$ docker pull odoo@sha256:6691ff61b15ce8817efe27273fcfe71e3e5b7d33a52ecf66d5c48ce7f9ddb254
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
$ docker pull odoo@sha256:ef0d31df078d09ddb797a72df6eab78e50887d6e1de214347cde205e550f57f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.3 MB (654326132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9872023cb8afd49eb858caa038e42064d529f4a166726c9f3bdcbe462a054e54`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc86e2d02e7fe1e2d279ac93fbb548747f0b603130d965ceb6e77f21b9d2b1`  
		Last Modified: Thu, 17 Oct 2024 21:01:15 GMT  
		Size: 255.6 MB (255640631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bc0a33b7ac3a3eb7427e248c83deca6ff00c1039d982894a6871e0f1710578`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 14.1 MB (14142285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10f2415553b172f4bc15ab4b6093cd34bdecf0729b30c4fcaa77d500bd8151`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 469.2 KB (469184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2bc153b51bc7ed997e3e4b5b50f5f73c7c0ec7f503094e738f1d1aa9b9be3`  
		Last Modified: Thu, 17 Oct 2024 21:01:17 GMT  
		Size: 354.3 MB (354321225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec48f6088b329208bc687bb52713fc9cf7e10accc74cfb2896b5be32a63151e`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06cd21e7d7c8189413af58167022ed3f8411f5408fe973e4e85e547e965ef6d`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eae684dedf6619026fc7df36c63e3ceda0f7915f720d810df2258b5ff7a94`  
		Last Modified: Thu, 17 Oct 2024 21:01:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7e619817d1eb977478e39bd7436df86e81d6cfba03c5aa16bd5dcab85a6c1102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55502298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acba12b5723fa2b5190d24a3f344fc3afa46b2805324b45c482bc2660c45827b`

```dockerfile
```

-	Layers:
	-	`sha256:e40d36202e0d2e121c7c70c79fa8368588cbbf64acacad8b7f67374bbf137219`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 55.5 MB (55475378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d87ae6f6c03f3113c8b6282ccb58389a5055440e24ef9e77a75190c60a2a24`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 26.9 KB (26920 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:28773f71d88334362048623ff48db7140f6b7c6041862d2f36da61ca965b1581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650660425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094289930a8330466b7d1076eb0f5b522723ebeaf93d5aa38a94340cb1cfa62f`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:44603eeaa0a2caa90bff30ffeb0a9a9633a7fc80d248661090778b787551c286`  
		Last Modified: Fri, 18 Oct 2024 00:10:27 GMT  
		Size: 354.2 MB (354184033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb82f0e37b31ff9016c2ab5df73102768fb715c4ef93b8dc8c26888587f373d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e495fd24ea24052955c43e027b43897e78c83beb045b0aacaab5f6585551e4d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa82569752d7a87bae0a2c281a2a72166a0b48ce4eeeac2f2c8cb7037f83f3`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9515b3ced336fc58165c976ef1f74316af5672543e6c7af6c656f24fe84640c6`  
		Last Modified: Fri, 18 Oct 2024 00:10:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a0233f1f712a6388ac1d70a3e4940ac871b66edb6dec32cae901e33b4248b08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55509750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4005bee07146b63612ed221daecd0c650f570c6218a0bad39aa905f3e48219`

```dockerfile
```

-	Layers:
	-	`sha256:fa945b99afed7745375c767a324d1cda2d5e4a897d027c07173577a94a3053ce`  
		Last Modified: Fri, 18 Oct 2024 00:10:21 GMT  
		Size: 55.5 MB (55482672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8606da8b322173f7d303d2e6f4c9b5600b3e30b084655bf72dabe50fdd4bb4ac`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

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

### `odoo:18.0` - unknown; unknown

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

## `odoo:18.0-20241017`

```console
$ docker pull odoo@sha256:6691ff61b15ce8817efe27273fcfe71e3e5b7d33a52ecf66d5c48ce7f9ddb254
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241017` - linux; amd64

```console
$ docker pull odoo@sha256:ef0d31df078d09ddb797a72df6eab78e50887d6e1de214347cde205e550f57f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.3 MB (654326132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9872023cb8afd49eb858caa038e42064d529f4a166726c9f3bdcbe462a054e54`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc86e2d02e7fe1e2d279ac93fbb548747f0b603130d965ceb6e77f21b9d2b1`  
		Last Modified: Thu, 17 Oct 2024 21:01:15 GMT  
		Size: 255.6 MB (255640631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bc0a33b7ac3a3eb7427e248c83deca6ff00c1039d982894a6871e0f1710578`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 14.1 MB (14142285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10f2415553b172f4bc15ab4b6093cd34bdecf0729b30c4fcaa77d500bd8151`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 469.2 KB (469184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2bc153b51bc7ed997e3e4b5b50f5f73c7c0ec7f503094e738f1d1aa9b9be3`  
		Last Modified: Thu, 17 Oct 2024 21:01:17 GMT  
		Size: 354.3 MB (354321225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec48f6088b329208bc687bb52713fc9cf7e10accc74cfb2896b5be32a63151e`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06cd21e7d7c8189413af58167022ed3f8411f5408fe973e4e85e547e965ef6d`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eae684dedf6619026fc7df36c63e3ceda0f7915f720d810df2258b5ff7a94`  
		Last Modified: Thu, 17 Oct 2024 21:01:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241017` - unknown; unknown

```console
$ docker pull odoo@sha256:7e619817d1eb977478e39bd7436df86e81d6cfba03c5aa16bd5dcab85a6c1102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55502298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acba12b5723fa2b5190d24a3f344fc3afa46b2805324b45c482bc2660c45827b`

```dockerfile
```

-	Layers:
	-	`sha256:e40d36202e0d2e121c7c70c79fa8368588cbbf64acacad8b7f67374bbf137219`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 55.5 MB (55475378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d87ae6f6c03f3113c8b6282ccb58389a5055440e24ef9e77a75190c60a2a24`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 26.9 KB (26920 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241017` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:28773f71d88334362048623ff48db7140f6b7c6041862d2f36da61ca965b1581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650660425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094289930a8330466b7d1076eb0f5b522723ebeaf93d5aa38a94340cb1cfa62f`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:44603eeaa0a2caa90bff30ffeb0a9a9633a7fc80d248661090778b787551c286`  
		Last Modified: Fri, 18 Oct 2024 00:10:27 GMT  
		Size: 354.2 MB (354184033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb82f0e37b31ff9016c2ab5df73102768fb715c4ef93b8dc8c26888587f373d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e495fd24ea24052955c43e027b43897e78c83beb045b0aacaab5f6585551e4d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa82569752d7a87bae0a2c281a2a72166a0b48ce4eeeac2f2c8cb7037f83f3`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9515b3ced336fc58165c976ef1f74316af5672543e6c7af6c656f24fe84640c6`  
		Last Modified: Fri, 18 Oct 2024 00:10:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241017` - unknown; unknown

```console
$ docker pull odoo@sha256:a0233f1f712a6388ac1d70a3e4940ac871b66edb6dec32cae901e33b4248b08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55509750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4005bee07146b63612ed221daecd0c650f570c6218a0bad39aa905f3e48219`

```dockerfile
```

-	Layers:
	-	`sha256:fa945b99afed7745375c767a324d1cda2d5e4a897d027c07173577a94a3053ce`  
		Last Modified: Fri, 18 Oct 2024 00:10:21 GMT  
		Size: 55.5 MB (55482672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8606da8b322173f7d303d2e6f4c9b5600b3e30b084655bf72dabe50fdd4bb4ac`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241017` - linux; ppc64le

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

### `odoo:18.0-20241017` - unknown; unknown

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

## `odoo:latest`

```console
$ docker pull odoo@sha256:6691ff61b15ce8817efe27273fcfe71e3e5b7d33a52ecf66d5c48ce7f9ddb254
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
$ docker pull odoo@sha256:ef0d31df078d09ddb797a72df6eab78e50887d6e1de214347cde205e550f57f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.3 MB (654326132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9872023cb8afd49eb858caa038e42064d529f4a166726c9f3bdcbe462a054e54`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badc86e2d02e7fe1e2d279ac93fbb548747f0b603130d965ceb6e77f21b9d2b1`  
		Last Modified: Thu, 17 Oct 2024 21:01:15 GMT  
		Size: 255.6 MB (255640631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37bc0a33b7ac3a3eb7427e248c83deca6ff00c1039d982894a6871e0f1710578`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 14.1 MB (14142285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10f2415553b172f4bc15ab4b6093cd34bdecf0729b30c4fcaa77d500bd8151`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 469.2 KB (469184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2bc153b51bc7ed997e3e4b5b50f5f73c7c0ec7f503094e738f1d1aa9b9be3`  
		Last Modified: Thu, 17 Oct 2024 21:01:17 GMT  
		Size: 354.3 MB (354321225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebdc18a75a8d8277caa7cb51eb2fdb668b699f100d1ee9f72e781f366874dcb`  
		Last Modified: Thu, 17 Oct 2024 21:00:27 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec48f6088b329208bc687bb52713fc9cf7e10accc74cfb2896b5be32a63151e`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06cd21e7d7c8189413af58167022ed3f8411f5408fe973e4e85e547e965ef6d`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eae684dedf6619026fc7df36c63e3ceda0f7915f720d810df2258b5ff7a94`  
		Last Modified: Thu, 17 Oct 2024 21:01:13 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7e619817d1eb977478e39bd7436df86e81d6cfba03c5aa16bd5dcab85a6c1102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55502298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acba12b5723fa2b5190d24a3f344fc3afa46b2805324b45c482bc2660c45827b`

```dockerfile
```

-	Layers:
	-	`sha256:e40d36202e0d2e121c7c70c79fa8368588cbbf64acacad8b7f67374bbf137219`  
		Last Modified: Thu, 17 Oct 2024 21:01:12 GMT  
		Size: 55.5 MB (55475378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d87ae6f6c03f3113c8b6282ccb58389a5055440e24ef9e77a75190c60a2a24`  
		Last Modified: Thu, 17 Oct 2024 21:01:11 GMT  
		Size: 26.9 KB (26920 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:28773f71d88334362048623ff48db7140f6b7c6041862d2f36da61ca965b1581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650660425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094289930a8330466b7d1076eb0f5b522723ebeaf93d5aa38a94340cb1cfa62f`
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
# Thu, 17 Oct 2024 13:36:11 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 17 Oct 2024 13:36:11 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 17 Oct 2024 13:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 17 Oct 2024 13:36:11 GMT
ARG TARGETARCH
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
ENV ODOO_VERSION=18.0
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_RELEASE=20241017
# Thu, 17 Oct 2024 13:36:11 GMT
ARG ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 17 Oct 2024 13:36:11 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241017 ODOO_SHA=dc1c1e8bb1323fd32ce1bd830bb1d6c6d93098c7
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
	-	`sha256:44603eeaa0a2caa90bff30ffeb0a9a9633a7fc80d248661090778b787551c286`  
		Last Modified: Fri, 18 Oct 2024 00:10:27 GMT  
		Size: 354.2 MB (354184033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb82f0e37b31ff9016c2ab5df73102768fb715c4ef93b8dc8c26888587f373d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e495fd24ea24052955c43e027b43897e78c83beb045b0aacaab5f6585551e4d`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fa82569752d7a87bae0a2c281a2a72166a0b48ce4eeeac2f2c8cb7037f83f3`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9515b3ced336fc58165c976ef1f74316af5672543e6c7af6c656f24fe84640c6`  
		Last Modified: Fri, 18 Oct 2024 00:10:20 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:a0233f1f712a6388ac1d70a3e4940ac871b66edb6dec32cae901e33b4248b08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55509750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4005bee07146b63612ed221daecd0c650f570c6218a0bad39aa905f3e48219`

```dockerfile
```

-	Layers:
	-	`sha256:fa945b99afed7745375c767a324d1cda2d5e4a897d027c07173577a94a3053ce`  
		Last Modified: Fri, 18 Oct 2024 00:10:21 GMT  
		Size: 55.5 MB (55482672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8606da8b322173f7d303d2e6f4c9b5600b3e30b084655bf72dabe50fdd4bb4ac`  
		Last Modified: Fri, 18 Oct 2024 00:10:19 GMT  
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
