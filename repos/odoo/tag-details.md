<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241125`](#odoo160-20241125)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241125`](#odoo170-20241125)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241125`](#odoo180-20241125)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:4b11bd27f34f5e44eebf5a7cc6048bd5ef71c99525ab90b95968e0dd42eae395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:7e232ffac82bf02a1be4a9da7454d080e8bf2204bc6380403460114eb14a9f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584835716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4e858674d35a88b21a997ebe1dfa7d84f534ade6d0fc4b43c9721f6d6b2325`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b01be562f53e40a748ab80cc7332bcf52d34a666f4605ea9a1eca6810e248d`  
		Last Modified: Mon, 25 Nov 2024 20:26:51 GMT  
		Size: 219.6 MB (219605720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4259a4043a00942d119c9dd4f5ecba3840562a10777b4e717602747f7076a8f2`  
		Last Modified: Mon, 25 Nov 2024 20:26:46 GMT  
		Size: 2.6 MB (2575925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da696bed9510ee87c8e15f556c203b199ab0671c2c70cfdf291a2ce2428ed243`  
		Last Modified: Mon, 25 Nov 2024 20:26:46 GMT  
		Size: 469.0 KB (469002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e1ff456b73816d9e82e028672d8d486dd289c2ac473db51c28b7017933c26`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 330.7 MB (330731073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef263ff77a3eb88e778f6943e044b6fc5e8f4c0eee128e21dfeb975a5849dc58`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec87014b3795e6e7363d69e710aedb0ba05512d6cef2ca8077cce4db91bc82d`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3731d2251a7978f7d08605b6301b86afde30a0e20b600d99576edbbb1638ec`  
		Last Modified: Mon, 25 Nov 2024 20:26:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cee2aec29e7a8ee661f622e82a2d3265341a4a0c8b139dd84b359a2f336a54d`  
		Last Modified: Mon, 25 Nov 2024 20:26:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:f6e04ce313343613524fd1ed99086f01dcec1892bc1c0a2c79980822f86454a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38892875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad1bec682dd6b6247c29c3a3614015ca58cfd6d169feb6e97381930344ac50`

```dockerfile
```

-	Layers:
	-	`sha256:587604f8b5d33d84decb06c9fbdcc06d84f9c9ec744213bfac7c63d4e92e5a50`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 38.9 MB (38866157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfafe5bda6028255f7ee3c9aaa785990008bc39bd16b6504429840195443e4d`  
		Last Modified: Mon, 25 Nov 2024 20:26:45 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e051491e75658a1eb669473267149a5822909b5fb327d9138013e3fb481b3f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580453062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16875e0056a4bff46723cf738d60f1366a94a175d3eff4d697b4979c9c216fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689abbf96956f625195182ac751906675f167eb79691c2d19bfa0593c6afa2c`  
		Last Modified: Mon, 18 Nov 2024 19:50:17 GMT  
		Size: 216.9 MB (216917317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073696c45fa176ea3f3fc4544f520fff34daacfdb49459ec9007c9702204c0b`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 2.6 MB (2583786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8a28c9d2e01dd95537d21c9026332df53afacfcd4af98db8dd25fa1dcec19`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 469.1 KB (469084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7074457b40194490ed3c184af02aacc4af5ac4c09a0a65f860bb1b1c1031cbb4`  
		Last Modified: Mon, 25 Nov 2024 20:38:43 GMT  
		Size: 330.4 MB (330388846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5546c4da3d0832f98844767ceb84c8458769cf9b32b14fe7847eea5d4a936b`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52be9f9c93882ea19f983214512424d18315ec29c088e513e76e23994b19bb8`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa8d5b2f37f3ee3975fe0380eace6c8790029f7fa60e78771777118b655697`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e99dcc784558c816ec25b9e36df5f72779742e92163b75df8ccbf9792bd288`  
		Last Modified: Mon, 25 Nov 2024 20:38:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:dfa96b740fe626c327ae2d9793f4d2a1c4e4477e5fc68fc9de849d6edaaf8ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff22b7c21f5c056f7c68eb3bc54f54eb3c23d8dcaab3d5cf48eb2757b0facfc`

```dockerfile
```

-	Layers:
	-	`sha256:6e564cb43960687b4cdcad2e746d58d9cd6c74e1c678f3e6d64925865106337f`  
		Last Modified: Mon, 25 Nov 2024 20:38:37 GMT  
		Size: 38.9 MB (38872633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16165af0824d57acbb9fee4c8bdb26ac5998c1a5b18aa5a4ef22f8e03159fda`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:4b11bd27f34f5e44eebf5a7cc6048bd5ef71c99525ab90b95968e0dd42eae395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:7e232ffac82bf02a1be4a9da7454d080e8bf2204bc6380403460114eb14a9f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584835716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4e858674d35a88b21a997ebe1dfa7d84f534ade6d0fc4b43c9721f6d6b2325`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b01be562f53e40a748ab80cc7332bcf52d34a666f4605ea9a1eca6810e248d`  
		Last Modified: Mon, 25 Nov 2024 20:26:51 GMT  
		Size: 219.6 MB (219605720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4259a4043a00942d119c9dd4f5ecba3840562a10777b4e717602747f7076a8f2`  
		Last Modified: Mon, 25 Nov 2024 20:26:46 GMT  
		Size: 2.6 MB (2575925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da696bed9510ee87c8e15f556c203b199ab0671c2c70cfdf291a2ce2428ed243`  
		Last Modified: Mon, 25 Nov 2024 20:26:46 GMT  
		Size: 469.0 KB (469002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e1ff456b73816d9e82e028672d8d486dd289c2ac473db51c28b7017933c26`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 330.7 MB (330731073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef263ff77a3eb88e778f6943e044b6fc5e8f4c0eee128e21dfeb975a5849dc58`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec87014b3795e6e7363d69e710aedb0ba05512d6cef2ca8077cce4db91bc82d`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3731d2251a7978f7d08605b6301b86afde30a0e20b600d99576edbbb1638ec`  
		Last Modified: Mon, 25 Nov 2024 20:26:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cee2aec29e7a8ee661f622e82a2d3265341a4a0c8b139dd84b359a2f336a54d`  
		Last Modified: Mon, 25 Nov 2024 20:26:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f6e04ce313343613524fd1ed99086f01dcec1892bc1c0a2c79980822f86454a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38892875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad1bec682dd6b6247c29c3a3614015ca58cfd6d169feb6e97381930344ac50`

```dockerfile
```

-	Layers:
	-	`sha256:587604f8b5d33d84decb06c9fbdcc06d84f9c9ec744213bfac7c63d4e92e5a50`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 38.9 MB (38866157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfafe5bda6028255f7ee3c9aaa785990008bc39bd16b6504429840195443e4d`  
		Last Modified: Mon, 25 Nov 2024 20:26:45 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e051491e75658a1eb669473267149a5822909b5fb327d9138013e3fb481b3f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580453062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16875e0056a4bff46723cf738d60f1366a94a175d3eff4d697b4979c9c216fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689abbf96956f625195182ac751906675f167eb79691c2d19bfa0593c6afa2c`  
		Last Modified: Mon, 18 Nov 2024 19:50:17 GMT  
		Size: 216.9 MB (216917317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073696c45fa176ea3f3fc4544f520fff34daacfdb49459ec9007c9702204c0b`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 2.6 MB (2583786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8a28c9d2e01dd95537d21c9026332df53afacfcd4af98db8dd25fa1dcec19`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 469.1 KB (469084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7074457b40194490ed3c184af02aacc4af5ac4c09a0a65f860bb1b1c1031cbb4`  
		Last Modified: Mon, 25 Nov 2024 20:38:43 GMT  
		Size: 330.4 MB (330388846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5546c4da3d0832f98844767ceb84c8458769cf9b32b14fe7847eea5d4a936b`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52be9f9c93882ea19f983214512424d18315ec29c088e513e76e23994b19bb8`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa8d5b2f37f3ee3975fe0380eace6c8790029f7fa60e78771777118b655697`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e99dcc784558c816ec25b9e36df5f72779742e92163b75df8ccbf9792bd288`  
		Last Modified: Mon, 25 Nov 2024 20:38:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:dfa96b740fe626c327ae2d9793f4d2a1c4e4477e5fc68fc9de849d6edaaf8ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff22b7c21f5c056f7c68eb3bc54f54eb3c23d8dcaab3d5cf48eb2757b0facfc`

```dockerfile
```

-	Layers:
	-	`sha256:6e564cb43960687b4cdcad2e746d58d9cd6c74e1c678f3e6d64925865106337f`  
		Last Modified: Mon, 25 Nov 2024 20:38:37 GMT  
		Size: 38.9 MB (38872633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16165af0824d57acbb9fee4c8bdb26ac5998c1a5b18aa5a4ef22f8e03159fda`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241125`

```console
$ docker pull odoo@sha256:4b11bd27f34f5e44eebf5a7cc6048bd5ef71c99525ab90b95968e0dd42eae395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20241125` - linux; amd64

```console
$ docker pull odoo@sha256:7e232ffac82bf02a1be4a9da7454d080e8bf2204bc6380403460114eb14a9f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.8 MB (584835716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4e858674d35a88b21a997ebe1dfa7d84f534ade6d0fc4b43c9721f6d6b2325`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b01be562f53e40a748ab80cc7332bcf52d34a666f4605ea9a1eca6810e248d`  
		Last Modified: Mon, 25 Nov 2024 20:26:51 GMT  
		Size: 219.6 MB (219605720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4259a4043a00942d119c9dd4f5ecba3840562a10777b4e717602747f7076a8f2`  
		Last Modified: Mon, 25 Nov 2024 20:26:46 GMT  
		Size: 2.6 MB (2575925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da696bed9510ee87c8e15f556c203b199ab0671c2c70cfdf291a2ce2428ed243`  
		Last Modified: Mon, 25 Nov 2024 20:26:46 GMT  
		Size: 469.0 KB (469002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54e1ff456b73816d9e82e028672d8d486dd289c2ac473db51c28b7017933c26`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 330.7 MB (330731073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef263ff77a3eb88e778f6943e044b6fc5e8f4c0eee128e21dfeb975a5849dc58`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec87014b3795e6e7363d69e710aedb0ba05512d6cef2ca8077cce4db91bc82d`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3731d2251a7978f7d08605b6301b86afde30a0e20b600d99576edbbb1638ec`  
		Last Modified: Mon, 25 Nov 2024 20:26:48 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cee2aec29e7a8ee661f622e82a2d3265341a4a0c8b139dd84b359a2f336a54d`  
		Last Modified: Mon, 25 Nov 2024 20:26:48 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:f6e04ce313343613524fd1ed99086f01dcec1892bc1c0a2c79980822f86454a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38892875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad1bec682dd6b6247c29c3a3614015ca58cfd6d169feb6e97381930344ac50`

```dockerfile
```

-	Layers:
	-	`sha256:587604f8b5d33d84decb06c9fbdcc06d84f9c9ec744213bfac7c63d4e92e5a50`  
		Last Modified: Mon, 25 Nov 2024 20:26:47 GMT  
		Size: 38.9 MB (38866157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfafe5bda6028255f7ee3c9aaa785990008bc39bd16b6504429840195443e4d`  
		Last Modified: Mon, 25 Nov 2024 20:26:45 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20241125` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e051491e75658a1eb669473267149a5822909b5fb327d9138013e3fb481b3f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.5 MB (580453062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16875e0056a4bff46723cf738d60f1366a94a175d3eff4d697b4979c9c216fcb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=C.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=16.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=3bf9f45278efc7ae579b581543686fe75893699a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e689abbf96956f625195182ac751906675f167eb79691c2d19bfa0593c6afa2c`  
		Last Modified: Mon, 18 Nov 2024 19:50:17 GMT  
		Size: 216.9 MB (216917317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073696c45fa176ea3f3fc4544f520fff34daacfdb49459ec9007c9702204c0b`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 2.6 MB (2583786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8a28c9d2e01dd95537d21c9026332df53afacfcd4af98db8dd25fa1dcec19`  
		Last Modified: Mon, 18 Nov 2024 19:50:12 GMT  
		Size: 469.1 KB (469084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7074457b40194490ed3c184af02aacc4af5ac4c09a0a65f860bb1b1c1031cbb4`  
		Last Modified: Mon, 25 Nov 2024 20:38:43 GMT  
		Size: 330.4 MB (330388846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5546c4da3d0832f98844767ceb84c8458769cf9b32b14fe7847eea5d4a936b`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52be9f9c93882ea19f983214512424d18315ec29c088e513e76e23994b19bb8`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa8d5b2f37f3ee3975fe0380eace6c8790029f7fa60e78771777118b655697`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e99dcc784558c816ec25b9e36df5f72779742e92163b75df8ccbf9792bd288`  
		Last Modified: Mon, 25 Nov 2024 20:38:37 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:dfa96b740fe626c327ae2d9793f4d2a1c4e4477e5fc68fc9de849d6edaaf8ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38899503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff22b7c21f5c056f7c68eb3bc54f54eb3c23d8dcaab3d5cf48eb2757b0facfc`

```dockerfile
```

-	Layers:
	-	`sha256:6e564cb43960687b4cdcad2e746d58d9cd6c74e1c678f3e6d64925865106337f`  
		Last Modified: Mon, 25 Nov 2024 20:38:37 GMT  
		Size: 38.9 MB (38872633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16165af0824d57acbb9fee4c8bdb26ac5998c1a5b18aa5a4ef22f8e03159fda`  
		Last Modified: Mon, 25 Nov 2024 20:38:36 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:2b56d8e7bc0cd9b7a89afc7ce3e17113fc6b1574db7fb810901e317cbcff7483
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
$ docker pull odoo@sha256:ca44785adfb1b902624066bccf92002e9eeb07d31ed1950f82dfc3eee27341bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.8 MB (598832329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac24b03f5ac1627e8d808570f22c5dc33b1493b7e2fa176a519c77735b8ea85`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30424451599047b1500a0fab1ef9d38f2c828e661bd2e5350c56dfc928350eea`  
		Last Modified: Mon, 25 Nov 2024 20:26:59 GMT  
		Size: 233.8 MB (233782155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baae6af1c87ae5333c07a228ada35da57650976beb0bef2c12caf14b4dddf0b3`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 2.5 MB (2493482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2962f1aa4a8766be7e3cb8bb418bed99a659c0c6f81e13948ffdf5adacdc0e7`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 470.0 KB (469978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f88912933c298c1ac88ca47b1b8b72713000a0bc7b116e8c8ff8e9a9d31c9`  
		Last Modified: Mon, 25 Nov 2024 20:27:00 GMT  
		Size: 332.5 MB (332548585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5964aa3a238938ec8e8e7b63861b243b47dfcf95a583b7fb875a3130221c13`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e8bb7da0425f9822cb14c466deaafdd005b3f3d73ee042987946d3d762b91`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71c67380a01e5bd54d556ec1c8fe5c6df68fbeb6efd97369f5eda70f3f0aa9c`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f646dc371b996a9bc5e48ab6362656f44b0694c17eb90ac4e531a2e0ff3358`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:816fdc65653221c9aa07481daded72579d70ac8010c8862cccd12b774b1787da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa8e27ecae8da39d6b0f4efba6beb362cd0ec18b6b318592396ce77dab383dd`

```dockerfile
```

-	Layers:
	-	`sha256:5647bcbe946868988a3cac48db6b499b32d8035785b5981671fc1449218c8027`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 39.6 MB (39615938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbaf3c586b91ac4df4945840fcc326d8d1abf77b5ba48f11e3a49ee097d3841`  
		Last Modified: Mon, 25 Nov 2024 20:26:52 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:95ea6e12801a53668907db6c49a289598823863e9cd05c9113d011f04dca404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.6 MB (593619343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491b6319c208de1ea73a1d23f754d73429b2c99cc9aa3a62e27629f4c7e4b2aa`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20d1f022d1d141a9953bbfae96125324b3efd6b22622c3596a95aaf028d273`  
		Last Modified: Mon, 25 Nov 2024 20:35:43 GMT  
		Size: 332.1 MB (332149204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423175ed130d608fd65bc155744764690738407ae8adf3504f935bdd48d5edd`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9875700ae72cdd80764a751e96a89ea3e27697a8f78372b01832b0b2f1be8547`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6061e87ce90a3c02fa7bd484747c2200d711399136dbe216c61d5bca02015351`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6b1aa67f2a61af1f5be66a759f906845bf1f2772824d991c2f12749d19414`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a11b479a8ef73e4156a30f7f9a547bd748ff666262a30d6e13da948203f8eed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39649442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ac5363a6244f3d12b19fa7451203d64217c6d87e4aef92ab24d75d9e45fb5`

```dockerfile
```

-	Layers:
	-	`sha256:e8146aa7abed03d6fc5c588368d9d315861750d7db5834aba8642a9f0da9cfd3`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 39.6 MB (39622455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a38a08112d0b1b545a9a0a06ee2acb9371e75a248f4922d04589de1cd35a55e`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:f2c54fcfb2376a8540d5021d05de088d2b888df3c1348ec17cccced0b5e8afbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615270446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f105d0d3228af94ff789c1a972ebbdae097e8f07e228e5723ebb2cf7f8c46b7`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58056fe26f87028c0af4ca8c6107fec08b0b2b04d2fbe413612d5c17ea83fb87`  
		Last Modified: Mon, 25 Nov 2024 20:39:49 GMT  
		Size: 334.3 MB (334253832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a1d101edc7322ce83fee2afe8c37c3daa4820d3711b6ef1dbb07a1a9245f4f`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f81806a914dc1a42ce92037ffa9723b6808e38a5acdb0a23049f345ac3b216`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafecc0ed4141f1b39c8c58683d3c4540ef373f86e1d318e83821fb407a8253`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b573c90062187a265712dcb628f6bd92a0afb9c2a9957788d2d848887ae03`  
		Last Modified: Mon, 25 Nov 2024 20:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1bc3e0597b01ad5d288653537436026a4a19e17f9964d4cd0e8516535faf6f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39651156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81e8b180999e99bfef4c76f8c2d5d4119001eefa9a2d8a4438b90b2a48ef77`

```dockerfile
```

-	Layers:
	-	`sha256:d77780107d99e547189cfcbc8fcbcae5f7c0be7eb1927097fb2d22e874d401ff`  
		Last Modified: Mon, 25 Nov 2024 20:39:19 GMT  
		Size: 39.6 MB (39624265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37e3220841ba75d53f657aaa3930eb10998475281bc43a7b93d17976f24cf41`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:2b56d8e7bc0cd9b7a89afc7ce3e17113fc6b1574db7fb810901e317cbcff7483
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
$ docker pull odoo@sha256:ca44785adfb1b902624066bccf92002e9eeb07d31ed1950f82dfc3eee27341bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.8 MB (598832329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac24b03f5ac1627e8d808570f22c5dc33b1493b7e2fa176a519c77735b8ea85`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30424451599047b1500a0fab1ef9d38f2c828e661bd2e5350c56dfc928350eea`  
		Last Modified: Mon, 25 Nov 2024 20:26:59 GMT  
		Size: 233.8 MB (233782155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baae6af1c87ae5333c07a228ada35da57650976beb0bef2c12caf14b4dddf0b3`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 2.5 MB (2493482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2962f1aa4a8766be7e3cb8bb418bed99a659c0c6f81e13948ffdf5adacdc0e7`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 470.0 KB (469978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f88912933c298c1ac88ca47b1b8b72713000a0bc7b116e8c8ff8e9a9d31c9`  
		Last Modified: Mon, 25 Nov 2024 20:27:00 GMT  
		Size: 332.5 MB (332548585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5964aa3a238938ec8e8e7b63861b243b47dfcf95a583b7fb875a3130221c13`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e8bb7da0425f9822cb14c466deaafdd005b3f3d73ee042987946d3d762b91`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71c67380a01e5bd54d556ec1c8fe5c6df68fbeb6efd97369f5eda70f3f0aa9c`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f646dc371b996a9bc5e48ab6362656f44b0694c17eb90ac4e531a2e0ff3358`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:816fdc65653221c9aa07481daded72579d70ac8010c8862cccd12b774b1787da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa8e27ecae8da39d6b0f4efba6beb362cd0ec18b6b318592396ce77dab383dd`

```dockerfile
```

-	Layers:
	-	`sha256:5647bcbe946868988a3cac48db6b499b32d8035785b5981671fc1449218c8027`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 39.6 MB (39615938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbaf3c586b91ac4df4945840fcc326d8d1abf77b5ba48f11e3a49ee097d3841`  
		Last Modified: Mon, 25 Nov 2024 20:26:52 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:95ea6e12801a53668907db6c49a289598823863e9cd05c9113d011f04dca404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.6 MB (593619343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491b6319c208de1ea73a1d23f754d73429b2c99cc9aa3a62e27629f4c7e4b2aa`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20d1f022d1d141a9953bbfae96125324b3efd6b22622c3596a95aaf028d273`  
		Last Modified: Mon, 25 Nov 2024 20:35:43 GMT  
		Size: 332.1 MB (332149204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423175ed130d608fd65bc155744764690738407ae8adf3504f935bdd48d5edd`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9875700ae72cdd80764a751e96a89ea3e27697a8f78372b01832b0b2f1be8547`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6061e87ce90a3c02fa7bd484747c2200d711399136dbe216c61d5bca02015351`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6b1aa67f2a61af1f5be66a759f906845bf1f2772824d991c2f12749d19414`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a11b479a8ef73e4156a30f7f9a547bd748ff666262a30d6e13da948203f8eed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39649442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ac5363a6244f3d12b19fa7451203d64217c6d87e4aef92ab24d75d9e45fb5`

```dockerfile
```

-	Layers:
	-	`sha256:e8146aa7abed03d6fc5c588368d9d315861750d7db5834aba8642a9f0da9cfd3`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 39.6 MB (39622455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a38a08112d0b1b545a9a0a06ee2acb9371e75a248f4922d04589de1cd35a55e`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f2c54fcfb2376a8540d5021d05de088d2b888df3c1348ec17cccced0b5e8afbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615270446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f105d0d3228af94ff789c1a972ebbdae097e8f07e228e5723ebb2cf7f8c46b7`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58056fe26f87028c0af4ca8c6107fec08b0b2b04d2fbe413612d5c17ea83fb87`  
		Last Modified: Mon, 25 Nov 2024 20:39:49 GMT  
		Size: 334.3 MB (334253832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a1d101edc7322ce83fee2afe8c37c3daa4820d3711b6ef1dbb07a1a9245f4f`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f81806a914dc1a42ce92037ffa9723b6808e38a5acdb0a23049f345ac3b216`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafecc0ed4141f1b39c8c58683d3c4540ef373f86e1d318e83821fb407a8253`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b573c90062187a265712dcb628f6bd92a0afb9c2a9957788d2d848887ae03`  
		Last Modified: Mon, 25 Nov 2024 20:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1bc3e0597b01ad5d288653537436026a4a19e17f9964d4cd0e8516535faf6f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39651156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81e8b180999e99bfef4c76f8c2d5d4119001eefa9a2d8a4438b90b2a48ef77`

```dockerfile
```

-	Layers:
	-	`sha256:d77780107d99e547189cfcbc8fcbcae5f7c0be7eb1927097fb2d22e874d401ff`  
		Last Modified: Mon, 25 Nov 2024 20:39:19 GMT  
		Size: 39.6 MB (39624265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37e3220841ba75d53f657aaa3930eb10998475281bc43a7b93d17976f24cf41`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241125`

```console
$ docker pull odoo@sha256:2b56d8e7bc0cd9b7a89afc7ce3e17113fc6b1574db7fb810901e317cbcff7483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241125` - linux; amd64

```console
$ docker pull odoo@sha256:ca44785adfb1b902624066bccf92002e9eeb07d31ed1950f82dfc3eee27341bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.8 MB (598832329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac24b03f5ac1627e8d808570f22c5dc33b1493b7e2fa176a519c77735b8ea85`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30424451599047b1500a0fab1ef9d38f2c828e661bd2e5350c56dfc928350eea`  
		Last Modified: Mon, 25 Nov 2024 20:26:59 GMT  
		Size: 233.8 MB (233782155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baae6af1c87ae5333c07a228ada35da57650976beb0bef2c12caf14b4dddf0b3`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 2.5 MB (2493482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2962f1aa4a8766be7e3cb8bb418bed99a659c0c6f81e13948ffdf5adacdc0e7`  
		Last Modified: Mon, 25 Nov 2024 20:26:53 GMT  
		Size: 470.0 KB (469978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f88912933c298c1ac88ca47b1b8b72713000a0bc7b116e8c8ff8e9a9d31c9`  
		Last Modified: Mon, 25 Nov 2024 20:27:00 GMT  
		Size: 332.5 MB (332548585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5964aa3a238938ec8e8e7b63861b243b47dfcf95a583b7fb875a3130221c13`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e8bb7da0425f9822cb14c466deaafdd005b3f3d73ee042987946d3d762b91`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71c67380a01e5bd54d556ec1c8fe5c6df68fbeb6efd97369f5eda70f3f0aa9c`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f646dc371b996a9bc5e48ab6362656f44b0694c17eb90ac4e531a2e0ff3358`  
		Last Modified: Mon, 25 Nov 2024 20:26:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:816fdc65653221c9aa07481daded72579d70ac8010c8862cccd12b774b1787da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39642773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa8e27ecae8da39d6b0f4efba6beb362cd0ec18b6b318592396ce77dab383dd`

```dockerfile
```

-	Layers:
	-	`sha256:5647bcbe946868988a3cac48db6b499b32d8035785b5981671fc1449218c8027`  
		Last Modified: Mon, 25 Nov 2024 20:26:54 GMT  
		Size: 39.6 MB (39615938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbaf3c586b91ac4df4945840fcc326d8d1abf77b5ba48f11e3a49ee097d3841`  
		Last Modified: Mon, 25 Nov 2024 20:26:52 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241125` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:95ea6e12801a53668907db6c49a289598823863e9cd05c9113d011f04dca404c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.6 MB (593619343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491b6319c208de1ea73a1d23f754d73429b2c99cc9aa3a62e27629f4c7e4b2aa`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9472bd8d79fbea99c71a8f55e25d2b01bfe2cdd566aa283345d4c574bc2e01`  
		Last Modified: Mon, 18 Nov 2024 19:46:18 GMT  
		Size: 231.2 MB (231154471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b706986c1b0c830c0646653baf0b1ffbdfefd57eb2f563ad05ae5eefb7ce3`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 2.5 MB (2484900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e76b45a4da60ecf2fb9f87d414fcb97659b49db5cd0791f17e966a48818bf1`  
		Last Modified: Mon, 18 Nov 2024 19:46:13 GMT  
		Size: 470.0 KB (469999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca20d1f022d1d141a9953bbfae96125324b3efd6b22622c3596a95aaf028d273`  
		Last Modified: Mon, 25 Nov 2024 20:35:43 GMT  
		Size: 332.1 MB (332149204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4423175ed130d608fd65bc155744764690738407ae8adf3504f935bdd48d5edd`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9875700ae72cdd80764a751e96a89ea3e27697a8f78372b01832b0b2f1be8547`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6061e87ce90a3c02fa7bd484747c2200d711399136dbe216c61d5bca02015351`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6b1aa67f2a61af1f5be66a759f906845bf1f2772824d991c2f12749d19414`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:a11b479a8ef73e4156a30f7f9a547bd748ff666262a30d6e13da948203f8eed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39649442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6ac5363a6244f3d12b19fa7451203d64217c6d87e4aef92ab24d75d9e45fb5`

```dockerfile
```

-	Layers:
	-	`sha256:e8146aa7abed03d6fc5c588368d9d315861750d7db5834aba8642a9f0da9cfd3`  
		Last Modified: Mon, 25 Nov 2024 20:35:34 GMT  
		Size: 39.6 MB (39622455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a38a08112d0b1b545a9a0a06ee2acb9371e75a248f4922d04589de1cd35a55e`  
		Last Modified: Mon, 25 Nov 2024 20:35:33 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241125` - linux; ppc64le

```console
$ docker pull odoo@sha256:f2c54fcfb2376a8540d5021d05de088d2b888df3c1348ec17cccced0b5e8afbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 MB (615270446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f105d0d3228af94ff789c1a972ebbdae097e8f07e228e5723ebb2cf7f8c46b7`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=17.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=10482830e9ce1d9850e9b8fd335875fa034a44a9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f3c419cad4316210132a5e9e968ef92ae53722d9ddb2303172461ff9580f41`  
		Last Modified: Mon, 18 Nov 2024 23:19:43 GMT  
		Size: 243.3 MB (243298186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c27aa99bbf2102a7b2b62b96f528bc4e0ac2429f5d8fdbe7bd21bcd2123134`  
		Last Modified: Mon, 18 Nov 2024 23:19:35 GMT  
		Size: 2.8 MB (2797689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a58049116ee57a652623cbf5f1ef0eee7e7fae1d88e7d73caa4b8d11633324`  
		Last Modified: Mon, 18 Nov 2024 23:19:34 GMT  
		Size: 470.1 KB (470056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58056fe26f87028c0af4ca8c6107fec08b0b2b04d2fbe413612d5c17ea83fb87`  
		Last Modified: Mon, 25 Nov 2024 20:39:49 GMT  
		Size: 334.3 MB (334253832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a1d101edc7322ce83fee2afe8c37c3daa4820d3711b6ef1dbb07a1a9245f4f`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f81806a914dc1a42ce92037ffa9723b6808e38a5acdb0a23049f345ac3b216`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafecc0ed4141f1b39c8c58683d3c4540ef373f86e1d318e83821fb407a8253`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b573c90062187a265712dcb628f6bd92a0afb9c2a9957788d2d848887ae03`  
		Last Modified: Mon, 25 Nov 2024 20:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:1bc3e0597b01ad5d288653537436026a4a19e17f9964d4cd0e8516535faf6f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39651156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81e8b180999e99bfef4c76f8c2d5d4119001eefa9a2d8a4438b90b2a48ef77`

```dockerfile
```

-	Layers:
	-	`sha256:d77780107d99e547189cfcbc8fcbcae5f7c0be7eb1927097fb2d22e874d401ff`  
		Last Modified: Mon, 25 Nov 2024 20:39:19 GMT  
		Size: 39.6 MB (39624265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37e3220841ba75d53f657aaa3930eb10998475281bc43a7b93d17976f24cf41`  
		Last Modified: Mon, 25 Nov 2024 20:39:17 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:55be8055bebb50cc6b9565e30ffb9a522b7c9b7c61a0558b005662ba9f0a06dc
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
$ docker pull odoo@sha256:c1937bf49fc09babde747a277b76e1c448b97a71a7bc1908d1dea0afc2f4cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661826305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9bc77230906d0a98c0a68d2cbca9c0b53c77a1d545ff21202b0b2bb787bd35`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d128a82529d7f28af0e23bc19a8d74cad84efc84ba3893b6f88cd9d65c57cb`  
		Last Modified: Mon, 25 Nov 2024 20:27:30 GMT  
		Size: 254.5 MB (254514976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c54e86137ce82f955e630c041345b730dad696ba14e446d4ed651fb924161d2`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 14.2 MB (14230240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470f846b2c4ac19e54ae3282c351d9e7f3bdb70aa031ae20c7ec26565ab4e56d`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 469.7 KB (469717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520674f58c111e938bc91c1880ec2396fb84b04126ae2925595895185348b1f`  
		Last Modified: Mon, 25 Nov 2024 20:27:32 GMT  
		Size: 362.9 MB (362857155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663db6c71feea36a64b3935fa528dd80a19ad90c027207737d986080836c6080`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3787ee00e67a74e30b531a36efba223e90527fe2e4008caae792de868527a07`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a6357344d35acba8166cf1be5df64acbd8b4a8a25e41f4112090d0aa41279f`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f145cef64dc7178611127c3b2adc5a0174f46e26c918770637132ebed09e5`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b1e73eb636656d2f0315585c9c9806eb847ca47b7eb26ec6ee791a14fa66ec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e47fd308d2b42ac39b532c65ff05ae0177acad5467962cf49fb20bc18cc4825`

```dockerfile
```

-	Layers:
	-	`sha256:0e5849635127ef6ee3ecb3c8e4ac8e69438e46d119285c8ba9ad58262414bcb6`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 57.3 MB (57253588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48b6cda47f47e47a42ef1d8d41c28c0b973e6a9d7368d3ee947d64a3789994b`  
		Last Modified: Mon, 25 Nov 2024 20:27:26 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a1b56d7071b2928346e5b0db697e380e308963787081ee095f8f2435b48c0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658199642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c5fcdc5afadd8ad803fdbe024500ebf5ff6ee8e6a72097d5281f2cbc333d5`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:14acc5f94928508504ccb131cb0e7cac6fb981267531c47028d0a39cf1ec6bb1`  
		Last Modified: Mon, 25 Nov 2024 20:31:34 GMT  
		Size: 362.7 MB (362686981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7cd84dc5a1410241f06c30b3bff9fef79f097614187bd0d75719672882accc`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15859d1c6a5683189016bbdb9f58bd08e052c64be5aedc6f782bee6b0eb063`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31ffc577a6edce14511e0404d73b48461b272bcfb60bab890cc7ccf4e61c0a`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3d6ead5b26e1a32d1d3c1b71d9767aa00743fc64733b871c6bbf2591d81d9d`  
		Last Modified: Mon, 25 Nov 2024 20:31:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:75ef835d7b856c1f934a370f28c1336a8bf0c0c0944462062a9317cf254d4ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a332ef769be7ab9d9d100bae943b3e2f1af4fc69a07fd08c591da9bf40f49`

```dockerfile
```

-	Layers:
	-	`sha256:3696bda8b095f58496bd3db9f0795eed260b1c194a955d81ee26ac412e6dbc02`  
		Last Modified: Mon, 25 Nov 2024 20:31:28 GMT  
		Size: 57.3 MB (57260886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a36439b8d122b7727196c04e60688c8493e56dc9dfdec71bab35384df7975b4`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:249394c80de1afe549e21df093182a3562ac870e8f33aef14ae7fcc1a33b1b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.2 MB (678165891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e527f4a1fdf4de582ad9fc12ca026d3ee07e71c92c30cbd8f52ff97887ff58`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:5b7171c978e079b5f38d49480060c57fbdc2109fe4dd925b4deec46f41d2a6ff`  
		Last Modified: Mon, 25 Nov 2024 20:33:47 GMT  
		Size: 363.4 MB (363393731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d226da017e27af535cefe9931994faddca35b7d916f648f1dd8368b8dabc5d`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ec2d2f254202a162279de968878bbd07d01e9a8e2cfe7865f85dd0f473fea`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584ad5a62aeeac9c71767750791bb6a7678373a2fdafaaeec5ae275695400c1`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77534b5938029530e4096968ea8c54f944e4746e8461b7989b949465b9301fb`  
		Last Modified: Mon, 25 Nov 2024 20:33:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b39d5177f242c90faf213fb94814d3f11ed56d89e4d977e3762a0c93f6d3f53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac861a439bba788c553fe1545ab03af9f83b0c25f2c10cca6c2e44a0c9f3adc5`

```dockerfile
```

-	Layers:
	-	`sha256:d0b34ce28ec2bd9d116d571ab93d2398bef6baedb218ac7f7ac926fa32be56b5`  
		Last Modified: Mon, 25 Nov 2024 20:33:26 GMT  
		Size: 57.3 MB (57261751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bac00a9d8108fec117b5d00b192de8d2f5cfd669f283d7d0654a1429a8e6c6`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:55be8055bebb50cc6b9565e30ffb9a522b7c9b7c61a0558b005662ba9f0a06dc
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
$ docker pull odoo@sha256:c1937bf49fc09babde747a277b76e1c448b97a71a7bc1908d1dea0afc2f4cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661826305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9bc77230906d0a98c0a68d2cbca9c0b53c77a1d545ff21202b0b2bb787bd35`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d128a82529d7f28af0e23bc19a8d74cad84efc84ba3893b6f88cd9d65c57cb`  
		Last Modified: Mon, 25 Nov 2024 20:27:30 GMT  
		Size: 254.5 MB (254514976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c54e86137ce82f955e630c041345b730dad696ba14e446d4ed651fb924161d2`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 14.2 MB (14230240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470f846b2c4ac19e54ae3282c351d9e7f3bdb70aa031ae20c7ec26565ab4e56d`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 469.7 KB (469717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520674f58c111e938bc91c1880ec2396fb84b04126ae2925595895185348b1f`  
		Last Modified: Mon, 25 Nov 2024 20:27:32 GMT  
		Size: 362.9 MB (362857155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663db6c71feea36a64b3935fa528dd80a19ad90c027207737d986080836c6080`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3787ee00e67a74e30b531a36efba223e90527fe2e4008caae792de868527a07`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a6357344d35acba8166cf1be5df64acbd8b4a8a25e41f4112090d0aa41279f`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f145cef64dc7178611127c3b2adc5a0174f46e26c918770637132ebed09e5`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b1e73eb636656d2f0315585c9c9806eb847ca47b7eb26ec6ee791a14fa66ec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e47fd308d2b42ac39b532c65ff05ae0177acad5467962cf49fb20bc18cc4825`

```dockerfile
```

-	Layers:
	-	`sha256:0e5849635127ef6ee3ecb3c8e4ac8e69438e46d119285c8ba9ad58262414bcb6`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 57.3 MB (57253588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48b6cda47f47e47a42ef1d8d41c28c0b973e6a9d7368d3ee947d64a3789994b`  
		Last Modified: Mon, 25 Nov 2024 20:27:26 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a1b56d7071b2928346e5b0db697e380e308963787081ee095f8f2435b48c0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658199642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c5fcdc5afadd8ad803fdbe024500ebf5ff6ee8e6a72097d5281f2cbc333d5`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:14acc5f94928508504ccb131cb0e7cac6fb981267531c47028d0a39cf1ec6bb1`  
		Last Modified: Mon, 25 Nov 2024 20:31:34 GMT  
		Size: 362.7 MB (362686981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7cd84dc5a1410241f06c30b3bff9fef79f097614187bd0d75719672882accc`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15859d1c6a5683189016bbdb9f58bd08e052c64be5aedc6f782bee6b0eb063`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31ffc577a6edce14511e0404d73b48461b272bcfb60bab890cc7ccf4e61c0a`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3d6ead5b26e1a32d1d3c1b71d9767aa00743fc64733b871c6bbf2591d81d9d`  
		Last Modified: Mon, 25 Nov 2024 20:31:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:75ef835d7b856c1f934a370f28c1336a8bf0c0c0944462062a9317cf254d4ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a332ef769be7ab9d9d100bae943b3e2f1af4fc69a07fd08c591da9bf40f49`

```dockerfile
```

-	Layers:
	-	`sha256:3696bda8b095f58496bd3db9f0795eed260b1c194a955d81ee26ac412e6dbc02`  
		Last Modified: Mon, 25 Nov 2024 20:31:28 GMT  
		Size: 57.3 MB (57260886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a36439b8d122b7727196c04e60688c8493e56dc9dfdec71bab35384df7975b4`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:249394c80de1afe549e21df093182a3562ac870e8f33aef14ae7fcc1a33b1b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.2 MB (678165891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e527f4a1fdf4de582ad9fc12ca026d3ee07e71c92c30cbd8f52ff97887ff58`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:5b7171c978e079b5f38d49480060c57fbdc2109fe4dd925b4deec46f41d2a6ff`  
		Last Modified: Mon, 25 Nov 2024 20:33:47 GMT  
		Size: 363.4 MB (363393731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d226da017e27af535cefe9931994faddca35b7d916f648f1dd8368b8dabc5d`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ec2d2f254202a162279de968878bbd07d01e9a8e2cfe7865f85dd0f473fea`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584ad5a62aeeac9c71767750791bb6a7678373a2fdafaaeec5ae275695400c1`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77534b5938029530e4096968ea8c54f944e4746e8461b7989b949465b9301fb`  
		Last Modified: Mon, 25 Nov 2024 20:33:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b39d5177f242c90faf213fb94814d3f11ed56d89e4d977e3762a0c93f6d3f53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac861a439bba788c553fe1545ab03af9f83b0c25f2c10cca6c2e44a0c9f3adc5`

```dockerfile
```

-	Layers:
	-	`sha256:d0b34ce28ec2bd9d116d571ab93d2398bef6baedb218ac7f7ac926fa32be56b5`  
		Last Modified: Mon, 25 Nov 2024 20:33:26 GMT  
		Size: 57.3 MB (57261751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bac00a9d8108fec117b5d00b192de8d2f5cfd669f283d7d0654a1429a8e6c6`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241125`

```console
$ docker pull odoo@sha256:55be8055bebb50cc6b9565e30ffb9a522b7c9b7c61a0558b005662ba9f0a06dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241125` - linux; amd64

```console
$ docker pull odoo@sha256:c1937bf49fc09babde747a277b76e1c448b97a71a7bc1908d1dea0afc2f4cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661826305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9bc77230906d0a98c0a68d2cbca9c0b53c77a1d545ff21202b0b2bb787bd35`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d128a82529d7f28af0e23bc19a8d74cad84efc84ba3893b6f88cd9d65c57cb`  
		Last Modified: Mon, 25 Nov 2024 20:27:30 GMT  
		Size: 254.5 MB (254514976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c54e86137ce82f955e630c041345b730dad696ba14e446d4ed651fb924161d2`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 14.2 MB (14230240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470f846b2c4ac19e54ae3282c351d9e7f3bdb70aa031ae20c7ec26565ab4e56d`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 469.7 KB (469717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520674f58c111e938bc91c1880ec2396fb84b04126ae2925595895185348b1f`  
		Last Modified: Mon, 25 Nov 2024 20:27:32 GMT  
		Size: 362.9 MB (362857155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663db6c71feea36a64b3935fa528dd80a19ad90c027207737d986080836c6080`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3787ee00e67a74e30b531a36efba223e90527fe2e4008caae792de868527a07`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a6357344d35acba8166cf1be5df64acbd8b4a8a25e41f4112090d0aa41279f`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f145cef64dc7178611127c3b2adc5a0174f46e26c918770637132ebed09e5`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:b1e73eb636656d2f0315585c9c9806eb847ca47b7eb26ec6ee791a14fa66ec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e47fd308d2b42ac39b532c65ff05ae0177acad5467962cf49fb20bc18cc4825`

```dockerfile
```

-	Layers:
	-	`sha256:0e5849635127ef6ee3ecb3c8e4ac8e69438e46d119285c8ba9ad58262414bcb6`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 57.3 MB (57253588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48b6cda47f47e47a42ef1d8d41c28c0b973e6a9d7368d3ee947d64a3789994b`  
		Last Modified: Mon, 25 Nov 2024 20:27:26 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241125` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a1b56d7071b2928346e5b0db697e380e308963787081ee095f8f2435b48c0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658199642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c5fcdc5afadd8ad803fdbe024500ebf5ff6ee8e6a72097d5281f2cbc333d5`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:14acc5f94928508504ccb131cb0e7cac6fb981267531c47028d0a39cf1ec6bb1`  
		Last Modified: Mon, 25 Nov 2024 20:31:34 GMT  
		Size: 362.7 MB (362686981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7cd84dc5a1410241f06c30b3bff9fef79f097614187bd0d75719672882accc`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15859d1c6a5683189016bbdb9f58bd08e052c64be5aedc6f782bee6b0eb063`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31ffc577a6edce14511e0404d73b48461b272bcfb60bab890cc7ccf4e61c0a`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3d6ead5b26e1a32d1d3c1b71d9767aa00743fc64733b871c6bbf2591d81d9d`  
		Last Modified: Mon, 25 Nov 2024 20:31:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:75ef835d7b856c1f934a370f28c1336a8bf0c0c0944462062a9317cf254d4ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a332ef769be7ab9d9d100bae943b3e2f1af4fc69a07fd08c591da9bf40f49`

```dockerfile
```

-	Layers:
	-	`sha256:3696bda8b095f58496bd3db9f0795eed260b1c194a955d81ee26ac412e6dbc02`  
		Last Modified: Mon, 25 Nov 2024 20:31:28 GMT  
		Size: 57.3 MB (57260886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a36439b8d122b7727196c04e60688c8493e56dc9dfdec71bab35384df7975b4`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241125` - linux; ppc64le

```console
$ docker pull odoo@sha256:249394c80de1afe549e21df093182a3562ac870e8f33aef14ae7fcc1a33b1b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.2 MB (678165891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e527f4a1fdf4de582ad9fc12ca026d3ee07e71c92c30cbd8f52ff97887ff58`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:5b7171c978e079b5f38d49480060c57fbdc2109fe4dd925b4deec46f41d2a6ff`  
		Last Modified: Mon, 25 Nov 2024 20:33:47 GMT  
		Size: 363.4 MB (363393731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d226da017e27af535cefe9931994faddca35b7d916f648f1dd8368b8dabc5d`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ec2d2f254202a162279de968878bbd07d01e9a8e2cfe7865f85dd0f473fea`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584ad5a62aeeac9c71767750791bb6a7678373a2fdafaaeec5ae275695400c1`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77534b5938029530e4096968ea8c54f944e4746e8461b7989b949465b9301fb`  
		Last Modified: Mon, 25 Nov 2024 20:33:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241125` - unknown; unknown

```console
$ docker pull odoo@sha256:b39d5177f242c90faf213fb94814d3f11ed56d89e4d977e3762a0c93f6d3f53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac861a439bba788c553fe1545ab03af9f83b0c25f2c10cca6c2e44a0c9f3adc5`

```dockerfile
```

-	Layers:
	-	`sha256:d0b34ce28ec2bd9d116d571ab93d2398bef6baedb218ac7f7ac926fa32be56b5`  
		Last Modified: Mon, 25 Nov 2024 20:33:26 GMT  
		Size: 57.3 MB (57261751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bac00a9d8108fec117b5d00b192de8d2f5cfd669f283d7d0654a1429a8e6c6`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:55be8055bebb50cc6b9565e30ffb9a522b7c9b7c61a0558b005662ba9f0a06dc
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
$ docker pull odoo@sha256:c1937bf49fc09babde747a277b76e1c448b97a71a7bc1908d1dea0afc2f4cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661826305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9bc77230906d0a98c0a68d2cbca9c0b53c77a1d545ff21202b0b2bb787bd35`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d128a82529d7f28af0e23bc19a8d74cad84efc84ba3893b6f88cd9d65c57cb`  
		Last Modified: Mon, 25 Nov 2024 20:27:30 GMT  
		Size: 254.5 MB (254514976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c54e86137ce82f955e630c041345b730dad696ba14e446d4ed651fb924161d2`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 14.2 MB (14230240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470f846b2c4ac19e54ae3282c351d9e7f3bdb70aa031ae20c7ec26565ab4e56d`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 469.7 KB (469717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520674f58c111e938bc91c1880ec2396fb84b04126ae2925595895185348b1f`  
		Last Modified: Mon, 25 Nov 2024 20:27:32 GMT  
		Size: 362.9 MB (362857155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663db6c71feea36a64b3935fa528dd80a19ad90c027207737d986080836c6080`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3787ee00e67a74e30b531a36efba223e90527fe2e4008caae792de868527a07`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a6357344d35acba8166cf1be5df64acbd8b4a8a25e41f4112090d0aa41279f`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f145cef64dc7178611127c3b2adc5a0174f46e26c918770637132ebed09e5`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b1e73eb636656d2f0315585c9c9806eb847ca47b7eb26ec6ee791a14fa66ec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e47fd308d2b42ac39b532c65ff05ae0177acad5467962cf49fb20bc18cc4825`

```dockerfile
```

-	Layers:
	-	`sha256:0e5849635127ef6ee3ecb3c8e4ac8e69438e46d119285c8ba9ad58262414bcb6`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 57.3 MB (57253588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48b6cda47f47e47a42ef1d8d41c28c0b973e6a9d7368d3ee947d64a3789994b`  
		Last Modified: Mon, 25 Nov 2024 20:27:26 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a1b56d7071b2928346e5b0db697e380e308963787081ee095f8f2435b48c0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658199642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c5fcdc5afadd8ad803fdbe024500ebf5ff6ee8e6a72097d5281f2cbc333d5`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:14acc5f94928508504ccb131cb0e7cac6fb981267531c47028d0a39cf1ec6bb1`  
		Last Modified: Mon, 25 Nov 2024 20:31:34 GMT  
		Size: 362.7 MB (362686981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7cd84dc5a1410241f06c30b3bff9fef79f097614187bd0d75719672882accc`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15859d1c6a5683189016bbdb9f58bd08e052c64be5aedc6f782bee6b0eb063`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31ffc577a6edce14511e0404d73b48461b272bcfb60bab890cc7ccf4e61c0a`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3d6ead5b26e1a32d1d3c1b71d9767aa00743fc64733b871c6bbf2591d81d9d`  
		Last Modified: Mon, 25 Nov 2024 20:31:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:75ef835d7b856c1f934a370f28c1336a8bf0c0c0944462062a9317cf254d4ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a332ef769be7ab9d9d100bae943b3e2f1af4fc69a07fd08c591da9bf40f49`

```dockerfile
```

-	Layers:
	-	`sha256:3696bda8b095f58496bd3db9f0795eed260b1c194a955d81ee26ac412e6dbc02`  
		Last Modified: Mon, 25 Nov 2024 20:31:28 GMT  
		Size: 57.3 MB (57260886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a36439b8d122b7727196c04e60688c8493e56dc9dfdec71bab35384df7975b4`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:249394c80de1afe549e21df093182a3562ac870e8f33aef14ae7fcc1a33b1b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.2 MB (678165891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e527f4a1fdf4de582ad9fc12ca026d3ee07e71c92c30cbd8f52ff97887ff58`
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
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
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
	-	`sha256:5b7171c978e079b5f38d49480060c57fbdc2109fe4dd925b4deec46f41d2a6ff`  
		Last Modified: Mon, 25 Nov 2024 20:33:47 GMT  
		Size: 363.4 MB (363393731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d226da017e27af535cefe9931994faddca35b7d916f648f1dd8368b8dabc5d`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ec2d2f254202a162279de968878bbd07d01e9a8e2cfe7865f85dd0f473fea`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584ad5a62aeeac9c71767750791bb6a7678373a2fdafaaeec5ae275695400c1`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77534b5938029530e4096968ea8c54f944e4746e8461b7989b949465b9301fb`  
		Last Modified: Mon, 25 Nov 2024 20:33:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b39d5177f242c90faf213fb94814d3f11ed56d89e4d977e3762a0c93f6d3f53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac861a439bba788c553fe1545ab03af9f83b0c25f2c10cca6c2e44a0c9f3adc5`

```dockerfile
```

-	Layers:
	-	`sha256:d0b34ce28ec2bd9d116d571ab93d2398bef6baedb218ac7f7ac926fa32be56b5`  
		Last Modified: Mon, 25 Nov 2024 20:33:26 GMT  
		Size: 57.3 MB (57261751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bac00a9d8108fec117b5d00b192de8d2f5cfd669f283d7d0654a1429a8e6c6`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
