<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20251208`](#odoo170-20251208)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20251208`](#odoo180-20251208)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20251208`](#odoo190-20251208)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:2337e19cb23f35211a0032020105fdf0c5f3d6eb5ba3a8612c6d8cfc3b0204e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:761a7fa7cbaab38b58384422133152b6d6789852d858b34afb54979f2ce37239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.8 MB (607807554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de59c8bfa6351550d79d5b7f241834a243ac7fa7b02a05f3a15cec4eb4ed78f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:47:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:47:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:47:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:47:56 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:47:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
ENV ODOO_VERSION=17.0
# Mon, 08 Dec 2025 18:48:03 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:03 GMT
ARG ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
# Mon, 08 Dec 2025 18:49:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9db555dd4a0813b949c3754049af43ce4c1a80f2e03ca3b9dcc04237d3f9cd`  
		Last Modified: Mon, 08 Dec 2025 18:50:52 GMT  
		Size: 233.8 MB (233813502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934782f45fd3eaf3d24cac3bd9651f04ca84b9eada40162f1cd6397ac6d5afd4`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 2.6 MB (2597226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496ad6c59a3fa6dbc3a26f1af54f927d1482116c4cd36a10e100bf219fc895a5`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 480.3 KB (480257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e48e0e7604b6fb709127b35e259ba8daffa707fbd8dc49a5fd2d5d626ae8a87`  
		Last Modified: Mon, 08 Dec 2025 18:51:09 GMT  
		Size: 341.4 MB (341377332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470db46110b21926c24ffa4e8f9c0bce727ed46d1da712c04ae8d413ac09a1d`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965809a5394238b945b478965d31906f597c43a5cce61de1272e89c15818638`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa22831df77d9272892077acc88370f5f665ab4b366761c13c7f1e8dc1ba9e9`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93724f6c5de0fac0bb40298b87357142db5b54a0bb81c24fd992022b9266edb7`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:f49500f54ce7b544de050f28d69527cd8fef650b39821d9a3c25ad60a25852c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41868254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0642bdf6f5e6aea9e26cb0a86f09eb34fa6c6b1be1f7c2653f4767208451fc`

```dockerfile
```

-	Layers:
	-	`sha256:95d6940a52f6692d0b7f210ebbe21a90280ab2b5f2c18eb2fe59b717e4101faa`  
		Last Modified: Mon, 08 Dec 2025 20:12:30 GMT  
		Size: 41.8 MB (41841462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c0ac425f9149cb2a9b26e4b7ffa6c70f735a5c6ecc8c91453a4fdb01fafd11`  
		Last Modified: Mon, 08 Dec 2025 20:12:31 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:83df3a2c83935c28bbd7e49af55eff3b6ac303e3485168fe04583627127216f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.6 MB (602646477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bce7a94d2e2de1f6bc9bc2df611ba8d8606af009cf6593e3860441ebd721b4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:23 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:23 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:23 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:31 GMT
ENV ODOO_VERSION=17.0
# Mon, 08 Dec 2025 18:48:31 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:31 GMT
ARG ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
# Mon, 08 Dec 2025 18:49:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec20c36429e04bd0858961b3e721d4549b8252589cd52632eb34147c0678fd8`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 231.2 MB (231197980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5faeef28be076ca88ed733616d6fadd2c722be8b026d2f622ed3c0b0fc68eb8`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 2.6 MB (2592494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61066836cb52f3a2d6cea5022c6241f67b34ba4e3c73ee09e5a7f19540d75ec`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 480.2 KB (480241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df882baf1ebe109ea5146dfaf7a7959d5cfbdc1bf230c2a94050f34b87606e11`  
		Last Modified: Mon, 08 Dec 2025 18:51:36 GMT  
		Size: 341.0 MB (340989444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027df9aaf48a91328fa172fe4140cf8cc59227a8a239085fd81f1b072abf2f65`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697452e88ae5500d6be1daebf5b939f0ae8f6f28987b4efe1a9b78c934cbdbd6`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28bf199399d0a884c8487c7fbcec4293dadafdca6ee1a939fbd82b51bffc84`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea5e275f755ef2514b70d7c8e837a3b0908917d0413342c41224c910f5c55e7`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1f7dde7f1c444e54b8ec2a9844f438bd584684b27d4a1bab50b343a643ca8051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41874913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9ee47f952c2157cae11865543020811c7908e5aa9008f1d7cb4a5e61e2f5d`

```dockerfile
```

-	Layers:
	-	`sha256:e280b0ba09085678d23d9dac281eb189ceb78729d8796fb82afee9bf9d397849`  
		Last Modified: Mon, 08 Dec 2025 20:13:14 GMT  
		Size: 41.8 MB (41847969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12dcf7e124ebb22f5dea4b4dbb32bfa0454ef47c7e89a9894e5900a5d49e26c`  
		Last Modified: Mon, 08 Dec 2025 20:13:15 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:2337e19cb23f35211a0032020105fdf0c5f3d6eb5ba3a8612c6d8cfc3b0204e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:761a7fa7cbaab38b58384422133152b6d6789852d858b34afb54979f2ce37239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.8 MB (607807554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de59c8bfa6351550d79d5b7f241834a243ac7fa7b02a05f3a15cec4eb4ed78f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:47:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:47:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:47:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:47:56 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:47:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
ENV ODOO_VERSION=17.0
# Mon, 08 Dec 2025 18:48:03 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:03 GMT
ARG ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
# Mon, 08 Dec 2025 18:49:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9db555dd4a0813b949c3754049af43ce4c1a80f2e03ca3b9dcc04237d3f9cd`  
		Last Modified: Mon, 08 Dec 2025 18:50:52 GMT  
		Size: 233.8 MB (233813502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934782f45fd3eaf3d24cac3bd9651f04ca84b9eada40162f1cd6397ac6d5afd4`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 2.6 MB (2597226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496ad6c59a3fa6dbc3a26f1af54f927d1482116c4cd36a10e100bf219fc895a5`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 480.3 KB (480257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e48e0e7604b6fb709127b35e259ba8daffa707fbd8dc49a5fd2d5d626ae8a87`  
		Last Modified: Mon, 08 Dec 2025 18:51:09 GMT  
		Size: 341.4 MB (341377332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470db46110b21926c24ffa4e8f9c0bce727ed46d1da712c04ae8d413ac09a1d`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965809a5394238b945b478965d31906f597c43a5cce61de1272e89c15818638`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa22831df77d9272892077acc88370f5f665ab4b366761c13c7f1e8dc1ba9e9`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93724f6c5de0fac0bb40298b87357142db5b54a0bb81c24fd992022b9266edb7`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f49500f54ce7b544de050f28d69527cd8fef650b39821d9a3c25ad60a25852c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41868254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0642bdf6f5e6aea9e26cb0a86f09eb34fa6c6b1be1f7c2653f4767208451fc`

```dockerfile
```

-	Layers:
	-	`sha256:95d6940a52f6692d0b7f210ebbe21a90280ab2b5f2c18eb2fe59b717e4101faa`  
		Last Modified: Mon, 08 Dec 2025 20:12:30 GMT  
		Size: 41.8 MB (41841462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c0ac425f9149cb2a9b26e4b7ffa6c70f735a5c6ecc8c91453a4fdb01fafd11`  
		Last Modified: Mon, 08 Dec 2025 20:12:31 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:83df3a2c83935c28bbd7e49af55eff3b6ac303e3485168fe04583627127216f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.6 MB (602646477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bce7a94d2e2de1f6bc9bc2df611ba8d8606af009cf6593e3860441ebd721b4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:23 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:23 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:23 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:31 GMT
ENV ODOO_VERSION=17.0
# Mon, 08 Dec 2025 18:48:31 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:31 GMT
ARG ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
# Mon, 08 Dec 2025 18:49:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec20c36429e04bd0858961b3e721d4549b8252589cd52632eb34147c0678fd8`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 231.2 MB (231197980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5faeef28be076ca88ed733616d6fadd2c722be8b026d2f622ed3c0b0fc68eb8`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 2.6 MB (2592494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61066836cb52f3a2d6cea5022c6241f67b34ba4e3c73ee09e5a7f19540d75ec`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 480.2 KB (480241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df882baf1ebe109ea5146dfaf7a7959d5cfbdc1bf230c2a94050f34b87606e11`  
		Last Modified: Mon, 08 Dec 2025 18:51:36 GMT  
		Size: 341.0 MB (340989444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027df9aaf48a91328fa172fe4140cf8cc59227a8a239085fd81f1b072abf2f65`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697452e88ae5500d6be1daebf5b939f0ae8f6f28987b4efe1a9b78c934cbdbd6`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28bf199399d0a884c8487c7fbcec4293dadafdca6ee1a939fbd82b51bffc84`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea5e275f755ef2514b70d7c8e837a3b0908917d0413342c41224c910f5c55e7`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1f7dde7f1c444e54b8ec2a9844f438bd584684b27d4a1bab50b343a643ca8051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41874913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9ee47f952c2157cae11865543020811c7908e5aa9008f1d7cb4a5e61e2f5d`

```dockerfile
```

-	Layers:
	-	`sha256:e280b0ba09085678d23d9dac281eb189ceb78729d8796fb82afee9bf9d397849`  
		Last Modified: Mon, 08 Dec 2025 20:13:14 GMT  
		Size: 41.8 MB (41847969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12dcf7e124ebb22f5dea4b4dbb32bfa0454ef47c7e89a9894e5900a5d49e26c`  
		Last Modified: Mon, 08 Dec 2025 20:13:15 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20251208`

```console
$ docker pull odoo@sha256:2337e19cb23f35211a0032020105fdf0c5f3d6eb5ba3a8612c6d8cfc3b0204e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20251208` - linux; amd64

```console
$ docker pull odoo@sha256:761a7fa7cbaab38b58384422133152b6d6789852d858b34afb54979f2ce37239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.8 MB (607807554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de59c8bfa6351550d79d5b7f241834a243ac7fa7b02a05f3a15cec4eb4ed78f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:47:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:47:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:47:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:47:56 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:47:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:03 GMT
ENV ODOO_VERSION=17.0
# Mon, 08 Dec 2025 18:48:03 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:03 GMT
ARG ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
# Mon, 08 Dec 2025 18:49:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:03 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9db555dd4a0813b949c3754049af43ce4c1a80f2e03ca3b9dcc04237d3f9cd`  
		Last Modified: Mon, 08 Dec 2025 18:50:52 GMT  
		Size: 233.8 MB (233813502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934782f45fd3eaf3d24cac3bd9651f04ca84b9eada40162f1cd6397ac6d5afd4`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 2.6 MB (2597226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496ad6c59a3fa6dbc3a26f1af54f927d1482116c4cd36a10e100bf219fc895a5`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 480.3 KB (480257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e48e0e7604b6fb709127b35e259ba8daffa707fbd8dc49a5fd2d5d626ae8a87`  
		Last Modified: Mon, 08 Dec 2025 18:51:09 GMT  
		Size: 341.4 MB (341377332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9470db46110b21926c24ffa4e8f9c0bce727ed46d1da712c04ae8d413ac09a1d`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965809a5394238b945b478965d31906f597c43a5cce61de1272e89c15818638`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa22831df77d9272892077acc88370f5f665ab4b366761c13c7f1e8dc1ba9e9`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93724f6c5de0fac0bb40298b87357142db5b54a0bb81c24fd992022b9266edb7`  
		Last Modified: Mon, 08 Dec 2025 18:50:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:f49500f54ce7b544de050f28d69527cd8fef650b39821d9a3c25ad60a25852c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41868254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0642bdf6f5e6aea9e26cb0a86f09eb34fa6c6b1be1f7c2653f4767208451fc`

```dockerfile
```

-	Layers:
	-	`sha256:95d6940a52f6692d0b7f210ebbe21a90280ab2b5f2c18eb2fe59b717e4101faa`  
		Last Modified: Mon, 08 Dec 2025 20:12:30 GMT  
		Size: 41.8 MB (41841462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c0ac425f9149cb2a9b26e4b7ffa6c70f735a5c6ecc8c91453a4fdb01fafd11`  
		Last Modified: Mon, 08 Dec 2025 20:12:31 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20251208` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:83df3a2c83935c28bbd7e49af55eff3b6ac303e3485168fe04583627127216f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.6 MB (602646477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bce7a94d2e2de1f6bc9bc2df611ba8d8606af009cf6593e3860441ebd721b4c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:23 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:23 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:23 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:23 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:23 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:31 GMT
ENV ODOO_VERSION=17.0
# Mon, 08 Dec 2025 18:48:31 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:31 GMT
ARG ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
# Mon, 08 Dec 2025 18:49:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=e85e44d173e4e2f56057c0d4f88fab18b80963ff
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:39 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec20c36429e04bd0858961b3e721d4549b8252589cd52632eb34147c0678fd8`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 231.2 MB (231197980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5faeef28be076ca88ed733616d6fadd2c722be8b026d2f622ed3c0b0fc68eb8`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 2.6 MB (2592494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61066836cb52f3a2d6cea5022c6241f67b34ba4e3c73ee09e5a7f19540d75ec`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 480.2 KB (480241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df882baf1ebe109ea5146dfaf7a7959d5cfbdc1bf230c2a94050f34b87606e11`  
		Last Modified: Mon, 08 Dec 2025 18:51:36 GMT  
		Size: 341.0 MB (340989444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027df9aaf48a91328fa172fe4140cf8cc59227a8a239085fd81f1b072abf2f65`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697452e88ae5500d6be1daebf5b939f0ae8f6f28987b4efe1a9b78c934cbdbd6`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc28bf199399d0a884c8487c7fbcec4293dadafdca6ee1a939fbd82b51bffc84`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea5e275f755ef2514b70d7c8e837a3b0908917d0413342c41224c910f5c55e7`  
		Last Modified: Mon, 08 Dec 2025 18:51:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:1f7dde7f1c444e54b8ec2a9844f438bd584684b27d4a1bab50b343a643ca8051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41874913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e9ee47f952c2157cae11865543020811c7908e5aa9008f1d7cb4a5e61e2f5d`

```dockerfile
```

-	Layers:
	-	`sha256:e280b0ba09085678d23d9dac281eb189ceb78729d8796fb82afee9bf9d397849`  
		Last Modified: Mon, 08 Dec 2025 20:13:14 GMT  
		Size: 41.8 MB (41847969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12dcf7e124ebb22f5dea4b4dbb32bfa0454ef47c7e89a9894e5900a5d49e26c`  
		Last Modified: Mon, 08 Dec 2025 20:13:15 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:9e270038249ef07a2b5a1e6dfe759e0164cd742d9004b980ee52c83b1c74bffe
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
$ docker pull odoo@sha256:627d056734f6905b9b0a5683a9f0d43870290cdf1ba7d1f2a743b36b68a7e2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 MB (679932152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935987581b2030af9f0ec7bd423162b25ef2264d86847e8ea17370069adb354b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:38 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:38 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:48:38 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:46 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:47 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:47 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:47 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:47 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:49:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:49 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:49 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975c49f68c8d3c1ba5d457a7b0b5de084ab24abe922d0f5a2abc10f7443b70b`  
		Last Modified: Mon, 08 Dec 2025 18:52:32 GMT  
		Size: 254.6 MB (254556714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8b0a60d8e1607eaafbf3bb0a55516c576f064dd3757606b8bae34cb66d3f58`  
		Last Modified: Mon, 08 Dec 2025 18:51:57 GMT  
		Size: 14.4 MB (14356505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a96859878bc01728ca28183771d473929e0fd87461d445337d9646d07bc6b45`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 480.0 KB (480002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53a35b9d20019a89daf3e4a75eecf940a6100bc77b1ecb1852f6a8f69bdf22`  
		Last Modified: Mon, 08 Dec 2025 18:52:15 GMT  
		Size: 380.8 MB (380811800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef19be01cef693e5ea79d4c0b1cd60cfa279913794b2d1fa862861dc086ed393`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f235f71504bf3ed5e010791757a0b649527393e85579a1d68d8ef259c3d7976`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787ffc84f405eed35225ca46200db05700bef99338e7f7a2265367af6979b91c`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2440a96503c8aebf70fbb95ac691c16bd2b883148db63b59b0cb24080333e9f`  
		Last Modified: Mon, 08 Dec 2025 18:52:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:768bf8ededb96ab6c7f62dc2be34cc75ae74c3d493b3c26f026f201f2cea5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61460811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf690cd5dea9eb050d49196770e733edad2d75cc33072b218d1e0c3fae2175dd`

```dockerfile
```

-	Layers:
	-	`sha256:f4c32deb6f9ff52b746479470f47d639946cff8b3691fcef4db61528342646e1`  
		Last Modified: Mon, 08 Dec 2025 20:12:48 GMT  
		Size: 61.4 MB (61434012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ba59c247e3510026b65507789c2c8af26dbeb45e01753143a761dbbc5b00dc`  
		Last Modified: Mon, 08 Dec 2025 20:12:50 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:68d34e9e063d429695e0e9a12c68e48008540f5bf901e5ee0a9b4159b207c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.3 MB (676292320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b82f84fc8db060b89e45f48b9106383d09013da58b3bb94e6c116405547d2d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:40 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:40 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:53 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:54 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:54 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:54 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:49:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:56 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:56 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5793802a2f9cadae9ddc58c80a935ce14a79492e0fc5a1983b88da3488225555`  
		Last Modified: Mon, 08 Dec 2025 18:53:37 GMT  
		Size: 252.0 MB (251954850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76e621e5080664edf955f277e37901f09d45a3b742e158e4ad122720d64da80`  
		Last Modified: Mon, 08 Dec 2025 18:52:43 GMT  
		Size: 14.3 MB (14334184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b5094c4876eea4fad1de50b0092a02d59db41ee551a8646075e4bd4ca194fe`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 480.1 KB (480069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cb890722779cda290c1b83ea4f75e56b563c7fa6ccf96ab5012785b06aab9f`  
		Last Modified: Mon, 08 Dec 2025 18:53:33 GMT  
		Size: 380.7 MB (380658820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c797af32de438ee90080489968ff2ccb69763213d31e7a44d71db6a1d03751`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd41858875a7cfae40208e5b1546265f98b053fabd5d7cd76024328bb8845d5`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25388f7ebb5f47d8f93ed1d30fd763f4a151de0fae0ff4b40e8cc0fcd277b31`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1c6cae64679e4bf73737340ad8715a11ba92f546b1d4cb2a488611952acd40`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7e6d8bd40f97242ebc699c677f00ef68cb6f02cecad8ccfe2679aa93b0580550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7764f58c0e03b7353ea5fb599c2710d9de61d7c418e4ad0fcae9ddd55b1b234f`

```dockerfile
```

-	Layers:
	-	`sha256:58b84c945e0aad6de3070a16fae675c225d8842127880651a5dd1030df8f3e26`  
		Last Modified: Mon, 08 Dec 2025 20:14:40 GMT  
		Size: 61.4 MB (61441287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e89c02114115949513ea18b238abba98fb70937932050cb16f850e41d039fe3`  
		Last Modified: Mon, 08 Dec 2025 20:14:42 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:63976b1a9b285c492cc38a6866b68b022ee86bcaa89a69942fef24c437727eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.1 MB (696107922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eafb90e25ad5f329774e700b82bf88a0485b1e103598d68330547ab67e313f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:51:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:51:37 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:51:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:51:38 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:51:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:51:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:51:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:51:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:51:39 GMT
USER odoo
# Mon, 08 Dec 2025 18:51:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:51:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759bd05064754db3d644003f10baa21d1bf0d3ff73ef16db49cb922245aaffea`  
		Last Modified: Mon, 08 Dec 2025 18:58:09 GMT  
		Size: 14.9 MB (14884994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115c6456a504ea6ce32b703d0eb1c0cdfe08cceb9eeeb786829c7c152d62cd`  
		Last Modified: Mon, 08 Dec 2025 18:58:13 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac1e310a930c7625eeb0387a057b9a889221735c9a8d0cd75a74b2ab8c35ef5`  
		Last Modified: Mon, 08 Dec 2025 18:59:32 GMT  
		Size: 381.4 MB (381358137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b9a892eb8e211887284cd006aec876fc2f1b9b49609067e8ad493c88c9cca9`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce0c7d51a0056a8e4f0fb66fcf212cf5f493b428b7fc9112c88eb71be628267`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8673ec82c797a20802f9e2009c8344bebf4624667e56f1c74ac320d8ca83d975`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600a1047fe14e8f74e59e92e340a6b707daac8ad621e0b3e8c39432436d0fa4`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:5886737a38757ee341cc8838ab66d9d3acdefc3d9f4a66547861d10d12bb5292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61469250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5667b2d79f7648939433570a5aea2148a970476a88fd655876e278d7b361a6`

```dockerfile
```

-	Layers:
	-	`sha256:c2e95f8f0ef315a7247d18e0e22ca4b5da146a76cb1ce769d3cb1f82db4ed4db`  
		Last Modified: Mon, 08 Dec 2025 20:16:27 GMT  
		Size: 61.4 MB (61442395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1cba30e71dc6196e38960b4ce985e5ca5d82885fcddabba06dc89dbe03c5bd9`  
		Last Modified: Mon, 08 Dec 2025 20:16:29 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:9e270038249ef07a2b5a1e6dfe759e0164cd742d9004b980ee52c83b1c74bffe
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
$ docker pull odoo@sha256:627d056734f6905b9b0a5683a9f0d43870290cdf1ba7d1f2a743b36b68a7e2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 MB (679932152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935987581b2030af9f0ec7bd423162b25ef2264d86847e8ea17370069adb354b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:38 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:38 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:48:38 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:46 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:47 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:47 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:47 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:47 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:49:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:49 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:49 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975c49f68c8d3c1ba5d457a7b0b5de084ab24abe922d0f5a2abc10f7443b70b`  
		Last Modified: Mon, 08 Dec 2025 18:52:32 GMT  
		Size: 254.6 MB (254556714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8b0a60d8e1607eaafbf3bb0a55516c576f064dd3757606b8bae34cb66d3f58`  
		Last Modified: Mon, 08 Dec 2025 18:51:57 GMT  
		Size: 14.4 MB (14356505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a96859878bc01728ca28183771d473929e0fd87461d445337d9646d07bc6b45`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 480.0 KB (480002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53a35b9d20019a89daf3e4a75eecf940a6100bc77b1ecb1852f6a8f69bdf22`  
		Last Modified: Mon, 08 Dec 2025 18:52:15 GMT  
		Size: 380.8 MB (380811800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef19be01cef693e5ea79d4c0b1cd60cfa279913794b2d1fa862861dc086ed393`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f235f71504bf3ed5e010791757a0b649527393e85579a1d68d8ef259c3d7976`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787ffc84f405eed35225ca46200db05700bef99338e7f7a2265367af6979b91c`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2440a96503c8aebf70fbb95ac691c16bd2b883148db63b59b0cb24080333e9f`  
		Last Modified: Mon, 08 Dec 2025 18:52:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:768bf8ededb96ab6c7f62dc2be34cc75ae74c3d493b3c26f026f201f2cea5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61460811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf690cd5dea9eb050d49196770e733edad2d75cc33072b218d1e0c3fae2175dd`

```dockerfile
```

-	Layers:
	-	`sha256:f4c32deb6f9ff52b746479470f47d639946cff8b3691fcef4db61528342646e1`  
		Last Modified: Mon, 08 Dec 2025 20:12:48 GMT  
		Size: 61.4 MB (61434012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ba59c247e3510026b65507789c2c8af26dbeb45e01753143a761dbbc5b00dc`  
		Last Modified: Mon, 08 Dec 2025 20:12:50 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:68d34e9e063d429695e0e9a12c68e48008540f5bf901e5ee0a9b4159b207c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.3 MB (676292320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b82f84fc8db060b89e45f48b9106383d09013da58b3bb94e6c116405547d2d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:40 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:40 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:53 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:54 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:54 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:54 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:49:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:56 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:56 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5793802a2f9cadae9ddc58c80a935ce14a79492e0fc5a1983b88da3488225555`  
		Last Modified: Mon, 08 Dec 2025 18:53:37 GMT  
		Size: 252.0 MB (251954850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76e621e5080664edf955f277e37901f09d45a3b742e158e4ad122720d64da80`  
		Last Modified: Mon, 08 Dec 2025 18:52:43 GMT  
		Size: 14.3 MB (14334184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b5094c4876eea4fad1de50b0092a02d59db41ee551a8646075e4bd4ca194fe`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 480.1 KB (480069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cb890722779cda290c1b83ea4f75e56b563c7fa6ccf96ab5012785b06aab9f`  
		Last Modified: Mon, 08 Dec 2025 18:53:33 GMT  
		Size: 380.7 MB (380658820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c797af32de438ee90080489968ff2ccb69763213d31e7a44d71db6a1d03751`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd41858875a7cfae40208e5b1546265f98b053fabd5d7cd76024328bb8845d5`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25388f7ebb5f47d8f93ed1d30fd763f4a151de0fae0ff4b40e8cc0fcd277b31`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1c6cae64679e4bf73737340ad8715a11ba92f546b1d4cb2a488611952acd40`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7e6d8bd40f97242ebc699c677f00ef68cb6f02cecad8ccfe2679aa93b0580550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7764f58c0e03b7353ea5fb599c2710d9de61d7c418e4ad0fcae9ddd55b1b234f`

```dockerfile
```

-	Layers:
	-	`sha256:58b84c945e0aad6de3070a16fae675c225d8842127880651a5dd1030df8f3e26`  
		Last Modified: Mon, 08 Dec 2025 20:14:40 GMT  
		Size: 61.4 MB (61441287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e89c02114115949513ea18b238abba98fb70937932050cb16f850e41d039fe3`  
		Last Modified: Mon, 08 Dec 2025 20:14:42 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:63976b1a9b285c492cc38a6866b68b022ee86bcaa89a69942fef24c437727eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.1 MB (696107922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eafb90e25ad5f329774e700b82bf88a0485b1e103598d68330547ab67e313f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:51:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:51:37 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:51:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:51:38 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:51:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:51:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:51:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:51:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:51:39 GMT
USER odoo
# Mon, 08 Dec 2025 18:51:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:51:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759bd05064754db3d644003f10baa21d1bf0d3ff73ef16db49cb922245aaffea`  
		Last Modified: Mon, 08 Dec 2025 18:58:09 GMT  
		Size: 14.9 MB (14884994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115c6456a504ea6ce32b703d0eb1c0cdfe08cceb9eeeb786829c7c152d62cd`  
		Last Modified: Mon, 08 Dec 2025 18:58:13 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac1e310a930c7625eeb0387a057b9a889221735c9a8d0cd75a74b2ab8c35ef5`  
		Last Modified: Mon, 08 Dec 2025 18:59:32 GMT  
		Size: 381.4 MB (381358137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b9a892eb8e211887284cd006aec876fc2f1b9b49609067e8ad493c88c9cca9`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce0c7d51a0056a8e4f0fb66fcf212cf5f493b428b7fc9112c88eb71be628267`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8673ec82c797a20802f9e2009c8344bebf4624667e56f1c74ac320d8ca83d975`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600a1047fe14e8f74e59e92e340a6b707daac8ad621e0b3e8c39432436d0fa4`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5886737a38757ee341cc8838ab66d9d3acdefc3d9f4a66547861d10d12bb5292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61469250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5667b2d79f7648939433570a5aea2148a970476a88fd655876e278d7b361a6`

```dockerfile
```

-	Layers:
	-	`sha256:c2e95f8f0ef315a7247d18e0e22ca4b5da146a76cb1ce769d3cb1f82db4ed4db`  
		Last Modified: Mon, 08 Dec 2025 20:16:27 GMT  
		Size: 61.4 MB (61442395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1cba30e71dc6196e38960b4ce985e5ca5d82885fcddabba06dc89dbe03c5bd9`  
		Last Modified: Mon, 08 Dec 2025 20:16:29 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251208`

```console
$ docker pull odoo@sha256:9e270038249ef07a2b5a1e6dfe759e0164cd742d9004b980ee52c83b1c74bffe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20251208` - linux; amd64

```console
$ docker pull odoo@sha256:627d056734f6905b9b0a5683a9f0d43870290cdf1ba7d1f2a743b36b68a7e2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 MB (679932152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935987581b2030af9f0ec7bd423162b25ef2264d86847e8ea17370069adb354b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:38 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:38 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:48:38 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:46 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:47 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:47 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:47 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:47 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:49:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:49 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:49 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:49 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975c49f68c8d3c1ba5d457a7b0b5de084ab24abe922d0f5a2abc10f7443b70b`  
		Last Modified: Mon, 08 Dec 2025 18:52:32 GMT  
		Size: 254.6 MB (254556714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8b0a60d8e1607eaafbf3bb0a55516c576f064dd3757606b8bae34cb66d3f58`  
		Last Modified: Mon, 08 Dec 2025 18:51:57 GMT  
		Size: 14.4 MB (14356505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a96859878bc01728ca28183771d473929e0fd87461d445337d9646d07bc6b45`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 480.0 KB (480002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53a35b9d20019a89daf3e4a75eecf940a6100bc77b1ecb1852f6a8f69bdf22`  
		Last Modified: Mon, 08 Dec 2025 18:52:15 GMT  
		Size: 380.8 MB (380811800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef19be01cef693e5ea79d4c0b1cd60cfa279913794b2d1fa862861dc086ed393`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f235f71504bf3ed5e010791757a0b649527393e85579a1d68d8ef259c3d7976`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787ffc84f405eed35225ca46200db05700bef99338e7f7a2265367af6979b91c`  
		Last Modified: Mon, 08 Dec 2025 18:51:56 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2440a96503c8aebf70fbb95ac691c16bd2b883148db63b59b0cb24080333e9f`  
		Last Modified: Mon, 08 Dec 2025 18:52:01 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:768bf8ededb96ab6c7f62dc2be34cc75ae74c3d493b3c26f026f201f2cea5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61460811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf690cd5dea9eb050d49196770e733edad2d75cc33072b218d1e0c3fae2175dd`

```dockerfile
```

-	Layers:
	-	`sha256:f4c32deb6f9ff52b746479470f47d639946cff8b3691fcef4db61528342646e1`  
		Last Modified: Mon, 08 Dec 2025 20:12:48 GMT  
		Size: 61.4 MB (61434012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ba59c247e3510026b65507789c2c8af26dbeb45e01753143a761dbbc5b00dc`  
		Last Modified: Mon, 08 Dec 2025 20:12:50 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251208` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:68d34e9e063d429695e0e9a12c68e48008540f5bf901e5ee0a9b4159b207c893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.3 MB (676292320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b82f84fc8db060b89e45f48b9106383d09013da58b3bb94e6c116405547d2d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:40 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:40 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:40 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:53 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:54 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:54 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:54 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:54 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:49:56 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:56 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:56 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:57 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:57 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:57 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5793802a2f9cadae9ddc58c80a935ce14a79492e0fc5a1983b88da3488225555`  
		Last Modified: Mon, 08 Dec 2025 18:53:37 GMT  
		Size: 252.0 MB (251954850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76e621e5080664edf955f277e37901f09d45a3b742e158e4ad122720d64da80`  
		Last Modified: Mon, 08 Dec 2025 18:52:43 GMT  
		Size: 14.3 MB (14334184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b5094c4876eea4fad1de50b0092a02d59db41ee551a8646075e4bd4ca194fe`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 480.1 KB (480069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cb890722779cda290c1b83ea4f75e56b563c7fa6ccf96ab5012785b06aab9f`  
		Last Modified: Mon, 08 Dec 2025 18:53:33 GMT  
		Size: 380.7 MB (380658820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c797af32de438ee90080489968ff2ccb69763213d31e7a44d71db6a1d03751`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd41858875a7cfae40208e5b1546265f98b053fabd5d7cd76024328bb8845d5`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25388f7ebb5f47d8f93ed1d30fd763f4a151de0fae0ff4b40e8cc0fcd277b31`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1c6cae64679e4bf73737340ad8715a11ba92f546b1d4cb2a488611952acd40`  
		Last Modified: Mon, 08 Dec 2025 18:52:41 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:7e6d8bd40f97242ebc699c677f00ef68cb6f02cecad8ccfe2679aa93b0580550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61468237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7764f58c0e03b7353ea5fb599c2710d9de61d7c418e4ad0fcae9ddd55b1b234f`

```dockerfile
```

-	Layers:
	-	`sha256:58b84c945e0aad6de3070a16fae675c225d8842127880651a5dd1030df8f3e26`  
		Last Modified: Mon, 08 Dec 2025 20:14:40 GMT  
		Size: 61.4 MB (61441287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e89c02114115949513ea18b238abba98fb70937932050cb16f850e41d039fe3`  
		Last Modified: Mon, 08 Dec 2025 20:14:42 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251208` - linux; ppc64le

```console
$ docker pull odoo@sha256:63976b1a9b285c492cc38a6866b68b022ee86bcaa89a69942fef24c437727eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.1 MB (696107922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eafb90e25ad5f329774e700b82bf88a0485b1e103598d68330547ab67e313f6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
ENV ODOO_VERSION=18.0
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
# Mon, 08 Dec 2025 18:51:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:51:37 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:51:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:51:38 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=617b8e935dec581d018a7c32bc6e0b759b904031
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:51:38 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:51:38 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:51:38 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:51:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:51:39 GMT
USER odoo
# Mon, 08 Dec 2025 18:51:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:51:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759bd05064754db3d644003f10baa21d1bf0d3ff73ef16db49cb922245aaffea`  
		Last Modified: Mon, 08 Dec 2025 18:58:09 GMT  
		Size: 14.9 MB (14884994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115c6456a504ea6ce32b703d0eb1c0cdfe08cceb9eeeb786829c7c152d62cd`  
		Last Modified: Mon, 08 Dec 2025 18:58:13 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac1e310a930c7625eeb0387a057b9a889221735c9a8d0cd75a74b2ab8c35ef5`  
		Last Modified: Mon, 08 Dec 2025 18:59:32 GMT  
		Size: 381.4 MB (381358137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b9a892eb8e211887284cd006aec876fc2f1b9b49609067e8ad493c88c9cca9`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce0c7d51a0056a8e4f0fb66fcf212cf5f493b428b7fc9112c88eb71be628267`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8673ec82c797a20802f9e2009c8344bebf4624667e56f1c74ac320d8ca83d975`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9600a1047fe14e8f74e59e92e340a6b707daac8ad621e0b3e8c39432436d0fa4`  
		Last Modified: Mon, 08 Dec 2025 18:58:06 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:5886737a38757ee341cc8838ab66d9d3acdefc3d9f4a66547861d10d12bb5292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61469250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5667b2d79f7648939433570a5aea2148a970476a88fd655876e278d7b361a6`

```dockerfile
```

-	Layers:
	-	`sha256:c2e95f8f0ef315a7247d18e0e22ca4b5da146a76cb1ce769d3cb1f82db4ed4db`  
		Last Modified: Mon, 08 Dec 2025 20:16:27 GMT  
		Size: 61.4 MB (61442395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1cba30e71dc6196e38960b4ce985e5ca5d82885fcddabba06dc89dbe03c5bd9`  
		Last Modified: Mon, 08 Dec 2025 20:16:29 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:4d344f40154dd0627b7078c3dcb40cf1db7c0944473c1898eb63492659b398ef
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
$ docker pull odoo@sha256:1a94f42236f77c4d03f448cb628998191c4ba3cbba66111cea2e094054ece873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.5 MB (690460915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e480ed7f7126db940133216710f1da02dfdea990cdfa40b3d20fef966a0c0af2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:15 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:15 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:15 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:15 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:48:15 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:25 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:49:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519f7aea1d4b927b7d6f38dc45c9c9033383653d88d0c55a6211ed18ed5e799`  
		Last Modified: Mon, 08 Dec 2025 18:52:32 GMT  
		Size: 254.6 MB (254556917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290a44abafc51bfc0445a3f3c6352ba512dfd96967797e465b39714d574e719`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 14.4 MB (14356488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0182b47140b900aee9388fbeff64532cc5ad404ab547a4b5c1602fbadbc79180`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a0787a6c7bb3bc9617976f5ed96a1a37fa9c432f376f515852609a31eb71bf`  
		Last Modified: Mon, 08 Dec 2025 18:53:00 GMT  
		Size: 391.3 MB (391340363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c937d3e00b3fdf79e7cccb7e922652b2ff51a98b1fc40ad3f83b0fc7931d23`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c398c0ddd5855f5ad6abff23451d043cdd45fe16f1c23fce259bfa5883ed273`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8009cf5ac077a457ed8c62e759c0e01139f3901afcd797924656b9896c8d353`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f36fb0164f52590dc4def278b697d10021b78ad1a483059e37dcf9deb34c53`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:3914ae30eb5d0c6f48ec933e3b4b96831d9c086efeb2e68cd759339cb9b21001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68830733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dfad5a6b12d95501efdd1cbdca00d3e96254b56b42b1d424dd35dc94e0496b`

```dockerfile
```

-	Layers:
	-	`sha256:8c5e680858cd1066e2a2927c48908ddfbcd2f8c5e23a85215cae3293f18d6072`  
		Last Modified: Mon, 08 Dec 2025 20:13:13 GMT  
		Size: 68.8 MB (68803640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e95b241ab0f22f3709186452dce32f2e1cf3f4db19144ee5f77cf660652dfa`  
		Last Modified: Mon, 08 Dec 2025 20:13:15 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:61dcbdedbc4acdfd614299a747a61b735de7f0763aef184538130488a78f1d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.8 MB (686834724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ae7143f5ed3f1b4ec3ff9e3b1ccc89d3361c4c7216b32a6774f3c921bcb92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:39 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:39 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:50:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:50:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:50:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:50:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
USER odoo
# Mon, 08 Dec 2025 18:50:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:50:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b7f9d7ee89d6736b9b5217119ed2546a0907348808d23407462a3663a2fc8b`  
		Last Modified: Mon, 08 Dec 2025 19:11:05 GMT  
		Size: 252.0 MB (251954320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b82dc4a1f8c23f604a009d7e720b926cc442d3de57da248d84ad2d7ba682ab6`  
		Last Modified: Mon, 08 Dec 2025 19:09:54 GMT  
		Size: 14.3 MB (14334128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d828f926ff16e5463882f70799f58b1947edc638e54cca47feb8ed80754747e`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce1812d64c95ba8e8b5d0bbca1f9da1303e2d0d12614edf8ce8a4ebbe51dee`  
		Last Modified: Mon, 08 Dec 2025 19:11:15 GMT  
		Size: 391.2 MB (391201872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a745c4069c2c2246d1b01d57a053bbbe14c9a19be58c0216fa932132f2698cf1`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a5c5a6cacab3baf2a5cf93d6c8e9650633e64d6ea63f02fb5da3a9b056c5c7`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55131d32740b2aaaf9e5bf9c87517a475d247f3d3bdec6e5c63eb44a55c5003`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e880cef190df70afb9f10bde4d083ae903af435aa7547cea2c21690f79627c`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:2af3cd4a4c467165894497d308beba6f8ea3c53527d4c9ee1849aa08181346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68838182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ee987809a274365d22d1d3af899d4824d142e2284cf05831f1bbcf5285530`

```dockerfile
```

-	Layers:
	-	`sha256:38ee64f59bef97b5b05459fdbdee397c4a24f323c0329d87c0619b7222fc0d7a`  
		Last Modified: Mon, 08 Dec 2025 20:14:56 GMT  
		Size: 68.8 MB (68810927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056dd5c9705bb4013cfcc5244e1f1b3af0035f3d3b91c09919c3112e67048887`  
		Last Modified: Mon, 08 Dec 2025 20:14:58 GMT  
		Size: 27.3 KB (27255 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:5c4b256a4590d2f6f27554ae7bfae52d11c871af7b20b6abd8245584df66fa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706624814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dc3e40700cd0b164a91029aeffc29632626d0b6a6c3a2e95bd3d126cf1cfd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:51:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:51:56 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:51:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:51:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:51:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:51:58 GMT
USER odoo
# Mon, 08 Dec 2025 18:51:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:51:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759bd05064754db3d644003f10baa21d1bf0d3ff73ef16db49cb922245aaffea`  
		Last Modified: Mon, 08 Dec 2025 18:58:09 GMT  
		Size: 14.9 MB (14884994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115c6456a504ea6ce32b703d0eb1c0cdfe08cceb9eeeb786829c7c152d62cd`  
		Last Modified: Mon, 08 Dec 2025 18:58:13 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6befe92033fab1710308b5218ee1939af1b92005a79d72537650d3006cb8644a`  
		Last Modified: Mon, 08 Dec 2025 18:58:51 GMT  
		Size: 391.9 MB (391875030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd52f20ec540671f2c6a79e60d003cf10e3ce2d52cf1ae32d65c2561c82a83`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cd746c4c2aa00f43faa506f063a68a056bdadf9edd0d45ec1d97af3ed1563`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37225865dc2b2782e3401546753031c1b483a58d1e562bbf0bb59f5d1c6acef`  
		Last Modified: Mon, 08 Dec 2025 18:58:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1d78cc94ee57a9285a9e3da1dcada1c35cbeea1c865fcdf6ea82acfbbaf91d`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:87469b197aae35c22ba8c2b52e6ac9635e608d80694a0980344357378e15c2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68839184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b82057fad447250b073fa9051b72f3f1930d9613a6874f59c37a9b3318fc44`

```dockerfile
```

-	Layers:
	-	`sha256:357850cb22d5df2c86eed24fddee5de600929329ff59e031e0551112e0915887`  
		Last Modified: Mon, 08 Dec 2025 20:16:35 GMT  
		Size: 68.8 MB (68812029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f48d1346f342ded74df06a26251d09af2122e38f1e423ad822fa2fde7a7cc8`  
		Last Modified: Mon, 08 Dec 2025 20:16:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:4d344f40154dd0627b7078c3dcb40cf1db7c0944473c1898eb63492659b398ef
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
$ docker pull odoo@sha256:1a94f42236f77c4d03f448cb628998191c4ba3cbba66111cea2e094054ece873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.5 MB (690460915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e480ed7f7126db940133216710f1da02dfdea990cdfa40b3d20fef966a0c0af2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:15 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:15 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:15 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:15 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:48:15 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:25 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:49:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519f7aea1d4b927b7d6f38dc45c9c9033383653d88d0c55a6211ed18ed5e799`  
		Last Modified: Mon, 08 Dec 2025 18:52:32 GMT  
		Size: 254.6 MB (254556917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290a44abafc51bfc0445a3f3c6352ba512dfd96967797e465b39714d574e719`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 14.4 MB (14356488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0182b47140b900aee9388fbeff64532cc5ad404ab547a4b5c1602fbadbc79180`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a0787a6c7bb3bc9617976f5ed96a1a37fa9c432f376f515852609a31eb71bf`  
		Last Modified: Mon, 08 Dec 2025 18:53:00 GMT  
		Size: 391.3 MB (391340363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c937d3e00b3fdf79e7cccb7e922652b2ff51a98b1fc40ad3f83b0fc7931d23`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c398c0ddd5855f5ad6abff23451d043cdd45fe16f1c23fce259bfa5883ed273`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8009cf5ac077a457ed8c62e759c0e01139f3901afcd797924656b9896c8d353`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f36fb0164f52590dc4def278b697d10021b78ad1a483059e37dcf9deb34c53`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3914ae30eb5d0c6f48ec933e3b4b96831d9c086efeb2e68cd759339cb9b21001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68830733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dfad5a6b12d95501efdd1cbdca00d3e96254b56b42b1d424dd35dc94e0496b`

```dockerfile
```

-	Layers:
	-	`sha256:8c5e680858cd1066e2a2927c48908ddfbcd2f8c5e23a85215cae3293f18d6072`  
		Last Modified: Mon, 08 Dec 2025 20:13:13 GMT  
		Size: 68.8 MB (68803640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e95b241ab0f22f3709186452dce32f2e1cf3f4db19144ee5f77cf660652dfa`  
		Last Modified: Mon, 08 Dec 2025 20:13:15 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:61dcbdedbc4acdfd614299a747a61b735de7f0763aef184538130488a78f1d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.8 MB (686834724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ae7143f5ed3f1b4ec3ff9e3b1ccc89d3361c4c7216b32a6774f3c921bcb92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:39 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:39 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:50:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:50:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:50:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:50:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
USER odoo
# Mon, 08 Dec 2025 18:50:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:50:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b7f9d7ee89d6736b9b5217119ed2546a0907348808d23407462a3663a2fc8b`  
		Last Modified: Mon, 08 Dec 2025 19:11:05 GMT  
		Size: 252.0 MB (251954320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b82dc4a1f8c23f604a009d7e720b926cc442d3de57da248d84ad2d7ba682ab6`  
		Last Modified: Mon, 08 Dec 2025 19:09:54 GMT  
		Size: 14.3 MB (14334128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d828f926ff16e5463882f70799f58b1947edc638e54cca47feb8ed80754747e`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce1812d64c95ba8e8b5d0bbca1f9da1303e2d0d12614edf8ce8a4ebbe51dee`  
		Last Modified: Mon, 08 Dec 2025 19:11:15 GMT  
		Size: 391.2 MB (391201872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a745c4069c2c2246d1b01d57a053bbbe14c9a19be58c0216fa932132f2698cf1`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a5c5a6cacab3baf2a5cf93d6c8e9650633e64d6ea63f02fb5da3a9b056c5c7`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55131d32740b2aaaf9e5bf9c87517a475d247f3d3bdec6e5c63eb44a55c5003`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e880cef190df70afb9f10bde4d083ae903af435aa7547cea2c21690f79627c`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2af3cd4a4c467165894497d308beba6f8ea3c53527d4c9ee1849aa08181346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68838182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ee987809a274365d22d1d3af899d4824d142e2284cf05831f1bbcf5285530`

```dockerfile
```

-	Layers:
	-	`sha256:38ee64f59bef97b5b05459fdbdee397c4a24f323c0329d87c0619b7222fc0d7a`  
		Last Modified: Mon, 08 Dec 2025 20:14:56 GMT  
		Size: 68.8 MB (68810927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056dd5c9705bb4013cfcc5244e1f1b3af0035f3d3b91c09919c3112e67048887`  
		Last Modified: Mon, 08 Dec 2025 20:14:58 GMT  
		Size: 27.3 KB (27255 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5c4b256a4590d2f6f27554ae7bfae52d11c871af7b20b6abd8245584df66fa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706624814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dc3e40700cd0b164a91029aeffc29632626d0b6a6c3a2e95bd3d126cf1cfd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:51:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:51:56 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:51:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:51:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:51:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:51:58 GMT
USER odoo
# Mon, 08 Dec 2025 18:51:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:51:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759bd05064754db3d644003f10baa21d1bf0d3ff73ef16db49cb922245aaffea`  
		Last Modified: Mon, 08 Dec 2025 18:58:09 GMT  
		Size: 14.9 MB (14884994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115c6456a504ea6ce32b703d0eb1c0cdfe08cceb9eeeb786829c7c152d62cd`  
		Last Modified: Mon, 08 Dec 2025 18:58:13 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6befe92033fab1710308b5218ee1939af1b92005a79d72537650d3006cb8644a`  
		Last Modified: Mon, 08 Dec 2025 18:58:51 GMT  
		Size: 391.9 MB (391875030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd52f20ec540671f2c6a79e60d003cf10e3ce2d52cf1ae32d65c2561c82a83`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cd746c4c2aa00f43faa506f063a68a056bdadf9edd0d45ec1d97af3ed1563`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37225865dc2b2782e3401546753031c1b483a58d1e562bbf0bb59f5d1c6acef`  
		Last Modified: Mon, 08 Dec 2025 18:58:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1d78cc94ee57a9285a9e3da1dcada1c35cbeea1c865fcdf6ea82acfbbaf91d`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:87469b197aae35c22ba8c2b52e6ac9635e608d80694a0980344357378e15c2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68839184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b82057fad447250b073fa9051b72f3f1930d9613a6874f59c37a9b3318fc44`

```dockerfile
```

-	Layers:
	-	`sha256:357850cb22d5df2c86eed24fddee5de600929329ff59e031e0551112e0915887`  
		Last Modified: Mon, 08 Dec 2025 20:16:35 GMT  
		Size: 68.8 MB (68812029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f48d1346f342ded74df06a26251d09af2122e38f1e423ad822fa2fde7a7cc8`  
		Last Modified: Mon, 08 Dec 2025 20:16:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251208`

```console
$ docker pull odoo@sha256:4d344f40154dd0627b7078c3dcb40cf1db7c0944473c1898eb63492659b398ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20251208` - linux; amd64

```console
$ docker pull odoo@sha256:1a94f42236f77c4d03f448cb628998191c4ba3cbba66111cea2e094054ece873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.5 MB (690460915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e480ed7f7126db940133216710f1da02dfdea990cdfa40b3d20fef966a0c0af2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:15 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:15 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:15 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:15 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:48:15 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:25 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:49:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519f7aea1d4b927b7d6f38dc45c9c9033383653d88d0c55a6211ed18ed5e799`  
		Last Modified: Mon, 08 Dec 2025 18:52:32 GMT  
		Size: 254.6 MB (254556917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290a44abafc51bfc0445a3f3c6352ba512dfd96967797e465b39714d574e719`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 14.4 MB (14356488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0182b47140b900aee9388fbeff64532cc5ad404ab547a4b5c1602fbadbc79180`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a0787a6c7bb3bc9617976f5ed96a1a37fa9c432f376f515852609a31eb71bf`  
		Last Modified: Mon, 08 Dec 2025 18:53:00 GMT  
		Size: 391.3 MB (391340363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c937d3e00b3fdf79e7cccb7e922652b2ff51a98b1fc40ad3f83b0fc7931d23`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c398c0ddd5855f5ad6abff23451d043cdd45fe16f1c23fce259bfa5883ed273`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8009cf5ac077a457ed8c62e759c0e01139f3901afcd797924656b9896c8d353`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f36fb0164f52590dc4def278b697d10021b78ad1a483059e37dcf9deb34c53`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:3914ae30eb5d0c6f48ec933e3b4b96831d9c086efeb2e68cd759339cb9b21001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68830733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dfad5a6b12d95501efdd1cbdca00d3e96254b56b42b1d424dd35dc94e0496b`

```dockerfile
```

-	Layers:
	-	`sha256:8c5e680858cd1066e2a2927c48908ddfbcd2f8c5e23a85215cae3293f18d6072`  
		Last Modified: Mon, 08 Dec 2025 20:13:13 GMT  
		Size: 68.8 MB (68803640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e95b241ab0f22f3709186452dce32f2e1cf3f4db19144ee5f77cf660652dfa`  
		Last Modified: Mon, 08 Dec 2025 20:13:15 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251208` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:61dcbdedbc4acdfd614299a747a61b735de7f0763aef184538130488a78f1d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.8 MB (686834724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ae7143f5ed3f1b4ec3ff9e3b1ccc89d3361c4c7216b32a6774f3c921bcb92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:39 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:39 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:50:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:50:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:50:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:50:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
USER odoo
# Mon, 08 Dec 2025 18:50:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:50:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b7f9d7ee89d6736b9b5217119ed2546a0907348808d23407462a3663a2fc8b`  
		Last Modified: Mon, 08 Dec 2025 19:11:05 GMT  
		Size: 252.0 MB (251954320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b82dc4a1f8c23f604a009d7e720b926cc442d3de57da248d84ad2d7ba682ab6`  
		Last Modified: Mon, 08 Dec 2025 19:09:54 GMT  
		Size: 14.3 MB (14334128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d828f926ff16e5463882f70799f58b1947edc638e54cca47feb8ed80754747e`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce1812d64c95ba8e8b5d0bbca1f9da1303e2d0d12614edf8ce8a4ebbe51dee`  
		Last Modified: Mon, 08 Dec 2025 19:11:15 GMT  
		Size: 391.2 MB (391201872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a745c4069c2c2246d1b01d57a053bbbe14c9a19be58c0216fa932132f2698cf1`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a5c5a6cacab3baf2a5cf93d6c8e9650633e64d6ea63f02fb5da3a9b056c5c7`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55131d32740b2aaaf9e5bf9c87517a475d247f3d3bdec6e5c63eb44a55c5003`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e880cef190df70afb9f10bde4d083ae903af435aa7547cea2c21690f79627c`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:2af3cd4a4c467165894497d308beba6f8ea3c53527d4c9ee1849aa08181346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68838182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ee987809a274365d22d1d3af899d4824d142e2284cf05831f1bbcf5285530`

```dockerfile
```

-	Layers:
	-	`sha256:38ee64f59bef97b5b05459fdbdee397c4a24f323c0329d87c0619b7222fc0d7a`  
		Last Modified: Mon, 08 Dec 2025 20:14:56 GMT  
		Size: 68.8 MB (68810927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056dd5c9705bb4013cfcc5244e1f1b3af0035f3d3b91c09919c3112e67048887`  
		Last Modified: Mon, 08 Dec 2025 20:14:58 GMT  
		Size: 27.3 KB (27255 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251208` - linux; ppc64le

```console
$ docker pull odoo@sha256:5c4b256a4590d2f6f27554ae7bfae52d11c871af7b20b6abd8245584df66fa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706624814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dc3e40700cd0b164a91029aeffc29632626d0b6a6c3a2e95bd3d126cf1cfd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:51:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:51:56 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:51:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:51:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:51:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:51:58 GMT
USER odoo
# Mon, 08 Dec 2025 18:51:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:51:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759bd05064754db3d644003f10baa21d1bf0d3ff73ef16db49cb922245aaffea`  
		Last Modified: Mon, 08 Dec 2025 18:58:09 GMT  
		Size: 14.9 MB (14884994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115c6456a504ea6ce32b703d0eb1c0cdfe08cceb9eeeb786829c7c152d62cd`  
		Last Modified: Mon, 08 Dec 2025 18:58:13 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6befe92033fab1710308b5218ee1939af1b92005a79d72537650d3006cb8644a`  
		Last Modified: Mon, 08 Dec 2025 18:58:51 GMT  
		Size: 391.9 MB (391875030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd52f20ec540671f2c6a79e60d003cf10e3ce2d52cf1ae32d65c2561c82a83`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cd746c4c2aa00f43faa506f063a68a056bdadf9edd0d45ec1d97af3ed1563`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37225865dc2b2782e3401546753031c1b483a58d1e562bbf0bb59f5d1c6acef`  
		Last Modified: Mon, 08 Dec 2025 18:58:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1d78cc94ee57a9285a9e3da1dcada1c35cbeea1c865fcdf6ea82acfbbaf91d`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251208` - unknown; unknown

```console
$ docker pull odoo@sha256:87469b197aae35c22ba8c2b52e6ac9635e608d80694a0980344357378e15c2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68839184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b82057fad447250b073fa9051b72f3f1930d9613a6874f59c37a9b3318fc44`

```dockerfile
```

-	Layers:
	-	`sha256:357850cb22d5df2c86eed24fddee5de600929329ff59e031e0551112e0915887`  
		Last Modified: Mon, 08 Dec 2025 20:16:35 GMT  
		Size: 68.8 MB (68812029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f48d1346f342ded74df06a26251d09af2122e38f1e423ad822fa2fde7a7cc8`  
		Last Modified: Mon, 08 Dec 2025 20:16:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:4d344f40154dd0627b7078c3dcb40cf1db7c0944473c1898eb63492659b398ef
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
$ docker pull odoo@sha256:1a94f42236f77c4d03f448cb628998191c4ba3cbba66111cea2e094054ece873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.5 MB (690460915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e480ed7f7126db940133216710f1da02dfdea990cdfa40b3d20fef966a0c0af2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:15 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:15 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:15 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:15 GMT
ARG TARGETARCH=amd64
# Mon, 08 Dec 2025 18:48:15 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:25 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:26 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:26 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:49:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:49:34 GMT
USER odoo
# Mon, 08 Dec 2025 18:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519f7aea1d4b927b7d6f38dc45c9c9033383653d88d0c55a6211ed18ed5e799`  
		Last Modified: Mon, 08 Dec 2025 18:52:32 GMT  
		Size: 254.6 MB (254556917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290a44abafc51bfc0445a3f3c6352ba512dfd96967797e465b39714d574e719`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 14.4 MB (14356488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0182b47140b900aee9388fbeff64532cc5ad404ab547a4b5c1602fbadbc79180`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a0787a6c7bb3bc9617976f5ed96a1a37fa9c432f376f515852609a31eb71bf`  
		Last Modified: Mon, 08 Dec 2025 18:53:00 GMT  
		Size: 391.3 MB (391340363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c937d3e00b3fdf79e7cccb7e922652b2ff51a98b1fc40ad3f83b0fc7931d23`  
		Last Modified: Mon, 08 Dec 2025 18:52:06 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c398c0ddd5855f5ad6abff23451d043cdd45fe16f1c23fce259bfa5883ed273`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8009cf5ac077a457ed8c62e759c0e01139f3901afcd797924656b9896c8d353`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f36fb0164f52590dc4def278b697d10021b78ad1a483059e37dcf9deb34c53`  
		Last Modified: Mon, 08 Dec 2025 18:52:05 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:3914ae30eb5d0c6f48ec933e3b4b96831d9c086efeb2e68cd759339cb9b21001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68830733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dfad5a6b12d95501efdd1cbdca00d3e96254b56b42b1d424dd35dc94e0496b`

```dockerfile
```

-	Layers:
	-	`sha256:8c5e680858cd1066e2a2927c48908ddfbcd2f8c5e23a85215cae3293f18d6072`  
		Last Modified: Mon, 08 Dec 2025 20:13:13 GMT  
		Size: 68.8 MB (68803640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e95b241ab0f22f3709186452dce32f2e1cf3f4db19144ee5f77cf660652dfa`  
		Last Modified: Mon, 08 Dec 2025 20:13:15 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:61dcbdedbc4acdfd614299a747a61b735de7f0763aef184538130488a78f1d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.8 MB (686834724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458ae7143f5ed3f1b4ec3ff9e3b1ccc89d3361c4c7216b32a6774f3c921bcb92`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 18:48:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 08 Dec 2025 18:48:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 08 Dec 2025 18:48:39 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 18:48:39 GMT
ARG TARGETARCH=arm64
# Mon, 08 Dec 2025 18:48:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:51 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:51 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:50:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:50:01 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:50:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:50:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:50:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:50:02 GMT
USER odoo
# Mon, 08 Dec 2025 18:50:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:50:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b7f9d7ee89d6736b9b5217119ed2546a0907348808d23407462a3663a2fc8b`  
		Last Modified: Mon, 08 Dec 2025 19:11:05 GMT  
		Size: 252.0 MB (251954320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b82dc4a1f8c23f604a009d7e720b926cc442d3de57da248d84ad2d7ba682ab6`  
		Last Modified: Mon, 08 Dec 2025 19:09:54 GMT  
		Size: 14.3 MB (14334128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d828f926ff16e5463882f70799f58b1947edc638e54cca47feb8ed80754747e`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce1812d64c95ba8e8b5d0bbca1f9da1303e2d0d12614edf8ce8a4ebbe51dee`  
		Last Modified: Mon, 08 Dec 2025 19:11:15 GMT  
		Size: 391.2 MB (391201872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a745c4069c2c2246d1b01d57a053bbbe14c9a19be58c0216fa932132f2698cf1`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a5c5a6cacab3baf2a5cf93d6c8e9650633e64d6ea63f02fb5da3a9b056c5c7`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55131d32740b2aaaf9e5bf9c87517a475d247f3d3bdec6e5c63eb44a55c5003`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e880cef190df70afb9f10bde4d083ae903af435aa7547cea2c21690f79627c`  
		Last Modified: Mon, 08 Dec 2025 19:09:52 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2af3cd4a4c467165894497d308beba6f8ea3c53527d4c9ee1849aa08181346d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68838182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936ee987809a274365d22d1d3af899d4824d142e2284cf05831f1bbcf5285530`

```dockerfile
```

-	Layers:
	-	`sha256:38ee64f59bef97b5b05459fdbdee397c4a24f323c0329d87c0619b7222fc0d7a`  
		Last Modified: Mon, 08 Dec 2025 20:14:56 GMT  
		Size: 68.8 MB (68810927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056dd5c9705bb4013cfcc5244e1f1b3af0035f3d3b91c09919c3112e67048887`  
		Last Modified: Mon, 08 Dec 2025 20:14:58 GMT  
		Size: 27.3 KB (27255 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:5c4b256a4590d2f6f27554ae7bfae52d11c871af7b20b6abd8245584df66fa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706624814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04dc3e40700cd0b164a91029aeffc29632626d0b6a6c3a2e95bd3d126cf1cfd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 21 Nov 2025 18:40:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 21 Nov 2025 18:40:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 21 Nov 2025 18:40:21 GMT
ENV LANG=en_US.UTF-8
# Fri, 21 Nov 2025 18:40:21 GMT
ARG TARGETARCH=ppc64le
# Fri, 21 Nov 2025 18:40:21 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 08 Dec 2025 18:48:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 08 Dec 2025 18:48:55 GMT
ENV ODOO_VERSION=19.0
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_RELEASE=20251208
# Mon, 08 Dec 2025 18:48:55 GMT
ARG ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
# Mon, 08 Dec 2025 18:51:54 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 08 Dec 2025 18:51:56 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251208 ODOO_SHA=76c8b61b443676477eea546635aca37b8431dd9d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 08 Dec 2025 18:51:57 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 08 Dec 2025 18:51:57 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 08 Dec 2025 18:51:57 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 08 Dec 2025 18:51:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 08 Dec 2025 18:51:58 GMT
USER odoo
# Mon, 08 Dec 2025 18:51:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 18:51:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce9a5c62c66358c67542e5ece6de34f2500e466a66dcf608cbebd7e139bbd7`  
		Last Modified: Fri, 21 Nov 2025 19:12:59 GMT  
		Size: 265.1 MB (265077893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759bd05064754db3d644003f10baa21d1bf0d3ff73ef16db49cb922245aaffea`  
		Last Modified: Mon, 08 Dec 2025 18:58:09 GMT  
		Size: 14.9 MB (14884994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f115c6456a504ea6ce32b703d0eb1c0cdfe08cceb9eeeb786829c7c152d62cd`  
		Last Modified: Mon, 08 Dec 2025 18:58:13 GMT  
		Size: 480.0 KB (480032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6befe92033fab1710308b5218ee1939af1b92005a79d72537650d3006cb8644a`  
		Last Modified: Mon, 08 Dec 2025 18:58:51 GMT  
		Size: 391.9 MB (391875030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd52f20ec540671f2c6a79e60d003cf10e3ce2d52cf1ae32d65c2561c82a83`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cd746c4c2aa00f43faa506f063a68a056bdadf9edd0d45ec1d97af3ed1563`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37225865dc2b2782e3401546753031c1b483a58d1e562bbf0bb59f5d1c6acef`  
		Last Modified: Mon, 08 Dec 2025 18:58:43 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1d78cc94ee57a9285a9e3da1dcada1c35cbeea1c865fcdf6ea82acfbbaf91d`  
		Last Modified: Mon, 08 Dec 2025 18:58:42 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:87469b197aae35c22ba8c2b52e6ac9635e608d80694a0980344357378e15c2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68839184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b82057fad447250b073fa9051b72f3f1930d9613a6874f59c37a9b3318fc44`

```dockerfile
```

-	Layers:
	-	`sha256:357850cb22d5df2c86eed24fddee5de600929329ff59e031e0551112e0915887`  
		Last Modified: Mon, 08 Dec 2025 20:16:35 GMT  
		Size: 68.8 MB (68812029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f48d1346f342ded74df06a26251d09af2122e38f1e423ad822fa2fde7a7cc8`  
		Last Modified: Mon, 08 Dec 2025 20:16:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
