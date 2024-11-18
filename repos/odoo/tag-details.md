<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241118`](#odoo160-20241118)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241118`](#odoo170-20241118)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241118`](#odoo180-20241118)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:28bb100818f3990c620b0b6b9704254291c95c8cb23ca0e6dfb78d025559fdc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:7bda4ba78c1a0eb7f4a56f76d90ecf948f38e4f8172ecf5cf3ec7ab526765d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584540965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d139ab2443d52845f62ac4d54e26a4695e90e4019315af97cd0fc8e4f9c09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 08 Nov 2024 10:31:04 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a6458d5081c8d9ad6bed8c965b5082aaafd0972bbb9c7fef454600cee80e1e`  
		Last Modified: Tue, 12 Nov 2024 02:42:42 GMT  
		Size: 219.6 MB (219606364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87919d16020b329624e114e662b74108d18b327366aa4e07d99872b71817aaaa`  
		Last Modified: Tue, 12 Nov 2024 02:42:38 GMT  
		Size: 2.5 MB (2493983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f7618b089a2b3d81528f39801a27c7d59e552585237adf075470d71113311`  
		Last Modified: Tue, 12 Nov 2024 02:42:38 GMT  
		Size: 469.0 KB (469029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13b7446e894c273c1cff0efca1b03600ac6381b6796cca6f07d6b2715f01ffa`  
		Last Modified: Tue, 12 Nov 2024 02:42:43 GMT  
		Size: 330.5 MB (330517596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a366305765257826ca29f8b87478dcbc7adca9e831b208df34d5accabfab1`  
		Last Modified: Tue, 12 Nov 2024 02:42:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6874a533e293b2af390392c2d4a3e63015450278af64e0c9fb116ea7c6441e45`  
		Last Modified: Tue, 12 Nov 2024 02:42:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3527b1f1daff1973e0291fc2162777204ce64f9135bfe808bf1ef1cf2dc9f63`  
		Last Modified: Tue, 12 Nov 2024 02:42:40 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32572b53df32ed0430ce959fbe4e639ae9030aaff9015ab9597d0d78b8acd14`  
		Last Modified: Tue, 12 Nov 2024 02:42:40 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:92b2a3c524966d9bf05d76736e0a5fa0dc2c84d439935e7b02c5d84ea6e8b2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38882492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3fcf1cfbba48e1436e9b7a077ea18c3b7f0e3b5d3c3466eaeaad17200230c3`

```dockerfile
```

-	Layers:
	-	`sha256:db7bb6e5bef047bf67af9980f4bc6b01e6bbbeca91af170f93309cefb4ed0a40`  
		Last Modified: Tue, 12 Nov 2024 02:42:39 GMT  
		Size: 38.9 MB (38855774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c77b881347c98635452df385ba644c78aa19d0a356945b257c366d412efac0`  
		Last Modified: Tue, 12 Nov 2024 02:42:38 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b4018c3ea352bdfd013a5104bfc5175f4a004392f13fd3042d29aa457782e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580147486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e167eb52f9562249f3403b475d003adcbfc602767b01a3e893d1501d0bba4564`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 08 Nov 2024 10:31:04 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f325f67dcdea3c7c37d04ebf758af75d8fa377127a1eeb9a2b57eb47236d01ae`  
		Last Modified: Tue, 12 Nov 2024 18:43:18 GMT  
		Size: 216.9 MB (216917318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4e5699e1771e02ef2e693da3d1e2a33ff6e4ff5329844bdc54423747c3f240`  
		Last Modified: Tue, 12 Nov 2024 18:43:14 GMT  
		Size: 2.5 MB (2504033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9a4b3774a0a797ab1832abe48ab92a1b5abcbd65b2e530136089977093f5f7`  
		Last Modified: Tue, 12 Nov 2024 18:43:14 GMT  
		Size: 469.1 KB (469064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6a855747d37eb46bf5176a2b3b14db5b8af6500cce23957b8c609318335f7d`  
		Last Modified: Tue, 12 Nov 2024 18:43:21 GMT  
		Size: 330.2 MB (330163040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968fbdfa14598642fcd51410eae70c421be54e2fe2568016b62ffc4861bc9831`  
		Last Modified: Tue, 12 Nov 2024 18:43:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a77e451d13e82def1864449890cf0e34f5c26cd20a70a9ff17b4e3051e87a6`  
		Last Modified: Tue, 12 Nov 2024 18:43:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39848f0511a876a36fc793011fe40bc001556d1db74190f3390a071cf6d69c`  
		Last Modified: Tue, 12 Nov 2024 18:43:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d24957eac22c275802bda57ed92b04e8c05aae591a43be3a59b557b44461a`  
		Last Modified: Tue, 12 Nov 2024 18:43:16 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:9a713ee735a9290e8a392fc474d53910afd0278ba889eb8384a0535ba4f57cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38889116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db6138856bde75084976e4d50accc8e325e03aa3e47e21d852b5e1bfd056f97`

```dockerfile
```

-	Layers:
	-	`sha256:c14fdbef5ac3a6edd522944d3b6314174972da230a4f5493e428ee91a7947837`  
		Last Modified: Tue, 12 Nov 2024 18:43:15 GMT  
		Size: 38.9 MB (38862246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162fa4d9af9e544aeab90ec92af92aba666cfe19e596fa57742f94a386cb3c97`  
		Last Modified: Tue, 12 Nov 2024 18:43:13 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:28bb100818f3990c620b0b6b9704254291c95c8cb23ca0e6dfb78d025559fdc2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:7bda4ba78c1a0eb7f4a56f76d90ecf948f38e4f8172ecf5cf3ec7ab526765d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584540965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d139ab2443d52845f62ac4d54e26a4695e90e4019315af97cd0fc8e4f9c09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 08 Nov 2024 10:31:04 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a6458d5081c8d9ad6bed8c965b5082aaafd0972bbb9c7fef454600cee80e1e`  
		Last Modified: Tue, 12 Nov 2024 02:42:42 GMT  
		Size: 219.6 MB (219606364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87919d16020b329624e114e662b74108d18b327366aa4e07d99872b71817aaaa`  
		Last Modified: Tue, 12 Nov 2024 02:42:38 GMT  
		Size: 2.5 MB (2493983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36f7618b089a2b3d81528f39801a27c7d59e552585237adf075470d71113311`  
		Last Modified: Tue, 12 Nov 2024 02:42:38 GMT  
		Size: 469.0 KB (469029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13b7446e894c273c1cff0efca1b03600ac6381b6796cca6f07d6b2715f01ffa`  
		Last Modified: Tue, 12 Nov 2024 02:42:43 GMT  
		Size: 330.5 MB (330517596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a366305765257826ca29f8b87478dcbc7adca9e831b208df34d5accabfab1`  
		Last Modified: Tue, 12 Nov 2024 02:42:39 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6874a533e293b2af390392c2d4a3e63015450278af64e0c9fb116ea7c6441e45`  
		Last Modified: Tue, 12 Nov 2024 02:42:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3527b1f1daff1973e0291fc2162777204ce64f9135bfe808bf1ef1cf2dc9f63`  
		Last Modified: Tue, 12 Nov 2024 02:42:40 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32572b53df32ed0430ce959fbe4e639ae9030aaff9015ab9597d0d78b8acd14`  
		Last Modified: Tue, 12 Nov 2024 02:42:40 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:92b2a3c524966d9bf05d76736e0a5fa0dc2c84d439935e7b02c5d84ea6e8b2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38882492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3fcf1cfbba48e1436e9b7a077ea18c3b7f0e3b5d3c3466eaeaad17200230c3`

```dockerfile
```

-	Layers:
	-	`sha256:db7bb6e5bef047bf67af9980f4bc6b01e6bbbeca91af170f93309cefb4ed0a40`  
		Last Modified: Tue, 12 Nov 2024 02:42:39 GMT  
		Size: 38.9 MB (38855774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c77b881347c98635452df385ba644c78aa19d0a356945b257c366d412efac0`  
		Last Modified: Tue, 12 Nov 2024 02:42:38 GMT  
		Size: 26.7 KB (26718 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b4018c3ea352bdfd013a5104bfc5175f4a004392f13fd3042d29aa457782e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.1 MB (580147486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e167eb52f9562249f3403b475d003adcbfc602767b01a3e893d1501d0bba4564`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 08 Nov 2024 10:31:04 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 08 Nov 2024 10:31:04 GMT
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f325f67dcdea3c7c37d04ebf758af75d8fa377127a1eeb9a2b57eb47236d01ae`  
		Last Modified: Tue, 12 Nov 2024 18:43:18 GMT  
		Size: 216.9 MB (216917318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4e5699e1771e02ef2e693da3d1e2a33ff6e4ff5329844bdc54423747c3f240`  
		Last Modified: Tue, 12 Nov 2024 18:43:14 GMT  
		Size: 2.5 MB (2504033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9a4b3774a0a797ab1832abe48ab92a1b5abcbd65b2e530136089977093f5f7`  
		Last Modified: Tue, 12 Nov 2024 18:43:14 GMT  
		Size: 469.1 KB (469064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6a855747d37eb46bf5176a2b3b14db5b8af6500cce23957b8c609318335f7d`  
		Last Modified: Tue, 12 Nov 2024 18:43:21 GMT  
		Size: 330.2 MB (330163040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968fbdfa14598642fcd51410eae70c421be54e2fe2568016b62ffc4861bc9831`  
		Last Modified: Tue, 12 Nov 2024 18:43:15 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a77e451d13e82def1864449890cf0e34f5c26cd20a70a9ff17b4e3051e87a6`  
		Last Modified: Tue, 12 Nov 2024 18:43:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f39848f0511a876a36fc793011fe40bc001556d1db74190f3390a071cf6d69c`  
		Last Modified: Tue, 12 Nov 2024 18:43:16 GMT  
		Size: 591.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74d24957eac22c275802bda57ed92b04e8c05aae591a43be3a59b557b44461a`  
		Last Modified: Tue, 12 Nov 2024 18:43:16 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9a713ee735a9290e8a392fc474d53910afd0278ba889eb8384a0535ba4f57cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38889116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db6138856bde75084976e4d50accc8e325e03aa3e47e21d852b5e1bfd056f97`

```dockerfile
```

-	Layers:
	-	`sha256:c14fdbef5ac3a6edd522944d3b6314174972da230a4f5493e428ee91a7947837`  
		Last Modified: Tue, 12 Nov 2024 18:43:15 GMT  
		Size: 38.9 MB (38862246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162fa4d9af9e544aeab90ec92af92aba666cfe19e596fa57742f94a386cb3c97`  
		Last Modified: Tue, 12 Nov 2024 18:43:13 GMT  
		Size: 26.9 KB (26870 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241118`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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

## `odoo:17.0-20241118`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:18`

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

### `odoo:18` - linux; amd64

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

### `odoo:18` - unknown; unknown

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

### `odoo:18` - linux; arm64 variant v8

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

### `odoo:18` - unknown; unknown

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

### `odoo:18` - linux; ppc64le

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

### `odoo:18` - unknown; unknown

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

## `odoo:18.0`

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

### `odoo:18.0` - linux; amd64

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

### `odoo:18.0` - unknown; unknown

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

### `odoo:18.0` - linux; arm64 variant v8

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

### `odoo:18.0` - unknown; unknown

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

### `odoo:18.0` - linux; ppc64le

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

### `odoo:18.0` - unknown; unknown

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

## `odoo:18.0-20241118`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

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
