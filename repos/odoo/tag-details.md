<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260513`](#odoo170-20260513)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260513`](#odoo180-20260513)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260513`](#odoo190-20260513)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:85a2833df8d9ec8ddd6f6ec1038c8611e54fd60493f7f9bb8730197b473168df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:8fcf8de65b634bcb3b1ada3784c7c81f80b6c9ca61b06728b3f83b9c638bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610628557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2572140f0e23357a842d2e239e13a053430f22eef6023cbac65aca71fd6e3082`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 23:14:46 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:14:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:14:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:14:46 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:14:46 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:14:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:14:52 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:14:52 GMT
ENV ODOO_VERSION=17.0
# Wed, 13 May 2026 23:14:52 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:14:52 GMT
ARG ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
# Wed, 13 May 2026 23:15:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:15:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:15:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:15:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:15:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:15:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:15:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:15:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:15:41 GMT
USER odoo
# Wed, 13 May 2026 23:15:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:15:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95daa777901a8e7d2f4469ec22fcb9fc14e97f77ea2157d11b3b89ccd77306f9`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 233.8 MB (233834552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6daa7b9eca49ecd4946233f0fb5a1fe133144dbb13f9ab6d071259161307f1`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 2.6 MB (2603676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05dab60c91b44a2aca945c856fd8647507b53597da6e3f1cee2d9bf520c2ed`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 484.0 KB (484024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ef0a359ef4a155bd8027b5c3251243bd965f81214c83b4bd2718490ef887f`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 344.0 MB (343967014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a3efb123736fd0c31efa0255a995027a3b67be2452252442110f50ce83161`  
		Last Modified: Wed, 13 May 2026 23:16:52 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37099717fb05ca6a29b704a9fc19e8e4d5bcf79fe6a03f8781b3f1287f675fe`  
		Last Modified: Wed, 13 May 2026 23:16:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8642cdad078545a670695576541f598cda5b5a6f17351ac517921410ef90f48`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0453ef06c20fd9a2953e73deee900e55c9a2411317f84577c1c8c5ab1f9b928`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:562e66254247c5f20ed6b46f390cfe73595fec06f2ff055398b613094d1510d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42907684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4253bdf049785c92315dac4225bf77194b58034aa97c2bf4336faae7f0bad02b`

```dockerfile
```

-	Layers:
	-	`sha256:bb76dfd955035aabd21a7d345b879c57d6c9b6d3285a3759a46eac32e9df4b08`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 42.9 MB (42880881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2acc95965b2c380974b1bee3923a7ab64c26d7f652941111a8f1e16a9ed687`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 26.8 KB (26803 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:41d8f2d0eafc18f723fba0283fa200b3b45fb86bd688c1a4f79894dd146a2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.5 MB (605475420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c430de344c1ea5a1fdf93f1543a0218e2b32eeac67556b68616b239a95d918d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 23:14:26 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:14:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:14:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:14:26 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:14:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:14:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:14:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:14:35 GMT
ENV ODOO_VERSION=17.0
# Wed, 13 May 2026 23:14:35 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:14:35 GMT
ARG ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
# Wed, 13 May 2026 23:15:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:15:39 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:15:39 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:15:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:15:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:15:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:15:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:15:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:15:40 GMT
USER odoo
# Wed, 13 May 2026 23:15:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:15:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6456f79dbf0d590c6e46c0d484d7b937bf445dae582e062d9b8e5433ac581a`  
		Last Modified: Wed, 13 May 2026 23:17:09 GMT  
		Size: 231.2 MB (231203127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c1e3469a5c08bb753c3415b91182ee5286f256ef80611edf49f0515e9184d`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 2.6 MB (2598084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d27bab19fd35237f6323ccb8da8001abc3587a792c6dbca56038c2567976c3b`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 484.0 KB (484020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948b7460573c346710b466c4fd6afb4371bdc310e6b3a6718d958596f5106542`  
		Last Modified: Wed, 13 May 2026 23:17:12 GMT  
		Size: 343.6 MB (343580854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161570f5ddcfcf6fea7a76140d74e37c547ce0eb15b3b7fffe08ff0e0c98c86`  
		Last Modified: Wed, 13 May 2026 23:17:02 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f27e63488627aacb2d05ee85add86cd89107e1b0f77bbdaf10592c7bdfcd2f`  
		Last Modified: Wed, 13 May 2026 23:17:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c7eedc1ac8a10fa1577b49d84067d0cbf06905ca3554216323a6d21f53bb5`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d5d87863e725a9105e9d89d6e1d7f5908a2cdce8d3010f8b3f400263a95ce2`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:173aee288f4d2ce716252406d9921af5702fb3e3107d3786a8ef86160eac4dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42914344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100a383782b88900fad4c4dfa2fc079aa78263c92d3dc52e1aefde37942054ec`

```dockerfile
```

-	Layers:
	-	`sha256:57ed28f2d338775432b9c9a5641ddf8f3cf4bddda0e4afac3a32c16fbd9b6302`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 42.9 MB (42887388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b340b470e1708bf44c8ea6d8a466eabc0e322d9231d00a49306f67f086c4d9`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:85a2833df8d9ec8ddd6f6ec1038c8611e54fd60493f7f9bb8730197b473168df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:8fcf8de65b634bcb3b1ada3784c7c81f80b6c9ca61b06728b3f83b9c638bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610628557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2572140f0e23357a842d2e239e13a053430f22eef6023cbac65aca71fd6e3082`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 23:14:46 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:14:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:14:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:14:46 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:14:46 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:14:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:14:52 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:14:52 GMT
ENV ODOO_VERSION=17.0
# Wed, 13 May 2026 23:14:52 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:14:52 GMT
ARG ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
# Wed, 13 May 2026 23:15:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:15:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:15:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:15:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:15:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:15:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:15:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:15:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:15:41 GMT
USER odoo
# Wed, 13 May 2026 23:15:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:15:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95daa777901a8e7d2f4469ec22fcb9fc14e97f77ea2157d11b3b89ccd77306f9`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 233.8 MB (233834552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6daa7b9eca49ecd4946233f0fb5a1fe133144dbb13f9ab6d071259161307f1`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 2.6 MB (2603676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05dab60c91b44a2aca945c856fd8647507b53597da6e3f1cee2d9bf520c2ed`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 484.0 KB (484024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ef0a359ef4a155bd8027b5c3251243bd965f81214c83b4bd2718490ef887f`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 344.0 MB (343967014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a3efb123736fd0c31efa0255a995027a3b67be2452252442110f50ce83161`  
		Last Modified: Wed, 13 May 2026 23:16:52 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37099717fb05ca6a29b704a9fc19e8e4d5bcf79fe6a03f8781b3f1287f675fe`  
		Last Modified: Wed, 13 May 2026 23:16:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8642cdad078545a670695576541f598cda5b5a6f17351ac517921410ef90f48`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0453ef06c20fd9a2953e73deee900e55c9a2411317f84577c1c8c5ab1f9b928`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:562e66254247c5f20ed6b46f390cfe73595fec06f2ff055398b613094d1510d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42907684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4253bdf049785c92315dac4225bf77194b58034aa97c2bf4336faae7f0bad02b`

```dockerfile
```

-	Layers:
	-	`sha256:bb76dfd955035aabd21a7d345b879c57d6c9b6d3285a3759a46eac32e9df4b08`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 42.9 MB (42880881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2acc95965b2c380974b1bee3923a7ab64c26d7f652941111a8f1e16a9ed687`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 26.8 KB (26803 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:41d8f2d0eafc18f723fba0283fa200b3b45fb86bd688c1a4f79894dd146a2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.5 MB (605475420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c430de344c1ea5a1fdf93f1543a0218e2b32eeac67556b68616b239a95d918d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 23:14:26 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:14:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:14:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:14:26 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:14:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:14:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:14:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:14:35 GMT
ENV ODOO_VERSION=17.0
# Wed, 13 May 2026 23:14:35 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:14:35 GMT
ARG ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
# Wed, 13 May 2026 23:15:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:15:39 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:15:39 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:15:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:15:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:15:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:15:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:15:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:15:40 GMT
USER odoo
# Wed, 13 May 2026 23:15:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:15:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6456f79dbf0d590c6e46c0d484d7b937bf445dae582e062d9b8e5433ac581a`  
		Last Modified: Wed, 13 May 2026 23:17:09 GMT  
		Size: 231.2 MB (231203127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c1e3469a5c08bb753c3415b91182ee5286f256ef80611edf49f0515e9184d`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 2.6 MB (2598084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d27bab19fd35237f6323ccb8da8001abc3587a792c6dbca56038c2567976c3b`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 484.0 KB (484020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948b7460573c346710b466c4fd6afb4371bdc310e6b3a6718d958596f5106542`  
		Last Modified: Wed, 13 May 2026 23:17:12 GMT  
		Size: 343.6 MB (343580854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161570f5ddcfcf6fea7a76140d74e37c547ce0eb15b3b7fffe08ff0e0c98c86`  
		Last Modified: Wed, 13 May 2026 23:17:02 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f27e63488627aacb2d05ee85add86cd89107e1b0f77bbdaf10592c7bdfcd2f`  
		Last Modified: Wed, 13 May 2026 23:17:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c7eedc1ac8a10fa1577b49d84067d0cbf06905ca3554216323a6d21f53bb5`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d5d87863e725a9105e9d89d6e1d7f5908a2cdce8d3010f8b3f400263a95ce2`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:173aee288f4d2ce716252406d9921af5702fb3e3107d3786a8ef86160eac4dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42914344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100a383782b88900fad4c4dfa2fc079aa78263c92d3dc52e1aefde37942054ec`

```dockerfile
```

-	Layers:
	-	`sha256:57ed28f2d338775432b9c9a5641ddf8f3cf4bddda0e4afac3a32c16fbd9b6302`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 42.9 MB (42887388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b340b470e1708bf44c8ea6d8a466eabc0e322d9231d00a49306f67f086c4d9`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260513`

```console
$ docker pull odoo@sha256:85a2833df8d9ec8ddd6f6ec1038c8611e54fd60493f7f9bb8730197b473168df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260513` - linux; amd64

```console
$ docker pull odoo@sha256:8fcf8de65b634bcb3b1ada3784c7c81f80b6c9ca61b06728b3f83b9c638bb16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **610.6 MB (610628557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2572140f0e23357a842d2e239e13a053430f22eef6023cbac65aca71fd6e3082`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 23:14:46 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:14:46 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:14:46 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:14:46 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:14:46 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:14:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:14:52 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:14:52 GMT
ENV ODOO_VERSION=17.0
# Wed, 13 May 2026 23:14:52 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:14:52 GMT
ARG ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
# Wed, 13 May 2026 23:15:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:15:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:15:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:15:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:15:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:15:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:15:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:15:41 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:15:41 GMT
USER odoo
# Wed, 13 May 2026 23:15:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:15:41 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95daa777901a8e7d2f4469ec22fcb9fc14e97f77ea2157d11b3b89ccd77306f9`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 233.8 MB (233834552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6daa7b9eca49ecd4946233f0fb5a1fe133144dbb13f9ab6d071259161307f1`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 2.6 MB (2603676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05dab60c91b44a2aca945c856fd8647507b53597da6e3f1cee2d9bf520c2ed`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 484.0 KB (484024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168ef0a359ef4a155bd8027b5c3251243bd965f81214c83b4bd2718490ef887f`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 344.0 MB (343967014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a3efb123736fd0c31efa0255a995027a3b67be2452252442110f50ce83161`  
		Last Modified: Wed, 13 May 2026 23:16:52 GMT  
		Size: 764.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37099717fb05ca6a29b704a9fc19e8e4d5bcf79fe6a03f8781b3f1287f675fe`  
		Last Modified: Wed, 13 May 2026 23:16:53 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8642cdad078545a670695576541f598cda5b5a6f17351ac517921410ef90f48`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0453ef06c20fd9a2953e73deee900e55c9a2411317f84577c1c8c5ab1f9b928`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:562e66254247c5f20ed6b46f390cfe73595fec06f2ff055398b613094d1510d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42907684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4253bdf049785c92315dac4225bf77194b58034aa97c2bf4336faae7f0bad02b`

```dockerfile
```

-	Layers:
	-	`sha256:bb76dfd955035aabd21a7d345b879c57d6c9b6d3285a3759a46eac32e9df4b08`  
		Last Modified: Wed, 13 May 2026 23:16:54 GMT  
		Size: 42.9 MB (42880881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2acc95965b2c380974b1bee3923a7ab64c26d7f652941111a8f1e16a9ed687`  
		Last Modified: Wed, 13 May 2026 23:16:51 GMT  
		Size: 26.8 KB (26803 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260513` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:41d8f2d0eafc18f723fba0283fa200b3b45fb86bd688c1a4f79894dd146a2b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.5 MB (605475420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c430de344c1ea5a1fdf93f1543a0218e2b32eeac67556b68616b239a95d918d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 23:14:26 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:14:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:14:26 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:14:26 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:14:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:14:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:14:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:14:35 GMT
ENV ODOO_VERSION=17.0
# Wed, 13 May 2026 23:14:35 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:14:35 GMT
ARG ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
# Wed, 13 May 2026 23:15:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:15:39 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:15:39 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:15:39 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=e4643d0e5f868abeade3920bc3d2009a063ae526
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:15:39 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:15:39 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:15:39 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:15:40 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:15:40 GMT
USER odoo
# Wed, 13 May 2026 23:15:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:15:40 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6456f79dbf0d590c6e46c0d484d7b937bf445dae582e062d9b8e5433ac581a`  
		Last Modified: Wed, 13 May 2026 23:17:09 GMT  
		Size: 231.2 MB (231203127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c1e3469a5c08bb753c3415b91182ee5286f256ef80611edf49f0515e9184d`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 2.6 MB (2598084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d27bab19fd35237f6323ccb8da8001abc3587a792c6dbca56038c2567976c3b`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 484.0 KB (484020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948b7460573c346710b466c4fd6afb4371bdc310e6b3a6718d958596f5106542`  
		Last Modified: Wed, 13 May 2026 23:17:12 GMT  
		Size: 343.6 MB (343580854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161570f5ddcfcf6fea7a76140d74e37c547ce0eb15b3b7fffe08ff0e0c98c86`  
		Last Modified: Wed, 13 May 2026 23:17:02 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f27e63488627aacb2d05ee85add86cd89107e1b0f77bbdaf10592c7bdfcd2f`  
		Last Modified: Wed, 13 May 2026 23:17:02 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c7eedc1ac8a10fa1577b49d84067d0cbf06905ca3554216323a6d21f53bb5`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d5d87863e725a9105e9d89d6e1d7f5908a2cdce8d3010f8b3f400263a95ce2`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:173aee288f4d2ce716252406d9921af5702fb3e3107d3786a8ef86160eac4dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42914344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100a383782b88900fad4c4dfa2fc079aa78263c92d3dc52e1aefde37942054ec`

```dockerfile
```

-	Layers:
	-	`sha256:57ed28f2d338775432b9c9a5641ddf8f3cf4bddda0e4afac3a32c16fbd9b6302`  
		Last Modified: Wed, 13 May 2026 23:17:03 GMT  
		Size: 42.9 MB (42887388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b340b470e1708bf44c8ea6d8a466eabc0e322d9231d00a49306f67f086c4d9`  
		Last Modified: Wed, 13 May 2026 23:17:00 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:b9fad113ae0274da19b769db65193bfdbcd1993128acd8b708bc842cbd7f4185
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
$ docker pull odoo@sha256:80dcc5ae4ad30a082d1f8b9415cf52dc8f477bd075d6d5c2f8e2640184a363d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.0 MB (684971764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b49b2f34953ea2a202d035409e4fc86227afd12d048afac1c327c5c03430bb`
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
# Wed, 13 May 2026 23:12:21 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:12:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:12:21 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:12:21 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:12:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:12:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:12:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:12:28 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:12:28 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:12:28 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:13:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:13:19 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:13:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:13:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:13:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:13:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:13:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:13:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:13:19 GMT
USER odoo
# Wed, 13 May 2026 23:13:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:13:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01196835f09e19d0903f4efdfafed98bf44b937dee848b945a629ddf7b2e440e`  
		Last Modified: Wed, 13 May 2026 23:15:16 GMT  
		Size: 254.6 MB (254596842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f39ab5e8027ca71d6fa967af34ffe2b7856743118253ce8c69f2d39252f4d69`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 14.4 MB (14360002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e0d61f6264be97cc7e92f38e63236f4711ac23ba06066aeef5972cdb39b134`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 483.8 KB (483763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef57ee3f951fd1916debfa1debe0fd8018e45d24a073ef6021353ceb6bbaada3`  
		Last Modified: Wed, 13 May 2026 23:15:18 GMT  
		Size: 385.8 MB (385795386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3e45580668d112aee8376e8d0842adeff29ab70f93169ea52abdfbb7619e3c`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e689396a77cf10b5cf85a2cad92b23296c8894007f7792b91070315217ebb7e`  
		Last Modified: Wed, 13 May 2026 23:15:08 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75629587342d0d9ecb36cb17a73b71e7838a364a881fb6000e4c5106b2450d36`  
		Last Modified: Wed, 13 May 2026 23:15:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482fff9dbcaf8c8646acab831e63e5a1e031ea12acd0f9ad6594535824839e5`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1aedec591a9ffca1504d10c810b12af43a1b1563714b7a7e9ed91b24b3ec44f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62295154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476bf359878beb67a9fad36ccad8380300d57f0bdf3469d8dae5fdb0b66ec01`

```dockerfile
```

-	Layers:
	-	`sha256:ed794cfc75c8bd48bd2c669cf71a1893da566856a24a3bdc9d9b518abdb20755`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 62.3 MB (62268343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9839228d0eab81350ba6231b156fc432a952604fe989f93702e206ccf90da01`  
		Last Modified: Wed, 13 May 2026 23:15:05 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:bebbb1f75848a2cd614809a9d1c3ea8ac67f07c01770e2a358ce3ea738aad944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.4 MB (681352324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31284c9e7d94c30ad7a1536181d69c3f754a1a7e6e423dd898b0a6e304379282`
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
# Wed, 13 May 2026 23:12:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:12:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:12:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:12:10 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:12:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:12:23 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:12:24 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:12:24 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:12:24 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:12:24 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:13:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:13:27 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:13:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:13:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:13:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:13:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:13:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:13:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:13:27 GMT
USER odoo
# Wed, 13 May 2026 23:13:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:13:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80c8b30e059e7043e8bca779e3a511077ae53bb8bb8aaa45d68b5fae41887a0`  
		Last Modified: Wed, 13 May 2026 23:15:54 GMT  
		Size: 252.0 MB (252025938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eda35117a833d8f229ed8d00a34f199a5e167415e65c75654e66487bc27d27`  
		Last Modified: Wed, 13 May 2026 23:15:41 GMT  
		Size: 14.3 MB (14340715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebad5085c0014ee64eb39f94a846755216026ba66f60f96a1b8b4eafa2dc62`  
		Last Modified: Wed, 13 May 2026 23:15:40 GMT  
		Size: 483.8 KB (483765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f4e420f102eacc660e939a58c83469e9f3a1af509979ad1eb4850e5144c698`  
		Last Modified: Wed, 13 May 2026 23:15:57 GMT  
		Size: 385.6 MB (385623326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e379665954b9eb040d36ec2821d037ebaf8a8cc72efdec2e031748a2fbdb859`  
		Last Modified: Wed, 13 May 2026 23:15:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42192f5fb822f7cccff1718c4ce03e0f7a661fd3a87d80a110da25bc881b2a97`  
		Last Modified: Wed, 13 May 2026 23:15:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a909c1663197952e16b8694458d050d11a911a53d15da6e330c872010cf708`  
		Last Modified: Wed, 13 May 2026 23:15:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ffc6b9eea4adea0565ab93939a19a8780a0a4d197dbfc562a7d51505452506`  
		Last Modified: Wed, 13 May 2026 23:15:44 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:8ec17592aa07a7d082f1ae045fda85ba5c4c04a8a6dda3458c2f44181d1fb846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62302581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898c5a5120ce6a25e6add2c6da34b0ec8537af0e36c15df449f3845643a37a37`

```dockerfile
```

-	Layers:
	-	`sha256:286a268334f7ae8b4906d723d25854e56e1815d4269b77cf8b76b1d60e59d12c`  
		Last Modified: Wed, 13 May 2026 23:15:44 GMT  
		Size: 62.3 MB (62275618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e280f6544603bdf398c5d7082709d5d01a598c587cde521ae05373294984472a`  
		Last Modified: Wed, 13 May 2026 23:15:40 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:e8e9459464f365c717a812fb19c7b05b72a01b6424d82a89ef58c80a1b3cbd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.1 MB (701122044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9958b7029b6e41a6f6258b041146b4e43df064636a968ea8b1fac79d14d205a`
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
# Wed, 13 May 2026 23:16:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:16:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:16:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:16:53 GMT
ARG TARGETARCH=ppc64le
# Wed, 13 May 2026 23:16:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:17:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:17:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:17:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:19:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:19:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:19:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:19:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:19:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:19:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:19:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:19:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:19:50 GMT
USER odoo
# Wed, 13 May 2026 23:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:19:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62faddfdfc852ed57a1f0f8439ea047ac9998c9a1bea1eb00e172cc3c9e39ed5`  
		Last Modified: Wed, 13 May 2026 23:25:09 GMT  
		Size: 265.1 MB (265099080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3d5329e6b271b46c68a19793b52687b3fa7d8716dce8455f3d7cd0c6dca244`  
		Last Modified: Wed, 13 May 2026 23:24:56 GMT  
		Size: 14.9 MB (14893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51430c34240175a60a1c25df4ab66a29e484cc7d6df935ae048fdb4d22b5d226`  
		Last Modified: Wed, 13 May 2026 23:24:54 GMT  
		Size: 483.9 KB (483900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f057466943359e2d9be6e944679614274b172365fa4db8f9947a4e6077ce16da`  
		Last Modified: Wed, 13 May 2026 23:25:12 GMT  
		Size: 386.3 MB (386328171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feae93163670807fe6057b0e550a8bc668016106f52160cabf739e314a2bd066`  
		Last Modified: Wed, 13 May 2026 23:24:55 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbc17332dd684ba26e6780fd04333b97362511a39941d724fa4d8997bb058aa`  
		Last Modified: Wed, 13 May 2026 23:24:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625e98c364f43719c6512912d9f8ff207e8ae5f03c0fd3a8d9656b66348ad0a`  
		Last Modified: Wed, 13 May 2026 23:24:57 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd3de01479716e18c3115260e1f056874139ff4bf96b9bdcaa035f84d716497`  
		Last Modified: Wed, 13 May 2026 23:24:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:be66e10b6fee6a4e884ea401d93c5c1745fc1b478d94ddddf8538f507b39a8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861a4d0c979a273ef2fbda1c2ad83947b784959e7a0a2f43754b4696aa343261`

```dockerfile
```

-	Layers:
	-	`sha256:b48b30b39c332c342fbc2ccb3eda2c80634cb537ec1e76e5d607635c3a84ece0`  
		Last Modified: Wed, 13 May 2026 23:24:59 GMT  
		Size: 62.3 MB (62276726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de37a96e26a00b52253e7369b1335105ca61add6ca6c6e349d6dbbbe361b742b`  
		Last Modified: Wed, 13 May 2026 23:24:53 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:b9fad113ae0274da19b769db65193bfdbcd1993128acd8b708bc842cbd7f4185
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
$ docker pull odoo@sha256:80dcc5ae4ad30a082d1f8b9415cf52dc8f477bd075d6d5c2f8e2640184a363d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.0 MB (684971764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b49b2f34953ea2a202d035409e4fc86227afd12d048afac1c327c5c03430bb`
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
# Wed, 13 May 2026 23:12:21 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:12:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:12:21 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:12:21 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:12:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:12:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:12:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:12:28 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:12:28 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:12:28 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:13:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:13:19 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:13:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:13:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:13:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:13:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:13:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:13:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:13:19 GMT
USER odoo
# Wed, 13 May 2026 23:13:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:13:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01196835f09e19d0903f4efdfafed98bf44b937dee848b945a629ddf7b2e440e`  
		Last Modified: Wed, 13 May 2026 23:15:16 GMT  
		Size: 254.6 MB (254596842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f39ab5e8027ca71d6fa967af34ffe2b7856743118253ce8c69f2d39252f4d69`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 14.4 MB (14360002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e0d61f6264be97cc7e92f38e63236f4711ac23ba06066aeef5972cdb39b134`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 483.8 KB (483763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef57ee3f951fd1916debfa1debe0fd8018e45d24a073ef6021353ceb6bbaada3`  
		Last Modified: Wed, 13 May 2026 23:15:18 GMT  
		Size: 385.8 MB (385795386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3e45580668d112aee8376e8d0842adeff29ab70f93169ea52abdfbb7619e3c`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e689396a77cf10b5cf85a2cad92b23296c8894007f7792b91070315217ebb7e`  
		Last Modified: Wed, 13 May 2026 23:15:08 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75629587342d0d9ecb36cb17a73b71e7838a364a881fb6000e4c5106b2450d36`  
		Last Modified: Wed, 13 May 2026 23:15:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482fff9dbcaf8c8646acab831e63e5a1e031ea12acd0f9ad6594535824839e5`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1aedec591a9ffca1504d10c810b12af43a1b1563714b7a7e9ed91b24b3ec44f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62295154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476bf359878beb67a9fad36ccad8380300d57f0bdf3469d8dae5fdb0b66ec01`

```dockerfile
```

-	Layers:
	-	`sha256:ed794cfc75c8bd48bd2c669cf71a1893da566856a24a3bdc9d9b518abdb20755`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 62.3 MB (62268343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9839228d0eab81350ba6231b156fc432a952604fe989f93702e206ccf90da01`  
		Last Modified: Wed, 13 May 2026 23:15:05 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:bebbb1f75848a2cd614809a9d1c3ea8ac67f07c01770e2a358ce3ea738aad944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.4 MB (681352324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31284c9e7d94c30ad7a1536181d69c3f754a1a7e6e423dd898b0a6e304379282`
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
# Wed, 13 May 2026 23:12:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:12:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:12:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:12:10 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:12:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:12:23 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:12:24 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:12:24 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:12:24 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:12:24 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:13:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:13:27 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:13:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:13:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:13:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:13:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:13:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:13:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:13:27 GMT
USER odoo
# Wed, 13 May 2026 23:13:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:13:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80c8b30e059e7043e8bca779e3a511077ae53bb8bb8aaa45d68b5fae41887a0`  
		Last Modified: Wed, 13 May 2026 23:15:54 GMT  
		Size: 252.0 MB (252025938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eda35117a833d8f229ed8d00a34f199a5e167415e65c75654e66487bc27d27`  
		Last Modified: Wed, 13 May 2026 23:15:41 GMT  
		Size: 14.3 MB (14340715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebad5085c0014ee64eb39f94a846755216026ba66f60f96a1b8b4eafa2dc62`  
		Last Modified: Wed, 13 May 2026 23:15:40 GMT  
		Size: 483.8 KB (483765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f4e420f102eacc660e939a58c83469e9f3a1af509979ad1eb4850e5144c698`  
		Last Modified: Wed, 13 May 2026 23:15:57 GMT  
		Size: 385.6 MB (385623326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e379665954b9eb040d36ec2821d037ebaf8a8cc72efdec2e031748a2fbdb859`  
		Last Modified: Wed, 13 May 2026 23:15:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42192f5fb822f7cccff1718c4ce03e0f7a661fd3a87d80a110da25bc881b2a97`  
		Last Modified: Wed, 13 May 2026 23:15:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a909c1663197952e16b8694458d050d11a911a53d15da6e330c872010cf708`  
		Last Modified: Wed, 13 May 2026 23:15:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ffc6b9eea4adea0565ab93939a19a8780a0a4d197dbfc562a7d51505452506`  
		Last Modified: Wed, 13 May 2026 23:15:44 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8ec17592aa07a7d082f1ae045fda85ba5c4c04a8a6dda3458c2f44181d1fb846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62302581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898c5a5120ce6a25e6add2c6da34b0ec8537af0e36c15df449f3845643a37a37`

```dockerfile
```

-	Layers:
	-	`sha256:286a268334f7ae8b4906d723d25854e56e1815d4269b77cf8b76b1d60e59d12c`  
		Last Modified: Wed, 13 May 2026 23:15:44 GMT  
		Size: 62.3 MB (62275618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e280f6544603bdf398c5d7082709d5d01a598c587cde521ae05373294984472a`  
		Last Modified: Wed, 13 May 2026 23:15:40 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:e8e9459464f365c717a812fb19c7b05b72a01b6424d82a89ef58c80a1b3cbd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.1 MB (701122044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9958b7029b6e41a6f6258b041146b4e43df064636a968ea8b1fac79d14d205a`
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
# Wed, 13 May 2026 23:16:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:16:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:16:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:16:53 GMT
ARG TARGETARCH=ppc64le
# Wed, 13 May 2026 23:16:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:17:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:17:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:17:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:19:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:19:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:19:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:19:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:19:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:19:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:19:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:19:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:19:50 GMT
USER odoo
# Wed, 13 May 2026 23:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:19:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62faddfdfc852ed57a1f0f8439ea047ac9998c9a1bea1eb00e172cc3c9e39ed5`  
		Last Modified: Wed, 13 May 2026 23:25:09 GMT  
		Size: 265.1 MB (265099080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3d5329e6b271b46c68a19793b52687b3fa7d8716dce8455f3d7cd0c6dca244`  
		Last Modified: Wed, 13 May 2026 23:24:56 GMT  
		Size: 14.9 MB (14893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51430c34240175a60a1c25df4ab66a29e484cc7d6df935ae048fdb4d22b5d226`  
		Last Modified: Wed, 13 May 2026 23:24:54 GMT  
		Size: 483.9 KB (483900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f057466943359e2d9be6e944679614274b172365fa4db8f9947a4e6077ce16da`  
		Last Modified: Wed, 13 May 2026 23:25:12 GMT  
		Size: 386.3 MB (386328171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feae93163670807fe6057b0e550a8bc668016106f52160cabf739e314a2bd066`  
		Last Modified: Wed, 13 May 2026 23:24:55 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbc17332dd684ba26e6780fd04333b97362511a39941d724fa4d8997bb058aa`  
		Last Modified: Wed, 13 May 2026 23:24:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625e98c364f43719c6512912d9f8ff207e8ae5f03c0fd3a8d9656b66348ad0a`  
		Last Modified: Wed, 13 May 2026 23:24:57 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd3de01479716e18c3115260e1f056874139ff4bf96b9bdcaa035f84d716497`  
		Last Modified: Wed, 13 May 2026 23:24:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:be66e10b6fee6a4e884ea401d93c5c1745fc1b478d94ddddf8538f507b39a8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861a4d0c979a273ef2fbda1c2ad83947b784959e7a0a2f43754b4696aa343261`

```dockerfile
```

-	Layers:
	-	`sha256:b48b30b39c332c342fbc2ccb3eda2c80634cb537ec1e76e5d607635c3a84ece0`  
		Last Modified: Wed, 13 May 2026 23:24:59 GMT  
		Size: 62.3 MB (62276726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de37a96e26a00b52253e7369b1335105ca61add6ca6c6e349d6dbbbe361b742b`  
		Last Modified: Wed, 13 May 2026 23:24:53 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260513`

```console
$ docker pull odoo@sha256:b9fad113ae0274da19b769db65193bfdbcd1993128acd8b708bc842cbd7f4185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260513` - linux; amd64

```console
$ docker pull odoo@sha256:80dcc5ae4ad30a082d1f8b9415cf52dc8f477bd075d6d5c2f8e2640184a363d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.0 MB (684971764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b49b2f34953ea2a202d035409e4fc86227afd12d048afac1c327c5c03430bb`
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
# Wed, 13 May 2026 23:12:21 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:12:21 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:12:21 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:12:21 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:12:21 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:12:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:12:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:12:28 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:12:28 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:12:28 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:13:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:13:19 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:13:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:13:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:13:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:13:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:13:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:13:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:13:19 GMT
USER odoo
# Wed, 13 May 2026 23:13:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:13:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01196835f09e19d0903f4efdfafed98bf44b937dee848b945a629ddf7b2e440e`  
		Last Modified: Wed, 13 May 2026 23:15:16 GMT  
		Size: 254.6 MB (254596842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f39ab5e8027ca71d6fa967af34ffe2b7856743118253ce8c69f2d39252f4d69`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 14.4 MB (14360002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e0d61f6264be97cc7e92f38e63236f4711ac23ba06066aeef5972cdb39b134`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 483.8 KB (483763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef57ee3f951fd1916debfa1debe0fd8018e45d24a073ef6021353ceb6bbaada3`  
		Last Modified: Wed, 13 May 2026 23:15:18 GMT  
		Size: 385.8 MB (385795386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3e45580668d112aee8376e8d0842adeff29ab70f93169ea52abdfbb7619e3c`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e689396a77cf10b5cf85a2cad92b23296c8894007f7792b91070315217ebb7e`  
		Last Modified: Wed, 13 May 2026 23:15:08 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75629587342d0d9ecb36cb17a73b71e7838a364a881fb6000e4c5106b2450d36`  
		Last Modified: Wed, 13 May 2026 23:15:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482fff9dbcaf8c8646acab831e63e5a1e031ea12acd0f9ad6594535824839e5`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:1aedec591a9ffca1504d10c810b12af43a1b1563714b7a7e9ed91b24b3ec44f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62295154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f476bf359878beb67a9fad36ccad8380300d57f0bdf3469d8dae5fdb0b66ec01`

```dockerfile
```

-	Layers:
	-	`sha256:ed794cfc75c8bd48bd2c669cf71a1893da566856a24a3bdc9d9b518abdb20755`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 62.3 MB (62268343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9839228d0eab81350ba6231b156fc432a952604fe989f93702e206ccf90da01`  
		Last Modified: Wed, 13 May 2026 23:15:05 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260513` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:bebbb1f75848a2cd614809a9d1c3ea8ac67f07c01770e2a358ce3ea738aad944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.4 MB (681352324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31284c9e7d94c30ad7a1536181d69c3f754a1a7e6e423dd898b0a6e304379282`
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
# Wed, 13 May 2026 23:12:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:12:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:12:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:12:10 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:12:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:12:23 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:12:24 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:12:24 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:12:24 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:12:24 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:13:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:13:27 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:13:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:13:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:13:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:13:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:13:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:13:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:13:27 GMT
USER odoo
# Wed, 13 May 2026 23:13:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:13:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80c8b30e059e7043e8bca779e3a511077ae53bb8bb8aaa45d68b5fae41887a0`  
		Last Modified: Wed, 13 May 2026 23:15:54 GMT  
		Size: 252.0 MB (252025938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50eda35117a833d8f229ed8d00a34f199a5e167415e65c75654e66487bc27d27`  
		Last Modified: Wed, 13 May 2026 23:15:41 GMT  
		Size: 14.3 MB (14340715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ebad5085c0014ee64eb39f94a846755216026ba66f60f96a1b8b4eafa2dc62`  
		Last Modified: Wed, 13 May 2026 23:15:40 GMT  
		Size: 483.8 KB (483765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f4e420f102eacc660e939a58c83469e9f3a1af509979ad1eb4850e5144c698`  
		Last Modified: Wed, 13 May 2026 23:15:57 GMT  
		Size: 385.6 MB (385623326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e379665954b9eb040d36ec2821d037ebaf8a8cc72efdec2e031748a2fbdb859`  
		Last Modified: Wed, 13 May 2026 23:15:42 GMT  
		Size: 765.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42192f5fb822f7cccff1718c4ce03e0f7a661fd3a87d80a110da25bc881b2a97`  
		Last Modified: Wed, 13 May 2026 23:15:43 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a909c1663197952e16b8694458d050d11a911a53d15da6e330c872010cf708`  
		Last Modified: Wed, 13 May 2026 23:15:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ffc6b9eea4adea0565ab93939a19a8780a0a4d197dbfc562a7d51505452506`  
		Last Modified: Wed, 13 May 2026 23:15:44 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:8ec17592aa07a7d082f1ae045fda85ba5c4c04a8a6dda3458c2f44181d1fb846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62302581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898c5a5120ce6a25e6add2c6da34b0ec8537af0e36c15df449f3845643a37a37`

```dockerfile
```

-	Layers:
	-	`sha256:286a268334f7ae8b4906d723d25854e56e1815d4269b77cf8b76b1d60e59d12c`  
		Last Modified: Wed, 13 May 2026 23:15:44 GMT  
		Size: 62.3 MB (62275618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e280f6544603bdf398c5d7082709d5d01a598c587cde521ae05373294984472a`  
		Last Modified: Wed, 13 May 2026 23:15:40 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260513` - linux; ppc64le

```console
$ docker pull odoo@sha256:e8e9459464f365c717a812fb19c7b05b72a01b6424d82a89ef58c80a1b3cbd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.1 MB (701122044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9958b7029b6e41a6f6258b041146b4e43df064636a968ea8b1fac79d14d205a`
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
# Wed, 13 May 2026 23:16:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:16:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:16:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:16:53 GMT
ARG TARGETARCH=ppc64le
# Wed, 13 May 2026 23:16:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:17:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:17:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:17:12 GMT
ENV ODOO_VERSION=18.0
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
# Wed, 13 May 2026 23:19:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:19:49 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:19:50 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:19:50 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=d38a0f9db707d146d8aea3315bf53303fe7784e9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:19:50 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:19:50 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:19:50 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:19:50 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:19:50 GMT
USER odoo
# Wed, 13 May 2026 23:19:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:19:50 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62faddfdfc852ed57a1f0f8439ea047ac9998c9a1bea1eb00e172cc3c9e39ed5`  
		Last Modified: Wed, 13 May 2026 23:25:09 GMT  
		Size: 265.1 MB (265099080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3d5329e6b271b46c68a19793b52687b3fa7d8716dce8455f3d7cd0c6dca244`  
		Last Modified: Wed, 13 May 2026 23:24:56 GMT  
		Size: 14.9 MB (14893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51430c34240175a60a1c25df4ab66a29e484cc7d6df935ae048fdb4d22b5d226`  
		Last Modified: Wed, 13 May 2026 23:24:54 GMT  
		Size: 483.9 KB (483900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f057466943359e2d9be6e944679614274b172365fa4db8f9947a4e6077ce16da`  
		Last Modified: Wed, 13 May 2026 23:25:12 GMT  
		Size: 386.3 MB (386328171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feae93163670807fe6057b0e550a8bc668016106f52160cabf739e314a2bd066`  
		Last Modified: Wed, 13 May 2026 23:24:55 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbc17332dd684ba26e6780fd04333b97362511a39941d724fa4d8997bb058aa`  
		Last Modified: Wed, 13 May 2026 23:24:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625e98c364f43719c6512912d9f8ff207e8ae5f03c0fd3a8d9656b66348ad0a`  
		Last Modified: Wed, 13 May 2026 23:24:57 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd3de01479716e18c3115260e1f056874139ff4bf96b9bdcaa035f84d716497`  
		Last Modified: Wed, 13 May 2026 23:24:58 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:be66e10b6fee6a4e884ea401d93c5c1745fc1b478d94ddddf8538f507b39a8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62303593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861a4d0c979a273ef2fbda1c2ad83947b784959e7a0a2f43754b4696aa343261`

```dockerfile
```

-	Layers:
	-	`sha256:b48b30b39c332c342fbc2ccb3eda2c80634cb537ec1e76e5d607635c3a84ece0`  
		Last Modified: Wed, 13 May 2026 23:24:59 GMT  
		Size: 62.3 MB (62276726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de37a96e26a00b52253e7369b1335105ca61add6ca6c6e349d6dbbbe361b742b`  
		Last Modified: Wed, 13 May 2026 23:24:53 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:83223b09a6245871a0a7118c2ac4a60e871e8bcda7168086abd3d355c0402ff7
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
$ docker pull odoo@sha256:fb0bc12e909f1657ff4c54cb192695b95b72a7892948ec8972b508e6e97b7989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.3 MB (704250122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7d3025b532f5772a19a2c0788ca8dee4cf9980e44912a223195ab2dbfa26ab`
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
# Wed, 13 May 2026 23:11:02 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:02 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:02 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:11:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:08 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:09 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:03 GMT
USER odoo
# Wed, 13 May 2026 23:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aecf47723a9e98b1f9b94a407ec6aad0f70186ff4a00a50a5be759156d9c09`  
		Last Modified: Wed, 13 May 2026 23:14:10 GMT  
		Size: 254.6 MB (254597347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b4ad9e06cd21adbaafb2075959acd312b53e97796c3504ec3a4b42dc98573`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 14.4 MB (14360001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d32422d907a6afc54d7b21aed1fba5e960acae121de0370ea2f33c8d51938`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 483.8 KB (483771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6c725bd8b27faa60c91afdf1ea7fcebf0df9ccb7b7cb00c9b0b9d37af5a7df`  
		Last Modified: Wed, 13 May 2026 23:14:14 GMT  
		Size: 405.1 MB (405073281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35d8fc749257c1d5db5ccdcb4d1be50bd30985667e18664c3fe7457ece9cebd`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c71aa6facf5ccf0d8440909802c5056b63caadc6d8a95457680659a1ceee678`  
		Last Modified: Wed, 13 May 2026 23:14:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0e6c5f7ff11263b5c357ff0ef5db005f65fbb0066344414705d52fdcce3283`  
		Last Modified: Wed, 13 May 2026 23:14:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e1820bdcecd63344cc662452f0acee25e0dbe03cb9499a2b915026faecb0cb`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:3c03d92d8b08ecca6bc44239322f8bc04d18ba335d9e79a6079d2ea8cce21ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70361850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8320dcdbc7f7d018720722093a7dcb0e49f9476e446d15120d911f422317716`

```dockerfile
```

-	Layers:
	-	`sha256:fa553c784165cd5f1a8746089bfe7582cefa2f6f49427f77e8e40b0acdfcfc61`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 70.3 MB (70334745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a90a471a32730b698ba709158e03aee5eabea60b7e095946709dc781895342`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a926e95676d2f1257a47a2e37f72319620494c8c72da4760e247fa550248e0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700653183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9c72496d62681c0447bcac4dbafbeb9992fe58952ba8a258c241f4e7ef5c38`
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
# Wed, 13 May 2026 23:11:18 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:18 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:11:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:29 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:42 GMT
USER odoo
# Wed, 13 May 2026 23:12:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd52f8bf8e54db271ac0200da94b7d78adbb8abd25e850ecf1d261f00c4556`  
		Last Modified: Wed, 13 May 2026 23:15:16 GMT  
		Size: 252.0 MB (252027472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13be8adf22d69f3888466a0a1820a4b9604265b82cbe65c8b82178ff8fee6ce0`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 14.3 MB (14340691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bcf22df18fc5dc8c0fd7a3bf162a97e6be7045a80fa39fe6194b844e30b374`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 483.8 KB (483840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01fe1bc15e16e79bc414732f45666d65939d6204f7ba4deb3e916a967415f7`  
		Last Modified: Wed, 13 May 2026 23:15:20 GMT  
		Size: 404.9 MB (404922650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab44deba3086ff1e3d9be8cd3ab99bfd1793f37dfb90be1aae01ab408332c528`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb02afc6a9517cbf917fda244504a12fe0fb5feb9696799d4f0c72662fa801`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ef61e6a22e619f7a9f8993ad0c42f6eff8969b02b7975304cc9482ad4257`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b76189da41c9ed6aa572722895e02b118d32cbc1b304baea34a2f7eb4511348`  
		Last Modified: Wed, 13 May 2026 23:15:10 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:7e1083ce623b39c1c0e401092f2ed870c98aeabcc1e10a0ef6d912efccdba284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70369300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457e0348ed95ab26cc97fd5444ded94bc65d05706448f514d582ab3c70b59271`

```dockerfile
```

-	Layers:
	-	`sha256:f18c188e01c9b25a515653f14be07a2f339be9e764decf6a0b6fae65f06e8606`  
		Last Modified: Wed, 13 May 2026 23:15:11 GMT  
		Size: 70.3 MB (70342032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613709111dc073e57ef93b0e9f2ed35d72014a6bfc73602b4f93c1490f1e7d6a`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 27.3 KB (27268 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:0cc0f80ca81094661caf0adfca8b6ce9d2957870e36a96f1ef90fec76c89c807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.4 MB (720395821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0856dd568b42b5c95c376b65336fa458bd6a147ae05ef07ddc0d0989c951ad`
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
# Wed, 13 May 2026 23:16:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:16:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:16:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:16:53 GMT
ARG TARGETARCH=ppc64le
# Wed, 13 May 2026 23:16:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:17:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:17:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:17:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:20:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:20:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:20:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:20:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:20:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:20:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:20:10 GMT
USER odoo
# Wed, 13 May 2026 23:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:20:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62faddfdfc852ed57a1f0f8439ea047ac9998c9a1bea1eb00e172cc3c9e39ed5`  
		Last Modified: Wed, 13 May 2026 23:25:09 GMT  
		Size: 265.1 MB (265099080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3d5329e6b271b46c68a19793b52687b3fa7d8716dce8455f3d7cd0c6dca244`  
		Last Modified: Wed, 13 May 2026 23:24:56 GMT  
		Size: 14.9 MB (14893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51430c34240175a60a1c25df4ab66a29e484cc7d6df935ae048fdb4d22b5d226`  
		Last Modified: Wed, 13 May 2026 23:24:54 GMT  
		Size: 483.9 KB (483900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0236a4293f37c048ec1be07e030c8a09bdf0840963b083c4084c3e049cb44d1`  
		Last Modified: Wed, 13 May 2026 23:26:20 GMT  
		Size: 405.6 MB (405602005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c1bfe20c18da901e760039d12cd0ef7786188e59ec9bd94bb0163806d152ce`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a047cedeeb5300e0e46174817c0a5082f692366ad7b0a443f86514e5e80cf`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4bc2b97398b4c30d5324f57ef413b4de16afe936b31747d755108c0210776`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ea6d0b15f3235cc9eff05985a9dbf4f5ea085c549c550c6a1b6d911beb8a0c`  
		Last Modified: Wed, 13 May 2026 23:26:09 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:3497f4e591e3b5687257db56f15111674e47d0616950aea35cb80d1e2698c365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70370301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c59693b29dee294787046a6ed9dce50f18c607dcad6f8517f81861cbedb171a`

```dockerfile
```

-	Layers:
	-	`sha256:c658159517b3c2f99096b1551d00cee1e37c1c11409017336a15d542e7a0fb37`  
		Last Modified: Wed, 13 May 2026 23:26:12 GMT  
		Size: 70.3 MB (70343134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d309a2a89b38c411eec3450564538c6c7df8709b22922100b987ce1ce3512e7`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:83223b09a6245871a0a7118c2ac4a60e871e8bcda7168086abd3d355c0402ff7
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
$ docker pull odoo@sha256:fb0bc12e909f1657ff4c54cb192695b95b72a7892948ec8972b508e6e97b7989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.3 MB (704250122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7d3025b532f5772a19a2c0788ca8dee4cf9980e44912a223195ab2dbfa26ab`
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
# Wed, 13 May 2026 23:11:02 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:02 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:02 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:11:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:08 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:09 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:03 GMT
USER odoo
# Wed, 13 May 2026 23:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aecf47723a9e98b1f9b94a407ec6aad0f70186ff4a00a50a5be759156d9c09`  
		Last Modified: Wed, 13 May 2026 23:14:10 GMT  
		Size: 254.6 MB (254597347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b4ad9e06cd21adbaafb2075959acd312b53e97796c3504ec3a4b42dc98573`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 14.4 MB (14360001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d32422d907a6afc54d7b21aed1fba5e960acae121de0370ea2f33c8d51938`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 483.8 KB (483771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6c725bd8b27faa60c91afdf1ea7fcebf0df9ccb7b7cb00c9b0b9d37af5a7df`  
		Last Modified: Wed, 13 May 2026 23:14:14 GMT  
		Size: 405.1 MB (405073281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35d8fc749257c1d5db5ccdcb4d1be50bd30985667e18664c3fe7457ece9cebd`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c71aa6facf5ccf0d8440909802c5056b63caadc6d8a95457680659a1ceee678`  
		Last Modified: Wed, 13 May 2026 23:14:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0e6c5f7ff11263b5c357ff0ef5db005f65fbb0066344414705d52fdcce3283`  
		Last Modified: Wed, 13 May 2026 23:14:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e1820bdcecd63344cc662452f0acee25e0dbe03cb9499a2b915026faecb0cb`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3c03d92d8b08ecca6bc44239322f8bc04d18ba335d9e79a6079d2ea8cce21ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70361850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8320dcdbc7f7d018720722093a7dcb0e49f9476e446d15120d911f422317716`

```dockerfile
```

-	Layers:
	-	`sha256:fa553c784165cd5f1a8746089bfe7582cefa2f6f49427f77e8e40b0acdfcfc61`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 70.3 MB (70334745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a90a471a32730b698ba709158e03aee5eabea60b7e095946709dc781895342`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a926e95676d2f1257a47a2e37f72319620494c8c72da4760e247fa550248e0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700653183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9c72496d62681c0447bcac4dbafbeb9992fe58952ba8a258c241f4e7ef5c38`
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
# Wed, 13 May 2026 23:11:18 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:18 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:11:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:29 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:42 GMT
USER odoo
# Wed, 13 May 2026 23:12:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd52f8bf8e54db271ac0200da94b7d78adbb8abd25e850ecf1d261f00c4556`  
		Last Modified: Wed, 13 May 2026 23:15:16 GMT  
		Size: 252.0 MB (252027472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13be8adf22d69f3888466a0a1820a4b9604265b82cbe65c8b82178ff8fee6ce0`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 14.3 MB (14340691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bcf22df18fc5dc8c0fd7a3bf162a97e6be7045a80fa39fe6194b844e30b374`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 483.8 KB (483840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01fe1bc15e16e79bc414732f45666d65939d6204f7ba4deb3e916a967415f7`  
		Last Modified: Wed, 13 May 2026 23:15:20 GMT  
		Size: 404.9 MB (404922650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab44deba3086ff1e3d9be8cd3ab99bfd1793f37dfb90be1aae01ab408332c528`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb02afc6a9517cbf917fda244504a12fe0fb5feb9696799d4f0c72662fa801`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ef61e6a22e619f7a9f8993ad0c42f6eff8969b02b7975304cc9482ad4257`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b76189da41c9ed6aa572722895e02b118d32cbc1b304baea34a2f7eb4511348`  
		Last Modified: Wed, 13 May 2026 23:15:10 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7e1083ce623b39c1c0e401092f2ed870c98aeabcc1e10a0ef6d912efccdba284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70369300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457e0348ed95ab26cc97fd5444ded94bc65d05706448f514d582ab3c70b59271`

```dockerfile
```

-	Layers:
	-	`sha256:f18c188e01c9b25a515653f14be07a2f339be9e764decf6a0b6fae65f06e8606`  
		Last Modified: Wed, 13 May 2026 23:15:11 GMT  
		Size: 70.3 MB (70342032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613709111dc073e57ef93b0e9f2ed35d72014a6bfc73602b4f93c1490f1e7d6a`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 27.3 KB (27268 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:0cc0f80ca81094661caf0adfca8b6ce9d2957870e36a96f1ef90fec76c89c807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.4 MB (720395821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0856dd568b42b5c95c376b65336fa458bd6a147ae05ef07ddc0d0989c951ad`
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
# Wed, 13 May 2026 23:16:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:16:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:16:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:16:53 GMT
ARG TARGETARCH=ppc64le
# Wed, 13 May 2026 23:16:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:17:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:17:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:17:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:20:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:20:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:20:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:20:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:20:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:20:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:20:10 GMT
USER odoo
# Wed, 13 May 2026 23:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:20:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62faddfdfc852ed57a1f0f8439ea047ac9998c9a1bea1eb00e172cc3c9e39ed5`  
		Last Modified: Wed, 13 May 2026 23:25:09 GMT  
		Size: 265.1 MB (265099080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3d5329e6b271b46c68a19793b52687b3fa7d8716dce8455f3d7cd0c6dca244`  
		Last Modified: Wed, 13 May 2026 23:24:56 GMT  
		Size: 14.9 MB (14893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51430c34240175a60a1c25df4ab66a29e484cc7d6df935ae048fdb4d22b5d226`  
		Last Modified: Wed, 13 May 2026 23:24:54 GMT  
		Size: 483.9 KB (483900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0236a4293f37c048ec1be07e030c8a09bdf0840963b083c4084c3e049cb44d1`  
		Last Modified: Wed, 13 May 2026 23:26:20 GMT  
		Size: 405.6 MB (405602005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c1bfe20c18da901e760039d12cd0ef7786188e59ec9bd94bb0163806d152ce`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a047cedeeb5300e0e46174817c0a5082f692366ad7b0a443f86514e5e80cf`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4bc2b97398b4c30d5324f57ef413b4de16afe936b31747d755108c0210776`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ea6d0b15f3235cc9eff05985a9dbf4f5ea085c549c550c6a1b6d911beb8a0c`  
		Last Modified: Wed, 13 May 2026 23:26:09 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3497f4e591e3b5687257db56f15111674e47d0616950aea35cb80d1e2698c365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70370301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c59693b29dee294787046a6ed9dce50f18c607dcad6f8517f81861cbedb171a`

```dockerfile
```

-	Layers:
	-	`sha256:c658159517b3c2f99096b1551d00cee1e37c1c11409017336a15d542e7a0fb37`  
		Last Modified: Wed, 13 May 2026 23:26:12 GMT  
		Size: 70.3 MB (70343134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d309a2a89b38c411eec3450564538c6c7df8709b22922100b987ce1ce3512e7`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260513`

```console
$ docker pull odoo@sha256:83223b09a6245871a0a7118c2ac4a60e871e8bcda7168086abd3d355c0402ff7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260513` - linux; amd64

```console
$ docker pull odoo@sha256:fb0bc12e909f1657ff4c54cb192695b95b72a7892948ec8972b508e6e97b7989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.3 MB (704250122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7d3025b532f5772a19a2c0788ca8dee4cf9980e44912a223195ab2dbfa26ab`
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
# Wed, 13 May 2026 23:11:02 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:02 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:02 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:11:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:08 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:09 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:03 GMT
USER odoo
# Wed, 13 May 2026 23:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aecf47723a9e98b1f9b94a407ec6aad0f70186ff4a00a50a5be759156d9c09`  
		Last Modified: Wed, 13 May 2026 23:14:10 GMT  
		Size: 254.6 MB (254597347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b4ad9e06cd21adbaafb2075959acd312b53e97796c3504ec3a4b42dc98573`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 14.4 MB (14360001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d32422d907a6afc54d7b21aed1fba5e960acae121de0370ea2f33c8d51938`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 483.8 KB (483771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6c725bd8b27faa60c91afdf1ea7fcebf0df9ccb7b7cb00c9b0b9d37af5a7df`  
		Last Modified: Wed, 13 May 2026 23:14:14 GMT  
		Size: 405.1 MB (405073281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35d8fc749257c1d5db5ccdcb4d1be50bd30985667e18664c3fe7457ece9cebd`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c71aa6facf5ccf0d8440909802c5056b63caadc6d8a95457680659a1ceee678`  
		Last Modified: Wed, 13 May 2026 23:14:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0e6c5f7ff11263b5c357ff0ef5db005f65fbb0066344414705d52fdcce3283`  
		Last Modified: Wed, 13 May 2026 23:14:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e1820bdcecd63344cc662452f0acee25e0dbe03cb9499a2b915026faecb0cb`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:3c03d92d8b08ecca6bc44239322f8bc04d18ba335d9e79a6079d2ea8cce21ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70361850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8320dcdbc7f7d018720722093a7dcb0e49f9476e446d15120d911f422317716`

```dockerfile
```

-	Layers:
	-	`sha256:fa553c784165cd5f1a8746089bfe7582cefa2f6f49427f77e8e40b0acdfcfc61`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 70.3 MB (70334745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a90a471a32730b698ba709158e03aee5eabea60b7e095946709dc781895342`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260513` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a926e95676d2f1257a47a2e37f72319620494c8c72da4760e247fa550248e0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700653183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9c72496d62681c0447bcac4dbafbeb9992fe58952ba8a258c241f4e7ef5c38`
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
# Wed, 13 May 2026 23:11:18 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:18 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:11:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:29 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:42 GMT
USER odoo
# Wed, 13 May 2026 23:12:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd52f8bf8e54db271ac0200da94b7d78adbb8abd25e850ecf1d261f00c4556`  
		Last Modified: Wed, 13 May 2026 23:15:16 GMT  
		Size: 252.0 MB (252027472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13be8adf22d69f3888466a0a1820a4b9604265b82cbe65c8b82178ff8fee6ce0`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 14.3 MB (14340691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bcf22df18fc5dc8c0fd7a3bf162a97e6be7045a80fa39fe6194b844e30b374`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 483.8 KB (483840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01fe1bc15e16e79bc414732f45666d65939d6204f7ba4deb3e916a967415f7`  
		Last Modified: Wed, 13 May 2026 23:15:20 GMT  
		Size: 404.9 MB (404922650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab44deba3086ff1e3d9be8cd3ab99bfd1793f37dfb90be1aae01ab408332c528`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb02afc6a9517cbf917fda244504a12fe0fb5feb9696799d4f0c72662fa801`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ef61e6a22e619f7a9f8993ad0c42f6eff8969b02b7975304cc9482ad4257`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b76189da41c9ed6aa572722895e02b118d32cbc1b304baea34a2f7eb4511348`  
		Last Modified: Wed, 13 May 2026 23:15:10 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:7e1083ce623b39c1c0e401092f2ed870c98aeabcc1e10a0ef6d912efccdba284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70369300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457e0348ed95ab26cc97fd5444ded94bc65d05706448f514d582ab3c70b59271`

```dockerfile
```

-	Layers:
	-	`sha256:f18c188e01c9b25a515653f14be07a2f339be9e764decf6a0b6fae65f06e8606`  
		Last Modified: Wed, 13 May 2026 23:15:11 GMT  
		Size: 70.3 MB (70342032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613709111dc073e57ef93b0e9f2ed35d72014a6bfc73602b4f93c1490f1e7d6a`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 27.3 KB (27268 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260513` - linux; ppc64le

```console
$ docker pull odoo@sha256:0cc0f80ca81094661caf0adfca8b6ce9d2957870e36a96f1ef90fec76c89c807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.4 MB (720395821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0856dd568b42b5c95c376b65336fa458bd6a147ae05ef07ddc0d0989c951ad`
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
# Wed, 13 May 2026 23:16:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:16:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:16:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:16:53 GMT
ARG TARGETARCH=ppc64le
# Wed, 13 May 2026 23:16:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:17:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:17:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:17:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:20:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:20:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:20:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:20:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:20:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:20:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:20:10 GMT
USER odoo
# Wed, 13 May 2026 23:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:20:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62faddfdfc852ed57a1f0f8439ea047ac9998c9a1bea1eb00e172cc3c9e39ed5`  
		Last Modified: Wed, 13 May 2026 23:25:09 GMT  
		Size: 265.1 MB (265099080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3d5329e6b271b46c68a19793b52687b3fa7d8716dce8455f3d7cd0c6dca244`  
		Last Modified: Wed, 13 May 2026 23:24:56 GMT  
		Size: 14.9 MB (14893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51430c34240175a60a1c25df4ab66a29e484cc7d6df935ae048fdb4d22b5d226`  
		Last Modified: Wed, 13 May 2026 23:24:54 GMT  
		Size: 483.9 KB (483900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0236a4293f37c048ec1be07e030c8a09bdf0840963b083c4084c3e049cb44d1`  
		Last Modified: Wed, 13 May 2026 23:26:20 GMT  
		Size: 405.6 MB (405602005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c1bfe20c18da901e760039d12cd0ef7786188e59ec9bd94bb0163806d152ce`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a047cedeeb5300e0e46174817c0a5082f692366ad7b0a443f86514e5e80cf`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4bc2b97398b4c30d5324f57ef413b4de16afe936b31747d755108c0210776`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ea6d0b15f3235cc9eff05985a9dbf4f5ea085c549c550c6a1b6d911beb8a0c`  
		Last Modified: Wed, 13 May 2026 23:26:09 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260513` - unknown; unknown

```console
$ docker pull odoo@sha256:3497f4e591e3b5687257db56f15111674e47d0616950aea35cb80d1e2698c365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70370301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c59693b29dee294787046a6ed9dce50f18c607dcad6f8517f81861cbedb171a`

```dockerfile
```

-	Layers:
	-	`sha256:c658159517b3c2f99096b1551d00cee1e37c1c11409017336a15d542e7a0fb37`  
		Last Modified: Wed, 13 May 2026 23:26:12 GMT  
		Size: 70.3 MB (70343134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d309a2a89b38c411eec3450564538c6c7df8709b22922100b987ce1ce3512e7`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:83223b09a6245871a0a7118c2ac4a60e871e8bcda7168086abd3d355c0402ff7
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
$ docker pull odoo@sha256:fb0bc12e909f1657ff4c54cb192695b95b72a7892948ec8972b508e6e97b7989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.3 MB (704250122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7d3025b532f5772a19a2c0788ca8dee4cf9980e44912a223195ab2dbfa26ab`
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
# Wed, 13 May 2026 23:11:02 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:02 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:02 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:02 GMT
ARG TARGETARCH=amd64
# Wed, 13 May 2026 23:11:02 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:08 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:09 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:09 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:09 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:03 GMT
USER odoo
# Wed, 13 May 2026 23:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aecf47723a9e98b1f9b94a407ec6aad0f70186ff4a00a50a5be759156d9c09`  
		Last Modified: Wed, 13 May 2026 23:14:10 GMT  
		Size: 254.6 MB (254597347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422b4ad9e06cd21adbaafb2075959acd312b53e97796c3504ec3a4b42dc98573`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 14.4 MB (14360001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d32422d907a6afc54d7b21aed1fba5e960acae121de0370ea2f33c8d51938`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 483.8 KB (483771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6c725bd8b27faa60c91afdf1ea7fcebf0df9ccb7b7cb00c9b0b9d37af5a7df`  
		Last Modified: Wed, 13 May 2026 23:14:14 GMT  
		Size: 405.1 MB (405073281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35d8fc749257c1d5db5ccdcb4d1be50bd30985667e18664c3fe7457ece9cebd`  
		Last Modified: Wed, 13 May 2026 23:14:01 GMT  
		Size: 714.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c71aa6facf5ccf0d8440909802c5056b63caadc6d8a95457680659a1ceee678`  
		Last Modified: Wed, 13 May 2026 23:14:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0e6c5f7ff11263b5c357ff0ef5db005f65fbb0066344414705d52fdcce3283`  
		Last Modified: Wed, 13 May 2026 23:14:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e1820bdcecd63344cc662452f0acee25e0dbe03cb9499a2b915026faecb0cb`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 876.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:3c03d92d8b08ecca6bc44239322f8bc04d18ba335d9e79a6079d2ea8cce21ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70361850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8320dcdbc7f7d018720722093a7dcb0e49f9476e446d15120d911f422317716`

```dockerfile
```

-	Layers:
	-	`sha256:fa553c784165cd5f1a8746089bfe7582cefa2f6f49427f77e8e40b0acdfcfc61`  
		Last Modified: Wed, 13 May 2026 23:14:04 GMT  
		Size: 70.3 MB (70334745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a90a471a32730b698ba709158e03aee5eabea60b7e095946709dc781895342`  
		Last Modified: Wed, 13 May 2026 23:14:00 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a926e95676d2f1257a47a2e37f72319620494c8c72da4760e247fa550248e0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.7 MB (700653183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9c72496d62681c0447bcac4dbafbeb9992fe58952ba8a258c241f4e7ef5c38`
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
# Wed, 13 May 2026 23:11:18 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:11:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:11:18 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:11:18 GMT
ARG TARGETARCH=arm64
# Wed, 13 May 2026 23:11:18 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:11:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:11:29 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:11:29 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:11:29 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:12:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:12:42 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:12:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:12:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:12:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:12:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:12:42 GMT
USER odoo
# Wed, 13 May 2026 23:12:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:12:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddd52f8bf8e54db271ac0200da94b7d78adbb8abd25e850ecf1d261f00c4556`  
		Last Modified: Wed, 13 May 2026 23:15:16 GMT  
		Size: 252.0 MB (252027472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13be8adf22d69f3888466a0a1820a4b9604265b82cbe65c8b82178ff8fee6ce0`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 14.3 MB (14340691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bcf22df18fc5dc8c0fd7a3bf162a97e6be7045a80fa39fe6194b844e30b374`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 483.8 KB (483840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc01fe1bc15e16e79bc414732f45666d65939d6204f7ba4deb3e916a967415f7`  
		Last Modified: Wed, 13 May 2026 23:15:20 GMT  
		Size: 404.9 MB (404922650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab44deba3086ff1e3d9be8cd3ab99bfd1793f37dfb90be1aae01ab408332c528`  
		Last Modified: Wed, 13 May 2026 23:15:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bb02afc6a9517cbf917fda244504a12fe0fb5feb9696799d4f0c72662fa801`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64ef61e6a22e619f7a9f8993ad0c42f6eff8969b02b7975304cc9482ad4257`  
		Last Modified: Wed, 13 May 2026 23:15:09 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b76189da41c9ed6aa572722895e02b118d32cbc1b304baea34a2f7eb4511348`  
		Last Modified: Wed, 13 May 2026 23:15:10 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7e1083ce623b39c1c0e401092f2ed870c98aeabcc1e10a0ef6d912efccdba284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70369300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457e0348ed95ab26cc97fd5444ded94bc65d05706448f514d582ab3c70b59271`

```dockerfile
```

-	Layers:
	-	`sha256:f18c188e01c9b25a515653f14be07a2f339be9e764decf6a0b6fae65f06e8606`  
		Last Modified: Wed, 13 May 2026 23:15:11 GMT  
		Size: 70.3 MB (70342032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613709111dc073e57ef93b0e9f2ed35d72014a6bfc73602b4f93c1490f1e7d6a`  
		Last Modified: Wed, 13 May 2026 23:15:06 GMT  
		Size: 27.3 KB (27268 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:0cc0f80ca81094661caf0adfca8b6ce9d2957870e36a96f1ef90fec76c89c807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.4 MB (720395821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0856dd568b42b5c95c376b65336fa458bd6a147ae05ef07ddc0d0989c951ad`
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
# Wed, 13 May 2026 23:16:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Wed, 13 May 2026 23:16:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 13 May 2026 23:16:53 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 May 2026 23:16:53 GMT
ARG TARGETARCH=ppc64le
# Wed, 13 May 2026 23:16:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 13 May 2026 23:17:09 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 23:17:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 13 May 2026 23:17:12 GMT
ENV ODOO_VERSION=19.0
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_RELEASE=20260513
# Wed, 13 May 2026 23:17:12 GMT
ARG ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
# Wed, 13 May 2026 23:20:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 13 May 2026 23:20:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 13 May 2026 23:20:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260513 ODOO_SHA=fa6a77178b629c7b65e55e5579188588c59a74cc
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 13 May 2026 23:20:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 13 May 2026 23:20:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 13 May 2026 23:20:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 13 May 2026 23:20:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 13 May 2026 23:20:10 GMT
USER odoo
# Wed, 13 May 2026 23:20:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 23:20:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62faddfdfc852ed57a1f0f8439ea047ac9998c9a1bea1eb00e172cc3c9e39ed5`  
		Last Modified: Wed, 13 May 2026 23:25:09 GMT  
		Size: 265.1 MB (265099080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3d5329e6b271b46c68a19793b52687b3fa7d8716dce8455f3d7cd0c6dca244`  
		Last Modified: Wed, 13 May 2026 23:24:56 GMT  
		Size: 14.9 MB (14893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51430c34240175a60a1c25df4ab66a29e484cc7d6df935ae048fdb4d22b5d226`  
		Last Modified: Wed, 13 May 2026 23:24:54 GMT  
		Size: 483.9 KB (483900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0236a4293f37c048ec1be07e030c8a09bdf0840963b083c4084c3e049cb44d1`  
		Last Modified: Wed, 13 May 2026 23:26:20 GMT  
		Size: 405.6 MB (405602005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c1bfe20c18da901e760039d12cd0ef7786188e59ec9bd94bb0163806d152ce`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3a047cedeeb5300e0e46174817c0a5082f692366ad7b0a443f86514e5e80cf`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4bc2b97398b4c30d5324f57ef413b4de16afe936b31747d755108c0210776`  
		Last Modified: Wed, 13 May 2026 23:26:08 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ea6d0b15f3235cc9eff05985a9dbf4f5ea085c549c550c6a1b6d911beb8a0c`  
		Last Modified: Wed, 13 May 2026 23:26:09 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:3497f4e591e3b5687257db56f15111674e47d0616950aea35cb80d1e2698c365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70370301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c59693b29dee294787046a6ed9dce50f18c607dcad6f8517f81861cbedb171a`

```dockerfile
```

-	Layers:
	-	`sha256:c658159517b3c2f99096b1551d00cee1e37c1c11409017336a15d542e7a0fb37`  
		Last Modified: Wed, 13 May 2026 23:26:12 GMT  
		Size: 70.3 MB (70343134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d309a2a89b38c411eec3450564538c6c7df8709b22922100b987ce1ce3512e7`  
		Last Modified: Wed, 13 May 2026 23:26:07 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json
