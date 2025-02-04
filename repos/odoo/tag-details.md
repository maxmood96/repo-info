<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20250131`](#odoo160-20250131)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250131`](#odoo170-20250131)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250131`](#odoo180-20250131)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:44ffb033b6766f428fd09d1faa53af67929c82a3144c1bf5002c523841dbd0c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:fe6434685a3e618767de336b5909ff7b4be579ad38d088570fc00167b7736507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583947457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9188eba0b945b8e298262f211f7198f2129b6f0d9459782354642d4328634f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9dff007ca8df83cd7549d05502e4e9cbe26c7e572e0255755fc0c723b73a9`  
		Last Modified: Tue, 04 Feb 2025 04:45:57 GMT  
		Size: 219.6 MB (219628422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461f20c6470e4105ab7ea5fa31ec10f0f0598b124e47a42dcb27b090e26c199`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 2.6 MB (2575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0e6c1c0aa0c0952ce6097b0621541495cabf7a2e0a86ad19aa0c8fbe06ab9`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a837939eb8de4ca3b858ef4c3ffe9019410c44b656ff5c14e60c7d8dd70ff`  
		Last Modified: Tue, 04 Feb 2025 04:46:01 GMT  
		Size: 331.0 MB (331003170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7066f5e377f4d63caf439d58b48859d6a066321ee2afe4556fa42d594cc431`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d030c50014b669d541e7859f33ee7d939f05e95f7fd00fc55163264e37bd159b`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83161e7cdaa2a92fd1a88f92fe45edf11f2d895332734d1383f32ad469ae26d`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a540d29e3e23ed474a821e7e9df3da0df1cf3561ee54e2f29e024c7e4c53a`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:c6e6e9fc6fd880313ef6f509f72637e77bd39fc44e55ed08d3ba09bc1697d503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38857726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cae739bab16ca246cda267aed81ba5a158e495f356ce9cd607b5194e3c7225`

```dockerfile
```

-	Layers:
	-	`sha256:b8d330cc74dd2c21ea4f6f27e02f30e3ee6e57e218025f576aaeed439dac87c3`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 38.8 MB (38831009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0d1c09a00999a605bb2c07a7ecb4094c090498afb7eaf30369ba6b687b2f2e`  
		Last Modified: Tue, 04 Feb 2025 04:45:51 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:159bc41c15bd708c44054359e4b6377f030a0f1b8fafc1affc5538101206229f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a65fea642d52ae475e8ff6b0f3b561d66c5af070bab7f1d0adea814728b59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185a4e5a9d1db1426978bb5d59f47ad557b0d06620f267e6922d2d466c0fa93`  
		Last Modified: Fri, 31 Jan 2025 20:40:05 GMT  
		Size: 330.7 MB (330677410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f7dd764c4c7241e104af3514c9992fdd89599886e9593ad69e45d0896a12cd`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eccb67e35b76d1f75cb09de83edd4afde66b87c5316fff55f3b42120ebf00`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25273c2baaa1c054bb690ddea956494052065317e49115f51fcc6f13258ba19b`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b090ff33699ab93a8408a5980bfa6cb98b2294286b71ec8eaa8448395c189cd1`  
		Last Modified: Fri, 31 Jan 2025 20:39:58 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:0d9553f2953d9fc05183586681eaab4cc5d1a51550cdd2fd8385792bd27e1fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38864331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa670bc355efd63aad7f506314fc8fc76de002a23979697899470fa1ffa5ff46`

```dockerfile
```

-	Layers:
	-	`sha256:71716b052dc6a0e4555e9b40145adaa83ad6cbf35a0b8288ae149e6ae9b8062f`  
		Last Modified: Fri, 31 Jan 2025 20:39:59 GMT  
		Size: 38.8 MB (38837461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c2455ae34c34a11a3b4b9a460403984a7a9f73a881f5f4536c30db07a0c90e`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:44ffb033b6766f428fd09d1faa53af67929c82a3144c1bf5002c523841dbd0c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:fe6434685a3e618767de336b5909ff7b4be579ad38d088570fc00167b7736507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583947457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9188eba0b945b8e298262f211f7198f2129b6f0d9459782354642d4328634f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9dff007ca8df83cd7549d05502e4e9cbe26c7e572e0255755fc0c723b73a9`  
		Last Modified: Tue, 04 Feb 2025 04:45:57 GMT  
		Size: 219.6 MB (219628422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461f20c6470e4105ab7ea5fa31ec10f0f0598b124e47a42dcb27b090e26c199`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 2.6 MB (2575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0e6c1c0aa0c0952ce6097b0621541495cabf7a2e0a86ad19aa0c8fbe06ab9`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a837939eb8de4ca3b858ef4c3ffe9019410c44b656ff5c14e60c7d8dd70ff`  
		Last Modified: Tue, 04 Feb 2025 04:46:01 GMT  
		Size: 331.0 MB (331003170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7066f5e377f4d63caf439d58b48859d6a066321ee2afe4556fa42d594cc431`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d030c50014b669d541e7859f33ee7d939f05e95f7fd00fc55163264e37bd159b`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83161e7cdaa2a92fd1a88f92fe45edf11f2d895332734d1383f32ad469ae26d`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a540d29e3e23ed474a821e7e9df3da0df1cf3561ee54e2f29e024c7e4c53a`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c6e6e9fc6fd880313ef6f509f72637e77bd39fc44e55ed08d3ba09bc1697d503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38857726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cae739bab16ca246cda267aed81ba5a158e495f356ce9cd607b5194e3c7225`

```dockerfile
```

-	Layers:
	-	`sha256:b8d330cc74dd2c21ea4f6f27e02f30e3ee6e57e218025f576aaeed439dac87c3`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 38.8 MB (38831009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0d1c09a00999a605bb2c07a7ecb4094c090498afb7eaf30369ba6b687b2f2e`  
		Last Modified: Tue, 04 Feb 2025 04:45:51 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:159bc41c15bd708c44054359e4b6377f030a0f1b8fafc1affc5538101206229f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a65fea642d52ae475e8ff6b0f3b561d66c5af070bab7f1d0adea814728b59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185a4e5a9d1db1426978bb5d59f47ad557b0d06620f267e6922d2d466c0fa93`  
		Last Modified: Fri, 31 Jan 2025 20:40:05 GMT  
		Size: 330.7 MB (330677410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f7dd764c4c7241e104af3514c9992fdd89599886e9593ad69e45d0896a12cd`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eccb67e35b76d1f75cb09de83edd4afde66b87c5316fff55f3b42120ebf00`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25273c2baaa1c054bb690ddea956494052065317e49115f51fcc6f13258ba19b`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b090ff33699ab93a8408a5980bfa6cb98b2294286b71ec8eaa8448395c189cd1`  
		Last Modified: Fri, 31 Jan 2025 20:39:58 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0d9553f2953d9fc05183586681eaab4cc5d1a51550cdd2fd8385792bd27e1fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38864331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa670bc355efd63aad7f506314fc8fc76de002a23979697899470fa1ffa5ff46`

```dockerfile
```

-	Layers:
	-	`sha256:71716b052dc6a0e4555e9b40145adaa83ad6cbf35a0b8288ae149e6ae9b8062f`  
		Last Modified: Fri, 31 Jan 2025 20:39:59 GMT  
		Size: 38.8 MB (38837461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c2455ae34c34a11a3b4b9a460403984a7a9f73a881f5f4536c30db07a0c90e`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20250131`

```console
$ docker pull odoo@sha256:44ffb033b6766f428fd09d1faa53af67929c82a3144c1bf5002c523841dbd0c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20250131` - linux; amd64

```console
$ docker pull odoo@sha256:fe6434685a3e618767de336b5909ff7b4be579ad38d088570fc00167b7736507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **583.9 MB (583947457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9188eba0b945b8e298262f211f7198f2129b6f0d9459782354642d4328634f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 31 Jan 2025 09:32:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a9dff007ca8df83cd7549d05502e4e9cbe26c7e572e0255755fc0c723b73a9`  
		Last Modified: Tue, 04 Feb 2025 04:45:57 GMT  
		Size: 219.6 MB (219628422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461f20c6470e4105ab7ea5fa31ec10f0f0598b124e47a42dcb27b090e26c199`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 2.6 MB (2575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc0e6c1c0aa0c0952ce6097b0621541495cabf7a2e0a86ad19aa0c8fbe06ab9`  
		Last Modified: Tue, 04 Feb 2025 04:45:52 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a837939eb8de4ca3b858ef4c3ffe9019410c44b656ff5c14e60c7d8dd70ff`  
		Last Modified: Tue, 04 Feb 2025 04:46:01 GMT  
		Size: 331.0 MB (331003170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7066f5e377f4d63caf439d58b48859d6a066321ee2afe4556fa42d594cc431`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d030c50014b669d541e7859f33ee7d939f05e95f7fd00fc55163264e37bd159b`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83161e7cdaa2a92fd1a88f92fe45edf11f2d895332734d1383f32ad469ae26d`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a540d29e3e23ed474a821e7e9df3da0df1cf3561ee54e2f29e024c7e4c53a`  
		Last Modified: Tue, 04 Feb 2025 04:45:54 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:c6e6e9fc6fd880313ef6f509f72637e77bd39fc44e55ed08d3ba09bc1697d503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38857726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cae739bab16ca246cda267aed81ba5a158e495f356ce9cd607b5194e3c7225`

```dockerfile
```

-	Layers:
	-	`sha256:b8d330cc74dd2c21ea4f6f27e02f30e3ee6e57e218025f576aaeed439dac87c3`  
		Last Modified: Tue, 04 Feb 2025 04:45:53 GMT  
		Size: 38.8 MB (38831009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f0d1c09a00999a605bb2c07a7ecb4094c090498afb7eaf30369ba6b687b2f2e`  
		Last Modified: Tue, 04 Feb 2025 04:45:51 GMT  
		Size: 26.7 KB (26717 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20250131` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:159bc41c15bd708c44054359e4b6377f030a0f1b8fafc1affc5538101206229f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579415900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04a65fea642d52ae475e8ff6b0f3b561d66c5af070bab7f1d0adea814728b59`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=C.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=16.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=ce36944289e17a9dcdde842ba9ad8508f9436237
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5d24d3e69c750d459da58fa8db7e255f0e6a8f27b1e06c76cc242cb82ee255`  
		Last Modified: Tue, 14 Jan 2025 07:42:55 GMT  
		Size: 216.9 MB (216921993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe08e0fd5c7f22cb24ce54385a0a3acf88fafb46c2b24d130642e7e3dbb47a95`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 2.6 MB (2583723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bb815672e62f69a2df6317a108d924edbe05d142421e9f9d00819a27ca84b1`  
		Last Modified: Tue, 14 Jan 2025 07:42:50 GMT  
		Size: 485.4 KB (485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a185a4e5a9d1db1426978bb5d59f47ad557b0d06620f267e6922d2d466c0fa93`  
		Last Modified: Fri, 31 Jan 2025 20:40:05 GMT  
		Size: 330.7 MB (330677410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f7dd764c4c7241e104af3514c9992fdd89599886e9593ad69e45d0896a12cd`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3eccb67e35b76d1f75cb09de83edd4afde66b87c5316fff55f3b42120ebf00`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25273c2baaa1c054bb690ddea956494052065317e49115f51fcc6f13258ba19b`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b090ff33699ab93a8408a5980bfa6cb98b2294286b71ec8eaa8448395c189cd1`  
		Last Modified: Fri, 31 Jan 2025 20:39:58 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:0d9553f2953d9fc05183586681eaab4cc5d1a51550cdd2fd8385792bd27e1fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38864331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa670bc355efd63aad7f506314fc8fc76de002a23979697899470fa1ffa5ff46`

```dockerfile
```

-	Layers:
	-	`sha256:71716b052dc6a0e4555e9b40145adaa83ad6cbf35a0b8288ae149e6ae9b8062f`  
		Last Modified: Fri, 31 Jan 2025 20:39:59 GMT  
		Size: 38.8 MB (38837461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c2455ae34c34a11a3b4b9a460403984a7a9f73a881f5f4536c30db07a0c90e`  
		Last Modified: Fri, 31 Jan 2025 20:39:57 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:e0a5969d21547a6e32f8f0b3e45e9a48e3c10c3c265ccf28c649c2f563bec51e
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
$ docker pull odoo@sha256:236a4c4fe28ef3c01da8af0ca7c4d385da82fa5d327e4600a1c0b7c9427920f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599537258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b514ab807f7892fd9b40dd3c2c3be930aca19ec4a18569592e449cb4cf24823`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f908ff198a15fa403ffc4bb2cdce2da98da5ff849f3212988a2a2d6f74ce9de`  
		Last Modified: Tue, 04 Feb 2025 04:45:46 GMT  
		Size: 233.8 MB (233764363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aceca15d2ebdd36e220bda2b54e8257e8451aec0c792c4c3671feff7b0440b3`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 2.5 MB (2493910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3b362ca2656783ef6f8ba0e825777e2b37877bc5f4374f2d03ec39fbac22e`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 486.0 KB (486000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bb09415fdd8065d0c4560d0af94ad48cd7c7cfbaf6328e4b356f099287a183`  
		Last Modified: Tue, 04 Feb 2025 04:45:47 GMT  
		Size: 333.3 MB (333254612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89299832330096893cb6121944768c85f230da3ad8d56ea350da4fa0ea9f841e`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027728759a34449b67f5bba56072c49afc8c7eb0fb59f92cf5417acaca33da61`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2028b1d6dd5724e4482a6eb54572978b452b53c1c7b3ac86c1452ffb066e4`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678fb4e4bab5ad7d80435ef443bfed7eada17d454d35f6461c9354e38f064fa0`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:56ff431306f0bcaffa8b31e82a39061681b982d4de89c1a07abcf2626a1dbe08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39719765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aee95bd053caf77aee3627469635d5a9a5928f45863626397ef114c9fc9ef43`

```dockerfile
```

-	Layers:
	-	`sha256:584618fe99d6945015124b4d4b438f5665e3ac36edc521b13c9a65c78bd5c9df`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 39.7 MB (39692930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f00b4b8bd19c62beb113dea9cc9c7c226cea87653713f5467e16899c0e9486`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:827ed17b4f1e8d8ad0a7c08da74882a8721bdf1812aa2b0003ac0565fe24cb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594332302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c0ecd64a246c23a8cdb49262d7839153d84ea1efce35afee34b07519b4fcac`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45900a4ce0fd8736000ffac1e54c8ac066b5906d765f7779b1b29eb934b2b859`  
		Last Modified: Fri, 31 Jan 2025 20:36:00 GMT  
		Size: 332.9 MB (332855426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a108442a99d21048ccaa6773899ce861c749b7f27bc08defdde0eb91cbcab3`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435bef9576de2cc3cd5dfb94f37cfe759ed87313a3dab8e179cfe446821c2f1`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe6b5a45a1e6931ef9f6114fce8f68cbb865659d5fb6cc9f092ef1e0bba96d5`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a6e61200fb87a8b09da9abf0d1b8f129c1f25a5655b403bef18f53615e517`  
		Last Modified: Fri, 31 Jan 2025 20:35:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:0e8b7f4119c2acc1c0fde32de2df1eab9d98d8ce6e9f7c778ba3ddd5cf07d5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5bc794309580d11c11a74bfe465fc70355e036bcb64ea8456b7b74cbac09c5`

```dockerfile
```

-	Layers:
	-	`sha256:63d3e747dd3048f2e3603307da16c6fc6b013a0f70e47e360c46e436afaf49b6`  
		Last Modified: Fri, 31 Jan 2025 20:35:49 GMT  
		Size: 39.7 MB (39701317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a11925c4a4cbadbebf7338acf38111814cc201ab75a37c29ebcb0f5675d6bab`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:ddcdaf78f0a12cca73de87c4a972e07903afb134cba842650a5b41cc4a230b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (616015434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f16b44ddbfc2d5163a4ab6041182b04a61183602824cd795e7e4de56cf43906`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95640386a59563b02e9bd78f70d93282b4df6c36928abf36f3ac2b9ceaaf9f40`  
		Last Modified: Fri, 31 Jan 2025 18:45:03 GMT  
		Size: 335.0 MB (334978453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1f55c4afab68ab13f10674cfe9b90a01366ebb0038ca86229741d0f882647b`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193342d0c655c430677124d77ec6f5901f2f31a076b6821261fd2dfca7c9458d`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f93b7ccd771e57338ee074e3b55bb2a6c55b91dc3d415d302357cd8fca962f2`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc67372cf65b7469a532f7efb7252d604f114da6079910ba731dd31056d23180`  
		Last Modified: Fri, 31 Jan 2025 18:44:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:85b7e0da44ceef23ac98e9e0dc5bb41b80ce2f738296399d33143bff63ded68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d4788873af0baae7055f1430488947f3c56e4dd736283365190fd542f984db`

```dockerfile
```

-	Layers:
	-	`sha256:2abb948223b4be9b48cccca7d72aade23a709755dc3acdf4b67ed47ad0364e74`  
		Last Modified: Fri, 31 Jan 2025 18:44:41 GMT  
		Size: 39.7 MB (39703133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9548e006232783ea18a95c3f3ae7365274b0f7aed0acd340f2ccfc8cf37c3e`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:e0a5969d21547a6e32f8f0b3e45e9a48e3c10c3c265ccf28c649c2f563bec51e
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
$ docker pull odoo@sha256:236a4c4fe28ef3c01da8af0ca7c4d385da82fa5d327e4600a1c0b7c9427920f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599537258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b514ab807f7892fd9b40dd3c2c3be930aca19ec4a18569592e449cb4cf24823`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f908ff198a15fa403ffc4bb2cdce2da98da5ff849f3212988a2a2d6f74ce9de`  
		Last Modified: Tue, 04 Feb 2025 04:45:46 GMT  
		Size: 233.8 MB (233764363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aceca15d2ebdd36e220bda2b54e8257e8451aec0c792c4c3671feff7b0440b3`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 2.5 MB (2493910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3b362ca2656783ef6f8ba0e825777e2b37877bc5f4374f2d03ec39fbac22e`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 486.0 KB (486000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bb09415fdd8065d0c4560d0af94ad48cd7c7cfbaf6328e4b356f099287a183`  
		Last Modified: Tue, 04 Feb 2025 04:45:47 GMT  
		Size: 333.3 MB (333254612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89299832330096893cb6121944768c85f230da3ad8d56ea350da4fa0ea9f841e`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027728759a34449b67f5bba56072c49afc8c7eb0fb59f92cf5417acaca33da61`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2028b1d6dd5724e4482a6eb54572978b452b53c1c7b3ac86c1452ffb066e4`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678fb4e4bab5ad7d80435ef443bfed7eada17d454d35f6461c9354e38f064fa0`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:56ff431306f0bcaffa8b31e82a39061681b982d4de89c1a07abcf2626a1dbe08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39719765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aee95bd053caf77aee3627469635d5a9a5928f45863626397ef114c9fc9ef43`

```dockerfile
```

-	Layers:
	-	`sha256:584618fe99d6945015124b4d4b438f5665e3ac36edc521b13c9a65c78bd5c9df`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 39.7 MB (39692930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f00b4b8bd19c62beb113dea9cc9c7c226cea87653713f5467e16899c0e9486`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:827ed17b4f1e8d8ad0a7c08da74882a8721bdf1812aa2b0003ac0565fe24cb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594332302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c0ecd64a246c23a8cdb49262d7839153d84ea1efce35afee34b07519b4fcac`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45900a4ce0fd8736000ffac1e54c8ac066b5906d765f7779b1b29eb934b2b859`  
		Last Modified: Fri, 31 Jan 2025 20:36:00 GMT  
		Size: 332.9 MB (332855426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a108442a99d21048ccaa6773899ce861c749b7f27bc08defdde0eb91cbcab3`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435bef9576de2cc3cd5dfb94f37cfe759ed87313a3dab8e179cfe446821c2f1`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe6b5a45a1e6931ef9f6114fce8f68cbb865659d5fb6cc9f092ef1e0bba96d5`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a6e61200fb87a8b09da9abf0d1b8f129c1f25a5655b403bef18f53615e517`  
		Last Modified: Fri, 31 Jan 2025 20:35:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0e8b7f4119c2acc1c0fde32de2df1eab9d98d8ce6e9f7c778ba3ddd5cf07d5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5bc794309580d11c11a74bfe465fc70355e036bcb64ea8456b7b74cbac09c5`

```dockerfile
```

-	Layers:
	-	`sha256:63d3e747dd3048f2e3603307da16c6fc6b013a0f70e47e360c46e436afaf49b6`  
		Last Modified: Fri, 31 Jan 2025 20:35:49 GMT  
		Size: 39.7 MB (39701317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a11925c4a4cbadbebf7338acf38111814cc201ab75a37c29ebcb0f5675d6bab`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:ddcdaf78f0a12cca73de87c4a972e07903afb134cba842650a5b41cc4a230b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (616015434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f16b44ddbfc2d5163a4ab6041182b04a61183602824cd795e7e4de56cf43906`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95640386a59563b02e9bd78f70d93282b4df6c36928abf36f3ac2b9ceaaf9f40`  
		Last Modified: Fri, 31 Jan 2025 18:45:03 GMT  
		Size: 335.0 MB (334978453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1f55c4afab68ab13f10674cfe9b90a01366ebb0038ca86229741d0f882647b`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193342d0c655c430677124d77ec6f5901f2f31a076b6821261fd2dfca7c9458d`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f93b7ccd771e57338ee074e3b55bb2a6c55b91dc3d415d302357cd8fca962f2`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc67372cf65b7469a532f7efb7252d604f114da6079910ba731dd31056d23180`  
		Last Modified: Fri, 31 Jan 2025 18:44:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:85b7e0da44ceef23ac98e9e0dc5bb41b80ce2f738296399d33143bff63ded68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d4788873af0baae7055f1430488947f3c56e4dd736283365190fd542f984db`

```dockerfile
```

-	Layers:
	-	`sha256:2abb948223b4be9b48cccca7d72aade23a709755dc3acdf4b67ed47ad0364e74`  
		Last Modified: Fri, 31 Jan 2025 18:44:41 GMT  
		Size: 39.7 MB (39703133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9548e006232783ea18a95c3f3ae7365274b0f7aed0acd340f2ccfc8cf37c3e`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250131`

```console
$ docker pull odoo@sha256:e0a5969d21547a6e32f8f0b3e45e9a48e3c10c3c265ccf28c649c2f563bec51e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20250131` - linux; amd64

```console
$ docker pull odoo@sha256:236a4c4fe28ef3c01da8af0ca7c4d385da82fa5d327e4600a1c0b7c9427920f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.5 MB (599537258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b514ab807f7892fd9b40dd3c2c3be930aca19ec4a18569592e449cb4cf24823`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f908ff198a15fa403ffc4bb2cdce2da98da5ff849f3212988a2a2d6f74ce9de`  
		Last Modified: Tue, 04 Feb 2025 04:45:46 GMT  
		Size: 233.8 MB (233764363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aceca15d2ebdd36e220bda2b54e8257e8451aec0c792c4c3671feff7b0440b3`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 2.5 MB (2493910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3b362ca2656783ef6f8ba0e825777e2b37877bc5f4374f2d03ec39fbac22e`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 486.0 KB (486000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bb09415fdd8065d0c4560d0af94ad48cd7c7cfbaf6328e4b356f099287a183`  
		Last Modified: Tue, 04 Feb 2025 04:45:47 GMT  
		Size: 333.3 MB (333254612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89299832330096893cb6121944768c85f230da3ad8d56ea350da4fa0ea9f841e`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027728759a34449b67f5bba56072c49afc8c7eb0fb59f92cf5417acaca33da61`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2028b1d6dd5724e4482a6eb54572978b452b53c1c7b3ac86c1452ffb066e4`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678fb4e4bab5ad7d80435ef443bfed7eada17d454d35f6461c9354e38f064fa0`  
		Last Modified: Tue, 04 Feb 2025 04:45:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:56ff431306f0bcaffa8b31e82a39061681b982d4de89c1a07abcf2626a1dbe08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39719765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aee95bd053caf77aee3627469635d5a9a5928f45863626397ef114c9fc9ef43`

```dockerfile
```

-	Layers:
	-	`sha256:584618fe99d6945015124b4d4b438f5665e3ac36edc521b13c9a65c78bd5c9df`  
		Last Modified: Tue, 04 Feb 2025 04:45:43 GMT  
		Size: 39.7 MB (39692930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f00b4b8bd19c62beb113dea9cc9c7c226cea87653713f5467e16899c0e9486`  
		Last Modified: Tue, 04 Feb 2025 04:45:42 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250131` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:827ed17b4f1e8d8ad0a7c08da74882a8721bdf1812aa2b0003ac0565fe24cb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 MB (594332302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c0ecd64a246c23a8cdb49262d7839153d84ea1efce35afee34b07519b4fcac`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ec4903ad06f15a77b5bc7d9478e4efe03e19574e069a1c323b755949712d13`  
		Last Modified: Wed, 15 Jan 2025 21:36:40 GMT  
		Size: 231.1 MB (231144470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1c9faabded86415f8b589a233b87683de10e663a1748509bca962962ab2e34`  
		Last Modified: Wed, 15 Jan 2025 21:36:36 GMT  
		Size: 2.5 MB (2485698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f75bb3ce3a1db5400a884b03e52a7205e67189d079b438a548bc9cc03a58f0c`  
		Last Modified: Wed, 15 Jan 2025 21:36:35 GMT  
		Size: 485.9 KB (485940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45900a4ce0fd8736000ffac1e54c8ac066b5906d765f7779b1b29eb934b2b859`  
		Last Modified: Fri, 31 Jan 2025 20:36:00 GMT  
		Size: 332.9 MB (332855426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a108442a99d21048ccaa6773899ce861c749b7f27bc08defdde0eb91cbcab3`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e435bef9576de2cc3cd5dfb94f37cfe759ed87313a3dab8e179cfe446821c2f1`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe6b5a45a1e6931ef9f6114fce8f68cbb865659d5fb6cc9f092ef1e0bba96d5`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a6e61200fb87a8b09da9abf0d1b8f129c1f25a5655b403bef18f53615e517`  
		Last Modified: Fri, 31 Jan 2025 20:35:48 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:0e8b7f4119c2acc1c0fde32de2df1eab9d98d8ce6e9f7c778ba3ddd5cf07d5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39728304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5bc794309580d11c11a74bfe465fc70355e036bcb64ea8456b7b74cbac09c5`

```dockerfile
```

-	Layers:
	-	`sha256:63d3e747dd3048f2e3603307da16c6fc6b013a0f70e47e360c46e436afaf49b6`  
		Last Modified: Fri, 31 Jan 2025 20:35:49 GMT  
		Size: 39.7 MB (39701317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a11925c4a4cbadbebf7338acf38111814cc201ab75a37c29ebcb0f5675d6bab`  
		Last Modified: Fri, 31 Jan 2025 20:35:47 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250131` - linux; ppc64le

```console
$ docker pull odoo@sha256:ddcdaf78f0a12cca73de87c4a972e07903afb134cba842650a5b41cc4a230b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.0 MB (616015434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f16b44ddbfc2d5163a4ab6041182b04a61183602824cd795e7e4de56cf43906`
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
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=17.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=985a939e070acb3ef2fa1b8b4f5d779c9e8d2733
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e20dd12a5dc90e18349f058ef6faab0e98932d66235accdd4fd4ecf560e9ad`  
		Last Modified: Sat, 21 Dec 2024 00:03:57 GMT  
		Size: 243.3 MB (243302074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36515bda1dae9f508aeb3a52dd6bcac45d347f81ada928cb84ae0eee75d9cf73`  
		Last Modified: Sat, 21 Dec 2024 00:03:39 GMT  
		Size: 2.8 MB (2798263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50956b86a0face373e64d0520f8600ad9870ea660dddb2d3c74cc015a90699c`  
		Last Modified: Wed, 15 Jan 2025 20:39:58 GMT  
		Size: 486.0 KB (485959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95640386a59563b02e9bd78f70d93282b4df6c36928abf36f3ac2b9ceaaf9f40`  
		Last Modified: Fri, 31 Jan 2025 18:45:03 GMT  
		Size: 335.0 MB (334978453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1f55c4afab68ab13f10674cfe9b90a01366ebb0038ca86229741d0f882647b`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193342d0c655c430677124d77ec6f5901f2f31a076b6821261fd2dfca7c9458d`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f93b7ccd771e57338ee074e3b55bb2a6c55b91dc3d415d302357cd8fca962f2`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc67372cf65b7469a532f7efb7252d604f114da6079910ba731dd31056d23180`  
		Last Modified: Fri, 31 Jan 2025 18:44:38 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:85b7e0da44ceef23ac98e9e0dc5bb41b80ce2f738296399d33143bff63ded68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39730024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d4788873af0baae7055f1430488947f3c56e4dd736283365190fd542f984db`

```dockerfile
```

-	Layers:
	-	`sha256:2abb948223b4be9b48cccca7d72aade23a709755dc3acdf4b67ed47ad0364e74`  
		Last Modified: Fri, 31 Jan 2025 18:44:41 GMT  
		Size: 39.7 MB (39703133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9548e006232783ea18a95c3f3ae7365274b0f7aed0acd340f2ccfc8cf37c3e`  
		Last Modified: Fri, 31 Jan 2025 18:44:37 GMT  
		Size: 26.9 KB (26891 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:889671e0c117cc26bb18d2a89128239145ede9b90109fbceddc5cce28e7f61e3
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
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29863bc386ef463585df0275d24f83033559df3c98ec21b4b74a979e05ff341e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662455932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ebc0135c1b6784b3ca1f1f7560ad75f08a6e54126ed2837f97ee8a2ad8bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0864eb75fed672897da4d8302dedb0804cd5aae60b0c6b2fc08b21efd9bb27f9`  
		Last Modified: Fri, 31 Jan 2025 20:32:02 GMT  
		Size: 366.9 MB (366928562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bb86cbea5bce0113e2ca6e2bb590ed66c8b6f41370ca079e879b4479e68bc`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30e2b074feb6d039bd9273c98b081bf16ff95cf9538e34548bb7ab4d10914cf`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea85760badc27c02026865ea289d5bf470c22975a0cf0d9649af85ec57f3d0e`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6bcacb8601498f783ea25b84da22e8adc91d1df31219d5aff677954d128b0c`  
		Last Modified: Fri, 31 Jan 2025 20:31:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:cc7fa732c5b14d3fc03d12e75d65afde5f6e3c14e48cc612a3fb3ec2efb3d3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58441753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dd55afdcb10e10dfae1e1b4885f79a179d70ce08563b372311594d8efad318`

```dockerfile
```

-	Layers:
	-	`sha256:894b842f11dd3bdcef02298df507336306a215a94b44b922ad41489677638b30`  
		Last Modified: Fri, 31 Jan 2025 20:31:57 GMT  
		Size: 58.4 MB (58414453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b3adbf5677aabf2ae0ace3d8d722444a5078d50c7154f2860e2090f1d107d4`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:07fa2cc506d8386e307fd5a9b9c85e626481d03f028c61e2cf82862b7b877893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.3 MB (682346994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d72bffc01dc1e7f836a1035d9ffc09ae825ee5f7116bddbc88249a863643af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdef60a8dcc9aec2ddd3343287ada6d70e33a0aa8303bc2b8b7e3f1d3030a72`  
		Last Modified: Fri, 31 Jan 2025 18:39:03 GMT  
		Size: 367.6 MB (367604296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2b6f0c1a007e4f6a69d284940a1e2f3155837ed6571aa2de3ba6f7dc28b674`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c9a04b24d1934fc6d44cb5544b5d8004c600a4deac6bd13f827ff465dc986b`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c7459f841a4ad511869b7618611be5fb6000aff44cb9c96034141a52a7c9ef`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43d86e3c2d80c60847ec380f9ffae752e98acbd9d16d6aacd20a967203a9828`  
		Last Modified: Fri, 31 Jan 2025 18:38:52 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:d1b4995eecb562d0c5227a10aef0cc6bd34536aa64ff24ad683a5738fbff8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58442523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99ceb0f39445c888b8e9bbd089a647bf2d37ad6dd654002a77ae027dad7f260`

```dockerfile
```

-	Layers:
	-	`sha256:acbab321fe98b4ff55f8c364d52a13dd12313de2aad30db1d3e7c1cebb37af25`  
		Last Modified: Fri, 31 Jan 2025 18:38:53 GMT  
		Size: 58.4 MB (58415325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a1be72caad2d693637453e9e0b0d72240fcf6b068d56520032fa4a095a7183`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:889671e0c117cc26bb18d2a89128239145ede9b90109fbceddc5cce28e7f61e3
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
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29863bc386ef463585df0275d24f83033559df3c98ec21b4b74a979e05ff341e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662455932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ebc0135c1b6784b3ca1f1f7560ad75f08a6e54126ed2837f97ee8a2ad8bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0864eb75fed672897da4d8302dedb0804cd5aae60b0c6b2fc08b21efd9bb27f9`  
		Last Modified: Fri, 31 Jan 2025 20:32:02 GMT  
		Size: 366.9 MB (366928562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bb86cbea5bce0113e2ca6e2bb590ed66c8b6f41370ca079e879b4479e68bc`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30e2b074feb6d039bd9273c98b081bf16ff95cf9538e34548bb7ab4d10914cf`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea85760badc27c02026865ea289d5bf470c22975a0cf0d9649af85ec57f3d0e`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6bcacb8601498f783ea25b84da22e8adc91d1df31219d5aff677954d128b0c`  
		Last Modified: Fri, 31 Jan 2025 20:31:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cc7fa732c5b14d3fc03d12e75d65afde5f6e3c14e48cc612a3fb3ec2efb3d3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58441753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dd55afdcb10e10dfae1e1b4885f79a179d70ce08563b372311594d8efad318`

```dockerfile
```

-	Layers:
	-	`sha256:894b842f11dd3bdcef02298df507336306a215a94b44b922ad41489677638b30`  
		Last Modified: Fri, 31 Jan 2025 20:31:57 GMT  
		Size: 58.4 MB (58414453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b3adbf5677aabf2ae0ace3d8d722444a5078d50c7154f2860e2090f1d107d4`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:07fa2cc506d8386e307fd5a9b9c85e626481d03f028c61e2cf82862b7b877893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.3 MB (682346994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d72bffc01dc1e7f836a1035d9ffc09ae825ee5f7116bddbc88249a863643af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdef60a8dcc9aec2ddd3343287ada6d70e33a0aa8303bc2b8b7e3f1d3030a72`  
		Last Modified: Fri, 31 Jan 2025 18:39:03 GMT  
		Size: 367.6 MB (367604296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2b6f0c1a007e4f6a69d284940a1e2f3155837ed6571aa2de3ba6f7dc28b674`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c9a04b24d1934fc6d44cb5544b5d8004c600a4deac6bd13f827ff465dc986b`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c7459f841a4ad511869b7618611be5fb6000aff44cb9c96034141a52a7c9ef`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43d86e3c2d80c60847ec380f9ffae752e98acbd9d16d6aacd20a967203a9828`  
		Last Modified: Fri, 31 Jan 2025 18:38:52 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d1b4995eecb562d0c5227a10aef0cc6bd34536aa64ff24ad683a5738fbff8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58442523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99ceb0f39445c888b8e9bbd089a647bf2d37ad6dd654002a77ae027dad7f260`

```dockerfile
```

-	Layers:
	-	`sha256:acbab321fe98b4ff55f8c364d52a13dd12313de2aad30db1d3e7c1cebb37af25`  
		Last Modified: Fri, 31 Jan 2025 18:38:53 GMT  
		Size: 58.4 MB (58415325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a1be72caad2d693637453e9e0b0d72240fcf6b068d56520032fa4a095a7183`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250131`

```console
$ docker pull odoo@sha256:889671e0c117cc26bb18d2a89128239145ede9b90109fbceddc5cce28e7f61e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250131` - linux; amd64

```console
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250131` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29863bc386ef463585df0275d24f83033559df3c98ec21b4b74a979e05ff341e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662455932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ebc0135c1b6784b3ca1f1f7560ad75f08a6e54126ed2837f97ee8a2ad8bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0864eb75fed672897da4d8302dedb0804cd5aae60b0c6b2fc08b21efd9bb27f9`  
		Last Modified: Fri, 31 Jan 2025 20:32:02 GMT  
		Size: 366.9 MB (366928562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bb86cbea5bce0113e2ca6e2bb590ed66c8b6f41370ca079e879b4479e68bc`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30e2b074feb6d039bd9273c98b081bf16ff95cf9538e34548bb7ab4d10914cf`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea85760badc27c02026865ea289d5bf470c22975a0cf0d9649af85ec57f3d0e`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6bcacb8601498f783ea25b84da22e8adc91d1df31219d5aff677954d128b0c`  
		Last Modified: Fri, 31 Jan 2025 20:31:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:cc7fa732c5b14d3fc03d12e75d65afde5f6e3c14e48cc612a3fb3ec2efb3d3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58441753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dd55afdcb10e10dfae1e1b4885f79a179d70ce08563b372311594d8efad318`

```dockerfile
```

-	Layers:
	-	`sha256:894b842f11dd3bdcef02298df507336306a215a94b44b922ad41489677638b30`  
		Last Modified: Fri, 31 Jan 2025 20:31:57 GMT  
		Size: 58.4 MB (58414453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b3adbf5677aabf2ae0ace3d8d722444a5078d50c7154f2860e2090f1d107d4`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250131` - linux; ppc64le

```console
$ docker pull odoo@sha256:07fa2cc506d8386e307fd5a9b9c85e626481d03f028c61e2cf82862b7b877893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.3 MB (682346994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d72bffc01dc1e7f836a1035d9ffc09ae825ee5f7116bddbc88249a863643af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdef60a8dcc9aec2ddd3343287ada6d70e33a0aa8303bc2b8b7e3f1d3030a72`  
		Last Modified: Fri, 31 Jan 2025 18:39:03 GMT  
		Size: 367.6 MB (367604296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2b6f0c1a007e4f6a69d284940a1e2f3155837ed6571aa2de3ba6f7dc28b674`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c9a04b24d1934fc6d44cb5544b5d8004c600a4deac6bd13f827ff465dc986b`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c7459f841a4ad511869b7618611be5fb6000aff44cb9c96034141a52a7c9ef`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43d86e3c2d80c60847ec380f9ffae752e98acbd9d16d6aacd20a967203a9828`  
		Last Modified: Fri, 31 Jan 2025 18:38:52 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250131` - unknown; unknown

```console
$ docker pull odoo@sha256:d1b4995eecb562d0c5227a10aef0cc6bd34536aa64ff24ad683a5738fbff8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58442523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99ceb0f39445c888b8e9bbd089a647bf2d37ad6dd654002a77ae027dad7f260`

```dockerfile
```

-	Layers:
	-	`sha256:acbab321fe98b4ff55f8c364d52a13dd12313de2aad30db1d3e7c1cebb37af25`  
		Last Modified: Fri, 31 Jan 2025 18:38:53 GMT  
		Size: 58.4 MB (58415325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a1be72caad2d693637453e9e0b0d72240fcf6b068d56520032fa4a095a7183`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:889671e0c117cc26bb18d2a89128239145ede9b90109fbceddc5cce28e7f61e3
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
$ docker pull odoo@sha256:18922200f004298d703387c6c3b2ffac39ab9cc5c586105a68a3fee421b28248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.5 MB (668451871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01068d87670c4de2d1a92219beea5e1f2fdc158e786a222f761a6961f9e28f6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=amd64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f64306616e5781b1a6ab1f2fdbdd2bd7bb8263a3072e3a929412da1211ec761`  
		Last Modified: Tue, 04 Feb 2025 04:46:41 GMT  
		Size: 254.5 MB (254512391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4939309b587bbc8111eb9909e22fa09c784ae8418967462c2a882884463ddba0`  
		Last Modified: Tue, 04 Feb 2025 04:46:35 GMT  
		Size: 16.6 MB (16634807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e498194b1d010c556ef13f215a0fd5d6ab461b859000f5dc69c376a5657f75`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 485.8 KB (485776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1974bb6baecede8575c5a305df544e966234a25143fa751751c9708f6a048ff1`  
		Last Modified: Tue, 04 Feb 2025 04:46:43 GMT  
		Size: 367.1 MB (367062167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc1660c216912b5c414fcf14882bfe18d5444aa38a8713d8bfb5daf4d28cd0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb89c83e12624d516ce38d75f32f3b162cf68a4a00a2acdcf630aaf79198fc0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bcb3c54a894f719fe58ca96d730adc9cf9af1312ffed4cf151f88563d435b5`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9a7f257cc13691c033b602d24c9ae947929d0e2e9a039c9bdaf110e71c8ed`  
		Last Modified: Tue, 04 Feb 2025 04:46:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:583447d7e1bb403357ec3cf3a8056490d0f2086dc0edf2385bc826605ad0826c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58437672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6f1c5686d723c2debd5996bf6a4db0bfc76db84da56627bb435c1fe143376`

```dockerfile
```

-	Layers:
	-	`sha256:11a32acd218c46bf97c2b2c719af9e879147571fc347fa113627df1e9d7b03f0`  
		Last Modified: Tue, 04 Feb 2025 04:46:36 GMT  
		Size: 58.4 MB (58410536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6315274aea712e007b78539387e6b656b305577f058f32c344935f75f2f42838`  
		Last Modified: Tue, 04 Feb 2025 04:46:34 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:29863bc386ef463585df0275d24f83033559df3c98ec21b4b74a979e05ff341e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.5 MB (662455932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223ebc0135c1b6784b3ca1f1f7560ad75f08a6e54126ed2837f97ee8a2ad8bd5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=arm64
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0ee3dc37083c88d416c17dbed8e797e8f0c5a483a27bc2bb5f9866637cd604`  
		Last Modified: Wed, 15 Jan 2025 21:29:48 GMT  
		Size: 251.9 MB (251942154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf31355664213f01d2ffaa2ff07ceb2a41cacd6b8d61b1aefdf91f894149be`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 14.2 MB (14204373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ed3c8a8f456bc9aa89bd20c60375a56af4be0c47c96ca7d2390addbc272e8d`  
		Last Modified: Wed, 15 Jan 2025 21:29:41 GMT  
		Size: 485.7 KB (485733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0864eb75fed672897da4d8302dedb0804cd5aae60b0c6b2fc08b21efd9bb27f9`  
		Last Modified: Fri, 31 Jan 2025 20:32:02 GMT  
		Size: 366.9 MB (366928562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bb86cbea5bce0113e2ca6e2bb590ed66c8b6f41370ca079e879b4479e68bc`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30e2b074feb6d039bd9273c98b081bf16ff95cf9538e34548bb7ab4d10914cf`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea85760badc27c02026865ea289d5bf470c22975a0cf0d9649af85ec57f3d0e`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6bcacb8601498f783ea25b84da22e8adc91d1df31219d5aff677954d128b0c`  
		Last Modified: Fri, 31 Jan 2025 20:31:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cc7fa732c5b14d3fc03d12e75d65afde5f6e3c14e48cc612a3fb3ec2efb3d3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58441753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dd55afdcb10e10dfae1e1b4885f79a179d70ce08563b372311594d8efad318`

```dockerfile
```

-	Layers:
	-	`sha256:894b842f11dd3bdcef02298df507336306a215a94b44b922ad41489677638b30`  
		Last Modified: Fri, 31 Jan 2025 20:31:57 GMT  
		Size: 58.4 MB (58414453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b3adbf5677aabf2ae0ace3d8d722444a5078d50c7154f2860e2090f1d107d4`  
		Last Modified: Fri, 31 Jan 2025 20:31:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:07fa2cc506d8386e307fd5a9b9c85e626481d03f028c61e2cf82862b7b877893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.3 MB (682346994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d72bffc01dc1e7f836a1035d9ffc09ae825ee5f7116bddbc88249a863643af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Fri, 31 Jan 2025 09:32:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 31 Jan 2025 09:32:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 31 Jan 2025 09:32:32 GMT
ARG TARGETARCH=ppc64le
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_VERSION=18.0
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_RELEASE=20250131
# Fri, 31 Jan 2025 09:32:32 GMT
ARG ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250131 ODOO_SHA=7ca4d5ab97b14573489bdef9c5bdcb9f694975ca
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 31 Jan 2025 09:32:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 31 Jan 2025 09:32:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 31 Jan 2025 09:32:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 31 Jan 2025 09:32:32 GMT
USER odoo
# Fri, 31 Jan 2025 09:32:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 31 Jan 2025 09:32:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e4f22669c2b218e3b4c8798711c74160bdbcc4d4ae6a4e5d8fa984c7c54292`  
		Last Modified: Wed, 15 Jan 2025 20:34:09 GMT  
		Size: 485.7 KB (485738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdef60a8dcc9aec2ddd3343287ada6d70e33a0aa8303bc2b8b7e3f1d3030a72`  
		Last Modified: Fri, 31 Jan 2025 18:39:03 GMT  
		Size: 367.6 MB (367604296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2b6f0c1a007e4f6a69d284940a1e2f3155837ed6571aa2de3ba6f7dc28b674`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c9a04b24d1934fc6d44cb5544b5d8004c600a4deac6bd13f827ff465dc986b`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c7459f841a4ad511869b7618611be5fb6000aff44cb9c96034141a52a7c9ef`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43d86e3c2d80c60847ec380f9ffae752e98acbd9d16d6aacd20a967203a9828`  
		Last Modified: Fri, 31 Jan 2025 18:38:52 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d1b4995eecb562d0c5227a10aef0cc6bd34536aa64ff24ad683a5738fbff8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58442523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99ceb0f39445c888b8e9bbd089a647bf2d37ad6dd654002a77ae027dad7f260`

```dockerfile
```

-	Layers:
	-	`sha256:acbab321fe98b4ff55f8c364d52a13dd12313de2aad30db1d3e7c1cebb37af25`  
		Last Modified: Fri, 31 Jan 2025 18:38:53 GMT  
		Size: 58.4 MB (58415325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a1be72caad2d693637453e9e0b0d72240fcf6b068d56520032fa4a095a7183`  
		Last Modified: Fri, 31 Jan 2025 18:38:51 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
