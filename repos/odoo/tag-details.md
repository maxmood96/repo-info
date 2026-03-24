<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260324`](#odoo170-20260324)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260324`](#odoo180-20260324)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260324`](#odoo190-20260324)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:d6d48ba40499d36bb7347e31c86eeb28589d40687b2412a3c65c51f2a5fcc6fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:10386f31e70327c59af96d7057a60b8ad3c404a21b5c55e354ab4fd03a44db2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.7 MB (610724929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec31e7a9cf2cec6663e78793d5baa16a514285c38a09c8a468b8a60324b0bb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:27:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:27:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:27:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:27:21 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:27:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:27:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:27:30 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:27:30 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Mar 2026 18:27:30 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:27:30 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Tue, 24 Mar 2026 18:28:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:28:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:28:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:28:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
USER odoo
# Tue, 24 Mar 2026 18:28:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:28:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e36658cdfe0051611fc272bc877c4013241071a205ed4596f0e649d56e4c8e5`  
		Last Modified: Tue, 24 Mar 2026 18:29:59 GMT  
		Size: 235.0 MB (234961488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fc2b1636b2c8d131611df60caae5d962957821ed1aa1aad61f48b87b2663a5`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 2.6 MB (2603924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c796ffd41b7eb31f3b340f040283b52acd857235a92b977a4873b06e1b9469d1`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 479.9 KB (479888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f80d5e118a52779b616228de3be31786a87899c67afd9ea5ec003d2479261d`  
		Last Modified: Tue, 24 Mar 2026 18:30:01 GMT  
		Size: 343.1 MB (343138669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a936ed3815f8482b3e471d1bc83745fdc21c292995f05f635052bf9baf6489d`  
		Last Modified: Tue, 24 Mar 2026 18:29:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b8243757e377d9b0f91ddab5055579636b655830bd0670aa0dd17326313910`  
		Last Modified: Tue, 24 Mar 2026 18:29:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a70b234a45164400da23ff74d78fa19076819c8884f79bab7825e200006ebd1`  
		Last Modified: Tue, 24 Mar 2026 18:29:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392d3e8d6cb8499d991d3b6d95c58bb6163e726fc32ea59c2b15a68274d26604`  
		Last Modified: Tue, 24 Mar 2026 18:29:54 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:5d37c9607288d9fb77dc8d0d491a17f5fd3dc6c856c14fb56197b0c0fc13672d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42890756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6b64c0edd0aab6aaa31e280857a2aaeb1f9a690b4b8f30352d82f292372e73`

```dockerfile
```

-	Layers:
	-	`sha256:e620aafdcad7c2a805fdaa2134be707d5b693c8f1af33f470e125113641b8826`  
		Last Modified: Tue, 24 Mar 2026 18:29:53 GMT  
		Size: 42.9 MB (42863964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59744a01d9dfee0dbfd23382afda16c36ca515f0e9294dc19da9b4229f082d9`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e209aabca20ace01bc4470b3858697a047987bab3418da03d3eaac460e196d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.5 MB (605513342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bd16ee3c1f2c84d277b1efefecd2809e6c14e92b0ce56ecffccbe34c43d8fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:27:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:27:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:27:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:27:37 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:27:37 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:27:46 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:27:47 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:27:47 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Mar 2026 18:27:47 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:27:47 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Tue, 24 Mar 2026 18:28:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:28:52 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:28:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:28:52 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
USER odoo
# Tue, 24 Mar 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:28:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8d72765b7e58185ce48abeed1c1e38b4e6d1e41d3259c185e97fd38df2f852`  
		Last Modified: Tue, 24 Mar 2026 18:30:17 GMT  
		Size: 232.3 MB (232296099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72363ded07770dbb9a5aab2a66ecddb47e1e05aec0e70a5b655963a8a578a7f5`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 2.6 MB (2598361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3981c188163e2fc662af77293a2cb90974a2d1bb2c657386245efc1e06c352`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 479.9 KB (479942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19784071f4975af1eaa43c9acc14603f572d384d8f5872f2b8406204f24c853`  
		Last Modified: Tue, 24 Mar 2026 18:30:18 GMT  
		Size: 342.7 MB (342747476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8357cad67755be054b8fd367633cdfa11c3ac5d82829b410cd1c8b9bb011f`  
		Last Modified: Tue, 24 Mar 2026 18:30:09 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db326f47651381cb052fdeddc298a99ae643d37b0f2969e6431fff1508193e7b`  
		Last Modified: Tue, 24 Mar 2026 18:30:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73acafd96e8d54ee127296d6dd01066ba620a091d08c4205452ed9262c0b3256`  
		Last Modified: Tue, 24 Mar 2026 18:30:11 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b386355847cbb52a78f235a54a91238f2a2f009dc4fbc4d2c61ec529d8f933`  
		Last Modified: Tue, 24 Mar 2026 18:30:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b87542e4d0678c43a810a0d65333a60c773de5ac8f983536b607582885f84919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42897415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeff613b9954d199ff22cee26e22a226d503d9009d16d6702b16c4599109de35`

```dockerfile
```

-	Layers:
	-	`sha256:3cd22193a340612bb7a7a616aa55b78c196e2eab869ae5f611d9737096018a35`  
		Last Modified: Tue, 24 Mar 2026 18:30:10 GMT  
		Size: 42.9 MB (42870471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aafa7dcdd81ef2865749130bfbb7a55b124889176f47984ffda16bd395f20b4`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:d6d48ba40499d36bb7347e31c86eeb28589d40687b2412a3c65c51f2a5fcc6fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:10386f31e70327c59af96d7057a60b8ad3c404a21b5c55e354ab4fd03a44db2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.7 MB (610724929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec31e7a9cf2cec6663e78793d5baa16a514285c38a09c8a468b8a60324b0bb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:27:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:27:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:27:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:27:21 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:27:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:27:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:27:30 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:27:30 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Mar 2026 18:27:30 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:27:30 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Tue, 24 Mar 2026 18:28:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:28:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:28:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:28:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
USER odoo
# Tue, 24 Mar 2026 18:28:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:28:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e36658cdfe0051611fc272bc877c4013241071a205ed4596f0e649d56e4c8e5`  
		Last Modified: Tue, 24 Mar 2026 18:29:59 GMT  
		Size: 235.0 MB (234961488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fc2b1636b2c8d131611df60caae5d962957821ed1aa1aad61f48b87b2663a5`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 2.6 MB (2603924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c796ffd41b7eb31f3b340f040283b52acd857235a92b977a4873b06e1b9469d1`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 479.9 KB (479888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f80d5e118a52779b616228de3be31786a87899c67afd9ea5ec003d2479261d`  
		Last Modified: Tue, 24 Mar 2026 18:30:01 GMT  
		Size: 343.1 MB (343138669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a936ed3815f8482b3e471d1bc83745fdc21c292995f05f635052bf9baf6489d`  
		Last Modified: Tue, 24 Mar 2026 18:29:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b8243757e377d9b0f91ddab5055579636b655830bd0670aa0dd17326313910`  
		Last Modified: Tue, 24 Mar 2026 18:29:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a70b234a45164400da23ff74d78fa19076819c8884f79bab7825e200006ebd1`  
		Last Modified: Tue, 24 Mar 2026 18:29:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392d3e8d6cb8499d991d3b6d95c58bb6163e726fc32ea59c2b15a68274d26604`  
		Last Modified: Tue, 24 Mar 2026 18:29:54 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5d37c9607288d9fb77dc8d0d491a17f5fd3dc6c856c14fb56197b0c0fc13672d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42890756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6b64c0edd0aab6aaa31e280857a2aaeb1f9a690b4b8f30352d82f292372e73`

```dockerfile
```

-	Layers:
	-	`sha256:e620aafdcad7c2a805fdaa2134be707d5b693c8f1af33f470e125113641b8826`  
		Last Modified: Tue, 24 Mar 2026 18:29:53 GMT  
		Size: 42.9 MB (42863964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59744a01d9dfee0dbfd23382afda16c36ca515f0e9294dc19da9b4229f082d9`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e209aabca20ace01bc4470b3858697a047987bab3418da03d3eaac460e196d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.5 MB (605513342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bd16ee3c1f2c84d277b1efefecd2809e6c14e92b0ce56ecffccbe34c43d8fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:27:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:27:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:27:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:27:37 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:27:37 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:27:46 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:27:47 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:27:47 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Mar 2026 18:27:47 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:27:47 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Tue, 24 Mar 2026 18:28:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:28:52 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:28:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:28:52 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
USER odoo
# Tue, 24 Mar 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:28:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8d72765b7e58185ce48abeed1c1e38b4e6d1e41d3259c185e97fd38df2f852`  
		Last Modified: Tue, 24 Mar 2026 18:30:17 GMT  
		Size: 232.3 MB (232296099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72363ded07770dbb9a5aab2a66ecddb47e1e05aec0e70a5b655963a8a578a7f5`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 2.6 MB (2598361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3981c188163e2fc662af77293a2cb90974a2d1bb2c657386245efc1e06c352`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 479.9 KB (479942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19784071f4975af1eaa43c9acc14603f572d384d8f5872f2b8406204f24c853`  
		Last Modified: Tue, 24 Mar 2026 18:30:18 GMT  
		Size: 342.7 MB (342747476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8357cad67755be054b8fd367633cdfa11c3ac5d82829b410cd1c8b9bb011f`  
		Last Modified: Tue, 24 Mar 2026 18:30:09 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db326f47651381cb052fdeddc298a99ae643d37b0f2969e6431fff1508193e7b`  
		Last Modified: Tue, 24 Mar 2026 18:30:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73acafd96e8d54ee127296d6dd01066ba620a091d08c4205452ed9262c0b3256`  
		Last Modified: Tue, 24 Mar 2026 18:30:11 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b386355847cbb52a78f235a54a91238f2a2f009dc4fbc4d2c61ec529d8f933`  
		Last Modified: Tue, 24 Mar 2026 18:30:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b87542e4d0678c43a810a0d65333a60c773de5ac8f983536b607582885f84919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42897415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeff613b9954d199ff22cee26e22a226d503d9009d16d6702b16c4599109de35`

```dockerfile
```

-	Layers:
	-	`sha256:3cd22193a340612bb7a7a616aa55b78c196e2eab869ae5f611d9737096018a35`  
		Last Modified: Tue, 24 Mar 2026 18:30:10 GMT  
		Size: 42.9 MB (42870471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aafa7dcdd81ef2865749130bfbb7a55b124889176f47984ffda16bd395f20b4`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260324`

```console
$ docker pull odoo@sha256:d6d48ba40499d36bb7347e31c86eeb28589d40687b2412a3c65c51f2a5fcc6fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260324` - linux; amd64

```console
$ docker pull odoo@sha256:10386f31e70327c59af96d7057a60b8ad3c404a21b5c55e354ab4fd03a44db2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.7 MB (610724929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec31e7a9cf2cec6663e78793d5baa16a514285c38a09c8a468b8a60324b0bb4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:27:21 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:27:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:27:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:27:21 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:27:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:27:29 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:27:30 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:27:30 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Mar 2026 18:27:30 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:27:30 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Tue, 24 Mar 2026 18:28:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:28:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:28:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:28:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:28:34 GMT
USER odoo
# Tue, 24 Mar 2026 18:28:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:28:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e36658cdfe0051611fc272bc877c4013241071a205ed4596f0e649d56e4c8e5`  
		Last Modified: Tue, 24 Mar 2026 18:29:59 GMT  
		Size: 235.0 MB (234961488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fc2b1636b2c8d131611df60caae5d962957821ed1aa1aad61f48b87b2663a5`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 2.6 MB (2603924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c796ffd41b7eb31f3b340f040283b52acd857235a92b977a4873b06e1b9469d1`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 479.9 KB (479888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f80d5e118a52779b616228de3be31786a87899c67afd9ea5ec003d2479261d`  
		Last Modified: Tue, 24 Mar 2026 18:30:01 GMT  
		Size: 343.1 MB (343138669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a936ed3815f8482b3e471d1bc83745fdc21c292995f05f635052bf9baf6489d`  
		Last Modified: Tue, 24 Mar 2026 18:29:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b8243757e377d9b0f91ddab5055579636b655830bd0670aa0dd17326313910`  
		Last Modified: Tue, 24 Mar 2026 18:29:52 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a70b234a45164400da23ff74d78fa19076819c8884f79bab7825e200006ebd1`  
		Last Modified: Tue, 24 Mar 2026 18:29:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392d3e8d6cb8499d991d3b6d95c58bb6163e726fc32ea59c2b15a68274d26604`  
		Last Modified: Tue, 24 Mar 2026 18:29:54 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:5d37c9607288d9fb77dc8d0d491a17f5fd3dc6c856c14fb56197b0c0fc13672d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42890756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6b64c0edd0aab6aaa31e280857a2aaeb1f9a690b4b8f30352d82f292372e73`

```dockerfile
```

-	Layers:
	-	`sha256:e620aafdcad7c2a805fdaa2134be707d5b693c8f1af33f470e125113641b8826`  
		Last Modified: Tue, 24 Mar 2026 18:29:53 GMT  
		Size: 42.9 MB (42863964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59744a01d9dfee0dbfd23382afda16c36ca515f0e9294dc19da9b4229f082d9`  
		Last Modified: Tue, 24 Mar 2026 18:29:51 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260324` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e209aabca20ace01bc4470b3858697a047987bab3418da03d3eaac460e196d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.5 MB (605513342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bd16ee3c1f2c84d277b1efefecd2809e6c14e92b0ce56ecffccbe34c43d8fb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:27:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:27:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:27:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:27:37 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:27:37 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:27:46 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:27:47 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:27:47 GMT
ENV ODOO_VERSION=17.0
# Tue, 24 Mar 2026 18:27:47 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:27:47 GMT
ARG ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
# Tue, 24 Mar 2026 18:28:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=60f679f9877f71d54b2853c008923f9fd0ec99a0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:28:52 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:28:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:28:52 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:28:52 GMT
USER odoo
# Tue, 24 Mar 2026 18:28:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:28:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8d72765b7e58185ce48abeed1c1e38b4e6d1e41d3259c185e97fd38df2f852`  
		Last Modified: Tue, 24 Mar 2026 18:30:17 GMT  
		Size: 232.3 MB (232296099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72363ded07770dbb9a5aab2a66ecddb47e1e05aec0e70a5b655963a8a578a7f5`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 2.6 MB (2598361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3981c188163e2fc662af77293a2cb90974a2d1bb2c657386245efc1e06c352`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 479.9 KB (479942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19784071f4975af1eaa43c9acc14603f572d384d8f5872f2b8406204f24c853`  
		Last Modified: Tue, 24 Mar 2026 18:30:18 GMT  
		Size: 342.7 MB (342747476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8357cad67755be054b8fd367633cdfa11c3ac5d82829b410cd1c8b9bb011f`  
		Last Modified: Tue, 24 Mar 2026 18:30:09 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db326f47651381cb052fdeddc298a99ae643d37b0f2969e6431fff1508193e7b`  
		Last Modified: Tue, 24 Mar 2026 18:30:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73acafd96e8d54ee127296d6dd01066ba620a091d08c4205452ed9262c0b3256`  
		Last Modified: Tue, 24 Mar 2026 18:30:11 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b386355847cbb52a78f235a54a91238f2a2f009dc4fbc4d2c61ec529d8f933`  
		Last Modified: Tue, 24 Mar 2026 18:30:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:b87542e4d0678c43a810a0d65333a60c773de5ac8f983536b607582885f84919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42897415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeff613b9954d199ff22cee26e22a226d503d9009d16d6702b16c4599109de35`

```dockerfile
```

-	Layers:
	-	`sha256:3cd22193a340612bb7a7a616aa55b78c196e2eab869ae5f611d9737096018a35`  
		Last Modified: Tue, 24 Mar 2026 18:30:10 GMT  
		Size: 42.9 MB (42870471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aafa7dcdd81ef2865749130bfbb7a55b124889176f47984ffda16bd395f20b4`  
		Last Modified: Tue, 24 Mar 2026 18:30:08 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:c1ad8ac124214c33f5d57a957ca88cb5c3d70255132794e32b7894d063ea1449
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
$ docker pull odoo@sha256:8375d3e73746ec454fc25c202e066df700af381fea061152200ad2a003f80ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.6 MB (683605889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df276b7ba54a32fa0ce5a2cf139877b61d6ebc55c788506d7fcac82501c32778`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:35 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:35 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:22:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:22:46 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:46 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:23:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e4b72f65ec80988a958fb6237f455e6aea58603ba27f7fd3e591ea3f8695e0`  
		Last Modified: Tue, 24 Mar 2026 18:25:43 GMT  
		Size: 254.6 MB (254566357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c4c85ea8449df52beb214d6df785927a950c0d552758ed46d0b306d2b1a50`  
		Last Modified: Tue, 24 Mar 2026 18:25:34 GMT  
		Size: 14.4 MB (14359961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785da4fb759684e26550fab1e497378b1238b9c1e8993debda92e95cde008da2`  
		Last Modified: Tue, 24 Mar 2026 18:25:33 GMT  
		Size: 479.6 KB (479639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4ee431022506c6b62af299bf05da37d3a21e8d5be3bf1636a42566d4042f3`  
		Last Modified: Tue, 24 Mar 2026 18:25:46 GMT  
		Size: 384.5 MB (384465501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5108ab6399a49d651e9473504b69ede3d43243f4a72d022250d59a432692b82f`  
		Last Modified: Tue, 24 Mar 2026 18:25:34 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac3ed23c0392c9970bfe958e111eac5202903b2f40ac1831974de36551fab2`  
		Last Modified: Tue, 24 Mar 2026 18:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b017750fb448d8678c0eb33f53c2f8e4a53efe593baba1e543c2c0117def7a`  
		Last Modified: Tue, 24 Mar 2026 18:25:36 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabf624291fa40f929218bb8d9b57bbe39209b0ce5bb70440500ff6f4737f79c`  
		Last Modified: Tue, 24 Mar 2026 18:25:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1866df97b223e6a6ffc3dc29c41584b80c6a9fc549abfff4def2c1f8af686070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62159366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ab720e2c2b8a06d8a2a7f736fabdfc4325f6447b67eb2874b6f720bbb79e7e`

```dockerfile
```

-	Layers:
	-	`sha256:ea41fb4a3c5da3ed3b26c7c0d87bdcd5dc94f19c7bad682041e6570f35c1938f`  
		Last Modified: Tue, 24 Mar 2026 18:25:37 GMT  
		Size: 62.1 MB (62132567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8924bce32404e6e4ff8db0c06c60094376b258bb25254e359769980a666f89b6`  
		Last Modified: Tue, 24 Mar 2026 18:25:33 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fa32b55acdf4f0b38463d00eea62eed0ada58da62b02a9a4ace446dce3716a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.0 MB (680001554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16016f3da78d7a882ae49f8978dbf235cf36abe5a1ce4f2723c909cd83076f3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:43 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:22:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:56 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:56 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:22:56 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:56 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:23:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99f5fbeb6fee02b1893a8cc8addfb704f41b18f838b297e684c3235aed8c93`  
		Last Modified: Tue, 24 Mar 2026 18:26:16 GMT  
		Size: 252.0 MB (251995638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a50dad2c848f32e3d6cfe9144d0f950bef5986208bc93a3b7a710f04b6567b`  
		Last Modified: Tue, 24 Mar 2026 18:26:08 GMT  
		Size: 14.3 MB (14340676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ae2f00adc9c805164f4a126e61c1971a94b26c2cc01efb14b037df3cd81cd`  
		Last Modified: Tue, 24 Mar 2026 18:26:07 GMT  
		Size: 479.6 KB (479648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b50e454b4a4f3a1ea1392cf401c225565e5289f2d5d7f1b7001d16e62661b6`  
		Last Modified: Tue, 24 Mar 2026 18:26:20 GMT  
		Size: 384.3 MB (384313444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b65d1d78b247e3872cb364bd19aafa949759937662893f1f479a233f5f78c4`  
		Last Modified: Tue, 24 Mar 2026 18:26:08 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc2be3843975cda87240ce1b24dcd692cd0d6495707733bf1cc1f523f0b8965`  
		Last Modified: Tue, 24 Mar 2026 18:26:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44890499d7cb21688a136b660fbb26cb642c90e95c27a755461904c66daf13cb`  
		Last Modified: Tue, 24 Mar 2026 18:26:09 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9833564912be7c6fe8c08cd122e0a877260b838660f45135e10fbe5735510c`  
		Last Modified: Tue, 24 Mar 2026 18:26:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:f4fa47360aa86baf2261d21b1096da2a197228860e9e9e5a31e01c083da56b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62166793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5da8ce9cd0469abbdd2790e1c63a96b3cd235695bd8f350ca5f0f8cf4c139f5`

```dockerfile
```

-	Layers:
	-	`sha256:75f3d4f5a0bbe94b65cbe80a0039b34487080dafcc4d37024fb41e440bab4597`  
		Last Modified: Tue, 24 Mar 2026 18:26:11 GMT  
		Size: 62.1 MB (62139842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab7866e39fca21ca5762ac536f2e45633e9a3347e284b1d1a3190943baf9167`  
		Last Modified: Tue, 24 Mar 2026 18:26:07 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:d18b8ca7d3e49c4b0b56dc608fc1b3fb3db57e0bb22b7da5ee519219b57d682e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.8 MB (699793189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3474fc8ebcb551aa0dcfa1bf74288fb83d1e43f4fd3c851679cf5c2d7435103`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:20:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:20:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:20:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:20:52 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Mar 2026 18:20:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:21:07 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:42:31 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:42:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:42:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:42:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:42:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:42:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
USER odoo
# Tue, 24 Mar 2026 18:42:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:42:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915164dd74f18bd04897fe989dbaf980d3f07e4767351cd00025bc6c1fb374b8`  
		Last Modified: Tue, 24 Mar 2026 18:28:47 GMT  
		Size: 265.1 MB (265109188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e0e387d453c47befff5578df88e0c36c14ae285f3ceb5418cbe53ce2b37f81`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 14.9 MB (14893001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfffa2c0db96bb28612d7e87eccf8756916bf1f024c6da84d894320cf564b01c`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 479.7 KB (479700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790aac0fee5bce35d510731f570883b5aa98d274a3494da2f87c9d7315429581`  
		Last Modified: Tue, 24 Mar 2026 18:46:35 GMT  
		Size: 385.0 MB (384998807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a787e565139873768d9053abaf2bea4e336c65543fdaca36929a06b4eeff269`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8d266579bd445ccbb9ba41f4f965fb434246f4e32ec761f7d9351ca03fc2`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4309fac518552b6c43f4b4e76b4e205de07efc78f51b3616611e129ff286e79b`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b1028313ee0cf44c05517b4578e747f25bd095e50e23ecad230ae0cd84837`  
		Last Modified: Tue, 24 Mar 2026 18:46:27 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c2019b5862b5c81b69c89d1d5a0ec1b7b6c35299114c92d93d7a64eb0fda852d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62167805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6c2c165aaa27844bf7f6ccbdb868b37ad20e37d72ffd04aa704b2824dc8492`

```dockerfile
```

-	Layers:
	-	`sha256:9e981390a8375342b057a3b61288f2534f8f3a7ed80d4d9dfa7300b25e314a95`  
		Last Modified: Tue, 24 Mar 2026 18:46:29 GMT  
		Size: 62.1 MB (62140950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d7f44a2058a8f33090682b3407a50289be126697c9897327057c965ed32da3`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:c1ad8ac124214c33f5d57a957ca88cb5c3d70255132794e32b7894d063ea1449
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
$ docker pull odoo@sha256:8375d3e73746ec454fc25c202e066df700af381fea061152200ad2a003f80ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.6 MB (683605889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df276b7ba54a32fa0ce5a2cf139877b61d6ebc55c788506d7fcac82501c32778`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:35 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:35 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:22:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:22:46 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:46 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:23:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e4b72f65ec80988a958fb6237f455e6aea58603ba27f7fd3e591ea3f8695e0`  
		Last Modified: Tue, 24 Mar 2026 18:25:43 GMT  
		Size: 254.6 MB (254566357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c4c85ea8449df52beb214d6df785927a950c0d552758ed46d0b306d2b1a50`  
		Last Modified: Tue, 24 Mar 2026 18:25:34 GMT  
		Size: 14.4 MB (14359961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785da4fb759684e26550fab1e497378b1238b9c1e8993debda92e95cde008da2`  
		Last Modified: Tue, 24 Mar 2026 18:25:33 GMT  
		Size: 479.6 KB (479639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4ee431022506c6b62af299bf05da37d3a21e8d5be3bf1636a42566d4042f3`  
		Last Modified: Tue, 24 Mar 2026 18:25:46 GMT  
		Size: 384.5 MB (384465501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5108ab6399a49d651e9473504b69ede3d43243f4a72d022250d59a432692b82f`  
		Last Modified: Tue, 24 Mar 2026 18:25:34 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac3ed23c0392c9970bfe958e111eac5202903b2f40ac1831974de36551fab2`  
		Last Modified: Tue, 24 Mar 2026 18:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b017750fb448d8678c0eb33f53c2f8e4a53efe593baba1e543c2c0117def7a`  
		Last Modified: Tue, 24 Mar 2026 18:25:36 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabf624291fa40f929218bb8d9b57bbe39209b0ce5bb70440500ff6f4737f79c`  
		Last Modified: Tue, 24 Mar 2026 18:25:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1866df97b223e6a6ffc3dc29c41584b80c6a9fc549abfff4def2c1f8af686070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62159366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ab720e2c2b8a06d8a2a7f736fabdfc4325f6447b67eb2874b6f720bbb79e7e`

```dockerfile
```

-	Layers:
	-	`sha256:ea41fb4a3c5da3ed3b26c7c0d87bdcd5dc94f19c7bad682041e6570f35c1938f`  
		Last Modified: Tue, 24 Mar 2026 18:25:37 GMT  
		Size: 62.1 MB (62132567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8924bce32404e6e4ff8db0c06c60094376b258bb25254e359769980a666f89b6`  
		Last Modified: Tue, 24 Mar 2026 18:25:33 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fa32b55acdf4f0b38463d00eea62eed0ada58da62b02a9a4ace446dce3716a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.0 MB (680001554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16016f3da78d7a882ae49f8978dbf235cf36abe5a1ce4f2723c909cd83076f3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:43 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:22:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:56 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:56 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:22:56 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:56 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:23:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99f5fbeb6fee02b1893a8cc8addfb704f41b18f838b297e684c3235aed8c93`  
		Last Modified: Tue, 24 Mar 2026 18:26:16 GMT  
		Size: 252.0 MB (251995638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a50dad2c848f32e3d6cfe9144d0f950bef5986208bc93a3b7a710f04b6567b`  
		Last Modified: Tue, 24 Mar 2026 18:26:08 GMT  
		Size: 14.3 MB (14340676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ae2f00adc9c805164f4a126e61c1971a94b26c2cc01efb14b037df3cd81cd`  
		Last Modified: Tue, 24 Mar 2026 18:26:07 GMT  
		Size: 479.6 KB (479648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b50e454b4a4f3a1ea1392cf401c225565e5289f2d5d7f1b7001d16e62661b6`  
		Last Modified: Tue, 24 Mar 2026 18:26:20 GMT  
		Size: 384.3 MB (384313444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b65d1d78b247e3872cb364bd19aafa949759937662893f1f479a233f5f78c4`  
		Last Modified: Tue, 24 Mar 2026 18:26:08 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc2be3843975cda87240ce1b24dcd692cd0d6495707733bf1cc1f523f0b8965`  
		Last Modified: Tue, 24 Mar 2026 18:26:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44890499d7cb21688a136b660fbb26cb642c90e95c27a755461904c66daf13cb`  
		Last Modified: Tue, 24 Mar 2026 18:26:09 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9833564912be7c6fe8c08cd122e0a877260b838660f45135e10fbe5735510c`  
		Last Modified: Tue, 24 Mar 2026 18:26:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f4fa47360aa86baf2261d21b1096da2a197228860e9e9e5a31e01c083da56b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62166793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5da8ce9cd0469abbdd2790e1c63a96b3cd235695bd8f350ca5f0f8cf4c139f5`

```dockerfile
```

-	Layers:
	-	`sha256:75f3d4f5a0bbe94b65cbe80a0039b34487080dafcc4d37024fb41e440bab4597`  
		Last Modified: Tue, 24 Mar 2026 18:26:11 GMT  
		Size: 62.1 MB (62139842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab7866e39fca21ca5762ac536f2e45633e9a3347e284b1d1a3190943baf9167`  
		Last Modified: Tue, 24 Mar 2026 18:26:07 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:d18b8ca7d3e49c4b0b56dc608fc1b3fb3db57e0bb22b7da5ee519219b57d682e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.8 MB (699793189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3474fc8ebcb551aa0dcfa1bf74288fb83d1e43f4fd3c851679cf5c2d7435103`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:20:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:20:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:20:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:20:52 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Mar 2026 18:20:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:21:07 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:42:31 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:42:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:42:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:42:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:42:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:42:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
USER odoo
# Tue, 24 Mar 2026 18:42:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:42:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915164dd74f18bd04897fe989dbaf980d3f07e4767351cd00025bc6c1fb374b8`  
		Last Modified: Tue, 24 Mar 2026 18:28:47 GMT  
		Size: 265.1 MB (265109188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e0e387d453c47befff5578df88e0c36c14ae285f3ceb5418cbe53ce2b37f81`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 14.9 MB (14893001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfffa2c0db96bb28612d7e87eccf8756916bf1f024c6da84d894320cf564b01c`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 479.7 KB (479700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790aac0fee5bce35d510731f570883b5aa98d274a3494da2f87c9d7315429581`  
		Last Modified: Tue, 24 Mar 2026 18:46:35 GMT  
		Size: 385.0 MB (384998807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a787e565139873768d9053abaf2bea4e336c65543fdaca36929a06b4eeff269`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8d266579bd445ccbb9ba41f4f965fb434246f4e32ec761f7d9351ca03fc2`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4309fac518552b6c43f4b4e76b4e205de07efc78f51b3616611e129ff286e79b`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b1028313ee0cf44c05517b4578e747f25bd095e50e23ecad230ae0cd84837`  
		Last Modified: Tue, 24 Mar 2026 18:46:27 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c2019b5862b5c81b69c89d1d5a0ec1b7b6c35299114c92d93d7a64eb0fda852d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62167805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6c2c165aaa27844bf7f6ccbdb868b37ad20e37d72ffd04aa704b2824dc8492`

```dockerfile
```

-	Layers:
	-	`sha256:9e981390a8375342b057a3b61288f2534f8f3a7ed80d4d9dfa7300b25e314a95`  
		Last Modified: Tue, 24 Mar 2026 18:46:29 GMT  
		Size: 62.1 MB (62140950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d7f44a2058a8f33090682b3407a50289be126697c9897327057c965ed32da3`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260324`

```console
$ docker pull odoo@sha256:c1ad8ac124214c33f5d57a957ca88cb5c3d70255132794e32b7894d063ea1449
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260324` - linux; amd64

```console
$ docker pull odoo@sha256:8375d3e73746ec454fc25c202e066df700af381fea061152200ad2a003f80ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.6 MB (683605889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df276b7ba54a32fa0ce5a2cf139877b61d6ebc55c788506d7fcac82501c32778`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:35 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:35 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:22:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:22:46 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:46 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:23:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:43 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e4b72f65ec80988a958fb6237f455e6aea58603ba27f7fd3e591ea3f8695e0`  
		Last Modified: Tue, 24 Mar 2026 18:25:43 GMT  
		Size: 254.6 MB (254566357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13c4c85ea8449df52beb214d6df785927a950c0d552758ed46d0b306d2b1a50`  
		Last Modified: Tue, 24 Mar 2026 18:25:34 GMT  
		Size: 14.4 MB (14359961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785da4fb759684e26550fab1e497378b1238b9c1e8993debda92e95cde008da2`  
		Last Modified: Tue, 24 Mar 2026 18:25:33 GMT  
		Size: 479.6 KB (479639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4ee431022506c6b62af299bf05da37d3a21e8d5be3bf1636a42566d4042f3`  
		Last Modified: Tue, 24 Mar 2026 18:25:46 GMT  
		Size: 384.5 MB (384465501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5108ab6399a49d651e9473504b69ede3d43243f4a72d022250d59a432692b82f`  
		Last Modified: Tue, 24 Mar 2026 18:25:34 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac3ed23c0392c9970bfe958e111eac5202903b2f40ac1831974de36551fab2`  
		Last Modified: Tue, 24 Mar 2026 18:25:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b017750fb448d8678c0eb33f53c2f8e4a53efe593baba1e543c2c0117def7a`  
		Last Modified: Tue, 24 Mar 2026 18:25:36 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabf624291fa40f929218bb8d9b57bbe39209b0ce5bb70440500ff6f4737f79c`  
		Last Modified: Tue, 24 Mar 2026 18:25:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:1866df97b223e6a6ffc3dc29c41584b80c6a9fc549abfff4def2c1f8af686070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62159366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ab720e2c2b8a06d8a2a7f736fabdfc4325f6447b67eb2874b6f720bbb79e7e`

```dockerfile
```

-	Layers:
	-	`sha256:ea41fb4a3c5da3ed3b26c7c0d87bdcd5dc94f19c7bad682041e6570f35c1938f`  
		Last Modified: Tue, 24 Mar 2026 18:25:37 GMT  
		Size: 62.1 MB (62132567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8924bce32404e6e4ff8db0c06c60094376b258bb25254e359769980a666f89b6`  
		Last Modified: Tue, 24 Mar 2026 18:25:33 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260324` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:fa32b55acdf4f0b38463d00eea62eed0ada58da62b02a9a4ace446dce3716a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.0 MB (680001554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16016f3da78d7a882ae49f8978dbf235cf36abe5a1ce4f2723c909cd83076f3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:43 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:22:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:56 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:56 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:22:56 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:56 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:23:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:55 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c99f5fbeb6fee02b1893a8cc8addfb704f41b18f838b297e684c3235aed8c93`  
		Last Modified: Tue, 24 Mar 2026 18:26:16 GMT  
		Size: 252.0 MB (251995638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a50dad2c848f32e3d6cfe9144d0f950bef5986208bc93a3b7a710f04b6567b`  
		Last Modified: Tue, 24 Mar 2026 18:26:08 GMT  
		Size: 14.3 MB (14340676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ae2f00adc9c805164f4a126e61c1971a94b26c2cc01efb14b037df3cd81cd`  
		Last Modified: Tue, 24 Mar 2026 18:26:07 GMT  
		Size: 479.6 KB (479648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b50e454b4a4f3a1ea1392cf401c225565e5289f2d5d7f1b7001d16e62661b6`  
		Last Modified: Tue, 24 Mar 2026 18:26:20 GMT  
		Size: 384.3 MB (384313444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b65d1d78b247e3872cb364bd19aafa949759937662893f1f479a233f5f78c4`  
		Last Modified: Tue, 24 Mar 2026 18:26:08 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc2be3843975cda87240ce1b24dcd692cd0d6495707733bf1cc1f523f0b8965`  
		Last Modified: Tue, 24 Mar 2026 18:26:09 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44890499d7cb21688a136b660fbb26cb642c90e95c27a755461904c66daf13cb`  
		Last Modified: Tue, 24 Mar 2026 18:26:09 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9833564912be7c6fe8c08cd122e0a877260b838660f45135e10fbe5735510c`  
		Last Modified: Tue, 24 Mar 2026 18:26:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:f4fa47360aa86baf2261d21b1096da2a197228860e9e9e5a31e01c083da56b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62166793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5da8ce9cd0469abbdd2790e1c63a96b3cd235695bd8f350ca5f0f8cf4c139f5`

```dockerfile
```

-	Layers:
	-	`sha256:75f3d4f5a0bbe94b65cbe80a0039b34487080dafcc4d37024fb41e440bab4597`  
		Last Modified: Tue, 24 Mar 2026 18:26:11 GMT  
		Size: 62.1 MB (62139842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab7866e39fca21ca5762ac536f2e45633e9a3347e284b1d1a3190943baf9167`  
		Last Modified: Tue, 24 Mar 2026 18:26:07 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260324` - linux; ppc64le

```console
$ docker pull odoo@sha256:d18b8ca7d3e49c4b0b56dc608fc1b3fb3db57e0bb22b7da5ee519219b57d682e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.8 MB (699793189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3474fc8ebcb551aa0dcfa1bf74288fb83d1e43f4fd3c851679cf5c2d7435103`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:20:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:20:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:20:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:20:52 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Mar 2026 18:20:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:21:07 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
ENV ODOO_VERSION=18.0
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
# Tue, 24 Mar 2026 18:42:31 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:42:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:42:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=ae28e50ed972a6e57f7de42fc3b267acd4ab1f33
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:42:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:42:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:42:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:42:33 GMT
USER odoo
# Tue, 24 Mar 2026 18:42:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:42:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915164dd74f18bd04897fe989dbaf980d3f07e4767351cd00025bc6c1fb374b8`  
		Last Modified: Tue, 24 Mar 2026 18:28:47 GMT  
		Size: 265.1 MB (265109188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e0e387d453c47befff5578df88e0c36c14ae285f3ceb5418cbe53ce2b37f81`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 14.9 MB (14893001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfffa2c0db96bb28612d7e87eccf8756916bf1f024c6da84d894320cf564b01c`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 479.7 KB (479700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790aac0fee5bce35d510731f570883b5aa98d274a3494da2f87c9d7315429581`  
		Last Modified: Tue, 24 Mar 2026 18:46:35 GMT  
		Size: 385.0 MB (384998807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a787e565139873768d9053abaf2bea4e336c65543fdaca36929a06b4eeff269`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710e8d266579bd445ccbb9ba41f4f965fb434246f4e32ec761f7d9351ca03fc2`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4309fac518552b6c43f4b4e76b4e205de07efc78f51b3616611e129ff286e79b`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b1028313ee0cf44c05517b4578e747f25bd095e50e23ecad230ae0cd84837`  
		Last Modified: Tue, 24 Mar 2026 18:46:27 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:c2019b5862b5c81b69c89d1d5a0ec1b7b6c35299114c92d93d7a64eb0fda852d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62167805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6c2c165aaa27844bf7f6ccbdb868b37ad20e37d72ffd04aa704b2824dc8492`

```dockerfile
```

-	Layers:
	-	`sha256:9e981390a8375342b057a3b61288f2534f8f3a7ed80d4d9dfa7300b25e314a95`  
		Last Modified: Tue, 24 Mar 2026 18:46:29 GMT  
		Size: 62.1 MB (62140950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6d7f44a2058a8f33090682b3407a50289be126697c9897327057c965ed32da3`  
		Last Modified: Tue, 24 Mar 2026 18:46:26 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:19b1d3cc053b31f418b3db1f57c709c0e589a9c29fdabdff966b60d05d757028
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
$ docker pull odoo@sha256:c0f90a67d38b91fb5388c69599fe1336846aec747c61fccec2daa4f9e200d9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702222756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9194aa4bd6431eb77cb9a2ce756b53287bafc9dc43ec7b067f38d7dc7712439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:23:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:23:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:23:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:23:08 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:23:08 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133260e68d690d818cca272dda40ab3057188bd9273fe85305cb4d2d70c9708d`  
		Last Modified: Tue, 24 Mar 2026 18:26:36 GMT  
		Size: 254.6 MB (254566939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282243a45e1296b995946a8ab6329c6965da996af3616c71cf8512bce8f003e1`  
		Last Modified: Tue, 24 Mar 2026 18:26:27 GMT  
		Size: 14.4 MB (14359889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050e5fe2d3944dd8f7a6e379e2fe1b5f61a929df494505ea07147d0bd9b81a0d`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 479.6 KB (479639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dada5132e8c7a7275ea92f846a14fa53b397810f708e81bdb6d3805169641d`  
		Last Modified: Tue, 24 Mar 2026 18:26:38 GMT  
		Size: 403.1 MB (403081859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3421f8b4af10dd7cec481b93528385de7a9390aa0c54a44e2d99a880e8baac74`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd116cf14c9df749adb9ede39426a74d9745d6fca150f3c952a9d933ac2ec57`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcd0df88d5f3ebd29551911f92e1a46a947c1ad5763c84ae66cdce61b7df6cb`  
		Last Modified: Tue, 24 Mar 2026 18:26:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0599430ccfaf9cf55832a6d90d07d71b7f41d023bf86d6a3580c13e34ec86e`  
		Last Modified: Tue, 24 Mar 2026 18:26:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:a681b68de6906ee5c138d46abdd18277fcf4783b58359ab665cfda107ddd0c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26acd2a47c07aa93b5c72436155dbff63c9669de3c84a2b0d70659eacb447d45`

```dockerfile
```

-	Layers:
	-	`sha256:de24cf55ba08080532c1a953a119801af23685c86d7d5973d4828a6a573b7a38`  
		Last Modified: Tue, 24 Mar 2026 18:26:31 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90819aea80cdc4b3dfdc57a5845ad42c8381d50276e03bbe0bc54fd6505bdea1`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7fd235f9d6af1f1de07401bf789140114915144d0ef7c55f09f3f752f75bf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698608366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f038f83304efd437bc0cb703eab83ab9b3af57e61c1b767776867b20b9794a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:39 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:22:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:49 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:01 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:01 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99263ff6a54dc45f69755c4b5bebb63bd750f1a9f24d114e0d07d9b78d7c475`  
		Last Modified: Tue, 24 Mar 2026 18:26:53 GMT  
		Size: 252.0 MB (251994807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e37ef8651bbf161b74a1a781e17dbe5f11a5dbaf94c0c02f13b7f874568f68`  
		Last Modified: Tue, 24 Mar 2026 18:26:45 GMT  
		Size: 14.3 MB (14340549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66d26a0f9f66bc39504c9263d7a34df393e8496ccddf8c8c7187d5de12ee10`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 479.6 KB (479647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704d6e8e2b3e7ce1697841db84f36b166078243adfea572cdce62089f1660eb0`  
		Last Modified: Tue, 24 Mar 2026 18:26:56 GMT  
		Size: 402.9 MB (402921216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4703181900d352653f765f355525457ef820b84ddf78d6cf4279fef4f4412`  
		Last Modified: Tue, 24 Mar 2026 18:26:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440673301970e5d9e4ef2035bfee68045676bcaf590dcadf640739f5a380cfab`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86dfe87dfdec50a3d4552326194a6c5f2f2dba239ba81cba0442dcf3c98f9c`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f81e94985555848c2075cd2b59a5f028fff3c4485e026ca427954222dd7c96`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:cb54d4b0353c8c399938b772e65f54910b79112f0c3a7723360f70c5554245d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1911a8e92ff2574621b89b3d42d3b000098902aac362efb62484730b6161d41`

```dockerfile
```

-	Layers:
	-	`sha256:499c9af97f16f4603b7e623ff73a2f797fd7cac68d1cf39ebbe25db403abc69d`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9b5475841bfe9ad7bc7224b4718ee26cf464bd990217c3dd60a1cb5b555899`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d000be2ba72ae244d0d1697fc3762b91d9a77a0ca913ca56412e9ace07057da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718419326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4059620278314767fbdc89bd6fd4f6d7085735783b639176b92bdff744f687e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:20:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:20:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:20:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:20:52 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Mar 2026 18:20:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:21:07 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:23:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:37 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915164dd74f18bd04897fe989dbaf980d3f07e4767351cd00025bc6c1fb374b8`  
		Last Modified: Tue, 24 Mar 2026 18:28:47 GMT  
		Size: 265.1 MB (265109188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e0e387d453c47befff5578df88e0c36c14ae285f3ceb5418cbe53ce2b37f81`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 14.9 MB (14893001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfffa2c0db96bb28612d7e87eccf8756916bf1f024c6da84d894320cf564b01c`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 479.7 KB (479700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bde1ff247817cc1880639ab111508be52b8316bce1eea63961dd31ad249eec`  
		Last Modified: Tue, 24 Mar 2026 18:28:52 GMT  
		Size: 403.6 MB (403624947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5abc4486f63125bd3440c31d2080e58dc5be56518fd047def47f025d472b54`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521d3d42bd797a4dcfde9977b1d803726efac45383b02bae04214d935a1f139`  
		Last Modified: Tue, 24 Mar 2026 18:28:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada80af41804fb9eff5edd599073dc01c0a074ea0803ce557397aa1e32ff703f`  
		Last Modified: Tue, 24 Mar 2026 18:28:39 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506e3a2863e861eab2021978f0a4876992ad8b66f17fc670554e06ae62ec9126`  
		Last Modified: Tue, 24 Mar 2026 18:28:40 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:6e85b5ff8f4d536918a51c106f541029590c32ecefcb89816cf3a3f8155c21f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e08e3fc6c63de0ab79b7cb10b55231388c609546c1b7f59d0ca5f2b3ba972c7`

```dockerfile
```

-	Layers:
	-	`sha256:6f6fc43bcbee6845a9e1dc2ec8ef97380cd084a4e4ce6ecbf23ed740ce2c68c4`  
		Last Modified: Tue, 24 Mar 2026 18:28:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99604b9f76cf14194ce6adc3045ae2e1bd5016f61cd951869cf42761e6c98ca6`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:19b1d3cc053b31f418b3db1f57c709c0e589a9c29fdabdff966b60d05d757028
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
$ docker pull odoo@sha256:c0f90a67d38b91fb5388c69599fe1336846aec747c61fccec2daa4f9e200d9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702222756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9194aa4bd6431eb77cb9a2ce756b53287bafc9dc43ec7b067f38d7dc7712439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:23:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:23:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:23:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:23:08 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:23:08 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133260e68d690d818cca272dda40ab3057188bd9273fe85305cb4d2d70c9708d`  
		Last Modified: Tue, 24 Mar 2026 18:26:36 GMT  
		Size: 254.6 MB (254566939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282243a45e1296b995946a8ab6329c6965da996af3616c71cf8512bce8f003e1`  
		Last Modified: Tue, 24 Mar 2026 18:26:27 GMT  
		Size: 14.4 MB (14359889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050e5fe2d3944dd8f7a6e379e2fe1b5f61a929df494505ea07147d0bd9b81a0d`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 479.6 KB (479639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dada5132e8c7a7275ea92f846a14fa53b397810f708e81bdb6d3805169641d`  
		Last Modified: Tue, 24 Mar 2026 18:26:38 GMT  
		Size: 403.1 MB (403081859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3421f8b4af10dd7cec481b93528385de7a9390aa0c54a44e2d99a880e8baac74`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd116cf14c9df749adb9ede39426a74d9745d6fca150f3c952a9d933ac2ec57`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcd0df88d5f3ebd29551911f92e1a46a947c1ad5763c84ae66cdce61b7df6cb`  
		Last Modified: Tue, 24 Mar 2026 18:26:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0599430ccfaf9cf55832a6d90d07d71b7f41d023bf86d6a3580c13e34ec86e`  
		Last Modified: Tue, 24 Mar 2026 18:26:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a681b68de6906ee5c138d46abdd18277fcf4783b58359ab665cfda107ddd0c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26acd2a47c07aa93b5c72436155dbff63c9669de3c84a2b0d70659eacb447d45`

```dockerfile
```

-	Layers:
	-	`sha256:de24cf55ba08080532c1a953a119801af23685c86d7d5973d4828a6a573b7a38`  
		Last Modified: Tue, 24 Mar 2026 18:26:31 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90819aea80cdc4b3dfdc57a5845ad42c8381d50276e03bbe0bc54fd6505bdea1`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7fd235f9d6af1f1de07401bf789140114915144d0ef7c55f09f3f752f75bf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698608366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f038f83304efd437bc0cb703eab83ab9b3af57e61c1b767776867b20b9794a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:39 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:22:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:49 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:01 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:01 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99263ff6a54dc45f69755c4b5bebb63bd750f1a9f24d114e0d07d9b78d7c475`  
		Last Modified: Tue, 24 Mar 2026 18:26:53 GMT  
		Size: 252.0 MB (251994807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e37ef8651bbf161b74a1a781e17dbe5f11a5dbaf94c0c02f13b7f874568f68`  
		Last Modified: Tue, 24 Mar 2026 18:26:45 GMT  
		Size: 14.3 MB (14340549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66d26a0f9f66bc39504c9263d7a34df393e8496ccddf8c8c7187d5de12ee10`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 479.6 KB (479647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704d6e8e2b3e7ce1697841db84f36b166078243adfea572cdce62089f1660eb0`  
		Last Modified: Tue, 24 Mar 2026 18:26:56 GMT  
		Size: 402.9 MB (402921216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4703181900d352653f765f355525457ef820b84ddf78d6cf4279fef4f4412`  
		Last Modified: Tue, 24 Mar 2026 18:26:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440673301970e5d9e4ef2035bfee68045676bcaf590dcadf640739f5a380cfab`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86dfe87dfdec50a3d4552326194a6c5f2f2dba239ba81cba0442dcf3c98f9c`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f81e94985555848c2075cd2b59a5f028fff3c4485e026ca427954222dd7c96`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cb54d4b0353c8c399938b772e65f54910b79112f0c3a7723360f70c5554245d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1911a8e92ff2574621b89b3d42d3b000098902aac362efb62484730b6161d41`

```dockerfile
```

-	Layers:
	-	`sha256:499c9af97f16f4603b7e623ff73a2f797fd7cac68d1cf39ebbe25db403abc69d`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9b5475841bfe9ad7bc7224b4718ee26cf464bd990217c3dd60a1cb5b555899`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d000be2ba72ae244d0d1697fc3762b91d9a77a0ca913ca56412e9ace07057da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718419326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4059620278314767fbdc89bd6fd4f6d7085735783b639176b92bdff744f687e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:20:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:20:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:20:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:20:52 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Mar 2026 18:20:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:21:07 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:23:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:37 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915164dd74f18bd04897fe989dbaf980d3f07e4767351cd00025bc6c1fb374b8`  
		Last Modified: Tue, 24 Mar 2026 18:28:47 GMT  
		Size: 265.1 MB (265109188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e0e387d453c47befff5578df88e0c36c14ae285f3ceb5418cbe53ce2b37f81`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 14.9 MB (14893001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfffa2c0db96bb28612d7e87eccf8756916bf1f024c6da84d894320cf564b01c`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 479.7 KB (479700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bde1ff247817cc1880639ab111508be52b8316bce1eea63961dd31ad249eec`  
		Last Modified: Tue, 24 Mar 2026 18:28:52 GMT  
		Size: 403.6 MB (403624947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5abc4486f63125bd3440c31d2080e58dc5be56518fd047def47f025d472b54`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521d3d42bd797a4dcfde9977b1d803726efac45383b02bae04214d935a1f139`  
		Last Modified: Tue, 24 Mar 2026 18:28:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada80af41804fb9eff5edd599073dc01c0a074ea0803ce557397aa1e32ff703f`  
		Last Modified: Tue, 24 Mar 2026 18:28:39 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506e3a2863e861eab2021978f0a4876992ad8b66f17fc670554e06ae62ec9126`  
		Last Modified: Tue, 24 Mar 2026 18:28:40 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6e85b5ff8f4d536918a51c106f541029590c32ecefcb89816cf3a3f8155c21f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e08e3fc6c63de0ab79b7cb10b55231388c609546c1b7f59d0ca5f2b3ba972c7`

```dockerfile
```

-	Layers:
	-	`sha256:6f6fc43bcbee6845a9e1dc2ec8ef97380cd084a4e4ce6ecbf23ed740ce2c68c4`  
		Last Modified: Tue, 24 Mar 2026 18:28:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99604b9f76cf14194ce6adc3045ae2e1bd5016f61cd951869cf42761e6c98ca6`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260324`

```console
$ docker pull odoo@sha256:19b1d3cc053b31f418b3db1f57c709c0e589a9c29fdabdff966b60d05d757028
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260324` - linux; amd64

```console
$ docker pull odoo@sha256:c0f90a67d38b91fb5388c69599fe1336846aec747c61fccec2daa4f9e200d9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702222756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9194aa4bd6431eb77cb9a2ce756b53287bafc9dc43ec7b067f38d7dc7712439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:23:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:23:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:23:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:23:08 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:23:08 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133260e68d690d818cca272dda40ab3057188bd9273fe85305cb4d2d70c9708d`  
		Last Modified: Tue, 24 Mar 2026 18:26:36 GMT  
		Size: 254.6 MB (254566939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282243a45e1296b995946a8ab6329c6965da996af3616c71cf8512bce8f003e1`  
		Last Modified: Tue, 24 Mar 2026 18:26:27 GMT  
		Size: 14.4 MB (14359889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050e5fe2d3944dd8f7a6e379e2fe1b5f61a929df494505ea07147d0bd9b81a0d`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 479.6 KB (479639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dada5132e8c7a7275ea92f846a14fa53b397810f708e81bdb6d3805169641d`  
		Last Modified: Tue, 24 Mar 2026 18:26:38 GMT  
		Size: 403.1 MB (403081859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3421f8b4af10dd7cec481b93528385de7a9390aa0c54a44e2d99a880e8baac74`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd116cf14c9df749adb9ede39426a74d9745d6fca150f3c952a9d933ac2ec57`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcd0df88d5f3ebd29551911f92e1a46a947c1ad5763c84ae66cdce61b7df6cb`  
		Last Modified: Tue, 24 Mar 2026 18:26:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0599430ccfaf9cf55832a6d90d07d71b7f41d023bf86d6a3580c13e34ec86e`  
		Last Modified: Tue, 24 Mar 2026 18:26:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:a681b68de6906ee5c138d46abdd18277fcf4783b58359ab665cfda107ddd0c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26acd2a47c07aa93b5c72436155dbff63c9669de3c84a2b0d70659eacb447d45`

```dockerfile
```

-	Layers:
	-	`sha256:de24cf55ba08080532c1a953a119801af23685c86d7d5973d4828a6a573b7a38`  
		Last Modified: Tue, 24 Mar 2026 18:26:31 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90819aea80cdc4b3dfdc57a5845ad42c8381d50276e03bbe0bc54fd6505bdea1`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260324` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7fd235f9d6af1f1de07401bf789140114915144d0ef7c55f09f3f752f75bf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698608366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f038f83304efd437bc0cb703eab83ab9b3af57e61c1b767776867b20b9794a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:39 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:22:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:49 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:01 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:01 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99263ff6a54dc45f69755c4b5bebb63bd750f1a9f24d114e0d07d9b78d7c475`  
		Last Modified: Tue, 24 Mar 2026 18:26:53 GMT  
		Size: 252.0 MB (251994807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e37ef8651bbf161b74a1a781e17dbe5f11a5dbaf94c0c02f13b7f874568f68`  
		Last Modified: Tue, 24 Mar 2026 18:26:45 GMT  
		Size: 14.3 MB (14340549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66d26a0f9f66bc39504c9263d7a34df393e8496ccddf8c8c7187d5de12ee10`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 479.6 KB (479647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704d6e8e2b3e7ce1697841db84f36b166078243adfea572cdce62089f1660eb0`  
		Last Modified: Tue, 24 Mar 2026 18:26:56 GMT  
		Size: 402.9 MB (402921216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4703181900d352653f765f355525457ef820b84ddf78d6cf4279fef4f4412`  
		Last Modified: Tue, 24 Mar 2026 18:26:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440673301970e5d9e4ef2035bfee68045676bcaf590dcadf640739f5a380cfab`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86dfe87dfdec50a3d4552326194a6c5f2f2dba239ba81cba0442dcf3c98f9c`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f81e94985555848c2075cd2b59a5f028fff3c4485e026ca427954222dd7c96`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:cb54d4b0353c8c399938b772e65f54910b79112f0c3a7723360f70c5554245d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1911a8e92ff2574621b89b3d42d3b000098902aac362efb62484730b6161d41`

```dockerfile
```

-	Layers:
	-	`sha256:499c9af97f16f4603b7e623ff73a2f797fd7cac68d1cf39ebbe25db403abc69d`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9b5475841bfe9ad7bc7224b4718ee26cf464bd990217c3dd60a1cb5b555899`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260324` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d000be2ba72ae244d0d1697fc3762b91d9a77a0ca913ca56412e9ace07057da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718419326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4059620278314767fbdc89bd6fd4f6d7085735783b639176b92bdff744f687e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:20:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:20:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:20:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:20:52 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Mar 2026 18:20:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:21:07 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:23:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:37 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915164dd74f18bd04897fe989dbaf980d3f07e4767351cd00025bc6c1fb374b8`  
		Last Modified: Tue, 24 Mar 2026 18:28:47 GMT  
		Size: 265.1 MB (265109188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e0e387d453c47befff5578df88e0c36c14ae285f3ceb5418cbe53ce2b37f81`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 14.9 MB (14893001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfffa2c0db96bb28612d7e87eccf8756916bf1f024c6da84d894320cf564b01c`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 479.7 KB (479700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bde1ff247817cc1880639ab111508be52b8316bce1eea63961dd31ad249eec`  
		Last Modified: Tue, 24 Mar 2026 18:28:52 GMT  
		Size: 403.6 MB (403624947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5abc4486f63125bd3440c31d2080e58dc5be56518fd047def47f025d472b54`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521d3d42bd797a4dcfde9977b1d803726efac45383b02bae04214d935a1f139`  
		Last Modified: Tue, 24 Mar 2026 18:28:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada80af41804fb9eff5edd599073dc01c0a074ea0803ce557397aa1e32ff703f`  
		Last Modified: Tue, 24 Mar 2026 18:28:39 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506e3a2863e861eab2021978f0a4876992ad8b66f17fc670554e06ae62ec9126`  
		Last Modified: Tue, 24 Mar 2026 18:28:40 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260324` - unknown; unknown

```console
$ docker pull odoo@sha256:6e85b5ff8f4d536918a51c106f541029590c32ecefcb89816cf3a3f8155c21f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e08e3fc6c63de0ab79b7cb10b55231388c609546c1b7f59d0ca5f2b3ba972c7`

```dockerfile
```

-	Layers:
	-	`sha256:6f6fc43bcbee6845a9e1dc2ec8ef97380cd084a4e4ce6ecbf23ed740ce2c68c4`  
		Last Modified: Tue, 24 Mar 2026 18:28:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99604b9f76cf14194ce6adc3045ae2e1bd5016f61cd951869cf42761e6c98ca6`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:19b1d3cc053b31f418b3db1f57c709c0e589a9c29fdabdff966b60d05d757028
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
$ docker pull odoo@sha256:c0f90a67d38b91fb5388c69599fe1336846aec747c61fccec2daa4f9e200d9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.2 MB (702222756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9194aa4bd6431eb77cb9a2ce756b53287bafc9dc43ec7b067f38d7dc7712439`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:23:08 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:23:08 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:23:08 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:23:08 GMT
ARG TARGETARCH=amd64
# Tue, 24 Mar 2026 18:23:08 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:23:17 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:23:17 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:19 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133260e68d690d818cca272dda40ab3057188bd9273fe85305cb4d2d70c9708d`  
		Last Modified: Tue, 24 Mar 2026 18:26:36 GMT  
		Size: 254.6 MB (254566939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282243a45e1296b995946a8ab6329c6965da996af3616c71cf8512bce8f003e1`  
		Last Modified: Tue, 24 Mar 2026 18:26:27 GMT  
		Size: 14.4 MB (14359889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050e5fe2d3944dd8f7a6e379e2fe1b5f61a929df494505ea07147d0bd9b81a0d`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 479.6 KB (479639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dada5132e8c7a7275ea92f846a14fa53b397810f708e81bdb6d3805169641d`  
		Last Modified: Tue, 24 Mar 2026 18:26:38 GMT  
		Size: 403.1 MB (403081859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3421f8b4af10dd7cec481b93528385de7a9390aa0c54a44e2d99a880e8baac74`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd116cf14c9df749adb9ede39426a74d9745d6fca150f3c952a9d933ac2ec57`  
		Last Modified: Tue, 24 Mar 2026 18:26:28 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcd0df88d5f3ebd29551911f92e1a46a947c1ad5763c84ae66cdce61b7df6cb`  
		Last Modified: Tue, 24 Mar 2026 18:26:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0599430ccfaf9cf55832a6d90d07d71b7f41d023bf86d6a3580c13e34ec86e`  
		Last Modified: Tue, 24 Mar 2026 18:26:30 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:a681b68de6906ee5c138d46abdd18277fcf4783b58359ab665cfda107ddd0c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69981971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26acd2a47c07aa93b5c72436155dbff63c9669de3c84a2b0d70659eacb447d45`

```dockerfile
```

-	Layers:
	-	`sha256:de24cf55ba08080532c1a953a119801af23685c86d7d5973d4828a6a573b7a38`  
		Last Modified: Tue, 24 Mar 2026 18:26:31 GMT  
		Size: 70.0 MB (69954878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90819aea80cdc4b3dfdc57a5845ad42c8381d50276e03bbe0bc54fd6505bdea1`  
		Last Modified: Tue, 24 Mar 2026 18:26:26 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7fd235f9d6af1f1de07401bf789140114915144d0ef7c55f09f3f752f75bf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.6 MB (698608366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f038f83304efd437bc0cb703eab83ab9b3af57e61c1b767776867b20b9794a3a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:22:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:22:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:22:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:22:39 GMT
ARG TARGETARCH=arm64
# Tue, 24 Mar 2026 18:22:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:22:49 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:22:50 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:22:50 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:24:00 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:24:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:24:01 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:24:01 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:24:01 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:24:01 GMT
USER odoo
# Tue, 24 Mar 2026 18:24:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:24:01 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99263ff6a54dc45f69755c4b5bebb63bd750f1a9f24d114e0d07d9b78d7c475`  
		Last Modified: Tue, 24 Mar 2026 18:26:53 GMT  
		Size: 252.0 MB (251994807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e37ef8651bbf161b74a1a781e17dbe5f11a5dbaf94c0c02f13b7f874568f68`  
		Last Modified: Tue, 24 Mar 2026 18:26:45 GMT  
		Size: 14.3 MB (14340549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66d26a0f9f66bc39504c9263d7a34df393e8496ccddf8c8c7187d5de12ee10`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 479.6 KB (479647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704d6e8e2b3e7ce1697841db84f36b166078243adfea572cdce62089f1660eb0`  
		Last Modified: Tue, 24 Mar 2026 18:26:56 GMT  
		Size: 402.9 MB (402921216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf4703181900d352653f765f355525457ef820b84ddf78d6cf4279fef4f4412`  
		Last Modified: Tue, 24 Mar 2026 18:26:46 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440673301970e5d9e4ef2035bfee68045676bcaf590dcadf640739f5a380cfab`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa86dfe87dfdec50a3d4552326194a6c5f2f2dba239ba81cba0442dcf3c98f9c`  
		Last Modified: Tue, 24 Mar 2026 18:26:47 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f81e94985555848c2075cd2b59a5f028fff3c4485e026ca427954222dd7c96`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cb54d4b0353c8c399938b772e65f54910b79112f0c3a7723360f70c5554245d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69989421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1911a8e92ff2574621b89b3d42d3b000098902aac362efb62484730b6161d41`

```dockerfile
```

-	Layers:
	-	`sha256:499c9af97f16f4603b7e623ff73a2f797fd7cac68d1cf39ebbe25db403abc69d`  
		Last Modified: Tue, 24 Mar 2026 18:26:48 GMT  
		Size: 70.0 MB (69962165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9b5475841bfe9ad7bc7224b4718ee26cf464bd990217c3dd60a1cb5b555899`  
		Last Modified: Tue, 24 Mar 2026 18:26:44 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:3d000be2ba72ae244d0d1697fc3762b91d9a77a0ca913ca56412e9ace07057da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.4 MB (718419326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4059620278314767fbdc89bd6fd4f6d7085735783b639176b92bdff744f687e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 24 Mar 2026 18:20:52 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 24 Mar 2026 18:20:52 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 24 Mar 2026 18:20:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 24 Mar 2026 18:20:52 GMT
ARG TARGETARCH=ppc64le
# Tue, 24 Mar 2026 18:20:52 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 24 Mar 2026 18:21:07 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 24 Mar 2026 18:21:10 GMT
ENV ODOO_VERSION=19.0
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_RELEASE=20260324
# Tue, 24 Mar 2026 18:21:10 GMT
ARG ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
# Tue, 24 Mar 2026 18:23:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260324 ODOO_SHA=2d822b95d55931787cbaf2bd09f4f2d54b276b3d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 24 Mar 2026 18:23:36 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 24 Mar 2026 18:23:36 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 24 Mar 2026 18:23:36 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 24 Mar 2026 18:23:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 24 Mar 2026 18:23:37 GMT
USER odoo
# Tue, 24 Mar 2026 18:23:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 24 Mar 2026 18:23:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915164dd74f18bd04897fe989dbaf980d3f07e4767351cd00025bc6c1fb374b8`  
		Last Modified: Tue, 24 Mar 2026 18:28:47 GMT  
		Size: 265.1 MB (265109188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e0e387d453c47befff5578df88e0c36c14ae285f3ceb5418cbe53ce2b37f81`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 14.9 MB (14893001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfffa2c0db96bb28612d7e87eccf8756916bf1f024c6da84d894320cf564b01c`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 479.7 KB (479700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bde1ff247817cc1880639ab111508be52b8316bce1eea63961dd31ad249eec`  
		Last Modified: Tue, 24 Mar 2026 18:28:52 GMT  
		Size: 403.6 MB (403624947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5abc4486f63125bd3440c31d2080e58dc5be56518fd047def47f025d472b54`  
		Last Modified: Tue, 24 Mar 2026 18:28:37 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521d3d42bd797a4dcfde9977b1d803726efac45383b02bae04214d935a1f139`  
		Last Modified: Tue, 24 Mar 2026 18:28:38 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada80af41804fb9eff5edd599073dc01c0a074ea0803ce557397aa1e32ff703f`  
		Last Modified: Tue, 24 Mar 2026 18:28:39 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506e3a2863e861eab2021978f0a4876992ad8b66f17fc670554e06ae62ec9126`  
		Last Modified: Tue, 24 Mar 2026 18:28:40 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6e85b5ff8f4d536918a51c106f541029590c32ecefcb89816cf3a3f8155c21f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69990422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e08e3fc6c63de0ab79b7cb10b55231388c609546c1b7f59d0ca5f2b3ba972c7`

```dockerfile
```

-	Layers:
	-	`sha256:6f6fc43bcbee6845a9e1dc2ec8ef97380cd084a4e4ce6ecbf23ed740ce2c68c4`  
		Last Modified: Tue, 24 Mar 2026 18:28:41 GMT  
		Size: 70.0 MB (69963267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99604b9f76cf14194ce6adc3045ae2e1bd5016f61cd951869cf42761e6c98ca6`  
		Last Modified: Tue, 24 Mar 2026 18:28:36 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
