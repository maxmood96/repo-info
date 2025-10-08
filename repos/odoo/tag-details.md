<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20251008`](#odoo170-20251008)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20251008`](#odoo180-20251008)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20251008`](#odoo190-20251008)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:9213e335f9ef476999391d4a94b07ae014331a199c86a58fc6e803436634e1cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:85918b09185dbdc00dce0c3572555353ef9dae7353687d1e8ebf2ed99cc05e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0fdb21016f91e42b3e9b222d4cd2e8ec8fd0ab232a0f045fc94c576fe086ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=17.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c05d6773480670fcf23083c5b18cc5297d68316128bdd6933e12febc03eb17`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 233.8 MB (233819153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a19f62779e106639666910a7c9a3b0597918fcb4586e84244e56c7c459b38`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 2.6 MB (2595063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ddca305f8385b8aaef8028cb1ba994db6290e70f4c0f26110784e6f3a831b4`  
		Last Modified: Wed, 08 Oct 2025 19:09:08 GMT  
		Size: 480.3 KB (480256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3c6eb5ea5e8db8e041dbae4beaf31ca16a97bdfa86d991956d8011fbc5eb20`  
		Last Modified: Wed, 08 Oct 2025 19:12:42 GMT  
		Size: 338.9 MB (338871148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e2daf3015f78bc17d842382a300a8e203a794adeb90a1a79a8aea5909e3294`  
		Last Modified: Wed, 08 Oct 2025 19:09:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e6ca3a8f80d02a84ac4a3aec3e8629fcdf95f5df872f55a38ad237c1125288`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7511c5ee31175e301c04e2c1aee0ccfa6c866eb9bf920aaf262f14c81f2539`  
		Last Modified: Wed, 08 Oct 2025 19:09:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e91dcc9a6ba6a91c611b74defa8d6306ff389101be6f29be4327f987d10812`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:7ae7a52e243b9d5d4d6cb625b1ed96ed202971ebe277c6f574df241bdebbf35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41510445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7378d67ebe311ca23e8261a8be1f91d1bc55693fa307535df5ed0c7c970b46`

```dockerfile
```

-	Layers:
	-	`sha256:b9b12c218fbc089c91638c5192214a6c75b2ce16fc6608c7bece1f0692499932`  
		Last Modified: Wed, 08 Oct 2025 19:12:28 GMT  
		Size: 41.5 MB (41483610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1524b7d8925234c85bcd097bd72c87944a88339fa21fc25915032936a286b166`  
		Last Modified: Wed, 08 Oct 2025 19:12:29 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a33fb4d79c4996b3b0199b6e7b0d774b2725d9ca57297930665e73060a3c529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600117923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff240f4e6beeecb6539ad05a97515247e09f9e99c240a7c19a19936a719322d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=17.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589dbeb0e391d076411d4a251df237c5c5580bc01d1bc0b55844d3045a751b7b`  
		Last Modified: Wed, 08 Oct 2025 19:14:07 GMT  
		Size: 231.2 MB (231187792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c42e1a8741c9f9265f818fe1233eb977e777166cbf3b05303fc4a3b8b7cb396`  
		Last Modified: Wed, 08 Oct 2025 18:16:16 GMT  
		Size: 2.6 MB (2590569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1415157ad91f8f7a19da9e48f0a51887a8fcf3f72dcc335a4125c2655c4ddd`  
		Last Modified: Wed, 08 Oct 2025 18:16:15 GMT  
		Size: 480.3 KB (480288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef1b056646bddba9f94f71406ce8b5b1de800da47cbd3133d73c7128a7cce0`  
		Last Modified: Wed, 08 Oct 2025 19:15:04 GMT  
		Size: 338.5 MB (338473731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58ae6023e67bfe98c80487be1233501b4c25741b85d1e7e79d726a42ca17ff1`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce068edc21f9a877049bf2efdeb87973ba5bba32844c0a88a5d2f8402c88d5ce`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6a7bf44ea86d6bdb6ebb1a46601c4425614dcbb81d8adb77013b0189445fc`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e617f530cf762d20cbb1a77452761517e7eaa81780b7abe739f5294b6cb313`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:95551098c711bbe4b91f0b841ae9f926a1189b61cd33f88f0512b73270ef19da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41517104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac25615e213902e592d03e36593d9d179a5cf694e1b3ac23894c58ac1423b60`

```dockerfile
```

-	Layers:
	-	`sha256:a42614e36b8edbe32509328b14e47e43e58821a8736d0df63b891b5e32c70485`  
		Last Modified: Wed, 08 Oct 2025 19:13:09 GMT  
		Size: 41.5 MB (41490117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4786c2733e48f0f1bed9164c81d4e6697ba037b39c83ae418fdeb61d32e92d`  
		Last Modified: Wed, 08 Oct 2025 19:13:10 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:9213e335f9ef476999391d4a94b07ae014331a199c86a58fc6e803436634e1cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:85918b09185dbdc00dce0c3572555353ef9dae7353687d1e8ebf2ed99cc05e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0fdb21016f91e42b3e9b222d4cd2e8ec8fd0ab232a0f045fc94c576fe086ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=17.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c05d6773480670fcf23083c5b18cc5297d68316128bdd6933e12febc03eb17`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 233.8 MB (233819153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a19f62779e106639666910a7c9a3b0597918fcb4586e84244e56c7c459b38`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 2.6 MB (2595063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ddca305f8385b8aaef8028cb1ba994db6290e70f4c0f26110784e6f3a831b4`  
		Last Modified: Wed, 08 Oct 2025 19:09:08 GMT  
		Size: 480.3 KB (480256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3c6eb5ea5e8db8e041dbae4beaf31ca16a97bdfa86d991956d8011fbc5eb20`  
		Last Modified: Wed, 08 Oct 2025 19:12:42 GMT  
		Size: 338.9 MB (338871148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e2daf3015f78bc17d842382a300a8e203a794adeb90a1a79a8aea5909e3294`  
		Last Modified: Wed, 08 Oct 2025 19:09:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e6ca3a8f80d02a84ac4a3aec3e8629fcdf95f5df872f55a38ad237c1125288`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7511c5ee31175e301c04e2c1aee0ccfa6c866eb9bf920aaf262f14c81f2539`  
		Last Modified: Wed, 08 Oct 2025 19:09:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e91dcc9a6ba6a91c611b74defa8d6306ff389101be6f29be4327f987d10812`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7ae7a52e243b9d5d4d6cb625b1ed96ed202971ebe277c6f574df241bdebbf35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41510445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7378d67ebe311ca23e8261a8be1f91d1bc55693fa307535df5ed0c7c970b46`

```dockerfile
```

-	Layers:
	-	`sha256:b9b12c218fbc089c91638c5192214a6c75b2ce16fc6608c7bece1f0692499932`  
		Last Modified: Wed, 08 Oct 2025 19:12:28 GMT  
		Size: 41.5 MB (41483610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1524b7d8925234c85bcd097bd72c87944a88339fa21fc25915032936a286b166`  
		Last Modified: Wed, 08 Oct 2025 19:12:29 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a33fb4d79c4996b3b0199b6e7b0d774b2725d9ca57297930665e73060a3c529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600117923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff240f4e6beeecb6539ad05a97515247e09f9e99c240a7c19a19936a719322d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=17.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589dbeb0e391d076411d4a251df237c5c5580bc01d1bc0b55844d3045a751b7b`  
		Last Modified: Wed, 08 Oct 2025 19:14:07 GMT  
		Size: 231.2 MB (231187792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c42e1a8741c9f9265f818fe1233eb977e777166cbf3b05303fc4a3b8b7cb396`  
		Last Modified: Wed, 08 Oct 2025 18:16:16 GMT  
		Size: 2.6 MB (2590569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1415157ad91f8f7a19da9e48f0a51887a8fcf3f72dcc335a4125c2655c4ddd`  
		Last Modified: Wed, 08 Oct 2025 18:16:15 GMT  
		Size: 480.3 KB (480288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef1b056646bddba9f94f71406ce8b5b1de800da47cbd3133d73c7128a7cce0`  
		Last Modified: Wed, 08 Oct 2025 19:15:04 GMT  
		Size: 338.5 MB (338473731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58ae6023e67bfe98c80487be1233501b4c25741b85d1e7e79d726a42ca17ff1`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce068edc21f9a877049bf2efdeb87973ba5bba32844c0a88a5d2f8402c88d5ce`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6a7bf44ea86d6bdb6ebb1a46601c4425614dcbb81d8adb77013b0189445fc`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e617f530cf762d20cbb1a77452761517e7eaa81780b7abe739f5294b6cb313`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:95551098c711bbe4b91f0b841ae9f926a1189b61cd33f88f0512b73270ef19da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41517104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac25615e213902e592d03e36593d9d179a5cf694e1b3ac23894c58ac1423b60`

```dockerfile
```

-	Layers:
	-	`sha256:a42614e36b8edbe32509328b14e47e43e58821a8736d0df63b891b5e32c70485`  
		Last Modified: Wed, 08 Oct 2025 19:13:09 GMT  
		Size: 41.5 MB (41490117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4786c2733e48f0f1bed9164c81d4e6697ba037b39c83ae418fdeb61d32e92d`  
		Last Modified: Wed, 08 Oct 2025 19:13:10 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20251008`

```console
$ docker pull odoo@sha256:9213e335f9ef476999391d4a94b07ae014331a199c86a58fc6e803436634e1cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20251008` - linux; amd64

```console
$ docker pull odoo@sha256:85918b09185dbdc00dce0c3572555353ef9dae7353687d1e8ebf2ed99cc05e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0fdb21016f91e42b3e9b222d4cd2e8ec8fd0ab232a0f045fc94c576fe086ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=17.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c05d6773480670fcf23083c5b18cc5297d68316128bdd6933e12febc03eb17`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 233.8 MB (233819153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66a19f62779e106639666910a7c9a3b0597918fcb4586e84244e56c7c459b38`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 2.6 MB (2595063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ddca305f8385b8aaef8028cb1ba994db6290e70f4c0f26110784e6f3a831b4`  
		Last Modified: Wed, 08 Oct 2025 19:09:08 GMT  
		Size: 480.3 KB (480256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3c6eb5ea5e8db8e041dbae4beaf31ca16a97bdfa86d991956d8011fbc5eb20`  
		Last Modified: Wed, 08 Oct 2025 19:12:42 GMT  
		Size: 338.9 MB (338871148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e2daf3015f78bc17d842382a300a8e203a794adeb90a1a79a8aea5909e3294`  
		Last Modified: Wed, 08 Oct 2025 19:09:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e6ca3a8f80d02a84ac4a3aec3e8629fcdf95f5df872f55a38ad237c1125288`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7511c5ee31175e301c04e2c1aee0ccfa6c866eb9bf920aaf262f14c81f2539`  
		Last Modified: Wed, 08 Oct 2025 19:09:11 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e91dcc9a6ba6a91c611b74defa8d6306ff389101be6f29be4327f987d10812`  
		Last Modified: Wed, 08 Oct 2025 19:09:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:7ae7a52e243b9d5d4d6cb625b1ed96ed202971ebe277c6f574df241bdebbf35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41510445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7378d67ebe311ca23e8261a8be1f91d1bc55693fa307535df5ed0c7c970b46`

```dockerfile
```

-	Layers:
	-	`sha256:b9b12c218fbc089c91638c5192214a6c75b2ce16fc6608c7bece1f0692499932`  
		Last Modified: Wed, 08 Oct 2025 19:12:28 GMT  
		Size: 41.5 MB (41483610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1524b7d8925234c85bcd097bd72c87944a88339fa21fc25915032936a286b166`  
		Last Modified: Wed, 08 Oct 2025 19:12:29 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20251008` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a33fb4d79c4996b3b0199b6e7b0d774b2725d9ca57297930665e73060a3c529e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.1 MB (600117923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff240f4e6beeecb6539ad05a97515247e09f9e99c240a7c19a19936a719322d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=17.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=108bdab1cd0f0b6dc6dc2a1f8fffa78871d9d9b5
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589dbeb0e391d076411d4a251df237c5c5580bc01d1bc0b55844d3045a751b7b`  
		Last Modified: Wed, 08 Oct 2025 19:14:07 GMT  
		Size: 231.2 MB (231187792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c42e1a8741c9f9265f818fe1233eb977e777166cbf3b05303fc4a3b8b7cb396`  
		Last Modified: Wed, 08 Oct 2025 18:16:16 GMT  
		Size: 2.6 MB (2590569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1415157ad91f8f7a19da9e48f0a51887a8fcf3f72dcc335a4125c2655c4ddd`  
		Last Modified: Wed, 08 Oct 2025 18:16:15 GMT  
		Size: 480.3 KB (480288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef1b056646bddba9f94f71406ce8b5b1de800da47cbd3133d73c7128a7cce0`  
		Last Modified: Wed, 08 Oct 2025 19:15:04 GMT  
		Size: 338.5 MB (338473731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58ae6023e67bfe98c80487be1233501b4c25741b85d1e7e79d726a42ca17ff1`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce068edc21f9a877049bf2efdeb87973ba5bba32844c0a88a5d2f8402c88d5ce`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd6a7bf44ea86d6bdb6ebb1a46601c4425614dcbb81d8adb77013b0189445fc`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e617f530cf762d20cbb1a77452761517e7eaa81780b7abe739f5294b6cb313`  
		Last Modified: Wed, 08 Oct 2025 18:16:17 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:95551098c711bbe4b91f0b841ae9f926a1189b61cd33f88f0512b73270ef19da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41517104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac25615e213902e592d03e36593d9d179a5cf694e1b3ac23894c58ac1423b60`

```dockerfile
```

-	Layers:
	-	`sha256:a42614e36b8edbe32509328b14e47e43e58821a8736d0df63b891b5e32c70485`  
		Last Modified: Wed, 08 Oct 2025 19:13:09 GMT  
		Size: 41.5 MB (41490117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4786c2733e48f0f1bed9164c81d4e6697ba037b39c83ae418fdeb61d32e92d`  
		Last Modified: Wed, 08 Oct 2025 19:13:10 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:1c2a0711c08344b93bc0ec6f66675173031eb8d7ef6de334e1e298e9e5443f1f
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
$ docker pull odoo@sha256:921ab31768127c75f8a0edc400c994b81a617d9558e821dc337612816c13d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.7 MB (679687311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f430f9e649723380c2001842f170e5875eafccfcd212f136653f552dedf84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed381ffbdbc1d83bc90d51beb7100a1ae93287261c2790cfe225da2082c6634`  
		Last Modified: Wed, 08 Oct 2025 19:12:50 GMT  
		Size: 256.9 MB (256943769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da84b2544c31404edd3f1b06048ae8e1a5db94a7834b7b6cda1e67465df4f2a`  
		Last Modified: Wed, 08 Oct 2025 18:16:26 GMT  
		Size: 14.3 MB (14339321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bf27d4b2af70f0f5d5b6a94b3ae14c0e16880e5d51f8148afeced6d415bd94`  
		Last Modified: Wed, 08 Oct 2025 18:16:24 GMT  
		Size: 480.1 KB (480075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96fe8a081d33b7710cedd26a1013d26b4ec799ff6f5ab638083afab05de9935`  
		Last Modified: Wed, 08 Oct 2025 19:14:02 GMT  
		Size: 378.2 MB (378198695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45cefddbcdca14036c9b1c23a9969186ab9e0e21cb3775ee464f209355d3c36`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077bb6635ddc859d0b76918190143c0f3bb4f322b8ed3e4c8b3e79285c8f50fb`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b0825b050425e4ab9b687d95b11d2db9d78d8dd3c7e23f4da890e0eee3294f`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50241139db3218d7c057965806a23177a03d891c040379c4c738fa8b367cb196`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:0b2d0b04ca13141f014307433b93b4483341eaa74de0f0216369c58bc5b316c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61134382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31648944bda99bf776eecf348221c0d967f01c8b5ff71c54bb2df4ce8c2ba2ee`

```dockerfile
```

-	Layers:
	-	`sha256:7c0dab7cdf0512a3a977dd091768717ab11e9cdca91b62d0a313f4490c320bef`  
		Last Modified: Wed, 08 Oct 2025 19:12:44 GMT  
		Size: 61.1 MB (61107540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d2f51a619da30ad912c6bbb097d32967ac505ca681b3601f9bf29d84cc6d2e`  
		Last Modified: Wed, 08 Oct 2025 19:12:45 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:06065c64b8e595d5b78f572557d6f75dc8fe576e54e534fe2f52cebaad943200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.9 MB (675923580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7285b837f4560f666ae820511ff43e7f1d1f8016c37231ac0367808745ac6795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d651204e7bc58b37300bbab21f73f236a51404f345826c35f316f123759a161`  
		Last Modified: Wed, 08 Oct 2025 19:13:26 GMT  
		Size: 254.2 MB (254201440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918e6295f8606365365bee8b463266bce265c0ba8a6a5dd04df734778d0aea86`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 14.3 MB (14319927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2534b9daae049396ef8891934b4fc188f51fb30a2f46ba37a2e808dff3140ac`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 480.0 KB (480035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79eaaef1b45cf1c0a2bc8447e115011caf744ad64c5b3894d62491f8023a9e5`  
		Last Modified: Wed, 08 Oct 2025 19:13:12 GMT  
		Size: 378.1 MB (378058163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d9f91f519152d3c576d739a32410e6c09f298425cd998bf13ccc9c7ff17c3d`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbc4edbd9ffd36387471049196e7cf6771617e397a6945ade8025b133b76d3`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375d8d6e8e9a6f34faa33ae3df77e99711ce19d3cd3f26962f089af19002cd35`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303b18df3290f0357911474141f1b34c7b4d0843ffe04fd80ce47555c9c63fa8`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:180d82d2459b7475a86d8ca1a155ae79cab139adf71c4fa1efc94f6ec7bba05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61141809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17543938e5d31d14472edc0e5db67913f23d408b18b1354a1142b5e2cd9335eb`

```dockerfile
```

-	Layers:
	-	`sha256:9443a615145df6dc9a9af48cffaa1b21a5b1431db51d174694677b2271f6026a`  
		Last Modified: Wed, 08 Oct 2025 19:14:43 GMT  
		Size: 61.1 MB (61114815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73a5c25612463e8efc5b1d7096f5e6f6a7feb47ff1923097c44f2bb4595d966`  
		Last Modified: Wed, 08 Oct 2025 19:14:44 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:1c3a7c963f6d5722bff11c2a93bacc4b704da869c7cbba3148df4fcd47a400dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.1 MB (696107813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53af280ca46178706b4a6f037544ac9ccc9a49d224f500c055ee481ee2cb82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:35:27 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:35:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:35:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:35:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:35:31 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 14:35:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
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
	-	`sha256:bbb110cafef2e34e479e4445e81e296c27a3e56de49cc58e3d7e2858ae3301bf`  
		Last Modified: Wed, 08 Oct 2025 18:26:02 GMT  
		Size: 378.7 MB (378726201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad5afc89e30eaa59f7713230a18d4bd050e806e9e2a6fb40bf51c36ead946dc`  
		Last Modified: Wed, 08 Oct 2025 18:25:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafea179163bf763e0b7a0b85e5b3a58cda454628f4868254e7ad26490d46a6`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8add19c753a3a038caccf35842034561060df21020b1cb09be2f0bda4bdf6e1`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87eebe59846a92fe3b949d786f5fa3b1f2d7716ab3d71325543d4e52b89f310`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:a49e998ad7f3ddd5ee06a52817869b3236ebb688b97b3e8c5f0eb6ec3fcc3b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61142820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a3157c4ef3ab53f2500f27e8a0dbb469adcc86d12288747a15a04f787de516`

```dockerfile
```

-	Layers:
	-	`sha256:08e9fff6aa5d894dab60a9df6e91a292aff021626a5c7aa6fdb6a88a2d10499c`  
		Last Modified: Wed, 08 Oct 2025 19:16:38 GMT  
		Size: 61.1 MB (61115923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d16009e4b84f210076518f74ec50d7f70ef7c10c164aa817240aa851c2748d8`  
		Last Modified: Wed, 08 Oct 2025 19:16:39 GMT  
		Size: 26.9 KB (26897 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:1c2a0711c08344b93bc0ec6f66675173031eb8d7ef6de334e1e298e9e5443f1f
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
$ docker pull odoo@sha256:921ab31768127c75f8a0edc400c994b81a617d9558e821dc337612816c13d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.7 MB (679687311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f430f9e649723380c2001842f170e5875eafccfcd212f136653f552dedf84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed381ffbdbc1d83bc90d51beb7100a1ae93287261c2790cfe225da2082c6634`  
		Last Modified: Wed, 08 Oct 2025 19:12:50 GMT  
		Size: 256.9 MB (256943769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da84b2544c31404edd3f1b06048ae8e1a5db94a7834b7b6cda1e67465df4f2a`  
		Last Modified: Wed, 08 Oct 2025 18:16:26 GMT  
		Size: 14.3 MB (14339321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bf27d4b2af70f0f5d5b6a94b3ae14c0e16880e5d51f8148afeced6d415bd94`  
		Last Modified: Wed, 08 Oct 2025 18:16:24 GMT  
		Size: 480.1 KB (480075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96fe8a081d33b7710cedd26a1013d26b4ec799ff6f5ab638083afab05de9935`  
		Last Modified: Wed, 08 Oct 2025 19:14:02 GMT  
		Size: 378.2 MB (378198695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45cefddbcdca14036c9b1c23a9969186ab9e0e21cb3775ee464f209355d3c36`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077bb6635ddc859d0b76918190143c0f3bb4f322b8ed3e4c8b3e79285c8f50fb`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b0825b050425e4ab9b687d95b11d2db9d78d8dd3c7e23f4da890e0eee3294f`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50241139db3218d7c057965806a23177a03d891c040379c4c738fa8b367cb196`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0b2d0b04ca13141f014307433b93b4483341eaa74de0f0216369c58bc5b316c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61134382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31648944bda99bf776eecf348221c0d967f01c8b5ff71c54bb2df4ce8c2ba2ee`

```dockerfile
```

-	Layers:
	-	`sha256:7c0dab7cdf0512a3a977dd091768717ab11e9cdca91b62d0a313f4490c320bef`  
		Last Modified: Wed, 08 Oct 2025 19:12:44 GMT  
		Size: 61.1 MB (61107540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d2f51a619da30ad912c6bbb097d32967ac505ca681b3601f9bf29d84cc6d2e`  
		Last Modified: Wed, 08 Oct 2025 19:12:45 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:06065c64b8e595d5b78f572557d6f75dc8fe576e54e534fe2f52cebaad943200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.9 MB (675923580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7285b837f4560f666ae820511ff43e7f1d1f8016c37231ac0367808745ac6795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d651204e7bc58b37300bbab21f73f236a51404f345826c35f316f123759a161`  
		Last Modified: Wed, 08 Oct 2025 19:13:26 GMT  
		Size: 254.2 MB (254201440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918e6295f8606365365bee8b463266bce265c0ba8a6a5dd04df734778d0aea86`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 14.3 MB (14319927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2534b9daae049396ef8891934b4fc188f51fb30a2f46ba37a2e808dff3140ac`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 480.0 KB (480035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79eaaef1b45cf1c0a2bc8447e115011caf744ad64c5b3894d62491f8023a9e5`  
		Last Modified: Wed, 08 Oct 2025 19:13:12 GMT  
		Size: 378.1 MB (378058163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d9f91f519152d3c576d739a32410e6c09f298425cd998bf13ccc9c7ff17c3d`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbc4edbd9ffd36387471049196e7cf6771617e397a6945ade8025b133b76d3`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375d8d6e8e9a6f34faa33ae3df77e99711ce19d3cd3f26962f089af19002cd35`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303b18df3290f0357911474141f1b34c7b4d0843ffe04fd80ce47555c9c63fa8`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:180d82d2459b7475a86d8ca1a155ae79cab139adf71c4fa1efc94f6ec7bba05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61141809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17543938e5d31d14472edc0e5db67913f23d408b18b1354a1142b5e2cd9335eb`

```dockerfile
```

-	Layers:
	-	`sha256:9443a615145df6dc9a9af48cffaa1b21a5b1431db51d174694677b2271f6026a`  
		Last Modified: Wed, 08 Oct 2025 19:14:43 GMT  
		Size: 61.1 MB (61114815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73a5c25612463e8efc5b1d7096f5e6f6a7feb47ff1923097c44f2bb4595d966`  
		Last Modified: Wed, 08 Oct 2025 19:14:44 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1c3a7c963f6d5722bff11c2a93bacc4b704da869c7cbba3148df4fcd47a400dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.1 MB (696107813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53af280ca46178706b4a6f037544ac9ccc9a49d224f500c055ee481ee2cb82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:35:27 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:35:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:35:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:35:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:35:31 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 14:35:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
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
	-	`sha256:bbb110cafef2e34e479e4445e81e296c27a3e56de49cc58e3d7e2858ae3301bf`  
		Last Modified: Wed, 08 Oct 2025 18:26:02 GMT  
		Size: 378.7 MB (378726201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad5afc89e30eaa59f7713230a18d4bd050e806e9e2a6fb40bf51c36ead946dc`  
		Last Modified: Wed, 08 Oct 2025 18:25:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafea179163bf763e0b7a0b85e5b3a58cda454628f4868254e7ad26490d46a6`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8add19c753a3a038caccf35842034561060df21020b1cb09be2f0bda4bdf6e1`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87eebe59846a92fe3b949d786f5fa3b1f2d7716ab3d71325543d4e52b89f310`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a49e998ad7f3ddd5ee06a52817869b3236ebb688b97b3e8c5f0eb6ec3fcc3b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61142820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a3157c4ef3ab53f2500f27e8a0dbb469adcc86d12288747a15a04f787de516`

```dockerfile
```

-	Layers:
	-	`sha256:08e9fff6aa5d894dab60a9df6e91a292aff021626a5c7aa6fdb6a88a2d10499c`  
		Last Modified: Wed, 08 Oct 2025 19:16:38 GMT  
		Size: 61.1 MB (61115923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d16009e4b84f210076518f74ec50d7f70ef7c10c164aa817240aa851c2748d8`  
		Last Modified: Wed, 08 Oct 2025 19:16:39 GMT  
		Size: 26.9 KB (26897 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251008`

```console
$ docker pull odoo@sha256:1c2a0711c08344b93bc0ec6f66675173031eb8d7ef6de334e1e298e9e5443f1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20251008` - linux; amd64

```console
$ docker pull odoo@sha256:921ab31768127c75f8a0edc400c994b81a617d9558e821dc337612816c13d71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.7 MB (679687311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f430f9e649723380c2001842f170e5875eafccfcd212f136653f552dedf84a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed381ffbdbc1d83bc90d51beb7100a1ae93287261c2790cfe225da2082c6634`  
		Last Modified: Wed, 08 Oct 2025 19:12:50 GMT  
		Size: 256.9 MB (256943769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da84b2544c31404edd3f1b06048ae8e1a5db94a7834b7b6cda1e67465df4f2a`  
		Last Modified: Wed, 08 Oct 2025 18:16:26 GMT  
		Size: 14.3 MB (14339321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bf27d4b2af70f0f5d5b6a94b3ae14c0e16880e5d51f8148afeced6d415bd94`  
		Last Modified: Wed, 08 Oct 2025 18:16:24 GMT  
		Size: 480.1 KB (480075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96fe8a081d33b7710cedd26a1013d26b4ec799ff6f5ab638083afab05de9935`  
		Last Modified: Wed, 08 Oct 2025 19:14:02 GMT  
		Size: 378.2 MB (378198695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45cefddbcdca14036c9b1c23a9969186ab9e0e21cb3775ee464f209355d3c36`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077bb6635ddc859d0b76918190143c0f3bb4f322b8ed3e4c8b3e79285c8f50fb`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b0825b050425e4ab9b687d95b11d2db9d78d8dd3c7e23f4da890e0eee3294f`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50241139db3218d7c057965806a23177a03d891c040379c4c738fa8b367cb196`  
		Last Modified: Wed, 08 Oct 2025 18:16:25 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:0b2d0b04ca13141f014307433b93b4483341eaa74de0f0216369c58bc5b316c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61134382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31648944bda99bf776eecf348221c0d967f01c8b5ff71c54bb2df4ce8c2ba2ee`

```dockerfile
```

-	Layers:
	-	`sha256:7c0dab7cdf0512a3a977dd091768717ab11e9cdca91b62d0a313f4490c320bef`  
		Last Modified: Wed, 08 Oct 2025 19:12:44 GMT  
		Size: 61.1 MB (61107540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d2f51a619da30ad912c6bbb097d32967ac505ca681b3601f9bf29d84cc6d2e`  
		Last Modified: Wed, 08 Oct 2025 19:12:45 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251008` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:06065c64b8e595d5b78f572557d6f75dc8fe576e54e534fe2f52cebaad943200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.9 MB (675923580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7285b837f4560f666ae820511ff43e7f1d1f8016c37231ac0367808745ac6795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d651204e7bc58b37300bbab21f73f236a51404f345826c35f316f123759a161`  
		Last Modified: Wed, 08 Oct 2025 19:13:26 GMT  
		Size: 254.2 MB (254201440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918e6295f8606365365bee8b463266bce265c0ba8a6a5dd04df734778d0aea86`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 14.3 MB (14319927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2534b9daae049396ef8891934b4fc188f51fb30a2f46ba37a2e808dff3140ac`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 480.0 KB (480035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79eaaef1b45cf1c0a2bc8447e115011caf744ad64c5b3894d62491f8023a9e5`  
		Last Modified: Wed, 08 Oct 2025 19:13:12 GMT  
		Size: 378.1 MB (378058163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d9f91f519152d3c576d739a32410e6c09f298425cd998bf13ccc9c7ff17c3d`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bbc4edbd9ffd36387471049196e7cf6771617e397a6945ade8025b133b76d3`  
		Last Modified: Wed, 08 Oct 2025 18:16:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375d8d6e8e9a6f34faa33ae3df77e99711ce19d3cd3f26962f089af19002cd35`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303b18df3290f0357911474141f1b34c7b4d0843ffe04fd80ce47555c9c63fa8`  
		Last Modified: Wed, 08 Oct 2025 18:16:37 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:180d82d2459b7475a86d8ca1a155ae79cab139adf71c4fa1efc94f6ec7bba05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61141809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17543938e5d31d14472edc0e5db67913f23d408b18b1354a1142b5e2cd9335eb`

```dockerfile
```

-	Layers:
	-	`sha256:9443a615145df6dc9a9af48cffaa1b21a5b1431db51d174694677b2271f6026a`  
		Last Modified: Wed, 08 Oct 2025 19:14:43 GMT  
		Size: 61.1 MB (61114815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73a5c25612463e8efc5b1d7096f5e6f6a7feb47ff1923097c44f2bb4595d966`  
		Last Modified: Wed, 08 Oct 2025 19:14:44 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251008` - linux; ppc64le

```console
$ docker pull odoo@sha256:1c3a7c963f6d5722bff11c2a93bacc4b704da869c7cbba3148df4fcd47a400dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.1 MB (696107813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53af280ca46178706b4a6f037544ac9ccc9a49d224f500c055ee481ee2cb82f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:35:27 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:35:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:35:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:35:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:35:31 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 14:35:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=18.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=c15a8eb3791e805b9cd3078f2dd4e0d78130b1c2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
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
	-	`sha256:bbb110cafef2e34e479e4445e81e296c27a3e56de49cc58e3d7e2858ae3301bf`  
		Last Modified: Wed, 08 Oct 2025 18:26:02 GMT  
		Size: 378.7 MB (378726201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad5afc89e30eaa59f7713230a18d4bd050e806e9e2a6fb40bf51c36ead946dc`  
		Last Modified: Wed, 08 Oct 2025 18:25:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eafea179163bf763e0b7a0b85e5b3a58cda454628f4868254e7ad26490d46a6`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8add19c753a3a038caccf35842034561060df21020b1cb09be2f0bda4bdf6e1`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87eebe59846a92fe3b949d786f5fa3b1f2d7716ab3d71325543d4e52b89f310`  
		Last Modified: Wed, 08 Oct 2025 18:25:09 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:a49e998ad7f3ddd5ee06a52817869b3236ebb688b97b3e8c5f0eb6ec3fcc3b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61142820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a3157c4ef3ab53f2500f27e8a0dbb469adcc86d12288747a15a04f787de516`

```dockerfile
```

-	Layers:
	-	`sha256:08e9fff6aa5d894dab60a9df6e91a292aff021626a5c7aa6fdb6a88a2d10499c`  
		Last Modified: Wed, 08 Oct 2025 19:16:38 GMT  
		Size: 61.1 MB (61115923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d16009e4b84f210076518f74ec50d7f70ef7c10c164aa817240aa851c2748d8`  
		Last Modified: Wed, 08 Oct 2025 19:16:39 GMT  
		Size: 26.9 KB (26897 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:33f73d73e8d9e2134b83ec9c83ef01cdf9d1c9b8c69bc84c576ab00aa3fcbfe6
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
$ docker pull odoo@sha256:b60b5302e3e2a0d7f0cfb5915b7ae3b76bd6d9abf2b4846d2c2e5010195ff3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.4 MB (683428847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b033f3bd7a25d95830aa48793389fe4ab62ea5f0e33d7a255858fca2cfddbf70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a3eea6e006230ada5ebeec426ec826c0b1aad71e06109336acb5d923787a5`  
		Last Modified: Wed, 08 Oct 2025 19:10:39 GMT  
		Size: 256.9 MB (256943344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3302d20dc92cd512869453a50e89b3e488ed05dd11f771e68ff0637d56d4b0e0`  
		Last Modified: Wed, 08 Oct 2025 18:13:19 GMT  
		Size: 14.3 MB (14339416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685f0a5ed0d04161bd440dd2b45d76ace45a865364edd1d2a354bcb5556ce6fd`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711338cddad36d14da8a405f7c169a7eba3a4c9cd233ce5da792e03c53f4154`  
		Last Modified: Wed, 08 Oct 2025 19:10:30 GMT  
		Size: 381.9 MB (381940635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00064fe09e3dc6a99dbb3abfd00da5bfe441530f29161c5e344c5daca91884a`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bbaace843364f0633cfe1c6e2dcbe8e2c95556c6cabbeb1888b9adf35bad57`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70dc5d0508ff4ede51d11089eb076011e0de6b9b0b79a8339b8a91099fff27`  
		Last Modified: Wed, 08 Oct 2025 18:13:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378f984d6ce24d3c93cb5deee70211901cfab886bf4701e864edb0b94e3d0fe`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:de683f55afc19173618df15c8333abc56829afee2191a91315c4daa6d65aee1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6daf25445993dc3390336eb9e50af7880e80b941dce5bf8e03bb2f29895e456f`

```dockerfile
```

-	Layers:
	-	`sha256:cdc0cdbd68094565339eb5a9c90191f8dac81f5749b3f9847fb600046a17a205`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504d4c4fd051abe5a446fc164cafd16aa670f014fac1e9c73d72e56962c3ce2d`  
		Last Modified: Wed, 08 Oct 2025 19:13:09 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d214913f4b836246c716784ec01012dd3ab8997508ad298de0f2acc82ec7929b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.6 MB (679633443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3664ba090b04469ad279a956757ada6aade1ce3d092541617124e6dc72e5981e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac3b64ffbfbfc1806843c6148f6453344ceac916093549ce773dff1d4c7519`  
		Last Modified: Wed, 08 Oct 2025 19:11:34 GMT  
		Size: 254.2 MB (254201087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b23ecdd80a25fa675df60a3cf8c8f0a707b5c32682fd2058e59d0104f75f78c`  
		Last Modified: Wed, 08 Oct 2025 18:15:07 GMT  
		Size: 14.3 MB (14320015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6678bab7dcba93d84355d1a8f52a2c7e22804bc929fe971fcb3e6d2c0f7400`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 480.0 KB (480047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6158d9f1d9b9da7a98acc8f2d471f2cf017b5decc0f1ce3f16964603fcd6c858`  
		Last Modified: Wed, 08 Oct 2025 19:11:19 GMT  
		Size: 381.8 MB (381768285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326dd004839b44f7d2172c071b4cda6621609a17e9b7b3662c6833f87e105c9e`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f737a03d32da42aced13177f5593decf8f13e0cab57282098486c6910d8491`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019655a0111f53edec146a4076b52dcc043192ead392122ed5abb6da22a68782`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a8de250762a97f178f1b5c190fb35c1867b3361df68e229012f46ddb8745`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:191f60550c2a8b026d054aaa3dd5e82e7eb2a3b514e9fee4595ae9dfdc973259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d1aca8c2344e65a5d744ea7d95a503778a7da416dfccbab55ce9f58fdabfe4`

```dockerfile
```

-	Layers:
	-	`sha256:e87bc8507d439a8eda47c457b995e108fd89b5a3f56baf709bb2a7ea1f26a2d4`  
		Last Modified: Wed, 08 Oct 2025 19:14:59 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890335b4814c62f3f6123effced57d14df8c72e9de8c92a8b583c2f8be230263`  
		Last Modified: Wed, 08 Oct 2025 19:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:a3ad951a698529c2ee6d69e2372795c8444ad8296b80dc998f432102f68dd91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.9 MB (699855043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b5cdc7638c78cb1f7901e10a1482e9940ab53f0cd524af599d9a3bd82863bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:35:27 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:35:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:35:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:35:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:35:31 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 14:35:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
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
	-	`sha256:33674132ca1eaa37ad2139348ad05026b1740d0f0cba0fa9cdc050c4195e44ab`  
		Last Modified: Wed, 08 Oct 2025 18:17:43 GMT  
		Size: 382.5 MB (382473438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea24b4d099b476d2c99d52620495cad8068a3fc1282a880f3857dc5b9d3f967e`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03926c56d7966dd65dfefdaf235db740da29fda443495533787e45e2b6ea4876`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d94edf79fafff36ea3617f8039dbcaa5f9bf7a56d8bba38b0a42698455cbe2a`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7dcfd71fe4c69da1d2348c5fa8e83f6f468f06be440c66514828789a80258`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:7458741af82b1402ae1660c8e8a43dc217414fa0696c45ba7b7be60b24428007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dc37e336372149c84eab6ff193ccb6714be103dcc37209afca6d82b57a2daf`

```dockerfile
```

-	Layers:
	-	`sha256:31d3bc1e4b18f2576b94367b33fe5a5ef4eab7de45446ef1b9a53864662d8862`  
		Last Modified: Wed, 08 Oct 2025 19:17:13 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7b31e2c5b46985e55463bedafbff0493229efdb93c8c0aeea9a2b1d0261678`  
		Last Modified: Wed, 08 Oct 2025 19:17:15 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:33f73d73e8d9e2134b83ec9c83ef01cdf9d1c9b8c69bc84c576ab00aa3fcbfe6
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
$ docker pull odoo@sha256:b60b5302e3e2a0d7f0cfb5915b7ae3b76bd6d9abf2b4846d2c2e5010195ff3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.4 MB (683428847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b033f3bd7a25d95830aa48793389fe4ab62ea5f0e33d7a255858fca2cfddbf70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a3eea6e006230ada5ebeec426ec826c0b1aad71e06109336acb5d923787a5`  
		Last Modified: Wed, 08 Oct 2025 19:10:39 GMT  
		Size: 256.9 MB (256943344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3302d20dc92cd512869453a50e89b3e488ed05dd11f771e68ff0637d56d4b0e0`  
		Last Modified: Wed, 08 Oct 2025 18:13:19 GMT  
		Size: 14.3 MB (14339416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685f0a5ed0d04161bd440dd2b45d76ace45a865364edd1d2a354bcb5556ce6fd`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711338cddad36d14da8a405f7c169a7eba3a4c9cd233ce5da792e03c53f4154`  
		Last Modified: Wed, 08 Oct 2025 19:10:30 GMT  
		Size: 381.9 MB (381940635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00064fe09e3dc6a99dbb3abfd00da5bfe441530f29161c5e344c5daca91884a`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bbaace843364f0633cfe1c6e2dcbe8e2c95556c6cabbeb1888b9adf35bad57`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70dc5d0508ff4ede51d11089eb076011e0de6b9b0b79a8339b8a91099fff27`  
		Last Modified: Wed, 08 Oct 2025 18:13:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378f984d6ce24d3c93cb5deee70211901cfab886bf4701e864edb0b94e3d0fe`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:de683f55afc19173618df15c8333abc56829afee2191a91315c4daa6d65aee1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6daf25445993dc3390336eb9e50af7880e80b941dce5bf8e03bb2f29895e456f`

```dockerfile
```

-	Layers:
	-	`sha256:cdc0cdbd68094565339eb5a9c90191f8dac81f5749b3f9847fb600046a17a205`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504d4c4fd051abe5a446fc164cafd16aa670f014fac1e9c73d72e56962c3ce2d`  
		Last Modified: Wed, 08 Oct 2025 19:13:09 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d214913f4b836246c716784ec01012dd3ab8997508ad298de0f2acc82ec7929b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.6 MB (679633443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3664ba090b04469ad279a956757ada6aade1ce3d092541617124e6dc72e5981e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac3b64ffbfbfc1806843c6148f6453344ceac916093549ce773dff1d4c7519`  
		Last Modified: Wed, 08 Oct 2025 19:11:34 GMT  
		Size: 254.2 MB (254201087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b23ecdd80a25fa675df60a3cf8c8f0a707b5c32682fd2058e59d0104f75f78c`  
		Last Modified: Wed, 08 Oct 2025 18:15:07 GMT  
		Size: 14.3 MB (14320015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6678bab7dcba93d84355d1a8f52a2c7e22804bc929fe971fcb3e6d2c0f7400`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 480.0 KB (480047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6158d9f1d9b9da7a98acc8f2d471f2cf017b5decc0f1ce3f16964603fcd6c858`  
		Last Modified: Wed, 08 Oct 2025 19:11:19 GMT  
		Size: 381.8 MB (381768285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326dd004839b44f7d2172c071b4cda6621609a17e9b7b3662c6833f87e105c9e`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f737a03d32da42aced13177f5593decf8f13e0cab57282098486c6910d8491`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019655a0111f53edec146a4076b52dcc043192ead392122ed5abb6da22a68782`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a8de250762a97f178f1b5c190fb35c1867b3361df68e229012f46ddb8745`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:191f60550c2a8b026d054aaa3dd5e82e7eb2a3b514e9fee4595ae9dfdc973259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d1aca8c2344e65a5d744ea7d95a503778a7da416dfccbab55ce9f58fdabfe4`

```dockerfile
```

-	Layers:
	-	`sha256:e87bc8507d439a8eda47c457b995e108fd89b5a3f56baf709bb2a7ea1f26a2d4`  
		Last Modified: Wed, 08 Oct 2025 19:14:59 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890335b4814c62f3f6123effced57d14df8c72e9de8c92a8b583c2f8be230263`  
		Last Modified: Wed, 08 Oct 2025 19:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:a3ad951a698529c2ee6d69e2372795c8444ad8296b80dc998f432102f68dd91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.9 MB (699855043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b5cdc7638c78cb1f7901e10a1482e9940ab53f0cd524af599d9a3bd82863bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:35:27 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:35:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:35:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:35:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:35:31 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 14:35:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
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
	-	`sha256:33674132ca1eaa37ad2139348ad05026b1740d0f0cba0fa9cdc050c4195e44ab`  
		Last Modified: Wed, 08 Oct 2025 18:17:43 GMT  
		Size: 382.5 MB (382473438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea24b4d099b476d2c99d52620495cad8068a3fc1282a880f3857dc5b9d3f967e`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03926c56d7966dd65dfefdaf235db740da29fda443495533787e45e2b6ea4876`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d94edf79fafff36ea3617f8039dbcaa5f9bf7a56d8bba38b0a42698455cbe2a`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7dcfd71fe4c69da1d2348c5fa8e83f6f468f06be440c66514828789a80258`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7458741af82b1402ae1660c8e8a43dc217414fa0696c45ba7b7be60b24428007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dc37e336372149c84eab6ff193ccb6714be103dcc37209afca6d82b57a2daf`

```dockerfile
```

-	Layers:
	-	`sha256:31d3bc1e4b18f2576b94367b33fe5a5ef4eab7de45446ef1b9a53864662d8862`  
		Last Modified: Wed, 08 Oct 2025 19:17:13 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7b31e2c5b46985e55463bedafbff0493229efdb93c8c0aeea9a2b1d0261678`  
		Last Modified: Wed, 08 Oct 2025 19:17:15 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251008`

```console
$ docker pull odoo@sha256:33f73d73e8d9e2134b83ec9c83ef01cdf9d1c9b8c69bc84c576ab00aa3fcbfe6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20251008` - linux; amd64

```console
$ docker pull odoo@sha256:b60b5302e3e2a0d7f0cfb5915b7ae3b76bd6d9abf2b4846d2c2e5010195ff3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.4 MB (683428847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b033f3bd7a25d95830aa48793389fe4ab62ea5f0e33d7a255858fca2cfddbf70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a3eea6e006230ada5ebeec426ec826c0b1aad71e06109336acb5d923787a5`  
		Last Modified: Wed, 08 Oct 2025 19:10:39 GMT  
		Size: 256.9 MB (256943344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3302d20dc92cd512869453a50e89b3e488ed05dd11f771e68ff0637d56d4b0e0`  
		Last Modified: Wed, 08 Oct 2025 18:13:19 GMT  
		Size: 14.3 MB (14339416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685f0a5ed0d04161bd440dd2b45d76ace45a865364edd1d2a354bcb5556ce6fd`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711338cddad36d14da8a405f7c169a7eba3a4c9cd233ce5da792e03c53f4154`  
		Last Modified: Wed, 08 Oct 2025 19:10:30 GMT  
		Size: 381.9 MB (381940635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00064fe09e3dc6a99dbb3abfd00da5bfe441530f29161c5e344c5daca91884a`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bbaace843364f0633cfe1c6e2dcbe8e2c95556c6cabbeb1888b9adf35bad57`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70dc5d0508ff4ede51d11089eb076011e0de6b9b0b79a8339b8a91099fff27`  
		Last Modified: Wed, 08 Oct 2025 18:13:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378f984d6ce24d3c93cb5deee70211901cfab886bf4701e864edb0b94e3d0fe`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:de683f55afc19173618df15c8333abc56829afee2191a91315c4daa6d65aee1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6daf25445993dc3390336eb9e50af7880e80b941dce5bf8e03bb2f29895e456f`

```dockerfile
```

-	Layers:
	-	`sha256:cdc0cdbd68094565339eb5a9c90191f8dac81f5749b3f9847fb600046a17a205`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504d4c4fd051abe5a446fc164cafd16aa670f014fac1e9c73d72e56962c3ce2d`  
		Last Modified: Wed, 08 Oct 2025 19:13:09 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251008` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d214913f4b836246c716784ec01012dd3ab8997508ad298de0f2acc82ec7929b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.6 MB (679633443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3664ba090b04469ad279a956757ada6aade1ce3d092541617124e6dc72e5981e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac3b64ffbfbfc1806843c6148f6453344ceac916093549ce773dff1d4c7519`  
		Last Modified: Wed, 08 Oct 2025 19:11:34 GMT  
		Size: 254.2 MB (254201087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b23ecdd80a25fa675df60a3cf8c8f0a707b5c32682fd2058e59d0104f75f78c`  
		Last Modified: Wed, 08 Oct 2025 18:15:07 GMT  
		Size: 14.3 MB (14320015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6678bab7dcba93d84355d1a8f52a2c7e22804bc929fe971fcb3e6d2c0f7400`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 480.0 KB (480047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6158d9f1d9b9da7a98acc8f2d471f2cf017b5decc0f1ce3f16964603fcd6c858`  
		Last Modified: Wed, 08 Oct 2025 19:11:19 GMT  
		Size: 381.8 MB (381768285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326dd004839b44f7d2172c071b4cda6621609a17e9b7b3662c6833f87e105c9e`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f737a03d32da42aced13177f5593decf8f13e0cab57282098486c6910d8491`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019655a0111f53edec146a4076b52dcc043192ead392122ed5abb6da22a68782`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a8de250762a97f178f1b5c190fb35c1867b3361df68e229012f46ddb8745`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:191f60550c2a8b026d054aaa3dd5e82e7eb2a3b514e9fee4595ae9dfdc973259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d1aca8c2344e65a5d744ea7d95a503778a7da416dfccbab55ce9f58fdabfe4`

```dockerfile
```

-	Layers:
	-	`sha256:e87bc8507d439a8eda47c457b995e108fd89b5a3f56baf709bb2a7ea1f26a2d4`  
		Last Modified: Wed, 08 Oct 2025 19:14:59 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890335b4814c62f3f6123effced57d14df8c72e9de8c92a8b583c2f8be230263`  
		Last Modified: Wed, 08 Oct 2025 19:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251008` - linux; ppc64le

```console
$ docker pull odoo@sha256:a3ad951a698529c2ee6d69e2372795c8444ad8296b80dc998f432102f68dd91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.9 MB (699855043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b5cdc7638c78cb1f7901e10a1482e9940ab53f0cd524af599d9a3bd82863bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:35:27 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:35:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:35:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:35:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:35:31 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 14:35:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
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
	-	`sha256:33674132ca1eaa37ad2139348ad05026b1740d0f0cba0fa9cdc050c4195e44ab`  
		Last Modified: Wed, 08 Oct 2025 18:17:43 GMT  
		Size: 382.5 MB (382473438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea24b4d099b476d2c99d52620495cad8068a3fc1282a880f3857dc5b9d3f967e`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03926c56d7966dd65dfefdaf235db740da29fda443495533787e45e2b6ea4876`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d94edf79fafff36ea3617f8039dbcaa5f9bf7a56d8bba38b0a42698455cbe2a`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7dcfd71fe4c69da1d2348c5fa8e83f6f468f06be440c66514828789a80258`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251008` - unknown; unknown

```console
$ docker pull odoo@sha256:7458741af82b1402ae1660c8e8a43dc217414fa0696c45ba7b7be60b24428007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dc37e336372149c84eab6ff193ccb6714be103dcc37209afca6d82b57a2daf`

```dockerfile
```

-	Layers:
	-	`sha256:31d3bc1e4b18f2576b94367b33fe5a5ef4eab7de45446ef1b9a53864662d8862`  
		Last Modified: Wed, 08 Oct 2025 19:17:13 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7b31e2c5b46985e55463bedafbff0493229efdb93c8c0aeea9a2b1d0261678`  
		Last Modified: Wed, 08 Oct 2025 19:17:15 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:33f73d73e8d9e2134b83ec9c83ef01cdf9d1c9b8c69bc84c576ab00aa3fcbfe6
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
$ docker pull odoo@sha256:b60b5302e3e2a0d7f0cfb5915b7ae3b76bd6d9abf2b4846d2c2e5010195ff3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.4 MB (683428847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b033f3bd7a25d95830aa48793389fe4ab62ea5f0e33d7a255858fca2cfddbf70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a3eea6e006230ada5ebeec426ec826c0b1aad71e06109336acb5d923787a5`  
		Last Modified: Wed, 08 Oct 2025 19:10:39 GMT  
		Size: 256.9 MB (256943344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3302d20dc92cd512869453a50e89b3e488ed05dd11f771e68ff0637d56d4b0e0`  
		Last Modified: Wed, 08 Oct 2025 18:13:19 GMT  
		Size: 14.3 MB (14339416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685f0a5ed0d04161bd440dd2b45d76ace45a865364edd1d2a354bcb5556ce6fd`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 480.0 KB (480004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711338cddad36d14da8a405f7c169a7eba3a4c9cd233ce5da792e03c53f4154`  
		Last Modified: Wed, 08 Oct 2025 19:10:30 GMT  
		Size: 381.9 MB (381940635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00064fe09e3dc6a99dbb3abfd00da5bfe441530f29161c5e344c5daca91884a`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bbaace843364f0633cfe1c6e2dcbe8e2c95556c6cabbeb1888b9adf35bad57`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70dc5d0508ff4ede51d11089eb076011e0de6b9b0b79a8339b8a91099fff27`  
		Last Modified: Wed, 08 Oct 2025 18:13:17 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378f984d6ce24d3c93cb5deee70211901cfab886bf4701e864edb0b94e3d0fe`  
		Last Modified: Wed, 08 Oct 2025 18:13:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:de683f55afc19173618df15c8333abc56829afee2191a91315c4daa6d65aee1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6daf25445993dc3390336eb9e50af7880e80b941dce5bf8e03bb2f29895e456f`

```dockerfile
```

-	Layers:
	-	`sha256:cdc0cdbd68094565339eb5a9c90191f8dac81f5749b3f9847fb600046a17a205`  
		Last Modified: Wed, 08 Oct 2025 19:13:06 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504d4c4fd051abe5a446fc164cafd16aa670f014fac1e9c73d72e56962c3ce2d`  
		Last Modified: Wed, 08 Oct 2025 19:13:09 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d214913f4b836246c716784ec01012dd3ab8997508ad298de0f2acc82ec7929b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.6 MB (679633443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3664ba090b04469ad279a956757ada6aade1ce3d092541617124e6dc72e5981e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac3b64ffbfbfc1806843c6148f6453344ceac916093549ce773dff1d4c7519`  
		Last Modified: Wed, 08 Oct 2025 19:11:34 GMT  
		Size: 254.2 MB (254201087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b23ecdd80a25fa675df60a3cf8c8f0a707b5c32682fd2058e59d0104f75f78c`  
		Last Modified: Wed, 08 Oct 2025 18:15:07 GMT  
		Size: 14.3 MB (14320015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6678bab7dcba93d84355d1a8f52a2c7e22804bc929fe971fcb3e6d2c0f7400`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 480.0 KB (480047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6158d9f1d9b9da7a98acc8f2d471f2cf017b5decc0f1ce3f16964603fcd6c858`  
		Last Modified: Wed, 08 Oct 2025 19:11:19 GMT  
		Size: 381.8 MB (381768285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326dd004839b44f7d2172c071b4cda6621609a17e9b7b3662c6833f87e105c9e`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f737a03d32da42aced13177f5593decf8f13e0cab57282098486c6910d8491`  
		Last Modified: Wed, 08 Oct 2025 18:15:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019655a0111f53edec146a4076b52dcc043192ead392122ed5abb6da22a68782`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a8de250762a97f178f1b5c190fb35c1867b3361df68e229012f46ddb8745`  
		Last Modified: Wed, 08 Oct 2025 18:15:04 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:191f60550c2a8b026d054aaa3dd5e82e7eb2a3b514e9fee4595ae9dfdc973259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d1aca8c2344e65a5d744ea7d95a503778a7da416dfccbab55ce9f58fdabfe4`

```dockerfile
```

-	Layers:
	-	`sha256:e87bc8507d439a8eda47c457b995e108fd89b5a3f56baf709bb2a7ea1f26a2d4`  
		Last Modified: Wed, 08 Oct 2025 19:14:59 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890335b4814c62f3f6123effced57d14df8c72e9de8c92a8b583c2f8be230263`  
		Last Modified: Wed, 08 Oct 2025 19:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:a3ad951a698529c2ee6d69e2372795c8444ad8296b80dc998f432102f68dd91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.9 MB (699855043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b5cdc7638c78cb1f7901e10a1482e9940ab53f0cd524af599d9a3bd82863bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 14:35:27 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:35:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:35:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:35:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:35:31 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 14:35:31 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
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
	-	`sha256:33674132ca1eaa37ad2139348ad05026b1740d0f0cba0fa9cdc050c4195e44ab`  
		Last Modified: Wed, 08 Oct 2025 18:17:43 GMT  
		Size: 382.5 MB (382473438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea24b4d099b476d2c99d52620495cad8068a3fc1282a880f3857dc5b9d3f967e`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03926c56d7966dd65dfefdaf235db740da29fda443495533787e45e2b6ea4876`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d94edf79fafff36ea3617f8039dbcaa5f9bf7a56d8bba38b0a42698455cbe2a`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7dcfd71fe4c69da1d2348c5fa8e83f6f468f06be440c66514828789a80258`  
		Last Modified: Wed, 08 Oct 2025 18:18:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7458741af82b1402ae1660c8e8a43dc217414fa0696c45ba7b7be60b24428007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dc37e336372149c84eab6ff193ccb6714be103dcc37209afca6d82b57a2daf`

```dockerfile
```

-	Layers:
	-	`sha256:31d3bc1e4b18f2576b94367b33fe5a5ef4eab7de45446ef1b9a53864662d8862`  
		Last Modified: Wed, 08 Oct 2025 19:17:13 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b7b31e2c5b46985e55463bedafbff0493229efdb93c8c0aeea9a2b1d0261678`  
		Last Modified: Wed, 08 Oct 2025 19:17:15 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
