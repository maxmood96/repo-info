<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20251021`](#odoo170-20251021)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20251021`](#odoo180-20251021)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20251021`](#odoo190-20251021)
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

## `odoo:17.0-20251021`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:18`

```console
$ docker pull odoo@sha256:e6914fce7a9fb5d0a38f728ecac7591a2cb733c84e8303a0b94b579778e524f2
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
$ docker pull odoo@sha256:6d8df6c39ec8399cc75c97028a6562515cc6026780d660d65f571b883c75203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.3 MB (677323732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c65d64c543f7864ccb66901a993a65109ae030f1b1daf2b7ae3aab854dc340`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f7b71b8bf35181a3ac7890a266f214b9fb699381de6645548ccb6f5e6dab0`  
		Last Modified: Thu, 09 Oct 2025 22:20:33 GMT  
		Size: 254.6 MB (254558073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141dca923ff7d172c76d422216fb402e85243e899a2863e53b754d31637a8821`  
		Last Modified: Thu, 09 Oct 2025 21:25:24 GMT  
		Size: 14.4 MB (14355903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c87f7206a022aa7ff3d80600880ea5a43c45bfe77b94d940b4cac01fa0821`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 480.0 KB (479992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1734a012d948901c31c8dd0530b1790e080975291f860e5e1e7d5fc6fac510b0`  
		Last Modified: Thu, 09 Oct 2025 22:20:11 GMT  
		Size: 378.2 MB (378204183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4845817a1a12255c68c86323199d044d2bfbc757a0f5dd23de0c2ee3119b0bec`  
		Last Modified: Thu, 09 Oct 2025 21:25:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8573e1b49361151109103654b6c95f6554b59d3333fb7cbe6283801206dc314`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d806c1eb1d6a2a27baa317fd6a048d94ccc69b536e6613e27a99f859bc88c5`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8c8fbe5d477d4812590a464f582ed3c11b5ccdab218ef6120246cdc211fa9b`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:e91f9be7867f21fd718efa408e63d4449d91fd5785e3a0576d63c443c607b161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61134382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f5585a085be89f29a99b610443df23f1e7b8aeae4b82093b6849b96b06a97`

```dockerfile
```

-	Layers:
	-	`sha256:c636bcae169c71ff039f8111b4d9e0c03f770ca35de04d26d9dfee47a6473072`  
		Last Modified: Fri, 10 Oct 2025 01:13:44 GMT  
		Size: 61.1 MB (61107540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10d0e03ef29e56bc532f0be3f5bfe94bcfc5bb1afc8703bdd26fab78bff0437`  
		Last Modified: Fri, 10 Oct 2025 01:13:46 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f279c695fe8f56ba4fc733ca58b194e3ff1d02aceb239f61cb399cb0a8730ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 MB (673691799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92b2481ad6a8ee0b903575df18fe6a6a6c7ee2ec3599071112318e3f93c320f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3366b88f3cf082e238fc3b131d605b49cddc711906e92acd0008377c22141e`  
		Last Modified: Thu, 09 Oct 2025 22:20:45 GMT  
		Size: 252.0 MB (251958409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b850c75bee36e40c2707f4aeaa11521b1e94c4a3b3f90e3ffbd0d80d1170fa3`  
		Last Modified: Thu, 09 Oct 2025 21:28:06 GMT  
		Size: 14.3 MB (14333797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780b569d545a0d061b73e3d8fcdebc0f1f5aa5a6377d46c40848f0547a6001`  
		Last Modified: Thu, 09 Oct 2025 21:28:06 GMT  
		Size: 480.1 KB (480098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f8d643b702372be8c47c6d8d1ea507615ac4454ddf165c08563684a301f1a1`  
		Last Modified: Thu, 09 Oct 2025 22:21:23 GMT  
		Size: 378.1 MB (378055343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accf43597cee088d39388e4a53746843deb69a3f27ed70cfcff4a54476fbd91b`  
		Last Modified: Thu, 09 Oct 2025 21:28:05 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc03b2574c03faea344bf1712b7bf8879b67c2f5f3c0c4af147b5481a8054a`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c8f4cf0997a43c326ba185b0236291e434f00a18467fa2d00560e11662e452`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1d4e73ea50e6721c3bcc2c9b18f0bf00c477e8d99f5a884ab987e482c8cf4`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:04f7d66d311a4ecbbdfa572ede0c227a742c065443c127aedb547ce2f843fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61141809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98ae4ce74d9a45795a5d7505c42d542a0a60c9974332e0432bbb6919274855f`

```dockerfile
```

-	Layers:
	-	`sha256:60d658f9634017c64441b5a25a5891354f8383954bc39d5d90ef4ea20d7fd8d3`  
		Last Modified: Fri, 10 Oct 2025 01:15:10 GMT  
		Size: 61.1 MB (61114815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e022402c17485935698f938b680b7d8583a1b623cc1e9b32badf855f9fb5e8d6`  
		Last Modified: Fri, 10 Oct 2025 01:15:11 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:b81d47872d94ce845ec9fe7c07b0dd4fd3fcc6d22c99a3ca802301b19dbeb440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.5 MB (693474166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6037e855cdc448ae6aca66706c915d4b458c12d37bf88e5628205c1d62856ab0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
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
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e10012916edf5827ab48daa2a0e2d76ab0fe26240a6d8585f47267e43c588`  
		Last Modified: Thu, 09 Oct 2025 22:17:22 GMT  
		Size: 265.1 MB (265079703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74db884b565963874180a2af82ba963a1d4611a8402d4708c1797097b804fb90`  
		Last Modified: Thu, 09 Oct 2025 22:07:00 GMT  
		Size: 14.9 MB (14883559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d234cbf81875448957faff2c426ab594a8402e92b0fe58fd91cdc13f3593801`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 480.1 KB (480093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f658641070fa84feca054e909121219f5402334ea4425beb3e0f41575d3d53`  
		Last Modified: Fri, 10 Oct 2025 01:15:01 GMT  
		Size: 378.7 MB (378724847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d91fb2f8bee2a46fa8e97f191b628cc4dd0fd0d139761b6f4f928cc2d1fb497`  
		Last Modified: Thu, 09 Oct 2025 22:13:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e805377f4c3aef2cb06810ea7a20089de50eda0e033a8f9a03188e99d4266a`  
		Last Modified: Thu, 09 Oct 2025 22:13:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e5ec66224ce50439c06667fd7bee6a1c0788cdde5ea68cf8b5951d854118b2`  
		Last Modified: Thu, 09 Oct 2025 22:13:16 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332776b1da155a6544eceddb9c4a227e6dac0b40386edc56ead02011f39ef0a3`  
		Last Modified: Thu, 09 Oct 2025 22:13:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:f318df724a22452c4b8fc2cd5209c0be6fbcf73a3fd1f43a467ace0f029db1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61142819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69375df421e83026aba79bd57d01f9cc5316504fe4ca0d2c3a2f1dee55db367b`

```dockerfile
```

-	Layers:
	-	`sha256:3e686363380e31014be90b83fa81ac443e7c002891f653562824ba13c4bb6856`  
		Last Modified: Fri, 10 Oct 2025 01:16:33 GMT  
		Size: 61.1 MB (61115923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a953dd29cdd2552fe4560a9c1533b8743599ece5b2625c0f11d0fec58c6dd1`  
		Last Modified: Fri, 10 Oct 2025 01:16:34 GMT  
		Size: 26.9 KB (26896 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:e6914fce7a9fb5d0a38f728ecac7591a2cb733c84e8303a0b94b579778e524f2
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
$ docker pull odoo@sha256:6d8df6c39ec8399cc75c97028a6562515cc6026780d660d65f571b883c75203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.3 MB (677323732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c65d64c543f7864ccb66901a993a65109ae030f1b1daf2b7ae3aab854dc340`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f7b71b8bf35181a3ac7890a266f214b9fb699381de6645548ccb6f5e6dab0`  
		Last Modified: Thu, 09 Oct 2025 22:20:33 GMT  
		Size: 254.6 MB (254558073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141dca923ff7d172c76d422216fb402e85243e899a2863e53b754d31637a8821`  
		Last Modified: Thu, 09 Oct 2025 21:25:24 GMT  
		Size: 14.4 MB (14355903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c87f7206a022aa7ff3d80600880ea5a43c45bfe77b94d940b4cac01fa0821`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 480.0 KB (479992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1734a012d948901c31c8dd0530b1790e080975291f860e5e1e7d5fc6fac510b0`  
		Last Modified: Thu, 09 Oct 2025 22:20:11 GMT  
		Size: 378.2 MB (378204183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4845817a1a12255c68c86323199d044d2bfbc757a0f5dd23de0c2ee3119b0bec`  
		Last Modified: Thu, 09 Oct 2025 21:25:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8573e1b49361151109103654b6c95f6554b59d3333fb7cbe6283801206dc314`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d806c1eb1d6a2a27baa317fd6a048d94ccc69b536e6613e27a99f859bc88c5`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8c8fbe5d477d4812590a464f582ed3c11b5ccdab218ef6120246cdc211fa9b`  
		Last Modified: Thu, 09 Oct 2025 21:25:23 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e91f9be7867f21fd718efa408e63d4449d91fd5785e3a0576d63c443c607b161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61134382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f5585a085be89f29a99b610443df23f1e7b8aeae4b82093b6849b96b06a97`

```dockerfile
```

-	Layers:
	-	`sha256:c636bcae169c71ff039f8111b4d9e0c03f770ca35de04d26d9dfee47a6473072`  
		Last Modified: Fri, 10 Oct 2025 01:13:44 GMT  
		Size: 61.1 MB (61107540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10d0e03ef29e56bc532f0be3f5bfe94bcfc5bb1afc8703bdd26fab78bff0437`  
		Last Modified: Fri, 10 Oct 2025 01:13:46 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f279c695fe8f56ba4fc733ca58b194e3ff1d02aceb239f61cb399cb0a8730ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 MB (673691799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92b2481ad6a8ee0b903575df18fe6a6a6c7ee2ec3599071112318e3f93c320f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3366b88f3cf082e238fc3b131d605b49cddc711906e92acd0008377c22141e`  
		Last Modified: Thu, 09 Oct 2025 22:20:45 GMT  
		Size: 252.0 MB (251958409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b850c75bee36e40c2707f4aeaa11521b1e94c4a3b3f90e3ffbd0d80d1170fa3`  
		Last Modified: Thu, 09 Oct 2025 21:28:06 GMT  
		Size: 14.3 MB (14333797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23780b569d545a0d061b73e3d8fcdebc0f1f5aa5a6377d46c40848f0547a6001`  
		Last Modified: Thu, 09 Oct 2025 21:28:06 GMT  
		Size: 480.1 KB (480098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f8d643b702372be8c47c6d8d1ea507615ac4454ddf165c08563684a301f1a1`  
		Last Modified: Thu, 09 Oct 2025 22:21:23 GMT  
		Size: 378.1 MB (378055343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accf43597cee088d39388e4a53746843deb69a3f27ed70cfcff4a54476fbd91b`  
		Last Modified: Thu, 09 Oct 2025 21:28:05 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fc03b2574c03faea344bf1712b7bf8879b67c2f5f3c0c4af147b5481a8054a`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c8f4cf0997a43c326ba185b0236291e434f00a18467fa2d00560e11662e452`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1d4e73ea50e6721c3bcc2c9b18f0bf00c477e8d99f5a884ab987e482c8cf4`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:04f7d66d311a4ecbbdfa572ede0c227a742c065443c127aedb547ce2f843fe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61141809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98ae4ce74d9a45795a5d7505c42d542a0a60c9974332e0432bbb6919274855f`

```dockerfile
```

-	Layers:
	-	`sha256:60d658f9634017c64441b5a25a5891354f8383954bc39d5d90ef4ea20d7fd8d3`  
		Last Modified: Fri, 10 Oct 2025 01:15:10 GMT  
		Size: 61.1 MB (61114815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e022402c17485935698f938b680b7d8583a1b623cc1e9b32badf855f9fb5e8d6`  
		Last Modified: Fri, 10 Oct 2025 01:15:11 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b81d47872d94ce845ec9fe7c07b0dd4fd3fcc6d22c99a3ca802301b19dbeb440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.5 MB (693474166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6037e855cdc448ae6aca66706c915d4b458c12d37bf88e5628205c1d62856ab0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
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
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e10012916edf5827ab48daa2a0e2d76ab0fe26240a6d8585f47267e43c588`  
		Last Modified: Thu, 09 Oct 2025 22:17:22 GMT  
		Size: 265.1 MB (265079703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74db884b565963874180a2af82ba963a1d4611a8402d4708c1797097b804fb90`  
		Last Modified: Thu, 09 Oct 2025 22:07:00 GMT  
		Size: 14.9 MB (14883559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d234cbf81875448957faff2c426ab594a8402e92b0fe58fd91cdc13f3593801`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 480.1 KB (480093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f658641070fa84feca054e909121219f5402334ea4425beb3e0f41575d3d53`  
		Last Modified: Fri, 10 Oct 2025 01:15:01 GMT  
		Size: 378.7 MB (378724847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d91fb2f8bee2a46fa8e97f191b628cc4dd0fd0d139761b6f4f928cc2d1fb497`  
		Last Modified: Thu, 09 Oct 2025 22:13:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e805377f4c3aef2cb06810ea7a20089de50eda0e033a8f9a03188e99d4266a`  
		Last Modified: Thu, 09 Oct 2025 22:13:17 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e5ec66224ce50439c06667fd7bee6a1c0788cdde5ea68cf8b5951d854118b2`  
		Last Modified: Thu, 09 Oct 2025 22:13:16 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332776b1da155a6544eceddb9c4a227e6dac0b40386edc56ead02011f39ef0a3`  
		Last Modified: Thu, 09 Oct 2025 22:13:16 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f318df724a22452c4b8fc2cd5209c0be6fbcf73a3fd1f43a467ace0f029db1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61142819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69375df421e83026aba79bd57d01f9cc5316504fe4ca0d2c3a2f1dee55db367b`

```dockerfile
```

-	Layers:
	-	`sha256:3e686363380e31014be90b83fa81ac443e7c002891f653562824ba13c4bb6856`  
		Last Modified: Fri, 10 Oct 2025 01:16:33 GMT  
		Size: 61.1 MB (61115923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a953dd29cdd2552fe4560a9c1533b8743599ece5b2625c0f11d0fec58c6dd1`  
		Last Modified: Fri, 10 Oct 2025 01:16:34 GMT  
		Size: 26.9 KB (26896 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251021`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:19`

```console
$ docker pull odoo@sha256:8d5ac4da0713865f9222230e0ec5e4b12131d02e3e677fbdd4586cf234c34d01
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
$ docker pull odoo@sha256:0816eccd81dcdfe7405c60ac3a8d7c18c5e362e3c03fe2794a8bc729c3824214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.1 MB (681052716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d5400790ca4dc2768ca19767c1adb74583ce81fc042fbcd66dd138f17cc974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a8ac81d94bde42e34ee4a1130b2d11c24abbfa8b9605d22775918c6a598744`  
		Last Modified: Fri, 10 Oct 2025 01:15:11 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fc2b39f87bfe22f66a47e2328b2e4265ff3e40f696e6ae1424fbebda91b07`  
		Last Modified: Fri, 10 Oct 2025 01:14:06 GMT  
		Size: 14.4 MB (14355897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad9ac3bf579d5c2297c991a1e690f0f0ad1d5f3104a4bf4ee73baa054d1382`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 480.0 KB (479990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a7cd7ddee95c71dcd500777eef020995eb4b373eb7b04f5d4d4bb9e263d426`  
		Last Modified: Fri, 10 Oct 2025 01:15:12 GMT  
		Size: 381.9 MB (381933305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0355a58aeb025d119b15445efab770268251b578622ce9294cddfe950ba41869`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5301470dc69464f9afb9844c2fbb49e4370ae1d66fab0dcf1e63ed263789e392`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7abbfab2606c7af4b42e281ba61f60b62dcd34c3309d588d80cd0d4b3973f7`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad329fad58aa2e2692a11cf1bba26f8ab8f8f05b84167a182e15b6d9d61efd32`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:c415a7fecfac8daa80333c16efd1960e6e90906e3c4565e1a5b712764db4ecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f28280c8c5565a21014036141c8bc29cecf5b45123df9c0cdee6506e0335d1`

```dockerfile
```

-	Layers:
	-	`sha256:72ec2abc6044ddcd5521c8009e9019e2201fa200e4793f7485ba5b3dae97a1c2`  
		Last Modified: Fri, 10 Oct 2025 01:14:01 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e73e617b7fc33a594fb000513cc4dcef01e6b76392acd882f5ff7cda491a02d`  
		Last Modified: Fri, 10 Oct 2025 01:14:03 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b4b519f42e4927dda2d754119b4f5bd07cac6638598d3075bf3fd794a79665f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.4 MB (677409644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbfa59155bb08c7537622ba80e57d850d0348f8c323a3ea8fe8c3aef21f76e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82e287495a5e85388b5a079cb0e406289ae6a33708551e3b963ae2eb7ffa9c9`  
		Last Modified: Fri, 10 Oct 2025 01:15:32 GMT  
		Size: 252.0 MB (251958001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258c4350f5ef1026c617ae2e603af78d4e33a59947ea48449143946d8bd2b5e4`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 14.3 MB (14333882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537148a17c731e0dd2d7c24e29bfa1e5df2a03f74f8aac9e885e7fa85c6e7e3c`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1da89032b23008d59f199d69cb70314369df7ef88560915eefaad179e3434`  
		Last Modified: Fri, 10 Oct 2025 01:15:22 GMT  
		Size: 381.8 MB (381773599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a000f0e70bced001eff4997d1ab0d2cdc02b98644f59dde2d2d1773e8e25b7`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999afe814c933091c329d7aa0815b31021d2f12b655df05b50ea3705128bcce9`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ed884d8f9d697cf1444db8850f58087fff1f28c1498c030c9ee0b75d7c6094`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55b995bb519239ac851d2654d311c332345bf8f7ffcc217d2484311f153e7b0`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:cbee11f44e30d09ad7816c526aa35c149b15a7024f277688387346b324e821d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527ede488d6e501fb22bdf921773746c5ba8f4dac372ec46aeb130d2dda1ef`

```dockerfile
```

-	Layers:
	-	`sha256:49e52d9aacbaad5b4cabbf12e099f240e5a83ab730452f9e3e1920a3e2cbd09e`  
		Last Modified: Fri, 10 Oct 2025 01:16:08 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab67edb7216439a7a6cf8eb6c95131a89369b51f4d15d744075839c22d2c33f`  
		Last Modified: Fri, 10 Oct 2025 01:16:12 GMT  
		Size: 27.3 KB (27298 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:1c4f621bc44fdbd4f89388fa2f30d7151ca86f5fc7dce249350a94811e8d9ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697223179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b977193a3433b32ba06a0c746da4d9abaf319965f6494cb70bcb56741227b0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
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
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e10012916edf5827ab48daa2a0e2d76ab0fe26240a6d8585f47267e43c588`  
		Last Modified: Thu, 09 Oct 2025 22:17:22 GMT  
		Size: 265.1 MB (265079703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74db884b565963874180a2af82ba963a1d4611a8402d4708c1797097b804fb90`  
		Last Modified: Thu, 09 Oct 2025 22:07:00 GMT  
		Size: 14.9 MB (14883559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d234cbf81875448957faff2c426ab594a8402e92b0fe58fd91cdc13f3593801`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 480.1 KB (480093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3865409814e38a7bd75e01d1dc1a0179cfaf8c3af6769b43d5f1f67f827088`  
		Last Modified: Thu, 09 Oct 2025 22:15:25 GMT  
		Size: 382.5 MB (382473853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f196f1ef328e58674d9e2c9278684874b3eafafffd083c2c04330e5ee1d60`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d709655517db715241f0b007b26c4e62c8e7ec2a719957e658bb0dc7b26d0`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01361e855b34f7e471f7e38049e551d2cfc872314c3ab252bb2e066da53cee18`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a9c37dd7fc840c7e268533c5f4d7cc708c0067e294a6b1d925cb021f0b841`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:2ad0f9da585335b978ddcd7c543d1b841bd576d7ef68bb279d4de438c946fba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165efa7311b385e3fcfe40acb7870d32cb2b59376dcaef61327aadd915ec0e45`

```dockerfile
```

-	Layers:
	-	`sha256:445ed5d82e3a44a48d7a5f5897d4a518d6e8952553f3f17610bc2d0f61a2f927`  
		Last Modified: Fri, 10 Oct 2025 01:18:16 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629eecb262c7a3bd0e31834d20806b749d7bb3e75f74c446fa58d4ee7b307aa0`  
		Last Modified: Fri, 10 Oct 2025 01:18:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:8d5ac4da0713865f9222230e0ec5e4b12131d02e3e677fbdd4586cf234c34d01
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
$ docker pull odoo@sha256:0816eccd81dcdfe7405c60ac3a8d7c18c5e362e3c03fe2794a8bc729c3824214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.1 MB (681052716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d5400790ca4dc2768ca19767c1adb74583ce81fc042fbcd66dd138f17cc974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a8ac81d94bde42e34ee4a1130b2d11c24abbfa8b9605d22775918c6a598744`  
		Last Modified: Fri, 10 Oct 2025 01:15:11 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fc2b39f87bfe22f66a47e2328b2e4265ff3e40f696e6ae1424fbebda91b07`  
		Last Modified: Fri, 10 Oct 2025 01:14:06 GMT  
		Size: 14.4 MB (14355897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad9ac3bf579d5c2297c991a1e690f0f0ad1d5f3104a4bf4ee73baa054d1382`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 480.0 KB (479990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a7cd7ddee95c71dcd500777eef020995eb4b373eb7b04f5d4d4bb9e263d426`  
		Last Modified: Fri, 10 Oct 2025 01:15:12 GMT  
		Size: 381.9 MB (381933305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0355a58aeb025d119b15445efab770268251b578622ce9294cddfe950ba41869`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5301470dc69464f9afb9844c2fbb49e4370ae1d66fab0dcf1e63ed263789e392`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7abbfab2606c7af4b42e281ba61f60b62dcd34c3309d588d80cd0d4b3973f7`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad329fad58aa2e2692a11cf1bba26f8ab8f8f05b84167a182e15b6d9d61efd32`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c415a7fecfac8daa80333c16efd1960e6e90906e3c4565e1a5b712764db4ecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f28280c8c5565a21014036141c8bc29cecf5b45123df9c0cdee6506e0335d1`

```dockerfile
```

-	Layers:
	-	`sha256:72ec2abc6044ddcd5521c8009e9019e2201fa200e4793f7485ba5b3dae97a1c2`  
		Last Modified: Fri, 10 Oct 2025 01:14:01 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e73e617b7fc33a594fb000513cc4dcef01e6b76392acd882f5ff7cda491a02d`  
		Last Modified: Fri, 10 Oct 2025 01:14:03 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b4b519f42e4927dda2d754119b4f5bd07cac6638598d3075bf3fd794a79665f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.4 MB (677409644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbfa59155bb08c7537622ba80e57d850d0348f8c323a3ea8fe8c3aef21f76e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82e287495a5e85388b5a079cb0e406289ae6a33708551e3b963ae2eb7ffa9c9`  
		Last Modified: Fri, 10 Oct 2025 01:15:32 GMT  
		Size: 252.0 MB (251958001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258c4350f5ef1026c617ae2e603af78d4e33a59947ea48449143946d8bd2b5e4`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 14.3 MB (14333882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537148a17c731e0dd2d7c24e29bfa1e5df2a03f74f8aac9e885e7fa85c6e7e3c`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1da89032b23008d59f199d69cb70314369df7ef88560915eefaad179e3434`  
		Last Modified: Fri, 10 Oct 2025 01:15:22 GMT  
		Size: 381.8 MB (381773599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a000f0e70bced001eff4997d1ab0d2cdc02b98644f59dde2d2d1773e8e25b7`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999afe814c933091c329d7aa0815b31021d2f12b655df05b50ea3705128bcce9`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ed884d8f9d697cf1444db8850f58087fff1f28c1498c030c9ee0b75d7c6094`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55b995bb519239ac851d2654d311c332345bf8f7ffcc217d2484311f153e7b0`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cbee11f44e30d09ad7816c526aa35c149b15a7024f277688387346b324e821d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527ede488d6e501fb22bdf921773746c5ba8f4dac372ec46aeb130d2dda1ef`

```dockerfile
```

-	Layers:
	-	`sha256:49e52d9aacbaad5b4cabbf12e099f240e5a83ab730452f9e3e1920a3e2cbd09e`  
		Last Modified: Fri, 10 Oct 2025 01:16:08 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab67edb7216439a7a6cf8eb6c95131a89369b51f4d15d744075839c22d2c33f`  
		Last Modified: Fri, 10 Oct 2025 01:16:12 GMT  
		Size: 27.3 KB (27298 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1c4f621bc44fdbd4f89388fa2f30d7151ca86f5fc7dce249350a94811e8d9ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697223179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b977193a3433b32ba06a0c746da4d9abaf319965f6494cb70bcb56741227b0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
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
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e10012916edf5827ab48daa2a0e2d76ab0fe26240a6d8585f47267e43c588`  
		Last Modified: Thu, 09 Oct 2025 22:17:22 GMT  
		Size: 265.1 MB (265079703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74db884b565963874180a2af82ba963a1d4611a8402d4708c1797097b804fb90`  
		Last Modified: Thu, 09 Oct 2025 22:07:00 GMT  
		Size: 14.9 MB (14883559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d234cbf81875448957faff2c426ab594a8402e92b0fe58fd91cdc13f3593801`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 480.1 KB (480093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3865409814e38a7bd75e01d1dc1a0179cfaf8c3af6769b43d5f1f67f827088`  
		Last Modified: Thu, 09 Oct 2025 22:15:25 GMT  
		Size: 382.5 MB (382473853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f196f1ef328e58674d9e2c9278684874b3eafafffd083c2c04330e5ee1d60`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d709655517db715241f0b007b26c4e62c8e7ec2a719957e658bb0dc7b26d0`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01361e855b34f7e471f7e38049e551d2cfc872314c3ab252bb2e066da53cee18`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a9c37dd7fc840c7e268533c5f4d7cc708c0067e294a6b1d925cb021f0b841`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2ad0f9da585335b978ddcd7c543d1b841bd576d7ef68bb279d4de438c946fba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165efa7311b385e3fcfe40acb7870d32cb2b59376dcaef61327aadd915ec0e45`

```dockerfile
```

-	Layers:
	-	`sha256:445ed5d82e3a44a48d7a5f5897d4a518d6e8952553f3f17610bc2d0f61a2f927`  
		Last Modified: Fri, 10 Oct 2025 01:18:16 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629eecb262c7a3bd0e31834d20806b749d7bb3e75f74c446fa58d4ee7b307aa0`  
		Last Modified: Fri, 10 Oct 2025 01:18:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251021`

```console
$ docker pull odoo@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `odoo:latest`

```console
$ docker pull odoo@sha256:8d5ac4da0713865f9222230e0ec5e4b12131d02e3e677fbdd4586cf234c34d01
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
$ docker pull odoo@sha256:0816eccd81dcdfe7405c60ac3a8d7c18c5e362e3c03fe2794a8bc729c3824214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.1 MB (681052716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d5400790ca4dc2768ca19767c1adb74583ce81fc042fbcd66dd138f17cc974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a8ac81d94bde42e34ee4a1130b2d11c24abbfa8b9605d22775918c6a598744`  
		Last Modified: Fri, 10 Oct 2025 01:15:11 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fc2b39f87bfe22f66a47e2328b2e4265ff3e40f696e6ae1424fbebda91b07`  
		Last Modified: Fri, 10 Oct 2025 01:14:06 GMT  
		Size: 14.4 MB (14355897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad9ac3bf579d5c2297c991a1e690f0f0ad1d5f3104a4bf4ee73baa054d1382`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 480.0 KB (479990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a7cd7ddee95c71dcd500777eef020995eb4b373eb7b04f5d4d4bb9e263d426`  
		Last Modified: Fri, 10 Oct 2025 01:15:12 GMT  
		Size: 381.9 MB (381933305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0355a58aeb025d119b15445efab770268251b578622ce9294cddfe950ba41869`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5301470dc69464f9afb9844c2fbb49e4370ae1d66fab0dcf1e63ed263789e392`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7abbfab2606c7af4b42e281ba61f60b62dcd34c3309d588d80cd0d4b3973f7`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad329fad58aa2e2692a11cf1bba26f8ab8f8f05b84167a182e15b6d9d61efd32`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c415a7fecfac8daa80333c16efd1960e6e90906e3c4565e1a5b712764db4ecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f28280c8c5565a21014036141c8bc29cecf5b45123df9c0cdee6506e0335d1`

```dockerfile
```

-	Layers:
	-	`sha256:72ec2abc6044ddcd5521c8009e9019e2201fa200e4793f7485ba5b3dae97a1c2`  
		Last Modified: Fri, 10 Oct 2025 01:14:01 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e73e617b7fc33a594fb000513cc4dcef01e6b76392acd882f5ff7cda491a02d`  
		Last Modified: Fri, 10 Oct 2025 01:14:03 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b4b519f42e4927dda2d754119b4f5bd07cac6638598d3075bf3fd794a79665f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.4 MB (677409644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbfa59155bb08c7537622ba80e57d850d0348f8c323a3ea8fe8c3aef21f76e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82e287495a5e85388b5a079cb0e406289ae6a33708551e3b963ae2eb7ffa9c9`  
		Last Modified: Fri, 10 Oct 2025 01:15:32 GMT  
		Size: 252.0 MB (251958001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258c4350f5ef1026c617ae2e603af78d4e33a59947ea48449143946d8bd2b5e4`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 14.3 MB (14333882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537148a17c731e0dd2d7c24e29bfa1e5df2a03f74f8aac9e885e7fa85c6e7e3c`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1da89032b23008d59f199d69cb70314369df7ef88560915eefaad179e3434`  
		Last Modified: Fri, 10 Oct 2025 01:15:22 GMT  
		Size: 381.8 MB (381773599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a000f0e70bced001eff4997d1ab0d2cdc02b98644f59dde2d2d1773e8e25b7`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999afe814c933091c329d7aa0815b31021d2f12b655df05b50ea3705128bcce9`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ed884d8f9d697cf1444db8850f58087fff1f28c1498c030c9ee0b75d7c6094`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55b995bb519239ac851d2654d311c332345bf8f7ffcc217d2484311f153e7b0`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cbee11f44e30d09ad7816c526aa35c149b15a7024f277688387346b324e821d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527ede488d6e501fb22bdf921773746c5ba8f4dac372ec46aeb130d2dda1ef`

```dockerfile
```

-	Layers:
	-	`sha256:49e52d9aacbaad5b4cabbf12e099f240e5a83ab730452f9e3e1920a3e2cbd09e`  
		Last Modified: Fri, 10 Oct 2025 01:16:08 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab67edb7216439a7a6cf8eb6c95131a89369b51f4d15d744075839c22d2c33f`  
		Last Modified: Fri, 10 Oct 2025 01:16:12 GMT  
		Size: 27.3 KB (27298 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:1c4f621bc44fdbd4f89388fa2f30d7151ca86f5fc7dce249350a94811e8d9ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697223179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b977193a3433b32ba06a0c746da4d9abaf319965f6494cb70bcb56741227b0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
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
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e10012916edf5827ab48daa2a0e2d76ab0fe26240a6d8585f47267e43c588`  
		Last Modified: Thu, 09 Oct 2025 22:17:22 GMT  
		Size: 265.1 MB (265079703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74db884b565963874180a2af82ba963a1d4611a8402d4708c1797097b804fb90`  
		Last Modified: Thu, 09 Oct 2025 22:07:00 GMT  
		Size: 14.9 MB (14883559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d234cbf81875448957faff2c426ab594a8402e92b0fe58fd91cdc13f3593801`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 480.1 KB (480093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3865409814e38a7bd75e01d1dc1a0179cfaf8c3af6769b43d5f1f67f827088`  
		Last Modified: Thu, 09 Oct 2025 22:15:25 GMT  
		Size: 382.5 MB (382473853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f196f1ef328e58674d9e2c9278684874b3eafafffd083c2c04330e5ee1d60`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d709655517db715241f0b007b26c4e62c8e7ec2a719957e658bb0dc7b26d0`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01361e855b34f7e471f7e38049e551d2cfc872314c3ab252bb2e066da53cee18`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a9c37dd7fc840c7e268533c5f4d7cc708c0067e294a6b1d925cb021f0b841`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2ad0f9da585335b978ddcd7c543d1b841bd576d7ef68bb279d4de438c946fba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165efa7311b385e3fcfe40acb7870d32cb2b59376dcaef61327aadd915ec0e45`

```dockerfile
```

-	Layers:
	-	`sha256:445ed5d82e3a44a48d7a5f5897d4a518d6e8952553f3f17610bc2d0f61a2f927`  
		Last Modified: Fri, 10 Oct 2025 01:18:16 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629eecb262c7a3bd0e31834d20806b749d7bb3e75f74c446fa58d4ee7b307aa0`  
		Last Modified: Fri, 10 Oct 2025 01:18:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
