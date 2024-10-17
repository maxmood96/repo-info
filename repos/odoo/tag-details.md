<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:16`](#odoo16)
-	[`odoo:16.0`](#odoo160)
-	[`odoo:16.0-20241007`](#odoo160-20241007)
-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20241007`](#odoo170-20241007)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20241007`](#odoo180-20241007)
-	[`odoo:latest`](#odoolatest)

## `odoo:16`

```console
$ docker pull odoo@sha256:61d62bbac91ed54a76e42718875e7ae19fa370f70b65aabff1cabc7dc718b74b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16` - linux; amd64

```console
$ docker pull odoo@sha256:d67dcafd13b5c4b678502aecf799521defe2d3062309e4d01849f00e83e8c410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584374518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3da7f0f97400685ecd48c71d8c95221f47b148fe9ea36c290a2b39fe3a0c80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899905dfcbcbdc089f1f7fad73b980277f5b65abf1675483ab0945cbe29207c0`  
		Last Modified: Thu, 17 Oct 2024 01:24:04 GMT  
		Size: 219.6 MB (219598947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884c55cc2c8f246d1b8b097ee9d7bb295bc9b88c57a22b39dbf683b595ede2cf`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 2.5 MB (2493949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacd1284c0d4d96bce359fd795c140bd075db6eae6b2b0b62a384e53d6425eb`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 468.5 KB (468538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6871a3091380ac01eb741c4ff6c6c555753a3a6020d684dde6ced7fba2b43d`  
		Last Modified: Thu, 17 Oct 2024 01:24:05 GMT  
		Size: 330.4 MB (330381853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888a2c9a6053434e8020841f39b1514e7d31ad64e430a4787099c086ae5002ac`  
		Last Modified: Thu, 17 Oct 2024 01:23:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac9b55bc4aa7589245eafe5d3edcdc16281da4e19d8bfc8c6def78f4fbf32db`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab238cd2bf81f5e87354d9e105fd5c301e92d57b85d26ae65b019a69d9b367b2`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d33f4edbed97304526629647aad5e514e9cd289e16fc8a2bae5393ebad2f425`  
		Last Modified: Thu, 17 Oct 2024 01:24:01 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:0489d4c558250be8b7cc9e567055de957d8bfa017f2d2ff3b9ee403be8b26ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38805038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdfe7376dfbd31b3898381abff43a93fe5e50cbf2de822f6a811fa31f9feb`

```dockerfile
```

-	Layers:
	-	`sha256:aa37f26eeae568fb566b05cb7731d107f335456070e0ac3d34a9d27da1fa9140`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 38.8 MB (38778459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89fc90b5697f8df49bf167bdf12d851c715695950dc818fab43b05726405fbfa`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 26.6 KB (26579 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:81d59325453a07e404bd21fa05f08fb63a49ed9670363f1f7c206d54a4e6ffbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579982940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaa8199a291d3783b31450fbf3065fb81c1f14d24f47926a4b9f135f5d7f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f0291d4d9e2db81d33157d590d424fd6e03723cc1d00047d19ddca19d5f16b`  
		Last Modified: Mon, 07 Oct 2024 20:25:10 GMT  
		Size: 216.9 MB (216900083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f2f870ea7a9b4b2f9d4be3c1e09934d97f9e7e56fcf77da5ce76e70846796`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 2.5 MB (2504056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beff7b55b3e3fd58a8be6ad3fa32257d2ac8ae6457056d0c3420fc99393c728`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 471.7 KB (471690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380c1560a15da8c102bdb37057db7c7e3e2b87db378ba9b0732090cb34a9e27`  
		Last Modified: Mon, 07 Oct 2024 20:25:12 GMT  
		Size: 330.0 MB (330029520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb769e447cc3ec8d8a171c617aa29641baeb8dc59000d0975b5fb8dadb4ebc65`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abcdacbbd32c0e27778067aa8bda6ddc2669c1bb2406a7df8c54b9a78696d4`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd10f55220f4b8fdcee7b054a079af3b1acbc87604827230aa01fa614371fe7`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b20e47548e96347eecade2a960ab613a8a120a85d4f5a28a7d7edd56a3102fd`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16` - unknown; unknown

```console
$ docker pull odoo@sha256:e8ccafa9392c95b84532063692d699fe1225b634a93c60d49a507fa88dbfcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38811426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f349479a4092b8be8614d33a5922879be2d757d582509c775f8a23fe29b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:920f986fa71ef5ee5d66d1e7472b0f3e5c706f1c503a95c60c005a58b5ae59f2`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 38.8 MB (38784733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838ecb6e4fba2c9bc2aebe2afa9fbfacffa9f90964df1b264688397ad8dd3e62`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 26.7 KB (26693 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0`

```console
$ docker pull odoo@sha256:61d62bbac91ed54a76e42718875e7ae19fa370f70b65aabff1cabc7dc718b74b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0` - linux; amd64

```console
$ docker pull odoo@sha256:d67dcafd13b5c4b678502aecf799521defe2d3062309e4d01849f00e83e8c410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584374518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3da7f0f97400685ecd48c71d8c95221f47b148fe9ea36c290a2b39fe3a0c80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899905dfcbcbdc089f1f7fad73b980277f5b65abf1675483ab0945cbe29207c0`  
		Last Modified: Thu, 17 Oct 2024 01:24:04 GMT  
		Size: 219.6 MB (219598947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884c55cc2c8f246d1b8b097ee9d7bb295bc9b88c57a22b39dbf683b595ede2cf`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 2.5 MB (2493949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacd1284c0d4d96bce359fd795c140bd075db6eae6b2b0b62a384e53d6425eb`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 468.5 KB (468538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6871a3091380ac01eb741c4ff6c6c555753a3a6020d684dde6ced7fba2b43d`  
		Last Modified: Thu, 17 Oct 2024 01:24:05 GMT  
		Size: 330.4 MB (330381853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888a2c9a6053434e8020841f39b1514e7d31ad64e430a4787099c086ae5002ac`  
		Last Modified: Thu, 17 Oct 2024 01:23:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac9b55bc4aa7589245eafe5d3edcdc16281da4e19d8bfc8c6def78f4fbf32db`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab238cd2bf81f5e87354d9e105fd5c301e92d57b85d26ae65b019a69d9b367b2`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d33f4edbed97304526629647aad5e514e9cd289e16fc8a2bae5393ebad2f425`  
		Last Modified: Thu, 17 Oct 2024 01:24:01 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0489d4c558250be8b7cc9e567055de957d8bfa017f2d2ff3b9ee403be8b26ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38805038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdfe7376dfbd31b3898381abff43a93fe5e50cbf2de822f6a811fa31f9feb`

```dockerfile
```

-	Layers:
	-	`sha256:aa37f26eeae568fb566b05cb7731d107f335456070e0ac3d34a9d27da1fa9140`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 38.8 MB (38778459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89fc90b5697f8df49bf167bdf12d851c715695950dc818fab43b05726405fbfa`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 26.6 KB (26579 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:81d59325453a07e404bd21fa05f08fb63a49ed9670363f1f7c206d54a4e6ffbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579982940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaa8199a291d3783b31450fbf3065fb81c1f14d24f47926a4b9f135f5d7f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f0291d4d9e2db81d33157d590d424fd6e03723cc1d00047d19ddca19d5f16b`  
		Last Modified: Mon, 07 Oct 2024 20:25:10 GMT  
		Size: 216.9 MB (216900083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f2f870ea7a9b4b2f9d4be3c1e09934d97f9e7e56fcf77da5ce76e70846796`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 2.5 MB (2504056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beff7b55b3e3fd58a8be6ad3fa32257d2ac8ae6457056d0c3420fc99393c728`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 471.7 KB (471690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380c1560a15da8c102bdb37057db7c7e3e2b87db378ba9b0732090cb34a9e27`  
		Last Modified: Mon, 07 Oct 2024 20:25:12 GMT  
		Size: 330.0 MB (330029520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb769e447cc3ec8d8a171c617aa29641baeb8dc59000d0975b5fb8dadb4ebc65`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abcdacbbd32c0e27778067aa8bda6ddc2669c1bb2406a7df8c54b9a78696d4`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd10f55220f4b8fdcee7b054a079af3b1acbc87604827230aa01fa614371fe7`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b20e47548e96347eecade2a960ab613a8a120a85d4f5a28a7d7edd56a3102fd`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e8ccafa9392c95b84532063692d699fe1225b634a93c60d49a507fa88dbfcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38811426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f349479a4092b8be8614d33a5922879be2d757d582509c775f8a23fe29b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:920f986fa71ef5ee5d66d1e7472b0f3e5c706f1c503a95c60c005a58b5ae59f2`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 38.8 MB (38784733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838ecb6e4fba2c9bc2aebe2afa9fbfacffa9f90964df1b264688397ad8dd3e62`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 26.7 KB (26693 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:16.0-20241007`

```console
$ docker pull odoo@sha256:61d62bbac91ed54a76e42718875e7ae19fa370f70b65aabff1cabc7dc718b74b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:16.0-20241007` - linux; amd64

```console
$ docker pull odoo@sha256:d67dcafd13b5c4b678502aecf799521defe2d3062309e4d01849f00e83e8c410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.4 MB (584374518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3da7f0f97400685ecd48c71d8c95221f47b148fe9ea36c290a2b39fe3a0c80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899905dfcbcbdc089f1f7fad73b980277f5b65abf1675483ab0945cbe29207c0`  
		Last Modified: Thu, 17 Oct 2024 01:24:04 GMT  
		Size: 219.6 MB (219598947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884c55cc2c8f246d1b8b097ee9d7bb295bc9b88c57a22b39dbf683b595ede2cf`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 2.5 MB (2493949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacd1284c0d4d96bce359fd795c140bd075db6eae6b2b0b62a384e53d6425eb`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 468.5 KB (468538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6871a3091380ac01eb741c4ff6c6c555753a3a6020d684dde6ced7fba2b43d`  
		Last Modified: Thu, 17 Oct 2024 01:24:05 GMT  
		Size: 330.4 MB (330381853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888a2c9a6053434e8020841f39b1514e7d31ad64e430a4787099c086ae5002ac`  
		Last Modified: Thu, 17 Oct 2024 01:23:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac9b55bc4aa7589245eafe5d3edcdc16281da4e19d8bfc8c6def78f4fbf32db`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab238cd2bf81f5e87354d9e105fd5c301e92d57b85d26ae65b019a69d9b367b2`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d33f4edbed97304526629647aad5e514e9cd289e16fc8a2bae5393ebad2f425`  
		Last Modified: Thu, 17 Oct 2024 01:24:01 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:0489d4c558250be8b7cc9e567055de957d8bfa017f2d2ff3b9ee403be8b26ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38805038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dbdfe7376dfbd31b3898381abff43a93fe5e50cbf2de822f6a811fa31f9feb`

```dockerfile
```

-	Layers:
	-	`sha256:aa37f26eeae568fb566b05cb7731d107f335456070e0ac3d34a9d27da1fa9140`  
		Last Modified: Thu, 17 Oct 2024 01:24:00 GMT  
		Size: 38.8 MB (38778459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89fc90b5697f8df49bf167bdf12d851c715695950dc818fab43b05726405fbfa`  
		Last Modified: Thu, 17 Oct 2024 01:23:58 GMT  
		Size: 26.6 KB (26579 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:16.0-20241007` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:81d59325453a07e404bd21fa05f08fb63a49ed9670363f1f7c206d54a4e6ffbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.0 MB (579982940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87aaa8199a291d3783b31450fbf3065fb81c1f14d24f47926a4b9f135f5d7f71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=C.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=9df8dd7b1e99782f1cfa19aca665969bbd9cc159  ;;     "arm64")  WKHTMLTOPDF_SHA=58c84db46b11ba0e14abb77a32324b1c257f1f22  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=7ed8f6dcedf5345a3dd4eeb58dc89704d862f9cd  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.bullseye_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=16.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=6fb4b7e5bbbc88991511c7ae1121c92625b99649
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f0291d4d9e2db81d33157d590d424fd6e03723cc1d00047d19ddca19d5f16b`  
		Last Modified: Mon, 07 Oct 2024 20:25:10 GMT  
		Size: 216.9 MB (216900083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4f2f870ea7a9b4b2f9d4be3c1e09934d97f9e7e56fcf77da5ce76e70846796`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 2.5 MB (2504056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0beff7b55b3e3fd58a8be6ad3fa32257d2ac8ae6457056d0c3420fc99393c728`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 471.7 KB (471690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380c1560a15da8c102bdb37057db7c7e3e2b87db378ba9b0732090cb34a9e27`  
		Last Modified: Mon, 07 Oct 2024 20:25:12 GMT  
		Size: 330.0 MB (330029520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb769e447cc3ec8d8a171c617aa29641baeb8dc59000d0975b5fb8dadb4ebc65`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abcdacbbd32c0e27778067aa8bda6ddc2669c1bb2406a7df8c54b9a78696d4`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd10f55220f4b8fdcee7b054a079af3b1acbc87604827230aa01fa614371fe7`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 590.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b20e47548e96347eecade2a960ab613a8a120a85d4f5a28a7d7edd56a3102fd`  
		Last Modified: Mon, 07 Oct 2024 20:25:07 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:16.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:e8ccafa9392c95b84532063692d699fe1225b634a93c60d49a507fa88dbfcf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38811426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f349479a4092b8be8614d33a5922879be2d757d582509c775f8a23fe29b1e5`

```dockerfile
```

-	Layers:
	-	`sha256:920f986fa71ef5ee5d66d1e7472b0f3e5c706f1c503a95c60c005a58b5ae59f2`  
		Last Modified: Mon, 07 Oct 2024 20:25:06 GMT  
		Size: 38.8 MB (38784733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838ecb6e4fba2c9bc2aebe2afa9fbfacffa9f90964df1b264688397ad8dd3e62`  
		Last Modified: Mon, 07 Oct 2024 20:25:05 GMT  
		Size: 26.7 KB (26693 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17`

```console
$ docker pull odoo@sha256:0777c7443e0912725b54be341ba84620576b65c15ab9090d3f07d59701cf2711
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
$ docker pull odoo@sha256:b83832e102b2043d78cf912ce2221808ea7e7b460c837e8e9a2664847d6f1d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9604c9c21589224485598f2f790eccdecf4d6fbf47fd8da3aacf9bbececea66a`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e72ba30aed51d4d6c0c237e8bc3c101132e74ae632f1e4eb10942be7b727e`  
		Last Modified: Mon, 07 Oct 2024 20:01:10 GMT  
		Size: 233.8 MB (233763083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ff36f497e26e69c3be270acdbaae0980ae0af88f9656d7bf0e2c6f53284c8`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 2.4 MB (2405343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fcec3c52a5f23aabdf2f205a460aa9aa230c2ca4a7db3376000d5fbd04f3e`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 472.6 KB (472578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d202538c69c111b18a706c8d54ac975532ec4a020ac0fc9cda7bae244428d1`  
		Last Modified: Mon, 07 Oct 2024 20:01:12 GMT  
		Size: 331.7 MB (331705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e01b86b7e7d04baa375c1e89e199796d3e97de17489556bfad943e4fe78a88`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1c4d0f9821a9672084c08e1dd88de11d03eabaf149afc539f90eceaf93700`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08d0548d80024105b6bea0212d3253ea206a0a41b67a4c837f4b4087e2b034`  
		Last Modified: Mon, 07 Oct 2024 20:01:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:427f42d6e67c6173a2d070089f876df7235cb398147292c38a5fc9a0621f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39507564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe4dafb4e572ef28684d70f9b0d76d77d75aa6c2ac0f413ca540723736f89bc`

```dockerfile
```

-	Layers:
	-	`sha256:c917111b60355c59304c6b634bd422af02b6a246ad09f92fe8790fb204cfd9c1`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 39.5 MB (39480979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba4355a0c07c5d4dc95087814aa74abac7572bf737ea00d359740417e8c4304`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 26.6 KB (26585 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1f1f6da85e17cd21290ace7a21fa67ffa8370e52b20fcab790f41a051ec066c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 MB (592698494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec5d5720bf27403a52539c521f18b7695c1e1dfc3dba8bf92edd32bc3f0a08`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaeceaa088b15b07a8b1315a8325a1999e684223cf5e67a6c006b850ac8848e`  
		Last Modified: Mon, 07 Oct 2024 20:21:17 GMT  
		Size: 231.2 MB (231157442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593da4ee3c2b9cf8ba865cf0bcf3b58fc15624ee1dd7685e9f43bf546d2f81c9`  
		Last Modified: Mon, 07 Oct 2024 20:21:12 GMT  
		Size: 2.4 MB (2398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6951d7a9161762682e478a3b71e8822a05e2af33e60248f4913a92e195005a`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 472.7 KB (472696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5005b6e94bcd93e08df067e60060f7c0b0f62d8e00f04aee488ef94768fca1f`  
		Last Modified: Mon, 07 Oct 2024 20:21:19 GMT  
		Size: 331.3 MB (331309334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff58e977e68009ac44f0b7414f7a0e2ac195bfb9fe4303955acc67a33929ea10`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb71664b6198a3568af98278a1163b9b0168bf6a98b6fda02756af5334c6664`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f231c2b8caa3c4c0257307b59bb859d93f314c023f13da4e2a8af313c89796f5`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ac6c81ec328e11241e07e75155f74e05cd7f870ebb6d5ec66a7ee099b24b7`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c5b4fa83d6e0d8a7d6fa4cd9cc9286af10333eebcb69f0729655b79542bc35cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc0439fa6e521d8db24ce56ca24c90db5cdcfcd29f30dd5b2606af5f50a216`

```dockerfile
```

-	Layers:
	-	`sha256:2588008565e78b6555ca86898390d6089bc8dd0919071cb09b668f711f497421`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 39.5 MB (39487492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3abd04ebaea97afb033a95ea0f403614da68216ef25fe607a9479795bdd970`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 26.7 KB (26732 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; ppc64le

```console
$ docker pull odoo@sha256:c9c7849a8914fc213cf0cdad653fbc49e7b4a3046869cddcaee6148bbb4cac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614348604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3fc0aaae4f6d58625a13efbb5a6261c5746b2770724140b65cce56e231c51e`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf22e9ecbdb17bae5948434399d20e985516ae45e11e72048320700f4c3002a`  
		Last Modified: Mon, 07 Oct 2024 20:21:39 GMT  
		Size: 243.3 MB (243294995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d72daf6d3193cf48405ab14e7b21e55790dcda77c3e506d6ff2d916be2e81ab`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 2.7 MB (2708338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dabc1a4222c36d4c42eb25f5f2f0249bf9eabf1c589f406f87173d3e7293431`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 472.7 KB (472718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124db12d8f486a52172344f99e4ef0b2bfb16d9821239b125e83d7806488074c`  
		Last Modified: Mon, 07 Oct 2024 20:21:44 GMT  
		Size: 333.4 MB (333421873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ded5e3af0dbff384e1805596730a23773fee78873edd6dfd2ab51bb230cbab3`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9878389a7cd65810b8a5288fa3df793a4061e0682ff3f2ed10dc7290e97dac1`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac2c5bcd93bd7c3ffd66f4cf3fe9e8de2c28275205ab2358b020bb63aef219`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad903c2d978fb03c0a2e37a11ec79b83d141641bbdd3cb51d967c80754de03e`  
		Last Modified: Mon, 07 Oct 2024 20:21:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:27e1f93d1227d6341fe89aed3f796c5ff11fda59937cd60d8bd66aa924da2700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89987f1998492b30276df26c0f81d79265de5d89aeeecda184af3f8bc302a359`

```dockerfile
```

-	Layers:
	-	`sha256:af3a4e5105b5664b62b8d0b287fee74a6c86c9a5a8a7ba319f13e55e14352b4f`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 39.5 MB (39489286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef433a4d91a323051092d6b2a91ae987563627672e47d65a5552cd3dfd7bb7c`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 26.6 KB (26636 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:0777c7443e0912725b54be341ba84620576b65c15ab9090d3f07d59701cf2711
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
$ docker pull odoo@sha256:b83832e102b2043d78cf912ce2221808ea7e7b460c837e8e9a2664847d6f1d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9604c9c21589224485598f2f790eccdecf4d6fbf47fd8da3aacf9bbececea66a`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e72ba30aed51d4d6c0c237e8bc3c101132e74ae632f1e4eb10942be7b727e`  
		Last Modified: Mon, 07 Oct 2024 20:01:10 GMT  
		Size: 233.8 MB (233763083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ff36f497e26e69c3be270acdbaae0980ae0af88f9656d7bf0e2c6f53284c8`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 2.4 MB (2405343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fcec3c52a5f23aabdf2f205a460aa9aa230c2ca4a7db3376000d5fbd04f3e`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 472.6 KB (472578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d202538c69c111b18a706c8d54ac975532ec4a020ac0fc9cda7bae244428d1`  
		Last Modified: Mon, 07 Oct 2024 20:01:12 GMT  
		Size: 331.7 MB (331705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e01b86b7e7d04baa375c1e89e199796d3e97de17489556bfad943e4fe78a88`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1c4d0f9821a9672084c08e1dd88de11d03eabaf149afc539f90eceaf93700`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08d0548d80024105b6bea0212d3253ea206a0a41b67a4c837f4b4087e2b034`  
		Last Modified: Mon, 07 Oct 2024 20:01:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:427f42d6e67c6173a2d070089f876df7235cb398147292c38a5fc9a0621f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39507564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe4dafb4e572ef28684d70f9b0d76d77d75aa6c2ac0f413ca540723736f89bc`

```dockerfile
```

-	Layers:
	-	`sha256:c917111b60355c59304c6b634bd422af02b6a246ad09f92fe8790fb204cfd9c1`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 39.5 MB (39480979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba4355a0c07c5d4dc95087814aa74abac7572bf737ea00d359740417e8c4304`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 26.6 KB (26585 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1f1f6da85e17cd21290ace7a21fa67ffa8370e52b20fcab790f41a051ec066c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 MB (592698494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec5d5720bf27403a52539c521f18b7695c1e1dfc3dba8bf92edd32bc3f0a08`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaeceaa088b15b07a8b1315a8325a1999e684223cf5e67a6c006b850ac8848e`  
		Last Modified: Mon, 07 Oct 2024 20:21:17 GMT  
		Size: 231.2 MB (231157442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593da4ee3c2b9cf8ba865cf0bcf3b58fc15624ee1dd7685e9f43bf546d2f81c9`  
		Last Modified: Mon, 07 Oct 2024 20:21:12 GMT  
		Size: 2.4 MB (2398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6951d7a9161762682e478a3b71e8822a05e2af33e60248f4913a92e195005a`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 472.7 KB (472696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5005b6e94bcd93e08df067e60060f7c0b0f62d8e00f04aee488ef94768fca1f`  
		Last Modified: Mon, 07 Oct 2024 20:21:19 GMT  
		Size: 331.3 MB (331309334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff58e977e68009ac44f0b7414f7a0e2ac195bfb9fe4303955acc67a33929ea10`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb71664b6198a3568af98278a1163b9b0168bf6a98b6fda02756af5334c6664`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f231c2b8caa3c4c0257307b59bb859d93f314c023f13da4e2a8af313c89796f5`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ac6c81ec328e11241e07e75155f74e05cd7f870ebb6d5ec66a7ee099b24b7`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c5b4fa83d6e0d8a7d6fa4cd9cc9286af10333eebcb69f0729655b79542bc35cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc0439fa6e521d8db24ce56ca24c90db5cdcfcd29f30dd5b2606af5f50a216`

```dockerfile
```

-	Layers:
	-	`sha256:2588008565e78b6555ca86898390d6089bc8dd0919071cb09b668f711f497421`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 39.5 MB (39487492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3abd04ebaea97afb033a95ea0f403614da68216ef25fe607a9479795bdd970`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 26.7 KB (26732 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c9c7849a8914fc213cf0cdad653fbc49e7b4a3046869cddcaee6148bbb4cac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614348604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3fc0aaae4f6d58625a13efbb5a6261c5746b2770724140b65cce56e231c51e`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf22e9ecbdb17bae5948434399d20e985516ae45e11e72048320700f4c3002a`  
		Last Modified: Mon, 07 Oct 2024 20:21:39 GMT  
		Size: 243.3 MB (243294995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d72daf6d3193cf48405ab14e7b21e55790dcda77c3e506d6ff2d916be2e81ab`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 2.7 MB (2708338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dabc1a4222c36d4c42eb25f5f2f0249bf9eabf1c589f406f87173d3e7293431`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 472.7 KB (472718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124db12d8f486a52172344f99e4ef0b2bfb16d9821239b125e83d7806488074c`  
		Last Modified: Mon, 07 Oct 2024 20:21:44 GMT  
		Size: 333.4 MB (333421873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ded5e3af0dbff384e1805596730a23773fee78873edd6dfd2ab51bb230cbab3`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9878389a7cd65810b8a5288fa3df793a4061e0682ff3f2ed10dc7290e97dac1`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac2c5bcd93bd7c3ffd66f4cf3fe9e8de2c28275205ab2358b020bb63aef219`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad903c2d978fb03c0a2e37a11ec79b83d141641bbdd3cb51d967c80754de03e`  
		Last Modified: Mon, 07 Oct 2024 20:21:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:27e1f93d1227d6341fe89aed3f796c5ff11fda59937cd60d8bd66aa924da2700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89987f1998492b30276df26c0f81d79265de5d89aeeecda184af3f8bc302a359`

```dockerfile
```

-	Layers:
	-	`sha256:af3a4e5105b5664b62b8d0b287fee74a6c86c9a5a8a7ba319f13e55e14352b4f`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 39.5 MB (39489286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef433a4d91a323051092d6b2a91ae987563627672e47d65a5552cd3dfd7bb7c`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 26.6 KB (26636 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20241007`

```console
$ docker pull odoo@sha256:0777c7443e0912725b54be341ba84620576b65c15ab9090d3f07d59701cf2711
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:17.0-20241007` - linux; amd64

```console
$ docker pull odoo@sha256:b83832e102b2043d78cf912ce2221808ea7e7b460c837e8e9a2664847d6f1d62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.9 MB (597884965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9604c9c21589224485598f2f790eccdecf4d6fbf47fd8da3aacf9bbececea66a`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e72ba30aed51d4d6c0c237e8bc3c101132e74ae632f1e4eb10942be7b727e`  
		Last Modified: Mon, 07 Oct 2024 20:01:10 GMT  
		Size: 233.8 MB (233763083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ff36f497e26e69c3be270acdbaae0980ae0af88f9656d7bf0e2c6f53284c8`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 2.4 MB (2405343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0fcec3c52a5f23aabdf2f205a460aa9aa230c2ca4a7db3376000d5fbd04f3e`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 472.6 KB (472578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d202538c69c111b18a706c8d54ac975532ec4a020ac0fc9cda7bae244428d1`  
		Last Modified: Mon, 07 Oct 2024 20:01:12 GMT  
		Size: 331.7 MB (331705835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b0b09512eccce0ce4563fa2e4665aa743988642bb6850a81f21b467d061f54`  
		Last Modified: Mon, 07 Oct 2024 20:00:57 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e01b86b7e7d04baa375c1e89e199796d3e97de17489556bfad943e4fe78a88`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1c4d0f9821a9672084c08e1dd88de11d03eabaf149afc539f90eceaf93700`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a08d0548d80024105b6bea0212d3253ea206a0a41b67a4c837f4b4087e2b034`  
		Last Modified: Mon, 07 Oct 2024 20:01:09 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:427f42d6e67c6173a2d070089f876df7235cb398147292c38a5fc9a0621f0c2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39507564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe4dafb4e572ef28684d70f9b0d76d77d75aa6c2ac0f413ca540723736f89bc`

```dockerfile
```

-	Layers:
	-	`sha256:c917111b60355c59304c6b634bd422af02b6a246ad09f92fe8790fb204cfd9c1`  
		Last Modified: Mon, 07 Oct 2024 20:01:08 GMT  
		Size: 39.5 MB (39480979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bba4355a0c07c5d4dc95087814aa74abac7572bf737ea00d359740417e8c4304`  
		Last Modified: Mon, 07 Oct 2024 20:01:07 GMT  
		Size: 26.6 KB (26585 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241007` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1f1f6da85e17cd21290ace7a21fa67ffa8370e52b20fcab790f41a051ec066c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.7 MB (592698494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dec5d5720bf27403a52539c521f18b7695c1e1dfc3dba8bf92edd32bc3f0a08`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaeceaa088b15b07a8b1315a8325a1999e684223cf5e67a6c006b850ac8848e`  
		Last Modified: Mon, 07 Oct 2024 20:21:17 GMT  
		Size: 231.2 MB (231157442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593da4ee3c2b9cf8ba865cf0bcf3b58fc15624ee1dd7685e9f43bf546d2f81c9`  
		Last Modified: Mon, 07 Oct 2024 20:21:12 GMT  
		Size: 2.4 MB (2398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6951d7a9161762682e478a3b71e8822a05e2af33e60248f4913a92e195005a`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 472.7 KB (472696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5005b6e94bcd93e08df067e60060f7c0b0f62d8e00f04aee488ef94768fca1f`  
		Last Modified: Mon, 07 Oct 2024 20:21:19 GMT  
		Size: 331.3 MB (331309334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff58e977e68009ac44f0b7414f7a0e2ac195bfb9fe4303955acc67a33929ea10`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb71664b6198a3568af98278a1163b9b0168bf6a98b6fda02756af5334c6664`  
		Last Modified: Mon, 07 Oct 2024 20:21:13 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f231c2b8caa3c4c0257307b59bb859d93f314c023f13da4e2a8af313c89796f5`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ac6c81ec328e11241e07e75155f74e05cd7f870ebb6d5ec66a7ee099b24b7`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:c5b4fa83d6e0d8a7d6fa4cd9cc9286af10333eebcb69f0729655b79542bc35cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39514224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bedc0439fa6e521d8db24ce56ca24c90db5cdcfcd29f30dd5b2606af5f50a216`

```dockerfile
```

-	Layers:
	-	`sha256:2588008565e78b6555ca86898390d6089bc8dd0919071cb09b668f711f497421`  
		Last Modified: Mon, 07 Oct 2024 20:21:14 GMT  
		Size: 39.5 MB (39487492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3abd04ebaea97afb033a95ea0f403614da68216ef25fe607a9479795bdd970`  
		Last Modified: Mon, 07 Oct 2024 20:21:11 GMT  
		Size: 26.7 KB (26732 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20241007` - linux; ppc64le

```console
$ docker pull odoo@sha256:c9c7849a8914fc213cf0cdad653fbc49e7b4a3046869cddcaee6148bbb4cac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614348604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3fc0aaae4f6d58625a13efbb5a6261c5746b2770724140b65cce56e231c51e`
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
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=17.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=4fa14c442f44693556bba99eb4a6b90c13be9b7d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf22e9ecbdb17bae5948434399d20e985516ae45e11e72048320700f4c3002a`  
		Last Modified: Mon, 07 Oct 2024 20:21:39 GMT  
		Size: 243.3 MB (243294995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d72daf6d3193cf48405ab14e7b21e55790dcda77c3e506d6ff2d916be2e81ab`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 2.7 MB (2708338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dabc1a4222c36d4c42eb25f5f2f0249bf9eabf1c589f406f87173d3e7293431`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 472.7 KB (472718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124db12d8f486a52172344f99e4ef0b2bfb16d9821239b125e83d7806488074c`  
		Last Modified: Mon, 07 Oct 2024 20:21:44 GMT  
		Size: 333.4 MB (333421873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ded5e3af0dbff384e1805596730a23773fee78873edd6dfd2ab51bb230cbab3`  
		Last Modified: Mon, 07 Oct 2024 20:21:23 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9878389a7cd65810b8a5288fa3df793a4061e0682ff3f2ed10dc7290e97dac1`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac2c5bcd93bd7c3ffd66f4cf3fe9e8de2c28275205ab2358b020bb63aef219`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad903c2d978fb03c0a2e37a11ec79b83d141641bbdd3cb51d967c80754de03e`  
		Last Modified: Mon, 07 Oct 2024 20:21:25 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:27e1f93d1227d6341fe89aed3f796c5ff11fda59937cd60d8bd66aa924da2700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89987f1998492b30276df26c0f81d79265de5d89aeeecda184af3f8bc302a359`

```dockerfile
```

-	Layers:
	-	`sha256:af3a4e5105b5664b62b8d0b287fee74a6c86c9a5a8a7ba319f13e55e14352b4f`  
		Last Modified: Mon, 07 Oct 2024 20:21:24 GMT  
		Size: 39.5 MB (39489286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef433a4d91a323051092d6b2a91ae987563627672e47d65a5552cd3dfd7bb7c`  
		Last Modified: Mon, 07 Oct 2024 20:21:22 GMT  
		Size: 26.6 KB (26636 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:27d158dc157b43c9521f287ab0a040ebfecec75930b3e0a1d6af5fa9add63d59
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
$ docker pull odoo@sha256:8cffb46374ee8739b24fdfdc2d7cfb883d22c5705a46de413a238be49b96b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.9 MB (651869767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61b2a73543257c065a7972b5280a4c659bf14846ad877ef3be9b112fb43502d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aae7ac0bfc0a6872e8969f199f134828f8b4dd51e0a07ca4f1bc4d81a32b38`  
		Last Modified: Wed, 16 Oct 2024 16:17:38 GMT  
		Size: 255.6 MB (255640144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e81a1e55bf84da6b59d98930228b4b95602851f8de4f94d293ac02d995306`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 14.1 MB (14142300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ea893cee06623227ecf4ce3a79b60e25ce6610fb492df8cdbfb2712c4e41fc`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 472.4 KB (472362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a979d7246f111af62240c5bc27535061f30444300f0c1e816739fe055123f`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 351.9 MB (351862162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72584808ad4aec1e455091f97c00db8b23c106db47f4fe4b6b0460bb4e99aeab`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a14f09b3a5520acd27b73266e5fe1689e5c7a9bef3a92df201c952d9824ff7`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6d64626a8b13a1068dddd36a6aab54510c89d741e6fe3d7b3a2e0f2895821`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae567b4dc9699a7e7ef77643946e0e4036062cb508eeb5c1a9c4685c6db4e07`  
		Last Modified: Wed, 16 Oct 2024 16:17:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:5bcc34aa8b05e2bf812e6d6940b87247f099d7804a745dcf60a06c2c138a3e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55458329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d324599cec8f86d92586f9e49563ca19ce14e83413b2c89a386f1ba5fc5d99f`

```dockerfile
```

-	Layers:
	-	`sha256:7128d76a457b0160c1b146fc57891d0701a4bc9c726f867d7883adb73acede73`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 55.4 MB (55431410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abba925dadde0910083173c3a852324cc585c3bc169a69fd6fed7fe1441d2d3`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8913c75bd3dc6e67d8431dee9d04a6448959eed23595ce4a158a628e9dc15b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.2 MB (648197509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af9685a139ad32ae45805f42b3961d0e648dc1c98c0a672bd33a2be01351880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f2ad32ab69058157eb9f48b389a68262192a44a447caa6e9a96c5180bcfc2c`  
		Last Modified: Wed, 16 Oct 2024 04:02:37 GMT  
		Size: 253.0 MB (252999920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926486042f16a6a923c24027c10f3c2d2689a0db8a32b06c4399917e1e81bd6`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 14.1 MB (14115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bf12eebe020f34f21d46aafe4e3f4eceaf72d4afa3f442408799cf1f9425b`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 472.5 KB (472451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f846a6fc22fa6c4793cd243587638dc80327e57c99fecc60f28137ee0be11e9`  
		Last Modified: Wed, 16 Oct 2024 04:02:38 GMT  
		Size: 351.7 MB (351721110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07e4f294cc4a6465b993dbd7414dec1c014eb35153f3c478cc146397c7e9fbb`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e089f1a16afe87fd0ab113d21c94389129bab9b5c6fb02b52ec1e165db283`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca584cd714316a6c6a591fba9dfb5f498148da60df3bbcd858e2025ea58f8`  
		Last Modified: Wed, 16 Oct 2024 04:02:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4473992f5a5868ca9fdfcf222827bff9f51a7f4aa8daef9b59be5da4e11f4af`  
		Last Modified: Wed, 16 Oct 2024 04:02:34 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:48393e90ddaea262e76ad8f90481194a3305f64d2eca28e190fafcb4aa11741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8008686d2770e1e233a5dd123571bb20f6b207554fb199e21c8d160a1bdf39`

```dockerfile
```

-	Layers:
	-	`sha256:5eff6ae8306c07bacbd54720d9fbed079e3ec25611163e4d0ef6550d34749edc`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 55.4 MB (55438704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb57283523a7623245dd547c2e3b372e5b1b870c16cfc574263911e68293589`  
		Last Modified: Wed, 16 Oct 2024 04:02:30 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:011ff4f4f29baff4ffdb4bab3e0be19bc4f8c503ff8ba439a6aa822756972849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668373208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbd9e888892f4ccc30e4d7bd40543841ad1c0eb23298ea5da73aa2e5f5aab4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4037c9b6d0c0632f5a24e8da67e2f7e0d54ab235bed1c95eaee7a713c81615c8`  
		Last Modified: Wed, 16 Oct 2024 02:26:33 GMT  
		Size: 266.4 MB (266405623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de43aba2291bddb140de3a8e00b78e9ff7f35c14f793e402c5360c40881388`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 14.7 MB (14686074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a8f06768eea9b11c0a1791df7a689ff8ceaf74ed2fdc4dfe0a2aa0f0b417a`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 472.4 KB (472411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5cbcf87d87d05ba418ab743ba4410197a617b9237408d3d13cb8258f064cf5`  
		Last Modified: Wed, 16 Oct 2024 02:26:42 GMT  
		Size: 352.4 MB (352417693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23d6df6855b36433bb18c67adc402fcc1c2bf82681beb48ae80f480e89c3e1c`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084d3605368aefa3028e4572c14936605c896a19f00812325f8d5fc8b260575`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5b5959293b2171b8780fb90855aa8da12caceb51ac8104bab67091dee7deb0`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2deb28a00e03948de2f02b8352994eb301c888c2556d1c064044354e59863a`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:4423f6afea3ec90a4dab67442a0f8d44012f55b9efa94aaafcff6f42efcc7c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed987b63657fcafcf68d6629912edef60d9680c560a2196b215fd656fcafc8df`

```dockerfile
```

-	Layers:
	-	`sha256:a447e0349eeb2a1273cdf38a2edec24802972df7fe4ad3605cf44415f1a15abd`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 55.4 MB (55439553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b9833bf5e374dd31958163b7e04e084f4875a549802a799a364174d27cd8fa`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:27d158dc157b43c9521f287ab0a040ebfecec75930b3e0a1d6af5fa9add63d59
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
$ docker pull odoo@sha256:8cffb46374ee8739b24fdfdc2d7cfb883d22c5705a46de413a238be49b96b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.9 MB (651869767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61b2a73543257c065a7972b5280a4c659bf14846ad877ef3be9b112fb43502d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aae7ac0bfc0a6872e8969f199f134828f8b4dd51e0a07ca4f1bc4d81a32b38`  
		Last Modified: Wed, 16 Oct 2024 16:17:38 GMT  
		Size: 255.6 MB (255640144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e81a1e55bf84da6b59d98930228b4b95602851f8de4f94d293ac02d995306`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 14.1 MB (14142300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ea893cee06623227ecf4ce3a79b60e25ce6610fb492df8cdbfb2712c4e41fc`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 472.4 KB (472362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a979d7246f111af62240c5bc27535061f30444300f0c1e816739fe055123f`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 351.9 MB (351862162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72584808ad4aec1e455091f97c00db8b23c106db47f4fe4b6b0460bb4e99aeab`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a14f09b3a5520acd27b73266e5fe1689e5c7a9bef3a92df201c952d9824ff7`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6d64626a8b13a1068dddd36a6aab54510c89d741e6fe3d7b3a2e0f2895821`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae567b4dc9699a7e7ef77643946e0e4036062cb508eeb5c1a9c4685c6db4e07`  
		Last Modified: Wed, 16 Oct 2024 16:17:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5bcc34aa8b05e2bf812e6d6940b87247f099d7804a745dcf60a06c2c138a3e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55458329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d324599cec8f86d92586f9e49563ca19ce14e83413b2c89a386f1ba5fc5d99f`

```dockerfile
```

-	Layers:
	-	`sha256:7128d76a457b0160c1b146fc57891d0701a4bc9c726f867d7883adb73acede73`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 55.4 MB (55431410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abba925dadde0910083173c3a852324cc585c3bc169a69fd6fed7fe1441d2d3`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8913c75bd3dc6e67d8431dee9d04a6448959eed23595ce4a158a628e9dc15b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.2 MB (648197509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af9685a139ad32ae45805f42b3961d0e648dc1c98c0a672bd33a2be01351880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f2ad32ab69058157eb9f48b389a68262192a44a447caa6e9a96c5180bcfc2c`  
		Last Modified: Wed, 16 Oct 2024 04:02:37 GMT  
		Size: 253.0 MB (252999920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926486042f16a6a923c24027c10f3c2d2689a0db8a32b06c4399917e1e81bd6`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 14.1 MB (14115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bf12eebe020f34f21d46aafe4e3f4eceaf72d4afa3f442408799cf1f9425b`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 472.5 KB (472451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f846a6fc22fa6c4793cd243587638dc80327e57c99fecc60f28137ee0be11e9`  
		Last Modified: Wed, 16 Oct 2024 04:02:38 GMT  
		Size: 351.7 MB (351721110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07e4f294cc4a6465b993dbd7414dec1c014eb35153f3c478cc146397c7e9fbb`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e089f1a16afe87fd0ab113d21c94389129bab9b5c6fb02b52ec1e165db283`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca584cd714316a6c6a591fba9dfb5f498148da60df3bbcd858e2025ea58f8`  
		Last Modified: Wed, 16 Oct 2024 04:02:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4473992f5a5868ca9fdfcf222827bff9f51a7f4aa8daef9b59be5da4e11f4af`  
		Last Modified: Wed, 16 Oct 2024 04:02:34 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:48393e90ddaea262e76ad8f90481194a3305f64d2eca28e190fafcb4aa11741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8008686d2770e1e233a5dd123571bb20f6b207554fb199e21c8d160a1bdf39`

```dockerfile
```

-	Layers:
	-	`sha256:5eff6ae8306c07bacbd54720d9fbed079e3ec25611163e4d0ef6550d34749edc`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 55.4 MB (55438704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb57283523a7623245dd547c2e3b372e5b1b870c16cfc574263911e68293589`  
		Last Modified: Wed, 16 Oct 2024 04:02:30 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:011ff4f4f29baff4ffdb4bab3e0be19bc4f8c503ff8ba439a6aa822756972849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668373208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbd9e888892f4ccc30e4d7bd40543841ad1c0eb23298ea5da73aa2e5f5aab4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4037c9b6d0c0632f5a24e8da67e2f7e0d54ab235bed1c95eaee7a713c81615c8`  
		Last Modified: Wed, 16 Oct 2024 02:26:33 GMT  
		Size: 266.4 MB (266405623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de43aba2291bddb140de3a8e00b78e9ff7f35c14f793e402c5360c40881388`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 14.7 MB (14686074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a8f06768eea9b11c0a1791df7a689ff8ceaf74ed2fdc4dfe0a2aa0f0b417a`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 472.4 KB (472411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5cbcf87d87d05ba418ab743ba4410197a617b9237408d3d13cb8258f064cf5`  
		Last Modified: Wed, 16 Oct 2024 02:26:42 GMT  
		Size: 352.4 MB (352417693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23d6df6855b36433bb18c67adc402fcc1c2bf82681beb48ae80f480e89c3e1c`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084d3605368aefa3028e4572c14936605c896a19f00812325f8d5fc8b260575`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5b5959293b2171b8780fb90855aa8da12caceb51ac8104bab67091dee7deb0`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2deb28a00e03948de2f02b8352994eb301c888c2556d1c064044354e59863a`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4423f6afea3ec90a4dab67442a0f8d44012f55b9efa94aaafcff6f42efcc7c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed987b63657fcafcf68d6629912edef60d9680c560a2196b215fd656fcafc8df`

```dockerfile
```

-	Layers:
	-	`sha256:a447e0349eeb2a1273cdf38a2edec24802972df7fe4ad3605cf44415f1a15abd`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 55.4 MB (55439553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b9833bf5e374dd31958163b7e04e084f4875a549802a799a364174d27cd8fa`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20241007`

```console
$ docker pull odoo@sha256:27d158dc157b43c9521f287ab0a040ebfecec75930b3e0a1d6af5fa9add63d59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20241007` - linux; amd64

```console
$ docker pull odoo@sha256:8cffb46374ee8739b24fdfdc2d7cfb883d22c5705a46de413a238be49b96b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.9 MB (651869767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61b2a73543257c065a7972b5280a4c659bf14846ad877ef3be9b112fb43502d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aae7ac0bfc0a6872e8969f199f134828f8b4dd51e0a07ca4f1bc4d81a32b38`  
		Last Modified: Wed, 16 Oct 2024 16:17:38 GMT  
		Size: 255.6 MB (255640144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e81a1e55bf84da6b59d98930228b4b95602851f8de4f94d293ac02d995306`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 14.1 MB (14142300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ea893cee06623227ecf4ce3a79b60e25ce6610fb492df8cdbfb2712c4e41fc`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 472.4 KB (472362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a979d7246f111af62240c5bc27535061f30444300f0c1e816739fe055123f`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 351.9 MB (351862162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72584808ad4aec1e455091f97c00db8b23c106db47f4fe4b6b0460bb4e99aeab`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a14f09b3a5520acd27b73266e5fe1689e5c7a9bef3a92df201c952d9824ff7`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6d64626a8b13a1068dddd36a6aab54510c89d741e6fe3d7b3a2e0f2895821`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae567b4dc9699a7e7ef77643946e0e4036062cb508eeb5c1a9c4685c6db4e07`  
		Last Modified: Wed, 16 Oct 2024 16:17:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:5bcc34aa8b05e2bf812e6d6940b87247f099d7804a745dcf60a06c2c138a3e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55458329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d324599cec8f86d92586f9e49563ca19ce14e83413b2c89a386f1ba5fc5d99f`

```dockerfile
```

-	Layers:
	-	`sha256:7128d76a457b0160c1b146fc57891d0701a4bc9c726f867d7883adb73acede73`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 55.4 MB (55431410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abba925dadde0910083173c3a852324cc585c3bc169a69fd6fed7fe1441d2d3`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241007` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8913c75bd3dc6e67d8431dee9d04a6448959eed23595ce4a158a628e9dc15b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.2 MB (648197509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af9685a139ad32ae45805f42b3961d0e648dc1c98c0a672bd33a2be01351880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f2ad32ab69058157eb9f48b389a68262192a44a447caa6e9a96c5180bcfc2c`  
		Last Modified: Wed, 16 Oct 2024 04:02:37 GMT  
		Size: 253.0 MB (252999920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926486042f16a6a923c24027c10f3c2d2689a0db8a32b06c4399917e1e81bd6`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 14.1 MB (14115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bf12eebe020f34f21d46aafe4e3f4eceaf72d4afa3f442408799cf1f9425b`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 472.5 KB (472451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f846a6fc22fa6c4793cd243587638dc80327e57c99fecc60f28137ee0be11e9`  
		Last Modified: Wed, 16 Oct 2024 04:02:38 GMT  
		Size: 351.7 MB (351721110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07e4f294cc4a6465b993dbd7414dec1c014eb35153f3c478cc146397c7e9fbb`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e089f1a16afe87fd0ab113d21c94389129bab9b5c6fb02b52ec1e165db283`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca584cd714316a6c6a591fba9dfb5f498148da60df3bbcd858e2025ea58f8`  
		Last Modified: Wed, 16 Oct 2024 04:02:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4473992f5a5868ca9fdfcf222827bff9f51a7f4aa8daef9b59be5da4e11f4af`  
		Last Modified: Wed, 16 Oct 2024 04:02:34 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:48393e90ddaea262e76ad8f90481194a3305f64d2eca28e190fafcb4aa11741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8008686d2770e1e233a5dd123571bb20f6b207554fb199e21c8d160a1bdf39`

```dockerfile
```

-	Layers:
	-	`sha256:5eff6ae8306c07bacbd54720d9fbed079e3ec25611163e4d0ef6550d34749edc`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 55.4 MB (55438704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb57283523a7623245dd547c2e3b372e5b1b870c16cfc574263911e68293589`  
		Last Modified: Wed, 16 Oct 2024 04:02:30 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20241007` - linux; ppc64le

```console
$ docker pull odoo@sha256:011ff4f4f29baff4ffdb4bab3e0be19bc4f8c503ff8ba439a6aa822756972849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668373208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbd9e888892f4ccc30e4d7bd40543841ad1c0eb23298ea5da73aa2e5f5aab4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4037c9b6d0c0632f5a24e8da67e2f7e0d54ab235bed1c95eaee7a713c81615c8`  
		Last Modified: Wed, 16 Oct 2024 02:26:33 GMT  
		Size: 266.4 MB (266405623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de43aba2291bddb140de3a8e00b78e9ff7f35c14f793e402c5360c40881388`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 14.7 MB (14686074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a8f06768eea9b11c0a1791df7a689ff8ceaf74ed2fdc4dfe0a2aa0f0b417a`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 472.4 KB (472411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5cbcf87d87d05ba418ab743ba4410197a617b9237408d3d13cb8258f064cf5`  
		Last Modified: Wed, 16 Oct 2024 02:26:42 GMT  
		Size: 352.4 MB (352417693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23d6df6855b36433bb18c67adc402fcc1c2bf82681beb48ae80f480e89c3e1c`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084d3605368aefa3028e4572c14936605c896a19f00812325f8d5fc8b260575`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5b5959293b2171b8780fb90855aa8da12caceb51ac8104bab67091dee7deb0`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2deb28a00e03948de2f02b8352994eb301c888c2556d1c064044354e59863a`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20241007` - unknown; unknown

```console
$ docker pull odoo@sha256:4423f6afea3ec90a4dab67442a0f8d44012f55b9efa94aaafcff6f42efcc7c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed987b63657fcafcf68d6629912edef60d9680c560a2196b215fd656fcafc8df`

```dockerfile
```

-	Layers:
	-	`sha256:a447e0349eeb2a1273cdf38a2edec24802972df7fe4ad3605cf44415f1a15abd`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 55.4 MB (55439553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b9833bf5e374dd31958163b7e04e084f4875a549802a799a364174d27cd8fa`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:27d158dc157b43c9521f287ab0a040ebfecec75930b3e0a1d6af5fa9add63d59
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
$ docker pull odoo@sha256:8cffb46374ee8739b24fdfdc2d7cfb883d22c5705a46de413a238be49b96b313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **651.9 MB (651869767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61b2a73543257c065a7972b5280a4c659bf14846ad877ef3be9b112fb43502d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47aae7ac0bfc0a6872e8969f199f134828f8b4dd51e0a07ca4f1bc4d81a32b38`  
		Last Modified: Wed, 16 Oct 2024 16:17:38 GMT  
		Size: 255.6 MB (255640144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e81a1e55bf84da6b59d98930228b4b95602851f8de4f94d293ac02d995306`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 14.1 MB (14142300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ea893cee06623227ecf4ce3a79b60e25ce6610fb492df8cdbfb2712c4e41fc`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 472.4 KB (472362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a979d7246f111af62240c5bc27535061f30444300f0c1e816739fe055123f`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 351.9 MB (351862162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72584808ad4aec1e455091f97c00db8b23c106db47f4fe4b6b0460bb4e99aeab`  
		Last Modified: Wed, 16 Oct 2024 16:17:33 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a14f09b3a5520acd27b73266e5fe1689e5c7a9bef3a92df201c952d9824ff7`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d6d64626a8b13a1068dddd36a6aab54510c89d741e6fe3d7b3a2e0f2895821`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae567b4dc9699a7e7ef77643946e0e4036062cb508eeb5c1a9c4685c6db4e07`  
		Last Modified: Wed, 16 Oct 2024 16:17:35 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:5bcc34aa8b05e2bf812e6d6940b87247f099d7804a745dcf60a06c2c138a3e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55458329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d324599cec8f86d92586f9e49563ca19ce14e83413b2c89a386f1ba5fc5d99f`

```dockerfile
```

-	Layers:
	-	`sha256:7128d76a457b0160c1b146fc57891d0701a4bc9c726f867d7883adb73acede73`  
		Last Modified: Wed, 16 Oct 2024 16:17:34 GMT  
		Size: 55.4 MB (55431410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abba925dadde0910083173c3a852324cc585c3bc169a69fd6fed7fe1441d2d3`  
		Last Modified: Wed, 16 Oct 2024 16:17:32 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:8913c75bd3dc6e67d8431dee9d04a6448959eed23595ce4a158a628e9dc15b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.2 MB (648197509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af9685a139ad32ae45805f42b3961d0e648dc1c98c0a672bd33a2be01351880`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f2ad32ab69058157eb9f48b389a68262192a44a447caa6e9a96c5180bcfc2c`  
		Last Modified: Wed, 16 Oct 2024 04:02:37 GMT  
		Size: 253.0 MB (252999920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2926486042f16a6a923c24027c10f3c2d2689a0db8a32b06c4399917e1e81bd6`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 14.1 MB (14115739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8bf12eebe020f34f21d46aafe4e3f4eceaf72d4afa3f442408799cf1f9425b`  
		Last Modified: Wed, 16 Oct 2024 04:02:31 GMT  
		Size: 472.5 KB (472451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f846a6fc22fa6c4793cd243587638dc80327e57c99fecc60f28137ee0be11e9`  
		Last Modified: Wed, 16 Oct 2024 04:02:38 GMT  
		Size: 351.7 MB (351721110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07e4f294cc4a6465b993dbd7414dec1c014eb35153f3c478cc146397c7e9fbb`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298e089f1a16afe87fd0ab113d21c94389129bab9b5c6fb02b52ec1e165db283`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca584cd714316a6c6a591fba9dfb5f498148da60df3bbcd858e2025ea58f8`  
		Last Modified: Wed, 16 Oct 2024 04:02:33 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4473992f5a5868ca9fdfcf222827bff9f51a7f4aa8daef9b59be5da4e11f4af`  
		Last Modified: Wed, 16 Oct 2024 04:02:34 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:48393e90ddaea262e76ad8f90481194a3305f64d2eca28e190fafcb4aa11741d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8008686d2770e1e233a5dd123571bb20f6b207554fb199e21c8d160a1bdf39`

```dockerfile
```

-	Layers:
	-	`sha256:5eff6ae8306c07bacbd54720d9fbed079e3ec25611163e4d0ef6550d34749edc`  
		Last Modified: Wed, 16 Oct 2024 04:02:32 GMT  
		Size: 55.4 MB (55438704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb57283523a7623245dd547c2e3b372e5b1b870c16cfc574263911e68293589`  
		Last Modified: Wed, 16 Oct 2024 04:02:30 GMT  
		Size: 27.1 KB (27078 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:011ff4f4f29baff4ffdb4bab3e0be19bc4f8c503ff8ba439a6aa822756972849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.4 MB (668373208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdbd9e888892f4ccc30e4d7bd40543841ad1c0eb23298ea5da73aa2e5f5aab4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 07 Oct 2024 08:31:27 GMT
ARG RELEASE
# Mon, 07 Oct 2024 08:31:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Oct 2024 08:31:27 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 07 Oct 2024 08:31:27 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["/bin/bash"]
# Mon, 07 Oct 2024 08:31:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 07 Oct 2024 08:31:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV LANG=en_US.UTF-8
# Mon, 07 Oct 2024 08:31:27 GMT
ARG TARGETARCH
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_VERSION=18.0
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_RELEASE=20241007
# Mon, 07 Oct 2024 08:31:27 GMT
ARG ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241007 ODOO_SHA=d96c137e1dc0a60a78767a3a959be49d9ba615c1
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 07 Oct 2024 08:31:27 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 07 Oct 2024 08:31:27 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 07 Oct 2024 08:31:27 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 07 Oct 2024 08:31:27 GMT
USER odoo
# Mon, 07 Oct 2024 08:31:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Oct 2024 08:31:27 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4037c9b6d0c0632f5a24e8da67e2f7e0d54ab235bed1c95eaee7a713c81615c8`  
		Last Modified: Wed, 16 Oct 2024 02:26:33 GMT  
		Size: 266.4 MB (266405623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de43aba2291bddb140de3a8e00b78e9ff7f35c14f793e402c5360c40881388`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 14.7 MB (14686074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666a8f06768eea9b11c0a1791df7a689ff8ceaf74ed2fdc4dfe0a2aa0f0b417a`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 472.4 KB (472411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5cbcf87d87d05ba418ab743ba4410197a617b9237408d3d13cb8258f064cf5`  
		Last Modified: Wed, 16 Oct 2024 02:26:42 GMT  
		Size: 352.4 MB (352417693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23d6df6855b36433bb18c67adc402fcc1c2bf82681beb48ae80f480e89c3e1c`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d084d3605368aefa3028e4572c14936605c896a19f00812325f8d5fc8b260575`  
		Last Modified: Wed, 16 Oct 2024 02:26:16 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5b5959293b2171b8780fb90855aa8da12caceb51ac8104bab67091dee7deb0`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2deb28a00e03948de2f02b8352994eb301c888c2556d1c064044354e59863a`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:4423f6afea3ec90a4dab67442a0f8d44012f55b9efa94aaafcff6f42efcc7c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55466529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed987b63657fcafcf68d6629912edef60d9680c560a2196b215fd656fcafc8df`

```dockerfile
```

-	Layers:
	-	`sha256:a447e0349eeb2a1273cdf38a2edec24802972df7fe4ad3605cf44415f1a15abd`  
		Last Modified: Wed, 16 Oct 2024 02:26:17 GMT  
		Size: 55.4 MB (55439553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b9833bf5e374dd31958163b7e04e084f4875a549802a799a364174d27cd8fa`  
		Last Modified: Wed, 16 Oct 2024 02:26:14 GMT  
		Size: 27.0 KB (26976 bytes)  
		MIME: application/vnd.in-toto+json
