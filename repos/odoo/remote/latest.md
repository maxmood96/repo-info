## `odoo:latest`

```console
$ docker pull odoo@sha256:6bcde1e043fa2958261e93d594d52e2c1e48a5c3792049db8fc1883260f4ee2a
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
$ docker pull odoo@sha256:52cf57ad834635dda524f54b83c4122d3e978078e43e0d2f4e75f65914017e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.7 MB (703666740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609235d439be0af5d2525592bc349c049483bfc0899e487f18f4c3e2bfa1ca63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 17:21:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Apr 2026 17:21:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Apr 2026 17:21:33 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Apr 2026 17:21:33 GMT
ARG TARGETARCH=amd64
# Tue, 21 Apr 2026 17:21:33 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Apr 2026 17:21:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Apr 2026 17:21:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_RELEASE=20260421
# Tue, 21 Apr 2026 17:21:44 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:22:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:22:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:22:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:22:51 GMT
USER odoo
# Tue, 21 Apr 2026 17:22:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:22:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172bed374753b7d34f37336fb7f07ced6765e3d83829604935205879f27e0ed7`  
		Last Modified: Tue, 21 Apr 2026 17:25:05 GMT  
		Size: 254.6 MB (254568497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1864809b7d4219e675d42d2f7130c9b0227420b724437d3beadddb8041358b58`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 14.4 MB (14360070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2205f275b3232be9b2fc0cbb5f57701ebce6485a2fae1dba8ee9343c4dfeb4`  
		Last Modified: Tue, 21 Apr 2026 17:24:56 GMT  
		Size: 481.3 KB (481290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24f638d354288c212821ab5c7811b907019aa18a471c4c1189154b4589d179f`  
		Last Modified: Tue, 21 Apr 2026 17:25:10 GMT  
		Size: 404.5 MB (404521468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c87b03fd8e0de2c5b15193f281364be5b241e9822b7c1f7534b1c02759e27fd`  
		Last Modified: Tue, 21 Apr 2026 17:24:57 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31902119af4bc1da9e2f910e02747689265fc3cf204abb608763fff3505a7005`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8113e92c8545c9101f7466df56f33aaa1ea20cd5cb69200786cfbd0a8a17fc`  
		Last Modified: Tue, 21 Apr 2026 17:24:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaf672cf5f456330dbf337add3a0dc1a48b84d95c4b872f8c3453a37c79fd88`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9dcf127d541fb01a096cc6f3d7dc93ef21708941305975477489cecfe615269f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70275145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f4a0b8e917a359011bfa7b251c589a8ab89ace0ece3e5fff3d11126f4ae60`

```dockerfile
```

-	Layers:
	-	`sha256:19ff740e6a2ceec4039e5c50cf643f1ad7d3f234e6ba84e642ff65e9d98f9e98`  
		Last Modified: Tue, 21 Apr 2026 17:25:00 GMT  
		Size: 70.2 MB (70248052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d367f345ce6d068f39e8af1ba3b2dd60233c4a8d821e93226d04fd71bbcf49`  
		Last Modified: Tue, 21 Apr 2026 17:24:55 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d2b4159fe6fb112e0686828f9a55a2ff2c777394177a4ecbf2e98c6a317714b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700401382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7c9599287b5949dde981e617872d23e4cb6f6c7b941a9213bcbec291b794e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:55:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 04 May 2026 20:55:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 04 May 2026 20:55:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2026 20:55:20 GMT
ARG TARGETARCH=arm64
# Mon, 04 May 2026 20:55:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 04 May 2026 20:55:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 04 May 2026 20:55:31 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 04 May 2026 20:55:31 GMT
ENV ODOO_VERSION=19.0
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_RELEASE=20260504
# Mon, 04 May 2026 20:55:31 GMT
ARG ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
# Mon, 04 May 2026 20:56:41 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 04 May 2026 20:56:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 04 May 2026 20:56:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260504 ODOO_SHA=9e6a56cc743eba6f8f601e95531fb4bbb0937d6d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 04 May 2026 20:56:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 04 May 2026 20:56:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 04 May 2026 20:56:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 04 May 2026 20:56:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 04 May 2026 20:56:42 GMT
USER odoo
# Mon, 04 May 2026 20:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 20:56:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfbe06a8655e68e283ffa415711962461ef24e8bb7f5b0e957dd0c77c56278e`  
		Last Modified: Mon, 04 May 2026 20:59:23 GMT  
		Size: 252.0 MB (252026961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825256de54a2119a78af8163d89ef94499ba1c6c3e9bf9fb009f8ce3f0c43411`  
		Last Modified: Mon, 04 May 2026 20:59:17 GMT  
		Size: 14.3 MB (14340650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ef242c368ba28fe6f7a0e5ae6303a29f6c7e5ec83224606e11657470ecd0cd`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 483.9 KB (483863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e097d21c26d854bbe48616ff79f876185dc4ecd6f600fa1c3650e95bba56`  
		Last Modified: Mon, 04 May 2026 20:59:27 GMT  
		Size: 404.7 MB (404671680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907fcd37b9b1a4b3960584b8c545b9eab128cfa6835f0e18ff9061b1e06d751`  
		Last Modified: Mon, 04 May 2026 20:59:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0419b0ccf1c28c6456c6cf24aa168971479eaac8e96cdcc68536d309c2602353`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36544f610f976e03c177e5c4b9d5629838a32ca65ffaa377cdaa57a2f76aef88`  
		Last Modified: Mon, 04 May 2026 20:59:18 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220884be2085bd50f09074bdb2e0414b39b1b8586303edfc2780185dedf7ddd3`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c1182da1918aa059e00717814bb60047023b21bc15b607ec7581ec45caf33c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70342122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15b7cc62f2ee59c3f8cf65bc5fa2ed7babe77a5d938e81cc45c887813fe90d6`

```dockerfile
```

-	Layers:
	-	`sha256:ffe2846196af277c42c6ec660939f59ad9bab3c99d3e3900bda71524625665de`  
		Last Modified: Mon, 04 May 2026 20:59:19 GMT  
		Size: 70.3 MB (70314865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f5d1188af39072e10a6baf72247be46c625ca581b46df95a7775a07a8479ce`  
		Last Modified: Mon, 04 May 2026 20:59:15 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:72af05da350386e0d42832379ee18481bdb750d94b6d2f2e7005e0defdcf8ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **719.9 MB (719857359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d532ab52bfa3ac1bbfeb2e3ac16d1136d0032676b02874015cc13570d773b2b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:08:55 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 15 Apr 2026 22:08:55 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 15 Apr 2026 22:08:55 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 22:08:55 GMT
ARG TARGETARCH=ppc64le
# Wed, 15 Apr 2026 22:08:55 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 15 Apr 2026 22:09:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 15 Apr 2026 22:09:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_RELEASE=20260421
# Wed, 15 Apr 2026 22:09:12 GMT
ARG ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
# Tue, 21 Apr 2026 17:24:18 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Apr 2026 17:24:19 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Apr 2026 17:24:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260421 ODOO_SHA=f9e219b07a6abf5b272cd016f828a8f40ec82eb6
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Apr 2026 17:24:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Apr 2026 17:24:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Apr 2026 17:24:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Apr 2026 17:24:21 GMT
USER odoo
# Tue, 21 Apr 2026 17:24:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Apr 2026 17:24:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84509be6176ec39d6e149b3e4c7334728556b7265b514393d3be9707c47e3fb9`  
		Last Modified: Wed, 15 Apr 2026 22:17:50 GMT  
		Size: 265.1 MB (265110646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebab96b9feb025d4121daec1f27407bdaa5ac3fb4dc05e55c8f5f128b8948218`  
		Last Modified: Wed, 15 Apr 2026 22:17:38 GMT  
		Size: 14.9 MB (14893523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae81cfc17782f623ffadc48285626c21c2efd900ee3e52749cbe22753e63801`  
		Last Modified: Wed, 15 Apr 2026 22:17:37 GMT  
		Size: 481.4 KB (481425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddab69462fde54ff0c12c3ec9a466d95af5a4114d63852edd2d2f4d9ce6421b`  
		Last Modified: Tue, 21 Apr 2026 17:30:27 GMT  
		Size: 405.1 MB (405055149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eb53249213be84b13171cfb115879a0022c207b82404adf19de892075029b2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef0223c562e510689150ffa76cbb7d8182813e27ccc655cc8ec63f9c5e62357`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4405878df9790bbd22d6d9cd1bd0c4685eec81aa5ce9c05bcfaf4d63f349c2`  
		Last Modified: Tue, 21 Apr 2026 17:30:17 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c63c374e6a1886c43433768ffb5ecc6206a3737ba25566d386fb08428a4e9d5`  
		Last Modified: Tue, 21 Apr 2026 17:30:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:75578d361f1e0c972c0a2b59bf14fe8713c2efa7e3307493193a28c9e0551fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70283596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877a8ba587ce7564b500e80193c0591a4fca8413200b32c94292027b9d7d4798`

```dockerfile
```

-	Layers:
	-	`sha256:1e025bdb1a77fdf791aaadd376128beb15c63231828bfa520dab96d896f9382a`  
		Last Modified: Tue, 21 Apr 2026 17:30:20 GMT  
		Size: 70.3 MB (70256441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ad3c96249ff64dda4c9ff470c726f532078ff2e47fd7b680f9385645d79dcc`  
		Last Modified: Tue, 21 Apr 2026 17:30:16 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
