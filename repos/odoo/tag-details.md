<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20251222`](#odoo170-20251222)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20251222`](#odoo180-20251222)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20251222`](#odoo190-20251222)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:29b92e3a4ced847290288d590edf1f4c2e17d2acc41cd1ba4b57b3ce861ae543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:00f14ba7291ef0ffa2aeacc4623f16ec85adf69446d51d960bcaa58fea943890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.0 MB (607994211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a701a20257e477720d7bffb20b7317182462e6d251184521666b8318adc49b3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:26 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
ENV ODOO_VERSION=17.0
# Thu, 15 Jan 2026 22:36:34 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:34 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Thu, 15 Jan 2026 22:37:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17c7c86c8fa6b3129536851d7f5488fcdda82e05202cc87457f2c03881998c`  
		Last Modified: Thu, 15 Jan 2026 22:38:56 GMT  
		Size: 233.8 MB (233821785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaee60253ae674dd4f8e5adf0a1e21086652c71812802eb160901c7d5c59fac`  
		Last Modified: Thu, 15 Jan 2026 22:38:48 GMT  
		Size: 2.6 MB (2597223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d647041e173c54d91dea24f4fa74343c0ca5eb7c12c47dc9eb8ae33934be01`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 480.3 KB (480253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e837f600940e19015d560e191e6df1899fb39a931890775c0be0673ed312712`  
		Last Modified: Thu, 15 Jan 2026 22:38:58 GMT  
		Size: 341.6 MB (341555845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337f6b598c03f1a7ae3ea655b8152d51a3187b357730d749dbc876b9c0224521`  
		Last Modified: Thu, 15 Jan 2026 22:38:49 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fdae804d289e192ba34caebcc65b5759ff366a9293173febe099f31bc33bc9`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06443106d233403828b80e52e7bdae88e5b5802010b649dc969517d1614539e`  
		Last Modified: Thu, 15 Jan 2026 22:38:50 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b1b985fc784681329079297784547521ce4906703f0e324d35456601ebea51`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:6b86d7ac7eac914176e9ca1a577e1eea6c60d6c44bf1fdfe2da0907904c76a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41889697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2da42d713a5ccfdcd4cc3eced71cd0cba9428d7fb02e8f05305352472fe7a4b`

```dockerfile
```

-	Layers:
	-	`sha256:01ecd1da425998e279bb19b6651771f51ede0e186bd869e7d35c98f21179b78f`  
		Last Modified: Fri, 16 Jan 2026 02:14:26 GMT  
		Size: 41.9 MB (41862905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7032ab48395c007b5aec3cef9050380a52f62c4c8e144235bf29b4bd472bf6d`  
		Last Modified: Fri, 16 Jan 2026 02:14:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e4c2d6046356ae2eb9d814afb5a513431e6064315bc210106184076318f5d691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 MB (602834629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f30f9122dacce7db1b89ca2c47f356c973487231f8ddb2872ba511f0aa2d7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:34 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:34 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:42 GMT
ENV ODOO_VERSION=17.0
# Thu, 15 Jan 2026 22:39:42 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:42 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Thu, 15 Jan 2026 22:40:45 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:46 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:46 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fc21cde908ee00edd5e5dfb1520ead5b1f164f458aa39023d180822520021c`  
		Last Modified: Thu, 15 Jan 2026 22:42:18 GMT  
		Size: 231.2 MB (231194970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8e0b082b6534c39debeee840ab3ae82c916ed455c213ab6133723637110d9`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 2.6 MB (2592419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db5b8d616fc6dfbc56a418e8128480f9e94965c58b0093b804f91feef8305e3`  
		Last Modified: Thu, 15 Jan 2026 22:42:08 GMT  
		Size: 480.3 KB (480269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7388506cd83eae41dfc7d405bd27708059b222d40c8e63915a84c12616164c7`  
		Last Modified: Thu, 15 Jan 2026 22:42:19 GMT  
		Size: 341.2 MB (341181035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5f01dd7b713942dde771d639a893633b5aedf93bd7a1dfeb11bb41163f1dda`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0eb22a42785c804ac76a1d86d8a58768a4f00cc5b8c9987e76be31e5bab8ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9f394f97de9c1f394e765991323bd3f7c2be28eceaf0099e33ec139b24bc55`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c48d485d62418a14c12cd519c125862f309db4748f2567e443f2fbc52755a82`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:cc54c486d692c885b5ad0eccadfba85444086e6c87d6eb5148f3ee90347c9154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c2f6e6915bae0febec5a3d1cdfee3af20bf31666912a67b0eacccfd6dc1339`

```dockerfile
```

-	Layers:
	-	`sha256:0d0edc42da73a3dee5ed95d138cde3df3f08d1fe14bdff93c145aee56239d3c2`  
		Last Modified: Fri, 16 Jan 2026 02:15:32 GMT  
		Size: 41.9 MB (41869412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac21f33c3d735d2e06d83b7d5fa629152c015f39b0ea9ba0bf043d20bce2743a`  
		Last Modified: Fri, 16 Jan 2026 02:15:29 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:29b92e3a4ced847290288d590edf1f4c2e17d2acc41cd1ba4b57b3ce861ae543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:00f14ba7291ef0ffa2aeacc4623f16ec85adf69446d51d960bcaa58fea943890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.0 MB (607994211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a701a20257e477720d7bffb20b7317182462e6d251184521666b8318adc49b3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:26 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
ENV ODOO_VERSION=17.0
# Thu, 15 Jan 2026 22:36:34 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:34 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Thu, 15 Jan 2026 22:37:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17c7c86c8fa6b3129536851d7f5488fcdda82e05202cc87457f2c03881998c`  
		Last Modified: Thu, 15 Jan 2026 22:38:56 GMT  
		Size: 233.8 MB (233821785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaee60253ae674dd4f8e5adf0a1e21086652c71812802eb160901c7d5c59fac`  
		Last Modified: Thu, 15 Jan 2026 22:38:48 GMT  
		Size: 2.6 MB (2597223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d647041e173c54d91dea24f4fa74343c0ca5eb7c12c47dc9eb8ae33934be01`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 480.3 KB (480253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e837f600940e19015d560e191e6df1899fb39a931890775c0be0673ed312712`  
		Last Modified: Thu, 15 Jan 2026 22:38:58 GMT  
		Size: 341.6 MB (341555845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337f6b598c03f1a7ae3ea655b8152d51a3187b357730d749dbc876b9c0224521`  
		Last Modified: Thu, 15 Jan 2026 22:38:49 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fdae804d289e192ba34caebcc65b5759ff366a9293173febe099f31bc33bc9`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06443106d233403828b80e52e7bdae88e5b5802010b649dc969517d1614539e`  
		Last Modified: Thu, 15 Jan 2026 22:38:50 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b1b985fc784681329079297784547521ce4906703f0e324d35456601ebea51`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6b86d7ac7eac914176e9ca1a577e1eea6c60d6c44bf1fdfe2da0907904c76a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41889697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2da42d713a5ccfdcd4cc3eced71cd0cba9428d7fb02e8f05305352472fe7a4b`

```dockerfile
```

-	Layers:
	-	`sha256:01ecd1da425998e279bb19b6651771f51ede0e186bd869e7d35c98f21179b78f`  
		Last Modified: Fri, 16 Jan 2026 02:14:26 GMT  
		Size: 41.9 MB (41862905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7032ab48395c007b5aec3cef9050380a52f62c4c8e144235bf29b4bd472bf6d`  
		Last Modified: Fri, 16 Jan 2026 02:14:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e4c2d6046356ae2eb9d814afb5a513431e6064315bc210106184076318f5d691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 MB (602834629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f30f9122dacce7db1b89ca2c47f356c973487231f8ddb2872ba511f0aa2d7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:34 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:34 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:42 GMT
ENV ODOO_VERSION=17.0
# Thu, 15 Jan 2026 22:39:42 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:42 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Thu, 15 Jan 2026 22:40:45 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:46 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:46 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fc21cde908ee00edd5e5dfb1520ead5b1f164f458aa39023d180822520021c`  
		Last Modified: Thu, 15 Jan 2026 22:42:18 GMT  
		Size: 231.2 MB (231194970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8e0b082b6534c39debeee840ab3ae82c916ed455c213ab6133723637110d9`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 2.6 MB (2592419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db5b8d616fc6dfbc56a418e8128480f9e94965c58b0093b804f91feef8305e3`  
		Last Modified: Thu, 15 Jan 2026 22:42:08 GMT  
		Size: 480.3 KB (480269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7388506cd83eae41dfc7d405bd27708059b222d40c8e63915a84c12616164c7`  
		Last Modified: Thu, 15 Jan 2026 22:42:19 GMT  
		Size: 341.2 MB (341181035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5f01dd7b713942dde771d639a893633b5aedf93bd7a1dfeb11bb41163f1dda`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0eb22a42785c804ac76a1d86d8a58768a4f00cc5b8c9987e76be31e5bab8ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9f394f97de9c1f394e765991323bd3f7c2be28eceaf0099e33ec139b24bc55`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c48d485d62418a14c12cd519c125862f309db4748f2567e443f2fbc52755a82`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cc54c486d692c885b5ad0eccadfba85444086e6c87d6eb5148f3ee90347c9154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c2f6e6915bae0febec5a3d1cdfee3af20bf31666912a67b0eacccfd6dc1339`

```dockerfile
```

-	Layers:
	-	`sha256:0d0edc42da73a3dee5ed95d138cde3df3f08d1fe14bdff93c145aee56239d3c2`  
		Last Modified: Fri, 16 Jan 2026 02:15:32 GMT  
		Size: 41.9 MB (41869412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac21f33c3d735d2e06d83b7d5fa629152c015f39b0ea9ba0bf043d20bce2743a`  
		Last Modified: Fri, 16 Jan 2026 02:15:29 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20251222`

```console
$ docker pull odoo@sha256:29b92e3a4ced847290288d590edf1f4c2e17d2acc41cd1ba4b57b3ce861ae543
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20251222` - linux; amd64

```console
$ docker pull odoo@sha256:00f14ba7291ef0ffa2aeacc4623f16ec85adf69446d51d960bcaa58fea943890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.0 MB (607994211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a701a20257e477720d7bffb20b7317182462e6d251184521666b8318adc49b3f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:26 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:34 GMT
ENV ODOO_VERSION=17.0
# Thu, 15 Jan 2026 22:36:34 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:34 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Thu, 15 Jan 2026 22:37:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:37 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17c7c86c8fa6b3129536851d7f5488fcdda82e05202cc87457f2c03881998c`  
		Last Modified: Thu, 15 Jan 2026 22:38:56 GMT  
		Size: 233.8 MB (233821785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaee60253ae674dd4f8e5adf0a1e21086652c71812802eb160901c7d5c59fac`  
		Last Modified: Thu, 15 Jan 2026 22:38:48 GMT  
		Size: 2.6 MB (2597223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d647041e173c54d91dea24f4fa74343c0ca5eb7c12c47dc9eb8ae33934be01`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 480.3 KB (480253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e837f600940e19015d560e191e6df1899fb39a931890775c0be0673ed312712`  
		Last Modified: Thu, 15 Jan 2026 22:38:58 GMT  
		Size: 341.6 MB (341555845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337f6b598c03f1a7ae3ea655b8152d51a3187b357730d749dbc876b9c0224521`  
		Last Modified: Thu, 15 Jan 2026 22:38:49 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fdae804d289e192ba34caebcc65b5759ff366a9293173febe099f31bc33bc9`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06443106d233403828b80e52e7bdae88e5b5802010b649dc969517d1614539e`  
		Last Modified: Thu, 15 Jan 2026 22:38:50 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b1b985fc784681329079297784547521ce4906703f0e324d35456601ebea51`  
		Last Modified: Thu, 15 Jan 2026 22:39:08 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:6b86d7ac7eac914176e9ca1a577e1eea6c60d6c44bf1fdfe2da0907904c76a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41889697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2da42d713a5ccfdcd4cc3eced71cd0cba9428d7fb02e8f05305352472fe7a4b`

```dockerfile
```

-	Layers:
	-	`sha256:01ecd1da425998e279bb19b6651771f51ede0e186bd869e7d35c98f21179b78f`  
		Last Modified: Fri, 16 Jan 2026 02:14:26 GMT  
		Size: 41.9 MB (41862905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7032ab48395c007b5aec3cef9050380a52f62c4c8e144235bf29b4bd472bf6d`  
		Last Modified: Fri, 16 Jan 2026 02:14:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20251222` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e4c2d6046356ae2eb9d814afb5a513431e6064315bc210106184076318f5d691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 MB (602834629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f30f9122dacce7db1b89ca2c47f356c973487231f8ddb2872ba511f0aa2d7d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:34 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:34 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:41 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:42 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:42 GMT
ENV ODOO_VERSION=17.0
# Thu, 15 Jan 2026 22:39:42 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:42 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Thu, 15 Jan 2026 22:40:45 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:46 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:46 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:46 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:46 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:46 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fc21cde908ee00edd5e5dfb1520ead5b1f164f458aa39023d180822520021c`  
		Last Modified: Thu, 15 Jan 2026 22:42:18 GMT  
		Size: 231.2 MB (231194970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8e0b082b6534c39debeee840ab3ae82c916ed455c213ab6133723637110d9`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 2.6 MB (2592419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db5b8d616fc6dfbc56a418e8128480f9e94965c58b0093b804f91feef8305e3`  
		Last Modified: Thu, 15 Jan 2026 22:42:08 GMT  
		Size: 480.3 KB (480269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7388506cd83eae41dfc7d405bd27708059b222d40c8e63915a84c12616164c7`  
		Last Modified: Thu, 15 Jan 2026 22:42:19 GMT  
		Size: 341.2 MB (341181035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5f01dd7b713942dde771d639a893633b5aedf93bd7a1dfeb11bb41163f1dda`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0eb22a42785c804ac76a1d86d8a58768a4f00cc5b8c9987e76be31e5bab8ff`  
		Last Modified: Thu, 15 Jan 2026 22:42:10 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9f394f97de9c1f394e765991323bd3f7c2be28eceaf0099e33ec139b24bc55`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c48d485d62418a14c12cd519c125862f309db4748f2567e443f2fbc52755a82`  
		Last Modified: Thu, 15 Jan 2026 22:42:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:cc54c486d692c885b5ad0eccadfba85444086e6c87d6eb5148f3ee90347c9154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c2f6e6915bae0febec5a3d1cdfee3af20bf31666912a67b0eacccfd6dc1339`

```dockerfile
```

-	Layers:
	-	`sha256:0d0edc42da73a3dee5ed95d138cde3df3f08d1fe14bdff93c145aee56239d3c2`  
		Last Modified: Fri, 16 Jan 2026 02:15:32 GMT  
		Size: 41.9 MB (41869412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac21f33c3d735d2e06d83b7d5fa629152c015f39b0ea9ba0bf043d20bce2743a`  
		Last Modified: Fri, 16 Jan 2026 02:15:29 GMT  
		Size: 26.9 KB (26943 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:d97b033cc20156af2bbbdf29c8f7a127a4c25e60ed5152758af815164527adfb
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
$ docker pull odoo@sha256:02f4a574c1eb878b21c3d1a82b232db9c8fa732e5082265cba8359ecb33c8d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680323001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbc3a21816723aeacc17e6e093bc9d9712fdbc668b2acc492117b6a1606e599`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:42 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:51 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 22:36:51 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:51 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 22:37:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f005fb6b0b8367cdc11598c47adc71adcf3041caaa6f31c618dc39a101df5`  
		Last Modified: Thu, 15 Jan 2026 22:40:42 GMT  
		Size: 254.6 MB (254559834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927448cea8d95a794d9714229e0c21f9cf141f648a55df1b35777f80c51ee77d`  
		Last Modified: Thu, 15 Jan 2026 22:39:54 GMT  
		Size: 14.4 MB (14356521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07c402f721d527ca20dbde0e20d50ad7da09dc1b7dd5d24281334898eaa45d4`  
		Last Modified: Thu, 15 Jan 2026 22:39:29 GMT  
		Size: 480.1 KB (480094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873938e0c0c8139e2c5ebe3b25f58b9378603c89b1231fd887726e4bee07e8d7`  
		Last Modified: Thu, 15 Jan 2026 22:41:18 GMT  
		Size: 381.2 MB (381198099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb07e00bf2b2351f4b7309366efe7f60a4e0ad3c89d463bfd36e78a6266363f3`  
		Last Modified: Thu, 15 Jan 2026 22:39:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77587c450ed28c1b085be8b709389f2a63c9d826c5e08fab21e0fcd18f2551b7`  
		Last Modified: Thu, 15 Jan 2026 22:39:48 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aed3627a453e956190b62ae425a110cf92416b6e4bc96fd859a34dfb919689`  
		Last Modified: Thu, 15 Jan 2026 22:39:32 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd1f45fa6b70b746f002b227671564cd879df1904e673474eeae4f97d2efe43`  
		Last Modified: Thu, 15 Jan 2026 22:39:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:8c09caf6f3bc395c5cc768f4ff3641d1ad4618c1dd129e3cd96f1a29ac348e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e1d7084493d53199e56c546766bdcb5a401bb91d1e34327530ad5c00305a5d`

```dockerfile
```

-	Layers:
	-	`sha256:f56e3620204da0e6b7ca6ea4ce0689a9c891bb49ce8c82cb5333e1f28079395c`  
		Last Modified: Fri, 16 Jan 2026 02:14:42 GMT  
		Size: 61.4 MB (61447215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09338d4884f043607c44bbafd0c7b713b726d66be3a330627f0a109244d4d87c`  
		Last Modified: Fri, 16 Jan 2026 02:14:41 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4423d4a394b2119b86ed2ba9d3a7f7d72e72bdd8a8180b32f0ee258afa7c9514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.7 MB (676702239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2284881f24eb3da5a8976cab56d87b63660744607565ffbd8be43d94daca8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:43 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:53 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 22:39:53 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:53 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 22:40:47 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc84c802cad157a317eee38bcd77d0cf565c26c59b1212746ae8f0d811afd4f2`  
		Last Modified: Thu, 15 Jan 2026 22:44:06 GMT  
		Size: 252.0 MB (251961006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320dc2a1047883f3c459cc13bbb3a76edb43c484d8c431c2be294f24d37606bf`  
		Last Modified: Thu, 15 Jan 2026 22:43:15 GMT  
		Size: 14.3 MB (14334266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d355ca4abe135e41c9ab62439e320dd404aff2732a42d73789118eaceee1ec`  
		Last Modified: Thu, 15 Jan 2026 22:42:55 GMT  
		Size: 480.0 KB (480026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23100f3c93c3b6f92170be0c521c565b9c7f64278514754f2426ddf911c8a670`  
		Last Modified: Thu, 15 Jan 2026 22:43:06 GMT  
		Size: 381.1 MB (381060677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8ede42107e98d16a12065a866f3381f00ade590fc8729826afc48a86243263`  
		Last Modified: Thu, 15 Jan 2026 22:42:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae2f215cdbcf600ed19fd8d24aad39afb860a4430ad50240292614458a913f`  
		Last Modified: Thu, 15 Jan 2026 22:43:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b46814d413726b2000f059ecae45bafc3ef1af338f06839afe0cd7527c31a`  
		Last Modified: Thu, 15 Jan 2026 22:42:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625adc5941f766d7752f73b10d591ad5c48e100112eec87a0043e6efc57ec14`  
		Last Modified: Thu, 15 Jan 2026 22:42:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:099f6761762c3ea026c99ab63c78035ff5e0230a1e7a10d7e27d317b762ccc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61481441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eed58089f5767fa9c2505a6cd280cdd05fc80d055bae9b2053828e3ebfa7566`

```dockerfile
```

-	Layers:
	-	`sha256:092ffa90daa25b25bb175f5169d3911afc2b02f3ddffbb15afc6d1ccab45e426`  
		Last Modified: Fri, 16 Jan 2026 02:17:17 GMT  
		Size: 61.5 MB (61454490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7621fc274d9488a82980dd162f3d3c25b7bb7c458c80a8e2796aa45910724b7b`  
		Last Modified: Fri, 16 Jan 2026 02:17:19 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:21dc855502ceb6d4a63463f0055ff5209794f354521200887f65261e9637d93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696483713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04539853d127877a73bd53df81a9c055d29546b3fcb5db93754058f5a915ed1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 23:07:06 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 23:07:07 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 23:07:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 23:07:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 23:07:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 23:07:09 GMT
USER odoo
# Thu, 15 Jan 2026 23:07:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f74237bc85ab57ae6d6b6456c6a5613986ef48b7e4ebcb59168d1493956290`  
		Last Modified: Thu, 15 Jan 2026 23:14:23 GMT  
		Size: 381.7 MB (381723841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b985b271c9f452a18a80d892b0897edbb5faca83e91463ec9099a38a7bb46e`  
		Last Modified: Thu, 15 Jan 2026 23:13:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61884a2229c8fb710b3647f0fc9d09833aafb9d126ac9bab5984cbf289cbb6`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fabff962265ffc45222b7133e5d291468e9d6e5bcb14d5625af81d58d284c62`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948fe82e6570e756ae27bfb0aabd21e5fbfb5055f69657921278454ec6b2813a`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:b9e2a930274e9bc14a12ba2b6bf3eee49cd7f5395313b6c48eafbcd41f526036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd23917d2305e8dad83466b729c06f2c2a461d62c713aa150dbe273eaf297b3`

```dockerfile
```

-	Layers:
	-	`sha256:9a884343b0d5496b12b549908951f2c85f32842119fdd5a0bb5e32b21ef8a84f`  
		Last Modified: Thu, 15 Jan 2026 23:13:46 GMT  
		Size: 61.5 MB (61455598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676235a5698fd9966ea45c08e4ae3113c3b0a55b3e9bb273e7272feb51259faa`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:d97b033cc20156af2bbbdf29c8f7a127a4c25e60ed5152758af815164527adfb
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
$ docker pull odoo@sha256:02f4a574c1eb878b21c3d1a82b232db9c8fa732e5082265cba8359ecb33c8d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680323001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbc3a21816723aeacc17e6e093bc9d9712fdbc668b2acc492117b6a1606e599`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:42 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:51 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 22:36:51 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:51 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 22:37:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f005fb6b0b8367cdc11598c47adc71adcf3041caaa6f31c618dc39a101df5`  
		Last Modified: Thu, 15 Jan 2026 22:40:42 GMT  
		Size: 254.6 MB (254559834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927448cea8d95a794d9714229e0c21f9cf141f648a55df1b35777f80c51ee77d`  
		Last Modified: Thu, 15 Jan 2026 22:39:54 GMT  
		Size: 14.4 MB (14356521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07c402f721d527ca20dbde0e20d50ad7da09dc1b7dd5d24281334898eaa45d4`  
		Last Modified: Thu, 15 Jan 2026 22:39:29 GMT  
		Size: 480.1 KB (480094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873938e0c0c8139e2c5ebe3b25f58b9378603c89b1231fd887726e4bee07e8d7`  
		Last Modified: Thu, 15 Jan 2026 22:41:18 GMT  
		Size: 381.2 MB (381198099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb07e00bf2b2351f4b7309366efe7f60a4e0ad3c89d463bfd36e78a6266363f3`  
		Last Modified: Thu, 15 Jan 2026 22:39:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77587c450ed28c1b085be8b709389f2a63c9d826c5e08fab21e0fcd18f2551b7`  
		Last Modified: Thu, 15 Jan 2026 22:39:48 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aed3627a453e956190b62ae425a110cf92416b6e4bc96fd859a34dfb919689`  
		Last Modified: Thu, 15 Jan 2026 22:39:32 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd1f45fa6b70b746f002b227671564cd879df1904e673474eeae4f97d2efe43`  
		Last Modified: Thu, 15 Jan 2026 22:39:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8c09caf6f3bc395c5cc768f4ff3641d1ad4618c1dd129e3cd96f1a29ac348e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e1d7084493d53199e56c546766bdcb5a401bb91d1e34327530ad5c00305a5d`

```dockerfile
```

-	Layers:
	-	`sha256:f56e3620204da0e6b7ca6ea4ce0689a9c891bb49ce8c82cb5333e1f28079395c`  
		Last Modified: Fri, 16 Jan 2026 02:14:42 GMT  
		Size: 61.4 MB (61447215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09338d4884f043607c44bbafd0c7b713b726d66be3a330627f0a109244d4d87c`  
		Last Modified: Fri, 16 Jan 2026 02:14:41 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4423d4a394b2119b86ed2ba9d3a7f7d72e72bdd8a8180b32f0ee258afa7c9514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.7 MB (676702239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2284881f24eb3da5a8976cab56d87b63660744607565ffbd8be43d94daca8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:43 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:53 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 22:39:53 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:53 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 22:40:47 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc84c802cad157a317eee38bcd77d0cf565c26c59b1212746ae8f0d811afd4f2`  
		Last Modified: Thu, 15 Jan 2026 22:44:06 GMT  
		Size: 252.0 MB (251961006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320dc2a1047883f3c459cc13bbb3a76edb43c484d8c431c2be294f24d37606bf`  
		Last Modified: Thu, 15 Jan 2026 22:43:15 GMT  
		Size: 14.3 MB (14334266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d355ca4abe135e41c9ab62439e320dd404aff2732a42d73789118eaceee1ec`  
		Last Modified: Thu, 15 Jan 2026 22:42:55 GMT  
		Size: 480.0 KB (480026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23100f3c93c3b6f92170be0c521c565b9c7f64278514754f2426ddf911c8a670`  
		Last Modified: Thu, 15 Jan 2026 22:43:06 GMT  
		Size: 381.1 MB (381060677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8ede42107e98d16a12065a866f3381f00ade590fc8729826afc48a86243263`  
		Last Modified: Thu, 15 Jan 2026 22:42:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae2f215cdbcf600ed19fd8d24aad39afb860a4430ad50240292614458a913f`  
		Last Modified: Thu, 15 Jan 2026 22:43:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b46814d413726b2000f059ecae45bafc3ef1af338f06839afe0cd7527c31a`  
		Last Modified: Thu, 15 Jan 2026 22:42:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625adc5941f766d7752f73b10d591ad5c48e100112eec87a0043e6efc57ec14`  
		Last Modified: Thu, 15 Jan 2026 22:42:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:099f6761762c3ea026c99ab63c78035ff5e0230a1e7a10d7e27d317b762ccc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61481441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eed58089f5767fa9c2505a6cd280cdd05fc80d055bae9b2053828e3ebfa7566`

```dockerfile
```

-	Layers:
	-	`sha256:092ffa90daa25b25bb175f5169d3911afc2b02f3ddffbb15afc6d1ccab45e426`  
		Last Modified: Fri, 16 Jan 2026 02:17:17 GMT  
		Size: 61.5 MB (61454490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7621fc274d9488a82980dd162f3d3c25b7bb7c458c80a8e2796aa45910724b7b`  
		Last Modified: Fri, 16 Jan 2026 02:17:19 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:21dc855502ceb6d4a63463f0055ff5209794f354521200887f65261e9637d93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696483713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04539853d127877a73bd53df81a9c055d29546b3fcb5db93754058f5a915ed1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 23:07:06 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 23:07:07 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 23:07:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 23:07:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 23:07:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 23:07:09 GMT
USER odoo
# Thu, 15 Jan 2026 23:07:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f74237bc85ab57ae6d6b6456c6a5613986ef48b7e4ebcb59168d1493956290`  
		Last Modified: Thu, 15 Jan 2026 23:14:23 GMT  
		Size: 381.7 MB (381723841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b985b271c9f452a18a80d892b0897edbb5faca83e91463ec9099a38a7bb46e`  
		Last Modified: Thu, 15 Jan 2026 23:13:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61884a2229c8fb710b3647f0fc9d09833aafb9d126ac9bab5984cbf289cbb6`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fabff962265ffc45222b7133e5d291468e9d6e5bcb14d5625af81d58d284c62`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948fe82e6570e756ae27bfb0aabd21e5fbfb5055f69657921278454ec6b2813a`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b9e2a930274e9bc14a12ba2b6bf3eee49cd7f5395313b6c48eafbcd41f526036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd23917d2305e8dad83466b729c06f2c2a461d62c713aa150dbe273eaf297b3`

```dockerfile
```

-	Layers:
	-	`sha256:9a884343b0d5496b12b549908951f2c85f32842119fdd5a0bb5e32b21ef8a84f`  
		Last Modified: Thu, 15 Jan 2026 23:13:46 GMT  
		Size: 61.5 MB (61455598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676235a5698fd9966ea45c08e4ae3113c3b0a55b3e9bb273e7272feb51259faa`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251222`

```console
$ docker pull odoo@sha256:d97b033cc20156af2bbbdf29c8f7a127a4c25e60ed5152758af815164527adfb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20251222` - linux; amd64

```console
$ docker pull odoo@sha256:02f4a574c1eb878b21c3d1a82b232db9c8fa732e5082265cba8359ecb33c8d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680323001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcbc3a21816723aeacc17e6e093bc9d9712fdbc668b2acc492117b6a1606e599`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:42 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:42 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:42 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:50 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:51 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 22:36:51 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:51 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 22:37:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:53 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441f005fb6b0b8367cdc11598c47adc71adcf3041caaa6f31c618dc39a101df5`  
		Last Modified: Thu, 15 Jan 2026 22:40:42 GMT  
		Size: 254.6 MB (254559834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927448cea8d95a794d9714229e0c21f9cf141f648a55df1b35777f80c51ee77d`  
		Last Modified: Thu, 15 Jan 2026 22:39:54 GMT  
		Size: 14.4 MB (14356521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07c402f721d527ca20dbde0e20d50ad7da09dc1b7dd5d24281334898eaa45d4`  
		Last Modified: Thu, 15 Jan 2026 22:39:29 GMT  
		Size: 480.1 KB (480094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873938e0c0c8139e2c5ebe3b25f58b9378603c89b1231fd887726e4bee07e8d7`  
		Last Modified: Thu, 15 Jan 2026 22:41:18 GMT  
		Size: 381.2 MB (381198099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb07e00bf2b2351f4b7309366efe7f60a4e0ad3c89d463bfd36e78a6266363f3`  
		Last Modified: Thu, 15 Jan 2026 22:39:46 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77587c450ed28c1b085be8b709389f2a63c9d826c5e08fab21e0fcd18f2551b7`  
		Last Modified: Thu, 15 Jan 2026 22:39:48 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aed3627a453e956190b62ae425a110cf92416b6e4bc96fd859a34dfb919689`  
		Last Modified: Thu, 15 Jan 2026 22:39:32 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd1f45fa6b70b746f002b227671564cd879df1904e673474eeae4f97d2efe43`  
		Last Modified: Thu, 15 Jan 2026 22:39:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:8c09caf6f3bc395c5cc768f4ff3641d1ad4618c1dd129e3cd96f1a29ac348e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e1d7084493d53199e56c546766bdcb5a401bb91d1e34327530ad5c00305a5d`

```dockerfile
```

-	Layers:
	-	`sha256:f56e3620204da0e6b7ca6ea4ce0689a9c891bb49ce8c82cb5333e1f28079395c`  
		Last Modified: Fri, 16 Jan 2026 02:14:42 GMT  
		Size: 61.4 MB (61447215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09338d4884f043607c44bbafd0c7b713b726d66be3a330627f0a109244d4d87c`  
		Last Modified: Fri, 16 Jan 2026 02:14:41 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251222` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4423d4a394b2119b86ed2ba9d3a7f7d72e72bdd8a8180b32f0ee258afa7c9514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.7 MB (676702239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2284881f24eb3da5a8976cab56d87b63660744607565ffbd8be43d94daca8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:43 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:52 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:53 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:53 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 22:39:53 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:53 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 22:40:47 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:48 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc84c802cad157a317eee38bcd77d0cf565c26c59b1212746ae8f0d811afd4f2`  
		Last Modified: Thu, 15 Jan 2026 22:44:06 GMT  
		Size: 252.0 MB (251961006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320dc2a1047883f3c459cc13bbb3a76edb43c484d8c431c2be294f24d37606bf`  
		Last Modified: Thu, 15 Jan 2026 22:43:15 GMT  
		Size: 14.3 MB (14334266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d355ca4abe135e41c9ab62439e320dd404aff2732a42d73789118eaceee1ec`  
		Last Modified: Thu, 15 Jan 2026 22:42:55 GMT  
		Size: 480.0 KB (480026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23100f3c93c3b6f92170be0c521c565b9c7f64278514754f2426ddf911c8a670`  
		Last Modified: Thu, 15 Jan 2026 22:43:06 GMT  
		Size: 381.1 MB (381060677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8ede42107e98d16a12065a866f3381f00ade590fc8729826afc48a86243263`  
		Last Modified: Thu, 15 Jan 2026 22:42:57 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae2f215cdbcf600ed19fd8d24aad39afb860a4430ad50240292614458a913f`  
		Last Modified: Thu, 15 Jan 2026 22:43:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26b46814d413726b2000f059ecae45bafc3ef1af338f06839afe0cd7527c31a`  
		Last Modified: Thu, 15 Jan 2026 22:42:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8625adc5941f766d7752f73b10d591ad5c48e100112eec87a0043e6efc57ec14`  
		Last Modified: Thu, 15 Jan 2026 22:42:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:099f6761762c3ea026c99ab63c78035ff5e0230a1e7a10d7e27d317b762ccc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61481441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eed58089f5767fa9c2505a6cd280cdd05fc80d055bae9b2053828e3ebfa7566`

```dockerfile
```

-	Layers:
	-	`sha256:092ffa90daa25b25bb175f5169d3911afc2b02f3ddffbb15afc6d1ccab45e426`  
		Last Modified: Fri, 16 Jan 2026 02:17:17 GMT  
		Size: 61.5 MB (61454490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7621fc274d9488a82980dd162f3d3c25b7bb7c458c80a8e2796aa45910724b7b`  
		Last Modified: Fri, 16 Jan 2026 02:17:19 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251222` - linux; ppc64le

```console
$ docker pull odoo@sha256:21dc855502ceb6d4a63463f0055ff5209794f354521200887f65261e9637d93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696483713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04539853d127877a73bd53df81a9c055d29546b3fcb5db93754058f5a915ed1a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=18.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Thu, 15 Jan 2026 23:07:06 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 23:07:07 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 23:07:08 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 23:07:08 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 23:07:08 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 23:07:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 23:07:09 GMT
USER odoo
# Thu, 15 Jan 2026 23:07:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f74237bc85ab57ae6d6b6456c6a5613986ef48b7e4ebcb59168d1493956290`  
		Last Modified: Thu, 15 Jan 2026 23:14:23 GMT  
		Size: 381.7 MB (381723841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b985b271c9f452a18a80d892b0897edbb5faca83e91463ec9099a38a7bb46e`  
		Last Modified: Thu, 15 Jan 2026 23:13:40 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a61884a2229c8fb710b3647f0fc9d09833aafb9d126ac9bab5984cbf289cbb6`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fabff962265ffc45222b7133e5d291468e9d6e5bcb14d5625af81d58d284c62`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948fe82e6570e756ae27bfb0aabd21e5fbfb5055f69657921278454ec6b2813a`  
		Last Modified: Thu, 15 Jan 2026 23:14:38 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:b9e2a930274e9bc14a12ba2b6bf3eee49cd7f5395313b6c48eafbcd41f526036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd23917d2305e8dad83466b729c06f2c2a461d62c713aa150dbe273eaf297b3`

```dockerfile
```

-	Layers:
	-	`sha256:9a884343b0d5496b12b549908951f2c85f32842119fdd5a0bb5e32b21ef8a84f`  
		Last Modified: Thu, 15 Jan 2026 23:13:46 GMT  
		Size: 61.5 MB (61455598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676235a5698fd9966ea45c08e4ae3113c3b0a55b3e9bb273e7272feb51259faa`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:023d430b00bd0a5c61d00e96e33b7eab0d2e6f6e4b87532da5afc9307e450099
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
$ docker pull odoo@sha256:31b4e53575fe4343bc23a03506cc1c214f94e95433bc42c3c05e2d03a31b6fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691614895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9939f5efda1297cb8588b3d6c3c186d386d98dd5e1cf43ce9e156e3ba8fd07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:37 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:37 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:37 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:37:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4958cc6986519e870c986f2d0f507d2d25430d0e8ebfec798665df90f83198d4`  
		Last Modified: Thu, 15 Jan 2026 22:40:06 GMT  
		Size: 254.6 MB (254560144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6ef8ce87d79389d106723e845d1091fd1adc3068da26bae31db64b24c9831`  
		Last Modified: Thu, 15 Jan 2026 22:39:58 GMT  
		Size: 14.4 MB (14356691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76572d87b1166780e3cc8c96de1efc2b92c07c51a3f60150c7830bdd76663585`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 480.0 KB (479998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d6b5dea911cd23086db063f2a07cdadd41ad12cb6dd734da6c659e9f312e18`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
		Size: 392.5 MB (392489614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeb33206d14e3a827cfacfc14120ba513716e6ee0134b083ce8b53a2dcea325`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a62294a44590fa7b13ab0ffd8cba277dbee30a66748e655c3c3d7305a71b7a`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2429fdc6629df2f4799f1251d07de252e2abd349586476b93b8b10bcb5bc04d`  
		Last Modified: Thu, 15 Jan 2026 22:39:59 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45652fc61218c95179addb47d986e7b9bc9bef7c8c380984a5ae432fd7b918f`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:d07410130bb5e44db40c77586ae5f1576eb6044b13ee8f156f17423a1960fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615834a443a5a571b5effdd01eaf4032dbd2980e3064be193e708af7b3d5e1f2`

```dockerfile
```

-	Layers:
	-	`sha256:6f42e35928f607beca55b66b3a75efc4f6835ef6baf268bb8ea63db0975b25b0`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 68.9 MB (68856442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8861e1c68bbc996c3911a5ab3fb2a7da903d395492c4153da862cbbb054128f`  
		Last Modified: Fri, 16 Jan 2026 02:15:04 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b5723f300a5cc88d1391d599240d7d34fac1829c910eb9479715b6b35fa3167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687961418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363f4ebd2277b561efbafad041fc9ef74e5bd116428b93de16a296119ba27138`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:10 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:40:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074e025f0c098757f391b645f4d042f8c0659a970876621d5baebb4bc4af1241`  
		Last Modified: Thu, 15 Jan 2026 22:43:15 GMT  
		Size: 252.0 MB (251959718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da616211d37160cd876e49ea58203e1ea5dae0c43d6a58a91154bd88c80bc22a`  
		Last Modified: Thu, 15 Jan 2026 22:43:13 GMT  
		Size: 14.3 MB (14334207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b861f9a397e2d47708ff2f839a8580e629cd6179d8b3a9cb02724c9d3ed886a6`  
		Last Modified: Thu, 15 Jan 2026 22:42:47 GMT  
		Size: 480.0 KB (480022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c455b138874c2373beb4347256c1bd00ea96bab8bd401c079ef467c14c9c85`  
		Last Modified: Fri, 16 Jan 2026 02:18:01 GMT  
		Size: 392.3 MB (392321217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2606668c065818fe835fd6956207aacee43bc2d4221ba580430a7e930fc4a17e`  
		Last Modified: Thu, 15 Jan 2026 22:42:48 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73e905dc63fce4ca07a367e1765bd307f37de7c66bd5999c2a2398eb4371804`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcc47060ab63667ae73ee89b6959bb17df5bf2de276945ddc64b0bf9588a3af`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c25f5c2627aa44f2bf8e32bd64fbbd1124de17297d89c2f5289e5f9f58574e`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:5f4381dd7f8d6c85a3dc0d06cea4f7ee047a999d096fca16f6b6b6ec1b6e18c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4075119310877b7badec24c212940735f9f1e32984708b54efeb7927c3113cf9`

```dockerfile
```

-	Layers:
	-	`sha256:64bea758f8b13dd17c9f820394a70adc41cfb5fa9a4ea0ba7a931fbd472d3da4`  
		Last Modified: Thu, 15 Jan 2026 22:42:51 GMT  
		Size: 68.9 MB (68863729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89a283939e7ac60579190184f05c0b04daabea1cc4047b754d5c84d5d07280a`  
		Last Modified: Fri, 16 Jan 2026 02:18:05 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:573ce20f55360adbcf5527c074de1a63704c3cd2d68f9cb224ba997fded4bee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d6d86ed3f619bb5c8b9ea0066429c23fca7c0e13af3e3b97e50dc98ff0a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 23:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 23:07:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 23:07:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 23:07:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 23:07:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
USER odoo
# Thu, 15 Jan 2026 23:07:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ef0ec9bea55fcca3dc1f53c117690eca39256799d90df827e11b3ab401b9a`  
		Last Modified: Thu, 15 Jan 2026 23:14:52 GMT  
		Size: 393.0 MB (393027092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cde8f3781f0b3d956a0d06d31ee34a984b3aa7a173b865624f71d2b91de4b4`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fab3eb0f6daa36e0ebccda05f17c59d8f56f92b680839c9d853ec6d8b1656`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca52f490d7427e29e854ab4d7f326b39df9fd0b052417aeacc204845e1f6c0`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e53857faef2670127a217f6a7ad3c04e83ddeee121fae61a7d33cf32ee55b`  
		Last Modified: Thu, 15 Jan 2026 23:14:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:4299a1aa6fa474d73439dbfe09fa52801cac669a42785dcbae3ff622c5198a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d69a3fe049fcc9ab89551a5279dba9af46f393248526e5863e5a30ac23bc63`

```dockerfile
```

-	Layers:
	-	`sha256:ab0695914803cb85581eaef8ddfc3cd2fce2fd3298701740e3873e90d22dfb56`  
		Last Modified: Thu, 15 Jan 2026 23:14:45 GMT  
		Size: 68.9 MB (68864831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f128409752f1136921a90b8db911f46ed1c143978b603b0d0b293748a5462b44`  
		Last Modified: Thu, 15 Jan 2026 23:14:41 GMT  
		Size: 27.2 KB (27153 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:023d430b00bd0a5c61d00e96e33b7eab0d2e6f6e4b87532da5afc9307e450099
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
$ docker pull odoo@sha256:31b4e53575fe4343bc23a03506cc1c214f94e95433bc42c3c05e2d03a31b6fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691614895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9939f5efda1297cb8588b3d6c3c186d386d98dd5e1cf43ce9e156e3ba8fd07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:37 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:37 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:37 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:37:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4958cc6986519e870c986f2d0f507d2d25430d0e8ebfec798665df90f83198d4`  
		Last Modified: Thu, 15 Jan 2026 22:40:06 GMT  
		Size: 254.6 MB (254560144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6ef8ce87d79389d106723e845d1091fd1adc3068da26bae31db64b24c9831`  
		Last Modified: Thu, 15 Jan 2026 22:39:58 GMT  
		Size: 14.4 MB (14356691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76572d87b1166780e3cc8c96de1efc2b92c07c51a3f60150c7830bdd76663585`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 480.0 KB (479998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d6b5dea911cd23086db063f2a07cdadd41ad12cb6dd734da6c659e9f312e18`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
		Size: 392.5 MB (392489614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeb33206d14e3a827cfacfc14120ba513716e6ee0134b083ce8b53a2dcea325`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a62294a44590fa7b13ab0ffd8cba277dbee30a66748e655c3c3d7305a71b7a`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2429fdc6629df2f4799f1251d07de252e2abd349586476b93b8b10bcb5bc04d`  
		Last Modified: Thu, 15 Jan 2026 22:39:59 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45652fc61218c95179addb47d986e7b9bc9bef7c8c380984a5ae432fd7b918f`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d07410130bb5e44db40c77586ae5f1576eb6044b13ee8f156f17423a1960fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615834a443a5a571b5effdd01eaf4032dbd2980e3064be193e708af7b3d5e1f2`

```dockerfile
```

-	Layers:
	-	`sha256:6f42e35928f607beca55b66b3a75efc4f6835ef6baf268bb8ea63db0975b25b0`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 68.9 MB (68856442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8861e1c68bbc996c3911a5ab3fb2a7da903d395492c4153da862cbbb054128f`  
		Last Modified: Fri, 16 Jan 2026 02:15:04 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b5723f300a5cc88d1391d599240d7d34fac1829c910eb9479715b6b35fa3167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687961418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363f4ebd2277b561efbafad041fc9ef74e5bd116428b93de16a296119ba27138`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:10 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:40:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074e025f0c098757f391b645f4d042f8c0659a970876621d5baebb4bc4af1241`  
		Last Modified: Thu, 15 Jan 2026 22:43:15 GMT  
		Size: 252.0 MB (251959718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da616211d37160cd876e49ea58203e1ea5dae0c43d6a58a91154bd88c80bc22a`  
		Last Modified: Thu, 15 Jan 2026 22:43:13 GMT  
		Size: 14.3 MB (14334207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b861f9a397e2d47708ff2f839a8580e629cd6179d8b3a9cb02724c9d3ed886a6`  
		Last Modified: Thu, 15 Jan 2026 22:42:47 GMT  
		Size: 480.0 KB (480022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c455b138874c2373beb4347256c1bd00ea96bab8bd401c079ef467c14c9c85`  
		Last Modified: Fri, 16 Jan 2026 02:18:01 GMT  
		Size: 392.3 MB (392321217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2606668c065818fe835fd6956207aacee43bc2d4221ba580430a7e930fc4a17e`  
		Last Modified: Thu, 15 Jan 2026 22:42:48 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73e905dc63fce4ca07a367e1765bd307f37de7c66bd5999c2a2398eb4371804`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcc47060ab63667ae73ee89b6959bb17df5bf2de276945ddc64b0bf9588a3af`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c25f5c2627aa44f2bf8e32bd64fbbd1124de17297d89c2f5289e5f9f58574e`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5f4381dd7f8d6c85a3dc0d06cea4f7ee047a999d096fca16f6b6b6ec1b6e18c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4075119310877b7badec24c212940735f9f1e32984708b54efeb7927c3113cf9`

```dockerfile
```

-	Layers:
	-	`sha256:64bea758f8b13dd17c9f820394a70adc41cfb5fa9a4ea0ba7a931fbd472d3da4`  
		Last Modified: Thu, 15 Jan 2026 22:42:51 GMT  
		Size: 68.9 MB (68863729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89a283939e7ac60579190184f05c0b04daabea1cc4047b754d5c84d5d07280a`  
		Last Modified: Fri, 16 Jan 2026 02:18:05 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:573ce20f55360adbcf5527c074de1a63704c3cd2d68f9cb224ba997fded4bee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d6d86ed3f619bb5c8b9ea0066429c23fca7c0e13af3e3b97e50dc98ff0a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 23:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 23:07:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 23:07:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 23:07:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 23:07:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
USER odoo
# Thu, 15 Jan 2026 23:07:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ef0ec9bea55fcca3dc1f53c117690eca39256799d90df827e11b3ab401b9a`  
		Last Modified: Thu, 15 Jan 2026 23:14:52 GMT  
		Size: 393.0 MB (393027092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cde8f3781f0b3d956a0d06d31ee34a984b3aa7a173b865624f71d2b91de4b4`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fab3eb0f6daa36e0ebccda05f17c59d8f56f92b680839c9d853ec6d8b1656`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca52f490d7427e29e854ab4d7f326b39df9fd0b052417aeacc204845e1f6c0`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e53857faef2670127a217f6a7ad3c04e83ddeee121fae61a7d33cf32ee55b`  
		Last Modified: Thu, 15 Jan 2026 23:14:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4299a1aa6fa474d73439dbfe09fa52801cac669a42785dcbae3ff622c5198a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d69a3fe049fcc9ab89551a5279dba9af46f393248526e5863e5a30ac23bc63`

```dockerfile
```

-	Layers:
	-	`sha256:ab0695914803cb85581eaef8ddfc3cd2fce2fd3298701740e3873e90d22dfb56`  
		Last Modified: Thu, 15 Jan 2026 23:14:45 GMT  
		Size: 68.9 MB (68864831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f128409752f1136921a90b8db911f46ed1c143978b603b0d0b293748a5462b44`  
		Last Modified: Thu, 15 Jan 2026 23:14:41 GMT  
		Size: 27.2 KB (27153 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251222`

```console
$ docker pull odoo@sha256:023d430b00bd0a5c61d00e96e33b7eab0d2e6f6e4b87532da5afc9307e450099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20251222` - linux; amd64

```console
$ docker pull odoo@sha256:31b4e53575fe4343bc23a03506cc1c214f94e95433bc42c3c05e2d03a31b6fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691614895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9939f5efda1297cb8588b3d6c3c186d386d98dd5e1cf43ce9e156e3ba8fd07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:37 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:37 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:37 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:37:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4958cc6986519e870c986f2d0f507d2d25430d0e8ebfec798665df90f83198d4`  
		Last Modified: Thu, 15 Jan 2026 22:40:06 GMT  
		Size: 254.6 MB (254560144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6ef8ce87d79389d106723e845d1091fd1adc3068da26bae31db64b24c9831`  
		Last Modified: Thu, 15 Jan 2026 22:39:58 GMT  
		Size: 14.4 MB (14356691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76572d87b1166780e3cc8c96de1efc2b92c07c51a3f60150c7830bdd76663585`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 480.0 KB (479998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d6b5dea911cd23086db063f2a07cdadd41ad12cb6dd734da6c659e9f312e18`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
		Size: 392.5 MB (392489614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeb33206d14e3a827cfacfc14120ba513716e6ee0134b083ce8b53a2dcea325`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a62294a44590fa7b13ab0ffd8cba277dbee30a66748e655c3c3d7305a71b7a`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2429fdc6629df2f4799f1251d07de252e2abd349586476b93b8b10bcb5bc04d`  
		Last Modified: Thu, 15 Jan 2026 22:39:59 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45652fc61218c95179addb47d986e7b9bc9bef7c8c380984a5ae432fd7b918f`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:d07410130bb5e44db40c77586ae5f1576eb6044b13ee8f156f17423a1960fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615834a443a5a571b5effdd01eaf4032dbd2980e3064be193e708af7b3d5e1f2`

```dockerfile
```

-	Layers:
	-	`sha256:6f42e35928f607beca55b66b3a75efc4f6835ef6baf268bb8ea63db0975b25b0`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 68.9 MB (68856442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8861e1c68bbc996c3911a5ab3fb2a7da903d395492c4153da862cbbb054128f`  
		Last Modified: Fri, 16 Jan 2026 02:15:04 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251222` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b5723f300a5cc88d1391d599240d7d34fac1829c910eb9479715b6b35fa3167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687961418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363f4ebd2277b561efbafad041fc9ef74e5bd116428b93de16a296119ba27138`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:10 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:40:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074e025f0c098757f391b645f4d042f8c0659a970876621d5baebb4bc4af1241`  
		Last Modified: Thu, 15 Jan 2026 22:43:15 GMT  
		Size: 252.0 MB (251959718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da616211d37160cd876e49ea58203e1ea5dae0c43d6a58a91154bd88c80bc22a`  
		Last Modified: Thu, 15 Jan 2026 22:43:13 GMT  
		Size: 14.3 MB (14334207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b861f9a397e2d47708ff2f839a8580e629cd6179d8b3a9cb02724c9d3ed886a6`  
		Last Modified: Thu, 15 Jan 2026 22:42:47 GMT  
		Size: 480.0 KB (480022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c455b138874c2373beb4347256c1bd00ea96bab8bd401c079ef467c14c9c85`  
		Last Modified: Fri, 16 Jan 2026 02:18:01 GMT  
		Size: 392.3 MB (392321217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2606668c065818fe835fd6956207aacee43bc2d4221ba580430a7e930fc4a17e`  
		Last Modified: Thu, 15 Jan 2026 22:42:48 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73e905dc63fce4ca07a367e1765bd307f37de7c66bd5999c2a2398eb4371804`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcc47060ab63667ae73ee89b6959bb17df5bf2de276945ddc64b0bf9588a3af`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c25f5c2627aa44f2bf8e32bd64fbbd1124de17297d89c2f5289e5f9f58574e`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:5f4381dd7f8d6c85a3dc0d06cea4f7ee047a999d096fca16f6b6b6ec1b6e18c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4075119310877b7badec24c212940735f9f1e32984708b54efeb7927c3113cf9`

```dockerfile
```

-	Layers:
	-	`sha256:64bea758f8b13dd17c9f820394a70adc41cfb5fa9a4ea0ba7a931fbd472d3da4`  
		Last Modified: Thu, 15 Jan 2026 22:42:51 GMT  
		Size: 68.9 MB (68863729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89a283939e7ac60579190184f05c0b04daabea1cc4047b754d5c84d5d07280a`  
		Last Modified: Fri, 16 Jan 2026 02:18:05 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251222` - linux; ppc64le

```console
$ docker pull odoo@sha256:573ce20f55360adbcf5527c074de1a63704c3cd2d68f9cb224ba997fded4bee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d6d86ed3f619bb5c8b9ea0066429c23fca7c0e13af3e3b97e50dc98ff0a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 23:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 23:07:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 23:07:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 23:07:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 23:07:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
USER odoo
# Thu, 15 Jan 2026 23:07:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ef0ec9bea55fcca3dc1f53c117690eca39256799d90df827e11b3ab401b9a`  
		Last Modified: Thu, 15 Jan 2026 23:14:52 GMT  
		Size: 393.0 MB (393027092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cde8f3781f0b3d956a0d06d31ee34a984b3aa7a173b865624f71d2b91de4b4`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fab3eb0f6daa36e0ebccda05f17c59d8f56f92b680839c9d853ec6d8b1656`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca52f490d7427e29e854ab4d7f326b39df9fd0b052417aeacc204845e1f6c0`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e53857faef2670127a217f6a7ad3c04e83ddeee121fae61a7d33cf32ee55b`  
		Last Modified: Thu, 15 Jan 2026 23:14:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:4299a1aa6fa474d73439dbfe09fa52801cac669a42785dcbae3ff622c5198a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d69a3fe049fcc9ab89551a5279dba9af46f393248526e5863e5a30ac23bc63`

```dockerfile
```

-	Layers:
	-	`sha256:ab0695914803cb85581eaef8ddfc3cd2fce2fd3298701740e3873e90d22dfb56`  
		Last Modified: Thu, 15 Jan 2026 23:14:45 GMT  
		Size: 68.9 MB (68864831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f128409752f1136921a90b8db911f46ed1c143978b603b0d0b293748a5462b44`  
		Last Modified: Thu, 15 Jan 2026 23:14:41 GMT  
		Size: 27.2 KB (27153 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:023d430b00bd0a5c61d00e96e33b7eab0d2e6f6e4b87532da5afc9307e450099
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
$ docker pull odoo@sha256:31b4e53575fe4343bc23a03506cc1c214f94e95433bc42c3c05e2d03a31b6fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691614895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9939f5efda1297cb8588b3d6c3c186d386d98dd5e1cf43ce9e156e3ba8fd07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:36:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:36:37 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:36:37 GMT
ARG TARGETARCH=amd64
# Thu, 15 Jan 2026 22:36:37 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:36:47 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:36:48 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:36:48 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:37:50 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:37:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:37:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:37:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:37:51 GMT
USER odoo
# Thu, 15 Jan 2026 22:37:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4958cc6986519e870c986f2d0f507d2d25430d0e8ebfec798665df90f83198d4`  
		Last Modified: Thu, 15 Jan 2026 22:40:06 GMT  
		Size: 254.6 MB (254560144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6ef8ce87d79389d106723e845d1091fd1adc3068da26bae31db64b24c9831`  
		Last Modified: Thu, 15 Jan 2026 22:39:58 GMT  
		Size: 14.4 MB (14356691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76572d87b1166780e3cc8c96de1efc2b92c07c51a3f60150c7830bdd76663585`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 480.0 KB (479998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d6b5dea911cd23086db063f2a07cdadd41ad12cb6dd734da6c659e9f312e18`  
		Last Modified: Thu, 15 Jan 2026 22:40:35 GMT  
		Size: 392.5 MB (392489614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeb33206d14e3a827cfacfc14120ba513716e6ee0134b083ce8b53a2dcea325`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a62294a44590fa7b13ab0ffd8cba277dbee30a66748e655c3c3d7305a71b7a`  
		Last Modified: Thu, 15 Jan 2026 22:40:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2429fdc6629df2f4799f1251d07de252e2abd349586476b93b8b10bcb5bc04d`  
		Last Modified: Thu, 15 Jan 2026 22:39:59 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45652fc61218c95179addb47d986e7b9bc9bef7c8c380984a5ae432fd7b918f`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d07410130bb5e44db40c77586ae5f1576eb6044b13ee8f156f17423a1960fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615834a443a5a571b5effdd01eaf4032dbd2980e3064be193e708af7b3d5e1f2`

```dockerfile
```

-	Layers:
	-	`sha256:6f42e35928f607beca55b66b3a75efc4f6835ef6baf268bb8ea63db0975b25b0`  
		Last Modified: Thu, 15 Jan 2026 22:40:01 GMT  
		Size: 68.9 MB (68856442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8861e1c68bbc996c3911a5ab3fb2a7da903d395492c4153da862cbbb054128f`  
		Last Modified: Fri, 16 Jan 2026 02:15:04 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b5723f300a5cc88d1391d599240d7d34fac1829c910eb9479715b6b35fa3167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687961418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363f4ebd2277b561efbafad041fc9ef74e5bd116428b93de16a296119ba27138`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:39:10 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 22:39:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 22:39:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:39:10 GMT
ARG TARGETARCH=arm64
# Thu, 15 Jan 2026 22:39:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 22:39:19 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 22:39:20 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 22:39:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 22:40:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 22:40:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 22:40:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 22:40:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 22:40:25 GMT
USER odoo
# Thu, 15 Jan 2026 22:40:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 22:40:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074e025f0c098757f391b645f4d042f8c0659a970876621d5baebb4bc4af1241`  
		Last Modified: Thu, 15 Jan 2026 22:43:15 GMT  
		Size: 252.0 MB (251959718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da616211d37160cd876e49ea58203e1ea5dae0c43d6a58a91154bd88c80bc22a`  
		Last Modified: Thu, 15 Jan 2026 22:43:13 GMT  
		Size: 14.3 MB (14334207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b861f9a397e2d47708ff2f839a8580e629cd6179d8b3a9cb02724c9d3ed886a6`  
		Last Modified: Thu, 15 Jan 2026 22:42:47 GMT  
		Size: 480.0 KB (480022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c455b138874c2373beb4347256c1bd00ea96bab8bd401c079ef467c14c9c85`  
		Last Modified: Fri, 16 Jan 2026 02:18:01 GMT  
		Size: 392.3 MB (392321217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2606668c065818fe835fd6956207aacee43bc2d4221ba580430a7e930fc4a17e`  
		Last Modified: Thu, 15 Jan 2026 22:42:48 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73e905dc63fce4ca07a367e1765bd307f37de7c66bd5999c2a2398eb4371804`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcc47060ab63667ae73ee89b6959bb17df5bf2de276945ddc64b0bf9588a3af`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c25f5c2627aa44f2bf8e32bd64fbbd1124de17297d89c2f5289e5f9f58574e`  
		Last Modified: Thu, 15 Jan 2026 22:43:04 GMT  
		Size: 577.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:5f4381dd7f8d6c85a3dc0d06cea4f7ee047a999d096fca16f6b6b6ec1b6e18c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4075119310877b7badec24c212940735f9f1e32984708b54efeb7927c3113cf9`

```dockerfile
```

-	Layers:
	-	`sha256:64bea758f8b13dd17c9f820394a70adc41cfb5fa9a4ea0ba7a931fbd472d3da4`  
		Last Modified: Thu, 15 Jan 2026 22:42:51 GMT  
		Size: 68.9 MB (68863729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f89a283939e7ac60579190184f05c0b04daabea1cc4047b754d5c84d5d07280a`  
		Last Modified: Fri, 16 Jan 2026 02:18:05 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:573ce20f55360adbcf5527c074de1a63704c3cd2d68f9cb224ba997fded4bee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d6d86ed3f619bb5c8b9ea0066429c23fca7c0e13af3e3b97e50dc98ff0a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:03:41 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 15 Jan 2026 23:03:41 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 15 Jan 2026 23:03:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 23:03:41 GMT
ARG TARGETARCH=ppc64le
# Thu, 15 Jan 2026 23:03:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 15 Jan 2026 23:03:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 15 Jan 2026 23:03:58 GMT
ENV ODOO_VERSION=19.0
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_RELEASE=20251222
# Thu, 15 Jan 2026 23:03:58 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Thu, 15 Jan 2026 23:07:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 15 Jan 2026 23:07:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 15 Jan 2026 23:07:38 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 15 Jan 2026 23:07:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 15 Jan 2026 23:07:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 15 Jan 2026 23:07:39 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 15 Jan 2026 23:07:39 GMT
USER odoo
# Thu, 15 Jan 2026 23:07:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jan 2026 23:07:39 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90922f8e214809ab22624ef8a00b7369f6a658b7732c295be899ed3323d50f6`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 265.1 MB (265085598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9198399be59b7de3ad3af18163a31dde6f48c7e75b3981d7fc88e8ad3599c79`  
		Last Modified: Thu, 15 Jan 2026 23:13:39 GMT  
		Size: 14.9 MB (14885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09b670fa7165a2e583eda3cbcaa02efa51bcb326123cb766a798ffff02ae8a8`  
		Last Modified: Thu, 15 Jan 2026 23:13:38 GMT  
		Size: 480.1 KB (480100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140ef0ec9bea55fcca3dc1f53c117690eca39256799d90df827e11b3ab401b9a`  
		Last Modified: Thu, 15 Jan 2026 23:14:52 GMT  
		Size: 393.0 MB (393027092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cde8f3781f0b3d956a0d06d31ee34a984b3aa7a173b865624f71d2b91de4b4`  
		Last Modified: Thu, 15 Jan 2026 23:15:02 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fab3eb0f6daa36e0ebccda05f17c59d8f56f92b680839c9d853ec6d8b1656`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca52f490d7427e29e854ab4d7f326b39df9fd0b052417aeacc204845e1f6c0`  
		Last Modified: Thu, 15 Jan 2026 23:14:57 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75e53857faef2670127a217f6a7ad3c04e83ddeee121fae61a7d33cf32ee55b`  
		Last Modified: Thu, 15 Jan 2026 23:14:43 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:4299a1aa6fa474d73439dbfe09fa52801cac669a42785dcbae3ff622c5198a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d69a3fe049fcc9ab89551a5279dba9af46f393248526e5863e5a30ac23bc63`

```dockerfile
```

-	Layers:
	-	`sha256:ab0695914803cb85581eaef8ddfc3cd2fce2fd3298701740e3873e90d22dfb56`  
		Last Modified: Thu, 15 Jan 2026 23:14:45 GMT  
		Size: 68.9 MB (68864831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f128409752f1136921a90b8db911f46ed1c143978b603b0d0b293748a5462b44`  
		Last Modified: Thu, 15 Jan 2026 23:14:41 GMT  
		Size: 27.2 KB (27153 bytes)  
		MIME: application/vnd.in-toto+json
