<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260217`](#odoo170-20260217)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260217`](#odoo180-20260217)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260217`](#odoo190-20260217)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:3dcbcfb395b33f5f308bfb8f6eafa6c3cc4a522ae5e0bdcb5b987bee3201047d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:b8e74dbcdfa895c3d0bc687822aeb51a51130ab5fe83a2c38cbad3d6b17a0039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (608970274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04de5e9e697bd0edb3bc9749f9ebde82e853c3e78386d6d7868877fa588720f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:18 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Feb 2026 20:30:28 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:28 GMT
ARG ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
# Tue, 17 Feb 2026 20:31:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be1e85ccdd4c77710c2aee1ee844311f465824136c1a6083af37ff2eb0495`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 233.8 MB (233826101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e0cf646d95f6423966a5ab4d95ea5bed950fa324b2f7505da45acc6481308`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 2.6 MB (2601307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93ebf5132d2d3ac3f9e17b644472a9ecde1c917e7a1fbd19b52bab5694f95d9`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 480.3 KB (480260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3242898933d645a3a285d43b9ab69664e714ec126238f98da5da2de8ebd6b`  
		Last Modified: Tue, 17 Feb 2026 20:32:54 GMT  
		Size: 342.5 MB (342522798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48ca2b1d4c46d1b37b1481ea4c9da7a97cd387b2a903b42e044c999b719d9f`  
		Last Modified: Tue, 17 Feb 2026 20:32:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f12b024407dd6295bd5cce4cbc987e1e875680200a102e2d10d41e95f862eab`  
		Last Modified: Tue, 17 Feb 2026 20:32:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d38e2b29b57066dfb93e5d9623c89af11bd89ab895fd8919574ee5e9f3bdf9a`  
		Last Modified: Tue, 17 Feb 2026 20:32:46 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771ad3895c1d2a13d8a8fbf2a4b0ca3f4faed17733b887bd87a0662b8054cdf4`  
		Last Modified: Tue, 17 Feb 2026 20:32:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:9fa14ea587c3af75627ee753dbaa141c676b50583f5bcc76625f605b0a8c2951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41991392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3a3e74ec0aaa266c15d86c0ac39bad216d3199f7922a81d53acfd3d916f7f`

```dockerfile
```

-	Layers:
	-	`sha256:be2c89bf1ceea07afa71683ae74a916e3fcdf76361e3c68364eb7ca34ef72d3c`  
		Last Modified: Tue, 17 Feb 2026 20:32:45 GMT  
		Size: 42.0 MB (41964600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e755b6d5ceead7ef7a745baaa8484d551459b372b123e5c1c7743a33d6697a39`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:447e02cdf7e026db9ce4ffc4efa9671bf9b71c622b746512acaa4ab830f4db6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.8 MB (603806712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130120af91c530e7559be58376706ad8b4636bff2c786b3f469b290e06c337c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:04 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:04 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Feb 2026 20:29:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:15 GMT
ARG ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
# Tue, 17 Feb 2026 20:30:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f89419fa9d69bf5991fdc7eba6e7f579300b384d7a19919a0f681af5de54d3d`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 231.2 MB (231197636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a228e05bd65a9cd8b9a6cb3164b84258a8101d757752d48200aa739585f240e7`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 2.6 MB (2595144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa08280b773481b0499c03887a6cd466b49be17765491623966583b5660113`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 480.3 KB (480267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff338d60ff3d64884e4d59c8c20a38ab8cc0e1d998d539ec7ffd81fd75dd55`  
		Last Modified: Tue, 17 Feb 2026 20:31:55 GMT  
		Size: 342.1 MB (342146284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b431441ab323a62dfe23e8497d88623771619a6a7ab779784bf50b553c22dec`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb12c6790c9965ea553267ecbcf6a349b83ea7b27293c0e2f949b5aef3c5ecf`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41032945d12a7dd790e50a7d84764a759d4292fa2a862bfefa3a0f57cc8ec99`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d631c1b4a3e43e941408ae8f4ad6850ca7b284f0b14a885cf639908375273`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:52d425161ef8fef4e93e5c10ead16ac8ab6512d757e356fa1ee14da670a40574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41998048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe347bb62723a7dbd14f192534ea00950cd3f9a06d7c94ac534566be54ee1ec`

```dockerfile
```

-	Layers:
	-	`sha256:d57de9836606a7d7e06d5bafc4af40e8e8d7712b87ef90d91ff69818f427665f`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 42.0 MB (41971107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b87d862b149959ef5b0130011cec2ff5aaf1acd406f19cfab1ac14db40e8bbf`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 26.9 KB (26941 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:3dcbcfb395b33f5f308bfb8f6eafa6c3cc4a522ae5e0bdcb5b987bee3201047d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:b8e74dbcdfa895c3d0bc687822aeb51a51130ab5fe83a2c38cbad3d6b17a0039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (608970274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04de5e9e697bd0edb3bc9749f9ebde82e853c3e78386d6d7868877fa588720f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:18 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Feb 2026 20:30:28 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:28 GMT
ARG ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
# Tue, 17 Feb 2026 20:31:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be1e85ccdd4c77710c2aee1ee844311f465824136c1a6083af37ff2eb0495`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 233.8 MB (233826101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e0cf646d95f6423966a5ab4d95ea5bed950fa324b2f7505da45acc6481308`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 2.6 MB (2601307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93ebf5132d2d3ac3f9e17b644472a9ecde1c917e7a1fbd19b52bab5694f95d9`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 480.3 KB (480260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3242898933d645a3a285d43b9ab69664e714ec126238f98da5da2de8ebd6b`  
		Last Modified: Tue, 17 Feb 2026 20:32:54 GMT  
		Size: 342.5 MB (342522798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48ca2b1d4c46d1b37b1481ea4c9da7a97cd387b2a903b42e044c999b719d9f`  
		Last Modified: Tue, 17 Feb 2026 20:32:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f12b024407dd6295bd5cce4cbc987e1e875680200a102e2d10d41e95f862eab`  
		Last Modified: Tue, 17 Feb 2026 20:32:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d38e2b29b57066dfb93e5d9623c89af11bd89ab895fd8919574ee5e9f3bdf9a`  
		Last Modified: Tue, 17 Feb 2026 20:32:46 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771ad3895c1d2a13d8a8fbf2a4b0ca3f4faed17733b887bd87a0662b8054cdf4`  
		Last Modified: Tue, 17 Feb 2026 20:32:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9fa14ea587c3af75627ee753dbaa141c676b50583f5bcc76625f605b0a8c2951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41991392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3a3e74ec0aaa266c15d86c0ac39bad216d3199f7922a81d53acfd3d916f7f`

```dockerfile
```

-	Layers:
	-	`sha256:be2c89bf1ceea07afa71683ae74a916e3fcdf76361e3c68364eb7ca34ef72d3c`  
		Last Modified: Tue, 17 Feb 2026 20:32:45 GMT  
		Size: 42.0 MB (41964600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e755b6d5ceead7ef7a745baaa8484d551459b372b123e5c1c7743a33d6697a39`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:447e02cdf7e026db9ce4ffc4efa9671bf9b71c622b746512acaa4ab830f4db6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.8 MB (603806712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130120af91c530e7559be58376706ad8b4636bff2c786b3f469b290e06c337c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:04 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:04 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Feb 2026 20:29:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:15 GMT
ARG ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
# Tue, 17 Feb 2026 20:30:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f89419fa9d69bf5991fdc7eba6e7f579300b384d7a19919a0f681af5de54d3d`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 231.2 MB (231197636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a228e05bd65a9cd8b9a6cb3164b84258a8101d757752d48200aa739585f240e7`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 2.6 MB (2595144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa08280b773481b0499c03887a6cd466b49be17765491623966583b5660113`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 480.3 KB (480267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff338d60ff3d64884e4d59c8c20a38ab8cc0e1d998d539ec7ffd81fd75dd55`  
		Last Modified: Tue, 17 Feb 2026 20:31:55 GMT  
		Size: 342.1 MB (342146284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b431441ab323a62dfe23e8497d88623771619a6a7ab779784bf50b553c22dec`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb12c6790c9965ea553267ecbcf6a349b83ea7b27293c0e2f949b5aef3c5ecf`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41032945d12a7dd790e50a7d84764a759d4292fa2a862bfefa3a0f57cc8ec99`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d631c1b4a3e43e941408ae8f4ad6850ca7b284f0b14a885cf639908375273`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:52d425161ef8fef4e93e5c10ead16ac8ab6512d757e356fa1ee14da670a40574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41998048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe347bb62723a7dbd14f192534ea00950cd3f9a06d7c94ac534566be54ee1ec`

```dockerfile
```

-	Layers:
	-	`sha256:d57de9836606a7d7e06d5bafc4af40e8e8d7712b87ef90d91ff69818f427665f`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 42.0 MB (41971107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b87d862b149959ef5b0130011cec2ff5aaf1acd406f19cfab1ac14db40e8bbf`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 26.9 KB (26941 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260217`

```console
$ docker pull odoo@sha256:3dcbcfb395b33f5f308bfb8f6eafa6c3cc4a522ae5e0bdcb5b987bee3201047d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260217` - linux; amd64

```console
$ docker pull odoo@sha256:b8e74dbcdfa895c3d0bc687822aeb51a51130ab5fe83a2c38cbad3d6b17a0039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (608970274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04de5e9e697bd0edb3bc9749f9ebde82e853c3e78386d6d7868877fa588720f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:18 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:18 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:18 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:18 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Feb 2026 20:30:28 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:28 GMT
ARG ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
# Tue, 17 Feb 2026 20:31:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:32 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:32 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:32 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:32 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:32 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be1e85ccdd4c77710c2aee1ee844311f465824136c1a6083af37ff2eb0495`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 233.8 MB (233826101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625e0cf646d95f6423966a5ab4d95ea5bed950fa324b2f7505da45acc6481308`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 2.6 MB (2601307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93ebf5132d2d3ac3f9e17b644472a9ecde1c917e7a1fbd19b52bab5694f95d9`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 480.3 KB (480260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3242898933d645a3a285d43b9ab69664e714ec126238f98da5da2de8ebd6b`  
		Last Modified: Tue, 17 Feb 2026 20:32:54 GMT  
		Size: 342.5 MB (342522798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48ca2b1d4c46d1b37b1481ea4c9da7a97cd387b2a903b42e044c999b719d9f`  
		Last Modified: Tue, 17 Feb 2026 20:32:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f12b024407dd6295bd5cce4cbc987e1e875680200a102e2d10d41e95f862eab`  
		Last Modified: Tue, 17 Feb 2026 20:32:45 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d38e2b29b57066dfb93e5d9623c89af11bd89ab895fd8919574ee5e9f3bdf9a`  
		Last Modified: Tue, 17 Feb 2026 20:32:46 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771ad3895c1d2a13d8a8fbf2a4b0ca3f4faed17733b887bd87a0662b8054cdf4`  
		Last Modified: Tue, 17 Feb 2026 20:32:46 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:9fa14ea587c3af75627ee753dbaa141c676b50583f5bcc76625f605b0a8c2951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41991392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de3a3e74ec0aaa266c15d86c0ac39bad216d3199f7922a81d53acfd3d916f7f`

```dockerfile
```

-	Layers:
	-	`sha256:be2c89bf1ceea07afa71683ae74a916e3fcdf76361e3c68364eb7ca34ef72d3c`  
		Last Modified: Tue, 17 Feb 2026 20:32:45 GMT  
		Size: 42.0 MB (41964600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e755b6d5ceead7ef7a745baaa8484d551459b372b123e5c1c7743a33d6697a39`  
		Last Modified: Tue, 17 Feb 2026 20:32:43 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260217` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:447e02cdf7e026db9ce4ffc4efa9671bf9b71c622b746512acaa4ab830f4db6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.8 MB (603806712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130120af91c530e7559be58376706ad8b4636bff2c786b3f469b290e06c337c8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:04 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:04 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:04 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:04 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:04 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:15 GMT
ENV ODOO_VERSION=17.0
# Tue, 17 Feb 2026 20:29:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:15 GMT
ARG ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
# Tue, 17 Feb 2026 20:30:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=1b6d221ed66be6e1e8ca402f5551c0ed3c301e27
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:23 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f89419fa9d69bf5991fdc7eba6e7f579300b384d7a19919a0f681af5de54d3d`  
		Last Modified: Tue, 17 Feb 2026 20:31:52 GMT  
		Size: 231.2 MB (231197636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a228e05bd65a9cd8b9a6cb3164b84258a8101d757752d48200aa739585f240e7`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 2.6 MB (2595144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aa08280b773481b0499c03887a6cd466b49be17765491623966583b5660113`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 480.3 KB (480267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff338d60ff3d64884e4d59c8c20a38ab8cc0e1d998d539ec7ffd81fd75dd55`  
		Last Modified: Tue, 17 Feb 2026 20:31:55 GMT  
		Size: 342.1 MB (342146284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b431441ab323a62dfe23e8497d88623771619a6a7ab779784bf50b553c22dec`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb12c6790c9965ea553267ecbcf6a349b83ea7b27293c0e2f949b5aef3c5ecf`  
		Last Modified: Tue, 17 Feb 2026 20:31:46 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41032945d12a7dd790e50a7d84764a759d4292fa2a862bfefa3a0f57cc8ec99`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d631c1b4a3e43e941408ae8f4ad6850ca7b284f0b14a885cf639908375273`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:52d425161ef8fef4e93e5c10ead16ac8ab6512d757e356fa1ee14da670a40574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (41998048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe347bb62723a7dbd14f192534ea00950cd3f9a06d7c94ac534566be54ee1ec`

```dockerfile
```

-	Layers:
	-	`sha256:d57de9836606a7d7e06d5bafc4af40e8e8d7712b87ef90d91ff69818f427665f`  
		Last Modified: Tue, 17 Feb 2026 20:31:47 GMT  
		Size: 42.0 MB (41971107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b87d862b149959ef5b0130011cec2ff5aaf1acd406f19cfab1ac14db40e8bbf`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 26.9 KB (26941 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:3cebb4f94bebb27c6e8a7a2fc22efbc5adc68d60a33ec3055eff9bda857561b4
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
$ docker pull odoo@sha256:f943845750728960f9c3891a7076a72bd257f5b2d50d1c3d993e29a6e06d9489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.5 MB (683540031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d7bc07d7ba5a9833135da2c0e2bc215071b9bad5b33b0f745406ee488c0a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:37 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:37 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:45 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:46 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:30:46 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:46 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 20:31:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756ba15cc7a6e4633cba6fd4713340c62ecf54ab51bf62ad032adbe917a861c6`  
		Last Modified: Tue, 17 Feb 2026 20:33:48 GMT  
		Size: 255.7 MB (255667982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5fda274fcf39d23f53c190742e308fa3a1c4727dcf7b37c036df7a80038075`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 14.4 MB (14359213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea74b60c03cf8ef6803a9040c47c561f018a5f7b765f00ac1628aa307f729376`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 480.0 KB (479991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8e6a84c7a1b548f03452f00acea751ffabf82555bebbf91aedf3fdd52ead26`  
		Last Modified: Tue, 17 Feb 2026 20:33:47 GMT  
		Size: 383.3 MB (383302792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a642a6f35f489f625d1a148053c0b1bb1fcb2a0efe380ccd12307a12fc98cb`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990de57c963be83f8ad03f6d84b8dfe4835f106e35dc17269602d0e26e56fc5`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f522850449ae9e37593ef27eb8df47f916cbb41cc47d4de88e623eb530b466`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f332abea05f7eb714ac5d5eae2405a181c88fddde6e99e4be8897712291fa5`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:84e16c9192f50630470d4414fba851b028bed133a1d57022a9504dd69330d3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61645391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9704e90698c07d178db216da46d83b6525ef4233a6b41565c9091112fbff43`

```dockerfile
```

-	Layers:
	-	`sha256:c08672c5c9e88b132f0911aea7c5ea3a5fbdb2b1470ddf3ee0eda9169c37e48c`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 61.6 MB (61618592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8699f3c986718bd4558cd698050677d23b567daf315a1e041e65cd098752113d`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c58c5b9b3dbf7896220bf3288da6aa38bc4e8cb96506097c875a6d8a389848dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 MB (679858243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7108361295145a458789956f5a738b855019a624ae90b1f30a43db15fe15fca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:27 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:27 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:38 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:29:38 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:38 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 20:30:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff461c982e1a8a6d1c4a4e4854c8a105c1f29666c23630d64eab6b93feebed1`  
		Last Modified: Tue, 17 Feb 2026 20:32:56 GMT  
		Size: 253.0 MB (253042532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e739627195c1654546f3267bab0286b61f221743db3816fe521603ed5cfbae`  
		Last Modified: Tue, 17 Feb 2026 20:32:49 GMT  
		Size: 14.3 MB (14339724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0ffccab55e47942386db870be79f069beb7add625f395caa912ff52afee57`  
		Last Modified: Tue, 17 Feb 2026 20:32:48 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337082f64eaa40c006b9f9b9a4bd6aef067bb3bf00416085a0c03d84d315fcef`  
		Last Modified: Tue, 17 Feb 2026 20:32:59 GMT  
		Size: 383.1 MB (383128410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3aa319417bc4f48a494ad19977c851b151c9a8842a42894d1a42084f3c9bc6`  
		Last Modified: Tue, 17 Feb 2026 20:32:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b55c7b19c52f17e7c25d05bdb8454a170c6a4baad1f04d0679737380aca3dd2`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cee277c383221917b37efd94b71ab6491d7cbb6bac1c1b22c502ea1f3e7d295`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd04946ac4f7feeb56c33b1e00acaf77563106d8e8eb1f4f402f15be1dbab803`  
		Last Modified: Tue, 17 Feb 2026 20:32:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c19f21963d9af2e87f115ff0fd0ae87acee044710cf54f6e357a42fec36ba497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61652817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e2d7f043a5a1844e680954edf981effb98b2cda5de579113e93500337ceac`

```dockerfile
```

-	Layers:
	-	`sha256:7fa6b9e8337a222215b67337dcad4e3d41a5f418f526fbc48c58d7aaf7a80135`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 61.6 MB (61625867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad1b8f1806fbb881e232ab47fd158c18e1eefd5d0ea7b94784adec24df17887`  
		Last Modified: Tue, 17 Feb 2026 20:32:48 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:6d82bdd53781f63f23e7d77c9bafbfb55a371084e4ef34fca656bdb82d3027db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.9 MB (699882241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d12323700639ec7a95db9161d56737c5cfa8fc2c677ec37325d762af54678b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:57:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:57:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:57:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:57:56 GMT
ARG TARGETARCH=ppc64le
# Tue, 17 Feb 2026 20:57:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:58:13 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 21:00:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 21:00:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 21:00:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 21:00:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 21:00:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
USER odoo
# Tue, 17 Feb 2026 21:00:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:00:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0169bf586568d779da1131c69587cc539ba8404f5cf298d3606a68076b46e`  
		Last Modified: Tue, 17 Feb 2026 21:06:01 GMT  
		Size: 266.4 MB (266360265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695e1dac687d4505fae48b4784af147d88ec0ed98b7a1fcb7cbddbaf5040b12`  
		Last Modified: Tue, 17 Feb 2026 21:05:50 GMT  
		Size: 14.9 MB (14888865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f2f1a7484f8b97f5992754300b1d623696d153b5c0b35c1f8b7854dd25a3`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 480.1 KB (480061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ba312fbb28049af395109952b81b03ca99f1c16981dd48bbbad162ed8a587`  
		Last Modified: Tue, 17 Feb 2026 21:06:03 GMT  
		Size: 383.8 MB (383843703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b2ae62cbeeff4227e57663a3a5cb5f79be054e198505d46cbf672aa3dfee7e`  
		Last Modified: Tue, 17 Feb 2026 21:05:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9923781140e7178f0a0ddc137548ed1e850b1d4d4566254fe3a13251cbe316`  
		Last Modified: Tue, 17 Feb 2026 21:05:52 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaeecfc00e81699ca3be9cbb9dbcb93fce494eb2279bf1dc3253f9a4c15819d1`  
		Last Modified: Tue, 17 Feb 2026 21:05:52 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d423631fd3fdbb34efc6b80d5d9b01f3d4f20866cd89743a9b8f1537147606c2`  
		Last Modified: Tue, 17 Feb 2026 21:05:53 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:df82546af4dadf3c05fdb51474354af8316eb2bde77d39c0d3a5c273879003a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61653830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291a5739cc0564074279b6f806dcc94b814050d968bc8f1860fb46a655998821`

```dockerfile
```

-	Layers:
	-	`sha256:a27c4dd3823c3f7b3b889a31ed6e4dc8eb5b2b4463c979a2553d6ba6c379b954`  
		Last Modified: Tue, 17 Feb 2026 21:05:54 GMT  
		Size: 61.6 MB (61626975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44393ee56263ec9c1c640d4d07a8b8099371d19457ca57a47f328502267040f8`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:3cebb4f94bebb27c6e8a7a2fc22efbc5adc68d60a33ec3055eff9bda857561b4
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
$ docker pull odoo@sha256:f943845750728960f9c3891a7076a72bd257f5b2d50d1c3d993e29a6e06d9489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.5 MB (683540031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d7bc07d7ba5a9833135da2c0e2bc215071b9bad5b33b0f745406ee488c0a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:37 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:37 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:45 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:46 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:30:46 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:46 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 20:31:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756ba15cc7a6e4633cba6fd4713340c62ecf54ab51bf62ad032adbe917a861c6`  
		Last Modified: Tue, 17 Feb 2026 20:33:48 GMT  
		Size: 255.7 MB (255667982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5fda274fcf39d23f53c190742e308fa3a1c4727dcf7b37c036df7a80038075`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 14.4 MB (14359213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea74b60c03cf8ef6803a9040c47c561f018a5f7b765f00ac1628aa307f729376`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 480.0 KB (479991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8e6a84c7a1b548f03452f00acea751ffabf82555bebbf91aedf3fdd52ead26`  
		Last Modified: Tue, 17 Feb 2026 20:33:47 GMT  
		Size: 383.3 MB (383302792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a642a6f35f489f625d1a148053c0b1bb1fcb2a0efe380ccd12307a12fc98cb`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990de57c963be83f8ad03f6d84b8dfe4835f106e35dc17269602d0e26e56fc5`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f522850449ae9e37593ef27eb8df47f916cbb41cc47d4de88e623eb530b466`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f332abea05f7eb714ac5d5eae2405a181c88fddde6e99e4be8897712291fa5`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:84e16c9192f50630470d4414fba851b028bed133a1d57022a9504dd69330d3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61645391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9704e90698c07d178db216da46d83b6525ef4233a6b41565c9091112fbff43`

```dockerfile
```

-	Layers:
	-	`sha256:c08672c5c9e88b132f0911aea7c5ea3a5fbdb2b1470ddf3ee0eda9169c37e48c`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 61.6 MB (61618592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8699f3c986718bd4558cd698050677d23b567daf315a1e041e65cd098752113d`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c58c5b9b3dbf7896220bf3288da6aa38bc4e8cb96506097c875a6d8a389848dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 MB (679858243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7108361295145a458789956f5a738b855019a624ae90b1f30a43db15fe15fca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:27 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:27 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:38 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:29:38 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:38 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 20:30:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff461c982e1a8a6d1c4a4e4854c8a105c1f29666c23630d64eab6b93feebed1`  
		Last Modified: Tue, 17 Feb 2026 20:32:56 GMT  
		Size: 253.0 MB (253042532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e739627195c1654546f3267bab0286b61f221743db3816fe521603ed5cfbae`  
		Last Modified: Tue, 17 Feb 2026 20:32:49 GMT  
		Size: 14.3 MB (14339724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0ffccab55e47942386db870be79f069beb7add625f395caa912ff52afee57`  
		Last Modified: Tue, 17 Feb 2026 20:32:48 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337082f64eaa40c006b9f9b9a4bd6aef067bb3bf00416085a0c03d84d315fcef`  
		Last Modified: Tue, 17 Feb 2026 20:32:59 GMT  
		Size: 383.1 MB (383128410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3aa319417bc4f48a494ad19977c851b151c9a8842a42894d1a42084f3c9bc6`  
		Last Modified: Tue, 17 Feb 2026 20:32:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b55c7b19c52f17e7c25d05bdb8454a170c6a4baad1f04d0679737380aca3dd2`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cee277c383221917b37efd94b71ab6491d7cbb6bac1c1b22c502ea1f3e7d295`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd04946ac4f7feeb56c33b1e00acaf77563106d8e8eb1f4f402f15be1dbab803`  
		Last Modified: Tue, 17 Feb 2026 20:32:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c19f21963d9af2e87f115ff0fd0ae87acee044710cf54f6e357a42fec36ba497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61652817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e2d7f043a5a1844e680954edf981effb98b2cda5de579113e93500337ceac`

```dockerfile
```

-	Layers:
	-	`sha256:7fa6b9e8337a222215b67337dcad4e3d41a5f418f526fbc48c58d7aaf7a80135`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 61.6 MB (61625867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad1b8f1806fbb881e232ab47fd158c18e1eefd5d0ea7b94784adec24df17887`  
		Last Modified: Tue, 17 Feb 2026 20:32:48 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:6d82bdd53781f63f23e7d77c9bafbfb55a371084e4ef34fca656bdb82d3027db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.9 MB (699882241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d12323700639ec7a95db9161d56737c5cfa8fc2c677ec37325d762af54678b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:57:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:57:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:57:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:57:56 GMT
ARG TARGETARCH=ppc64le
# Tue, 17 Feb 2026 20:57:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:58:13 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 21:00:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 21:00:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 21:00:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 21:00:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 21:00:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
USER odoo
# Tue, 17 Feb 2026 21:00:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:00:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0169bf586568d779da1131c69587cc539ba8404f5cf298d3606a68076b46e`  
		Last Modified: Tue, 17 Feb 2026 21:06:01 GMT  
		Size: 266.4 MB (266360265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695e1dac687d4505fae48b4784af147d88ec0ed98b7a1fcb7cbddbaf5040b12`  
		Last Modified: Tue, 17 Feb 2026 21:05:50 GMT  
		Size: 14.9 MB (14888865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f2f1a7484f8b97f5992754300b1d623696d153b5c0b35c1f8b7854dd25a3`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 480.1 KB (480061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ba312fbb28049af395109952b81b03ca99f1c16981dd48bbbad162ed8a587`  
		Last Modified: Tue, 17 Feb 2026 21:06:03 GMT  
		Size: 383.8 MB (383843703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b2ae62cbeeff4227e57663a3a5cb5f79be054e198505d46cbf672aa3dfee7e`  
		Last Modified: Tue, 17 Feb 2026 21:05:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9923781140e7178f0a0ddc137548ed1e850b1d4d4566254fe3a13251cbe316`  
		Last Modified: Tue, 17 Feb 2026 21:05:52 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaeecfc00e81699ca3be9cbb9dbcb93fce494eb2279bf1dc3253f9a4c15819d1`  
		Last Modified: Tue, 17 Feb 2026 21:05:52 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d423631fd3fdbb34efc6b80d5d9b01f3d4f20866cd89743a9b8f1537147606c2`  
		Last Modified: Tue, 17 Feb 2026 21:05:53 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:df82546af4dadf3c05fdb51474354af8316eb2bde77d39c0d3a5c273879003a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61653830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291a5739cc0564074279b6f806dcc94b814050d968bc8f1860fb46a655998821`

```dockerfile
```

-	Layers:
	-	`sha256:a27c4dd3823c3f7b3b889a31ed6e4dc8eb5b2b4463c979a2553d6ba6c379b954`  
		Last Modified: Tue, 17 Feb 2026 21:05:54 GMT  
		Size: 61.6 MB (61626975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44393ee56263ec9c1c640d4d07a8b8099371d19457ca57a47f328502267040f8`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260217`

```console
$ docker pull odoo@sha256:3cebb4f94bebb27c6e8a7a2fc22efbc5adc68d60a33ec3055eff9bda857561b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260217` - linux; amd64

```console
$ docker pull odoo@sha256:f943845750728960f9c3891a7076a72bd257f5b2d50d1c3d993e29a6e06d9489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.5 MB (683540031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d7bc07d7ba5a9833135da2c0e2bc215071b9bad5b33b0f745406ee488c0a7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:37 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:37 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:37 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:37 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:37 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:45 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:46 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:46 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:30:46 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:46 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 20:31:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:42 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756ba15cc7a6e4633cba6fd4713340c62ecf54ab51bf62ad032adbe917a861c6`  
		Last Modified: Tue, 17 Feb 2026 20:33:48 GMT  
		Size: 255.7 MB (255667982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5fda274fcf39d23f53c190742e308fa3a1c4727dcf7b37c036df7a80038075`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 14.4 MB (14359213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea74b60c03cf8ef6803a9040c47c561f018a5f7b765f00ac1628aa307f729376`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 480.0 KB (479991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8e6a84c7a1b548f03452f00acea751ffabf82555bebbf91aedf3fdd52ead26`  
		Last Modified: Tue, 17 Feb 2026 20:33:47 GMT  
		Size: 383.3 MB (383302792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a642a6f35f489f625d1a148053c0b1bb1fcb2a0efe380ccd12307a12fc98cb`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990de57c963be83f8ad03f6d84b8dfe4835f106e35dc17269602d0e26e56fc5`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f522850449ae9e37593ef27eb8df47f916cbb41cc47d4de88e623eb530b466`  
		Last Modified: Tue, 17 Feb 2026 20:33:36 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f332abea05f7eb714ac5d5eae2405a181c88fddde6e99e4be8897712291fa5`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:84e16c9192f50630470d4414fba851b028bed133a1d57022a9504dd69330d3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61645391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9704e90698c07d178db216da46d83b6525ef4233a6b41565c9091112fbff43`

```dockerfile
```

-	Layers:
	-	`sha256:c08672c5c9e88b132f0911aea7c5ea3a5fbdb2b1470ddf3ee0eda9169c37e48c`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 61.6 MB (61618592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8699f3c986718bd4558cd698050677d23b567daf315a1e041e65cd098752113d`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260217` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c58c5b9b3dbf7896220bf3288da6aa38bc4e8cb96506097c875a6d8a389848dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **679.9 MB (679858243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7108361295145a458789956f5a738b855019a624ae90b1f30a43db15fe15fca`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:27 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:27 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:27 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:27 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:27 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:36 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:38 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:38 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:29:38 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:38 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 20:30:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:33 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff461c982e1a8a6d1c4a4e4854c8a105c1f29666c23630d64eab6b93feebed1`  
		Last Modified: Tue, 17 Feb 2026 20:32:56 GMT  
		Size: 253.0 MB (253042532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e739627195c1654546f3267bab0286b61f221743db3816fe521603ed5cfbae`  
		Last Modified: Tue, 17 Feb 2026 20:32:49 GMT  
		Size: 14.3 MB (14339724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c0ffccab55e47942386db870be79f069beb7add625f395caa912ff52afee57`  
		Last Modified: Tue, 17 Feb 2026 20:32:48 GMT  
		Size: 480.0 KB (480018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337082f64eaa40c006b9f9b9a4bd6aef067bb3bf00416085a0c03d84d315fcef`  
		Last Modified: Tue, 17 Feb 2026 20:32:59 GMT  
		Size: 383.1 MB (383128410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3aa319417bc4f48a494ad19977c851b151c9a8842a42894d1a42084f3c9bc6`  
		Last Modified: Tue, 17 Feb 2026 20:32:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b55c7b19c52f17e7c25d05bdb8454a170c6a4baad1f04d0679737380aca3dd2`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cee277c383221917b37efd94b71ab6491d7cbb6bac1c1b22c502ea1f3e7d295`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd04946ac4f7feeb56c33b1e00acaf77563106d8e8eb1f4f402f15be1dbab803`  
		Last Modified: Tue, 17 Feb 2026 20:32:52 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:c19f21963d9af2e87f115ff0fd0ae87acee044710cf54f6e357a42fec36ba497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61652817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e2d7f043a5a1844e680954edf981effb98b2cda5de579113e93500337ceac`

```dockerfile
```

-	Layers:
	-	`sha256:7fa6b9e8337a222215b67337dcad4e3d41a5f418f526fbc48c58d7aaf7a80135`  
		Last Modified: Tue, 17 Feb 2026 20:32:51 GMT  
		Size: 61.6 MB (61625867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad1b8f1806fbb881e232ab47fd158c18e1eefd5d0ea7b94784adec24df17887`  
		Last Modified: Tue, 17 Feb 2026 20:32:48 GMT  
		Size: 26.9 KB (26950 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260217` - linux; ppc64le

```console
$ docker pull odoo@sha256:6d82bdd53781f63f23e7d77c9bafbfb55a371084e4ef34fca656bdb82d3027db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.9 MB (699882241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d12323700639ec7a95db9161d56737c5cfa8fc2c677ec37325d762af54678b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:57:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:57:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:57:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:57:56 GMT
ARG TARGETARCH=ppc64le
# Tue, 17 Feb 2026 20:57:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:58:13 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
ENV ODOO_VERSION=18.0
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
# Tue, 17 Feb 2026 21:00:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 21:00:50 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=512f99d2d5bc218fe7a34d47e710ae2fe3e0ab21
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 21:00:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 21:00:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 21:00:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 21:00:51 GMT
USER odoo
# Tue, 17 Feb 2026 21:00:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:00:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0169bf586568d779da1131c69587cc539ba8404f5cf298d3606a68076b46e`  
		Last Modified: Tue, 17 Feb 2026 21:06:01 GMT  
		Size: 266.4 MB (266360265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695e1dac687d4505fae48b4784af147d88ec0ed98b7a1fcb7cbddbaf5040b12`  
		Last Modified: Tue, 17 Feb 2026 21:05:50 GMT  
		Size: 14.9 MB (14888865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f2f1a7484f8b97f5992754300b1d623696d153b5c0b35c1f8b7854dd25a3`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 480.1 KB (480061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527ba312fbb28049af395109952b81b03ca99f1c16981dd48bbbad162ed8a587`  
		Last Modified: Tue, 17 Feb 2026 21:06:03 GMT  
		Size: 383.8 MB (383843703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b2ae62cbeeff4227e57663a3a5cb5f79be054e198505d46cbf672aa3dfee7e`  
		Last Modified: Tue, 17 Feb 2026 21:05:51 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9923781140e7178f0a0ddc137548ed1e850b1d4d4566254fe3a13251cbe316`  
		Last Modified: Tue, 17 Feb 2026 21:05:52 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaeecfc00e81699ca3be9cbb9dbcb93fce494eb2279bf1dc3253f9a4c15819d1`  
		Last Modified: Tue, 17 Feb 2026 21:05:52 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d423631fd3fdbb34efc6b80d5d9b01f3d4f20866cd89743a9b8f1537147606c2`  
		Last Modified: Tue, 17 Feb 2026 21:05:53 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:df82546af4dadf3c05fdb51474354af8316eb2bde77d39c0d3a5c273879003a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61653830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291a5739cc0564074279b6f806dcc94b814050d968bc8f1860fb46a655998821`

```dockerfile
```

-	Layers:
	-	`sha256:a27c4dd3823c3f7b3b889a31ed6e4dc8eb5b2b4463c979a2553d6ba6c379b954`  
		Last Modified: Tue, 17 Feb 2026 21:05:54 GMT  
		Size: 61.6 MB (61626975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44393ee56263ec9c1c640d4d07a8b8099371d19457ca57a47f328502267040f8`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:aba5b4d3b94e568fb34aa5527f5e65b4d49c8f972692249850126767bcb35ec0
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
$ docker pull odoo@sha256:8491aac9d72b638be743a759ec1775c9a6cdb2f1d2fbb89cb40c8882b700f7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.5 MB (699497965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4f9383490e33b312d2666ecabf69770095783f649ffa2a04b1fb9f8d04fa82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:32 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:31:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6735ee3bdaef4228dc4e531cb53bcc996f0f32e5834865e7ccc66a50a50502`  
		Last Modified: Tue, 17 Feb 2026 20:34:24 GMT  
		Size: 255.7 MB (255668500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87af3648ad18dfde79b99e4b957011ce1505e22e3761b2aeb7501a935fb392f`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 14.4 MB (14359425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd1cc25ff2b7645203cb56b3e3056338d06c89ec06844e31e73a48dd3a9d0c5`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bbd5d666dbb1813d715bc82b976fa8a3aca5d069c83507b7af37f2a0c289e0`  
		Last Modified: Tue, 17 Feb 2026 20:34:32 GMT  
		Size: 399.3 MB (399259978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9abe4373e6fa657e781e5ad9328096625f9c476e343c4116c2083cd55168d`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214958689b08f64e23c2c02c4da48a17609b691b576a772ec47b71670fbfc025`  
		Last Modified: Tue, 17 Feb 2026 20:34:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fea82fdd08bb312364a4afafacbfbb84dd64fb558763da863fc99b8be3c505`  
		Last Modified: Tue, 17 Feb 2026 20:34:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d8ed336b70304fa38a71eb687832d798a4e2c483d348c8d677fa30351f0b8`  
		Last Modified: Tue, 17 Feb 2026 20:34:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:cf845e43d66eebcc55c66e23be382aed5f57476b5674952e08699d1d3295fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69693107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19137d6b93565559d0fed544648fa0d204323cd35a20bafbd83d87887d10e43e`

```dockerfile
```

-	Layers:
	-	`sha256:c06937fe7d2a506a1dd1bcaf4d3670a37c1e17e2838b3a8d40cc2c3d0d3c45f1`  
		Last Modified: Tue, 17 Feb 2026 20:34:06 GMT  
		Size: 69.7 MB (69666015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7289d4083f3d8569783d9bdba74d01d198743ad301ea1e58201a876e11da10bd`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce080bcf41fcb5e3c55d2398542b33500fcd40d25e86f7e3b15a2b941779a5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695824107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd82db2ed5c39f67b45c96b5438312c4a54852f010a02741cacce46e446cfa2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:20 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30d47b13630c92dc3cbd28e8f420f1ed4f8b9c768314755590c181ba589304`  
		Last Modified: Tue, 17 Feb 2026 20:33:49 GMT  
		Size: 253.0 MB (253043124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3000a9b1576bf8aab0afbad56424435485e5b81b475a766a82db9c55c05f8749`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 14.3 MB (14339765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2b2f1cd337576c1e28f75c9cf9c6c131e70c159a4b48ab4f1545d2bd9a6967`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a1981cdbcbc4c2c2f61d78ad1f38819941592102bb1146181febea3082cf1`  
		Last Modified: Tue, 17 Feb 2026 20:33:54 GMT  
		Size: 399.1 MB (399093555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad49658de2fb1e71b018a464990451a823fa91424235a43e7cb05b1dccc022`  
		Last Modified: Tue, 17 Feb 2026 20:33:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d0d349c3e095f554a443f5dee66e8ba5cbee3afadae64aeea3730db6707699`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d3dfcacc65b1932c5bec1db50b3ee663da804150b3feaef33929a38eff684`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe46df713ea3d2e9bb618f2a8314d19b44452ad176d9dc5e3dbeb9b4380aa8`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:9658bf177d88db672d73ce5bd5746c0ea46c69482824d3de01fe33fcc2bfd751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94928c44acfe0a7461680a6fdb405d3660188beb8df31c5c220eb440ef01f3`

```dockerfile
```

-	Layers:
	-	`sha256:ea222b18e43ed71da0dbe0388cdd9cb07f4e8de2913e67285ecee94a633170e2`  
		Last Modified: Tue, 17 Feb 2026 20:33:39 GMT  
		Size: 69.7 MB (69673302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104610d88431e289e46d0ce40fdfe4a344cc6acdeb459a354dfdfdcd72c1147f`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:2c4dcba075f803637fe24a9a72aaaf9bd9b3e1bf3f0fdf837f0f3c1788570d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.8 MB (715839703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903e2cacf280b7d6beb67e9da0b52b9628a7a91cde4b37336d7f62d7cb781c6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:57:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:57:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:57:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:57:56 GMT
ARG TARGETARCH=ppc64le
# Tue, 17 Feb 2026 20:57:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:58:13 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 21:01:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 21:01:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 21:01:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 21:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 21:01:12 GMT
USER odoo
# Tue, 17 Feb 2026 21:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0169bf586568d779da1131c69587cc539ba8404f5cf298d3606a68076b46e`  
		Last Modified: Tue, 17 Feb 2026 21:06:01 GMT  
		Size: 266.4 MB (266360265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695e1dac687d4505fae48b4784af147d88ec0ed98b7a1fcb7cbddbaf5040b12`  
		Last Modified: Tue, 17 Feb 2026 21:05:50 GMT  
		Size: 14.9 MB (14888865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f2f1a7484f8b97f5992754300b1d623696d153b5c0b35c1f8b7854dd25a3`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 480.1 KB (480061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abc00dea3b1a44d24e2c959706ec072eecf8164b932224145481b5a5fe7a036`  
		Last Modified: Tue, 17 Feb 2026 21:07:59 GMT  
		Size: 399.8 MB (399801159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed63c1bd8f28e2959998a5133afe15443980c8a9c332c56c624753e8a25c7ae6`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a4168953c7696577cd4cedd526477025830fa0f5d0a3f0b54376d3f263b193`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec75267b0c01eb6e303140016baea921805e9fa99e9b4e7455695a39da31b90`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b398406825a899163c58c76642b17ab0be9c525c13fa6b19a901458e79928e09`  
		Last Modified: Tue, 17 Feb 2026 21:07:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:e882a1936fc80ddb238781ed5a6d0950b5d00eb1c06596e618e86dcaad4abec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69701559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7b9cd38a54e5f930d6e3f8abd8fa955a3c9b2fc34df37b4eb1ff8fb4fea091`

```dockerfile
```

-	Layers:
	-	`sha256:f3318899f2b4f37e8deac7df53e2836d54ff2e7f044745d00c5d3507cd6b3476`  
		Last Modified: Tue, 17 Feb 2026 21:07:39 GMT  
		Size: 69.7 MB (69674404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bd52fea9f1c05d467782122e6b245e08f812e1a6caecaffbfdafc00d18e4ce`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:aba5b4d3b94e568fb34aa5527f5e65b4d49c8f972692249850126767bcb35ec0
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
$ docker pull odoo@sha256:8491aac9d72b638be743a759ec1775c9a6cdb2f1d2fbb89cb40c8882b700f7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.5 MB (699497965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4f9383490e33b312d2666ecabf69770095783f649ffa2a04b1fb9f8d04fa82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:32 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:31:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6735ee3bdaef4228dc4e531cb53bcc996f0f32e5834865e7ccc66a50a50502`  
		Last Modified: Tue, 17 Feb 2026 20:34:24 GMT  
		Size: 255.7 MB (255668500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87af3648ad18dfde79b99e4b957011ce1505e22e3761b2aeb7501a935fb392f`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 14.4 MB (14359425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd1cc25ff2b7645203cb56b3e3056338d06c89ec06844e31e73a48dd3a9d0c5`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bbd5d666dbb1813d715bc82b976fa8a3aca5d069c83507b7af37f2a0c289e0`  
		Last Modified: Tue, 17 Feb 2026 20:34:32 GMT  
		Size: 399.3 MB (399259978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9abe4373e6fa657e781e5ad9328096625f9c476e343c4116c2083cd55168d`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214958689b08f64e23c2c02c4da48a17609b691b576a772ec47b71670fbfc025`  
		Last Modified: Tue, 17 Feb 2026 20:34:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fea82fdd08bb312364a4afafacbfbb84dd64fb558763da863fc99b8be3c505`  
		Last Modified: Tue, 17 Feb 2026 20:34:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d8ed336b70304fa38a71eb687832d798a4e2c483d348c8d677fa30351f0b8`  
		Last Modified: Tue, 17 Feb 2026 20:34:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:cf845e43d66eebcc55c66e23be382aed5f57476b5674952e08699d1d3295fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69693107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19137d6b93565559d0fed544648fa0d204323cd35a20bafbd83d87887d10e43e`

```dockerfile
```

-	Layers:
	-	`sha256:c06937fe7d2a506a1dd1bcaf4d3670a37c1e17e2838b3a8d40cc2c3d0d3c45f1`  
		Last Modified: Tue, 17 Feb 2026 20:34:06 GMT  
		Size: 69.7 MB (69666015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7289d4083f3d8569783d9bdba74d01d198743ad301ea1e58201a876e11da10bd`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce080bcf41fcb5e3c55d2398542b33500fcd40d25e86f7e3b15a2b941779a5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695824107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd82db2ed5c39f67b45c96b5438312c4a54852f010a02741cacce46e446cfa2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:20 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30d47b13630c92dc3cbd28e8f420f1ed4f8b9c768314755590c181ba589304`  
		Last Modified: Tue, 17 Feb 2026 20:33:49 GMT  
		Size: 253.0 MB (253043124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3000a9b1576bf8aab0afbad56424435485e5b81b475a766a82db9c55c05f8749`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 14.3 MB (14339765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2b2f1cd337576c1e28f75c9cf9c6c131e70c159a4b48ab4f1545d2bd9a6967`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a1981cdbcbc4c2c2f61d78ad1f38819941592102bb1146181febea3082cf1`  
		Last Modified: Tue, 17 Feb 2026 20:33:54 GMT  
		Size: 399.1 MB (399093555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad49658de2fb1e71b018a464990451a823fa91424235a43e7cb05b1dccc022`  
		Last Modified: Tue, 17 Feb 2026 20:33:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d0d349c3e095f554a443f5dee66e8ba5cbee3afadae64aeea3730db6707699`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d3dfcacc65b1932c5bec1db50b3ee663da804150b3feaef33929a38eff684`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe46df713ea3d2e9bb618f2a8314d19b44452ad176d9dc5e3dbeb9b4380aa8`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9658bf177d88db672d73ce5bd5746c0ea46c69482824d3de01fe33fcc2bfd751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94928c44acfe0a7461680a6fdb405d3660188beb8df31c5c220eb440ef01f3`

```dockerfile
```

-	Layers:
	-	`sha256:ea222b18e43ed71da0dbe0388cdd9cb07f4e8de2913e67285ecee94a633170e2`  
		Last Modified: Tue, 17 Feb 2026 20:33:39 GMT  
		Size: 69.7 MB (69673302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104610d88431e289e46d0ce40fdfe4a344cc6acdeb459a354dfdfdcd72c1147f`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:2c4dcba075f803637fe24a9a72aaaf9bd9b3e1bf3f0fdf837f0f3c1788570d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.8 MB (715839703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903e2cacf280b7d6beb67e9da0b52b9628a7a91cde4b37336d7f62d7cb781c6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:57:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:57:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:57:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:57:56 GMT
ARG TARGETARCH=ppc64le
# Tue, 17 Feb 2026 20:57:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:58:13 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 21:01:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 21:01:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 21:01:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 21:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 21:01:12 GMT
USER odoo
# Tue, 17 Feb 2026 21:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0169bf586568d779da1131c69587cc539ba8404f5cf298d3606a68076b46e`  
		Last Modified: Tue, 17 Feb 2026 21:06:01 GMT  
		Size: 266.4 MB (266360265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695e1dac687d4505fae48b4784af147d88ec0ed98b7a1fcb7cbddbaf5040b12`  
		Last Modified: Tue, 17 Feb 2026 21:05:50 GMT  
		Size: 14.9 MB (14888865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f2f1a7484f8b97f5992754300b1d623696d153b5c0b35c1f8b7854dd25a3`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 480.1 KB (480061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abc00dea3b1a44d24e2c959706ec072eecf8164b932224145481b5a5fe7a036`  
		Last Modified: Tue, 17 Feb 2026 21:07:59 GMT  
		Size: 399.8 MB (399801159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed63c1bd8f28e2959998a5133afe15443980c8a9c332c56c624753e8a25c7ae6`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a4168953c7696577cd4cedd526477025830fa0f5d0a3f0b54376d3f263b193`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec75267b0c01eb6e303140016baea921805e9fa99e9b4e7455695a39da31b90`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b398406825a899163c58c76642b17ab0be9c525c13fa6b19a901458e79928e09`  
		Last Modified: Tue, 17 Feb 2026 21:07:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:e882a1936fc80ddb238781ed5a6d0950b5d00eb1c06596e618e86dcaad4abec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69701559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7b9cd38a54e5f930d6e3f8abd8fa955a3c9b2fc34df37b4eb1ff8fb4fea091`

```dockerfile
```

-	Layers:
	-	`sha256:f3318899f2b4f37e8deac7df53e2836d54ff2e7f044745d00c5d3507cd6b3476`  
		Last Modified: Tue, 17 Feb 2026 21:07:39 GMT  
		Size: 69.7 MB (69674404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bd52fea9f1c05d467782122e6b245e08f812e1a6caecaffbfdafc00d18e4ce`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260217`

```console
$ docker pull odoo@sha256:aba5b4d3b94e568fb34aa5527f5e65b4d49c8f972692249850126767bcb35ec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260217` - linux; amd64

```console
$ docker pull odoo@sha256:8491aac9d72b638be743a759ec1775c9a6cdb2f1d2fbb89cb40c8882b700f7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.5 MB (699497965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4f9383490e33b312d2666ecabf69770095783f649ffa2a04b1fb9f8d04fa82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:32 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:31:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6735ee3bdaef4228dc4e531cb53bcc996f0f32e5834865e7ccc66a50a50502`  
		Last Modified: Tue, 17 Feb 2026 20:34:24 GMT  
		Size: 255.7 MB (255668500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87af3648ad18dfde79b99e4b957011ce1505e22e3761b2aeb7501a935fb392f`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 14.4 MB (14359425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd1cc25ff2b7645203cb56b3e3056338d06c89ec06844e31e73a48dd3a9d0c5`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bbd5d666dbb1813d715bc82b976fa8a3aca5d069c83507b7af37f2a0c289e0`  
		Last Modified: Tue, 17 Feb 2026 20:34:32 GMT  
		Size: 399.3 MB (399259978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9abe4373e6fa657e781e5ad9328096625f9c476e343c4116c2083cd55168d`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214958689b08f64e23c2c02c4da48a17609b691b576a772ec47b71670fbfc025`  
		Last Modified: Tue, 17 Feb 2026 20:34:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fea82fdd08bb312364a4afafacbfbb84dd64fb558763da863fc99b8be3c505`  
		Last Modified: Tue, 17 Feb 2026 20:34:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d8ed336b70304fa38a71eb687832d798a4e2c483d348c8d677fa30351f0b8`  
		Last Modified: Tue, 17 Feb 2026 20:34:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:cf845e43d66eebcc55c66e23be382aed5f57476b5674952e08699d1d3295fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69693107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19137d6b93565559d0fed544648fa0d204323cd35a20bafbd83d87887d10e43e`

```dockerfile
```

-	Layers:
	-	`sha256:c06937fe7d2a506a1dd1bcaf4d3670a37c1e17e2838b3a8d40cc2c3d0d3c45f1`  
		Last Modified: Tue, 17 Feb 2026 20:34:06 GMT  
		Size: 69.7 MB (69666015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7289d4083f3d8569783d9bdba74d01d198743ad301ea1e58201a876e11da10bd`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260217` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce080bcf41fcb5e3c55d2398542b33500fcd40d25e86f7e3b15a2b941779a5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695824107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd82db2ed5c39f67b45c96b5438312c4a54852f010a02741cacce46e446cfa2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:20 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30d47b13630c92dc3cbd28e8f420f1ed4f8b9c768314755590c181ba589304`  
		Last Modified: Tue, 17 Feb 2026 20:33:49 GMT  
		Size: 253.0 MB (253043124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3000a9b1576bf8aab0afbad56424435485e5b81b475a766a82db9c55c05f8749`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 14.3 MB (14339765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2b2f1cd337576c1e28f75c9cf9c6c131e70c159a4b48ab4f1545d2bd9a6967`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a1981cdbcbc4c2c2f61d78ad1f38819941592102bb1146181febea3082cf1`  
		Last Modified: Tue, 17 Feb 2026 20:33:54 GMT  
		Size: 399.1 MB (399093555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad49658de2fb1e71b018a464990451a823fa91424235a43e7cb05b1dccc022`  
		Last Modified: Tue, 17 Feb 2026 20:33:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d0d349c3e095f554a443f5dee66e8ba5cbee3afadae64aeea3730db6707699`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d3dfcacc65b1932c5bec1db50b3ee663da804150b3feaef33929a38eff684`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe46df713ea3d2e9bb618f2a8314d19b44452ad176d9dc5e3dbeb9b4380aa8`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:9658bf177d88db672d73ce5bd5746c0ea46c69482824d3de01fe33fcc2bfd751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94928c44acfe0a7461680a6fdb405d3660188beb8df31c5c220eb440ef01f3`

```dockerfile
```

-	Layers:
	-	`sha256:ea222b18e43ed71da0dbe0388cdd9cb07f4e8de2913e67285ecee94a633170e2`  
		Last Modified: Tue, 17 Feb 2026 20:33:39 GMT  
		Size: 69.7 MB (69673302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104610d88431e289e46d0ce40fdfe4a344cc6acdeb459a354dfdfdcd72c1147f`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260217` - linux; ppc64le

```console
$ docker pull odoo@sha256:2c4dcba075f803637fe24a9a72aaaf9bd9b3e1bf3f0fdf837f0f3c1788570d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.8 MB (715839703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903e2cacf280b7d6beb67e9da0b52b9628a7a91cde4b37336d7f62d7cb781c6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:57:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:57:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:57:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:57:56 GMT
ARG TARGETARCH=ppc64le
# Tue, 17 Feb 2026 20:57:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:58:13 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 21:01:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 21:01:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 21:01:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 21:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 21:01:12 GMT
USER odoo
# Tue, 17 Feb 2026 21:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0169bf586568d779da1131c69587cc539ba8404f5cf298d3606a68076b46e`  
		Last Modified: Tue, 17 Feb 2026 21:06:01 GMT  
		Size: 266.4 MB (266360265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695e1dac687d4505fae48b4784af147d88ec0ed98b7a1fcb7cbddbaf5040b12`  
		Last Modified: Tue, 17 Feb 2026 21:05:50 GMT  
		Size: 14.9 MB (14888865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f2f1a7484f8b97f5992754300b1d623696d153b5c0b35c1f8b7854dd25a3`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 480.1 KB (480061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abc00dea3b1a44d24e2c959706ec072eecf8164b932224145481b5a5fe7a036`  
		Last Modified: Tue, 17 Feb 2026 21:07:59 GMT  
		Size: 399.8 MB (399801159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed63c1bd8f28e2959998a5133afe15443980c8a9c332c56c624753e8a25c7ae6`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a4168953c7696577cd4cedd526477025830fa0f5d0a3f0b54376d3f263b193`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec75267b0c01eb6e303140016baea921805e9fa99e9b4e7455695a39da31b90`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b398406825a899163c58c76642b17ab0be9c525c13fa6b19a901458e79928e09`  
		Last Modified: Tue, 17 Feb 2026 21:07:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260217` - unknown; unknown

```console
$ docker pull odoo@sha256:e882a1936fc80ddb238781ed5a6d0950b5d00eb1c06596e618e86dcaad4abec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69701559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7b9cd38a54e5f930d6e3f8abd8fa955a3c9b2fc34df37b4eb1ff8fb4fea091`

```dockerfile
```

-	Layers:
	-	`sha256:f3318899f2b4f37e8deac7df53e2836d54ff2e7f044745d00c5d3507cd6b3476`  
		Last Modified: Tue, 17 Feb 2026 21:07:39 GMT  
		Size: 69.7 MB (69674404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bd52fea9f1c05d467782122e6b245e08f812e1a6caecaffbfdafc00d18e4ce`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:aba5b4d3b94e568fb34aa5527f5e65b4d49c8f972692249850126767bcb35ec0
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
$ docker pull odoo@sha256:8491aac9d72b638be743a759ec1775c9a6cdb2f1d2fbb89cb40c8882b700f7d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.5 MB (699497965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4f9383490e33b312d2666ecabf69770095783f649ffa2a04b1fb9f8d04fa82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:30:32 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:30:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:30:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:30:32 GMT
ARG TARGETARCH=amd64
# Tue, 17 Feb 2026 20:30:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:30:44 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:31:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:31:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:31:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:31:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:31:53 GMT
USER odoo
# Tue, 17 Feb 2026 20:31:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:31:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6735ee3bdaef4228dc4e531cb53bcc996f0f32e5834865e7ccc66a50a50502`  
		Last Modified: Tue, 17 Feb 2026 20:34:24 GMT  
		Size: 255.7 MB (255668500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87af3648ad18dfde79b99e4b957011ce1505e22e3761b2aeb7501a935fb392f`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 14.4 MB (14359425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd1cc25ff2b7645203cb56b3e3056338d06c89ec06844e31e73a48dd3a9d0c5`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bbd5d666dbb1813d715bc82b976fa8a3aca5d069c83507b7af37f2a0c289e0`  
		Last Modified: Tue, 17 Feb 2026 20:34:32 GMT  
		Size: 399.3 MB (399259978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9abe4373e6fa657e781e5ad9328096625f9c476e343c4116c2083cd55168d`  
		Last Modified: Tue, 17 Feb 2026 20:34:01 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214958689b08f64e23c2c02c4da48a17609b691b576a772ec47b71670fbfc025`  
		Last Modified: Tue, 17 Feb 2026 20:34:02 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fea82fdd08bb312364a4afafacbfbb84dd64fb558763da863fc99b8be3c505`  
		Last Modified: Tue, 17 Feb 2026 20:34:03 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408d8ed336b70304fa38a71eb687832d798a4e2c483d348c8d677fa30351f0b8`  
		Last Modified: Tue, 17 Feb 2026 20:34:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cf845e43d66eebcc55c66e23be382aed5f57476b5674952e08699d1d3295fe2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69693107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19137d6b93565559d0fed544648fa0d204323cd35a20bafbd83d87887d10e43e`

```dockerfile
```

-	Layers:
	-	`sha256:c06937fe7d2a506a1dd1bcaf4d3670a37c1e17e2838b3a8d40cc2c3d0d3c45f1`  
		Last Modified: Tue, 17 Feb 2026 20:34:06 GMT  
		Size: 69.7 MB (69666015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7289d4083f3d8569783d9bdba74d01d198743ad301ea1e58201a876e11da10bd`  
		Last Modified: Tue, 17 Feb 2026 20:34:00 GMT  
		Size: 27.1 KB (27092 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ce080bcf41fcb5e3c55d2398542b33500fcd40d25e86f7e3b15a2b941779a5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695824107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd82db2ed5c39f67b45c96b5438312c4a54852f010a02741cacce46e446cfa2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:29:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:29:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:29:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:29:20 GMT
ARG TARGETARCH=arm64
# Tue, 17 Feb 2026 20:29:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:29:30 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:29:32 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:29:32 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 20:30:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 20:30:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 20:30:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 20:30:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 20:30:44 GMT
USER odoo
# Tue, 17 Feb 2026 20:30:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 20:30:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30d47b13630c92dc3cbd28e8f420f1ed4f8b9c768314755590c181ba589304`  
		Last Modified: Tue, 17 Feb 2026 20:33:49 GMT  
		Size: 253.0 MB (253043124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3000a9b1576bf8aab0afbad56424435485e5b81b475a766a82db9c55c05f8749`  
		Last Modified: Tue, 17 Feb 2026 20:33:33 GMT  
		Size: 14.3 MB (14339765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2b2f1cd337576c1e28f75c9cf9c6c131e70c159a4b48ab4f1545d2bd9a6967`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 480.1 KB (480106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0a1981cdbcbc4c2c2f61d78ad1f38819941592102bb1146181febea3082cf1`  
		Last Modified: Tue, 17 Feb 2026 20:33:54 GMT  
		Size: 399.1 MB (399093555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad49658de2fb1e71b018a464990451a823fa91424235a43e7cb05b1dccc022`  
		Last Modified: Tue, 17 Feb 2026 20:33:34 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d0d349c3e095f554a443f5dee66e8ba5cbee3afadae64aeea3730db6707699`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d3dfcacc65b1932c5bec1db50b3ee663da804150b3feaef33929a38eff684`  
		Last Modified: Tue, 17 Feb 2026 20:33:35 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe46df713ea3d2e9bb618f2a8314d19b44452ad176d9dc5e3dbeb9b4380aa8`  
		Last Modified: Tue, 17 Feb 2026 20:33:37 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9658bf177d88db672d73ce5bd5746c0ea46c69482824d3de01fe33fcc2bfd751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69700559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f94928c44acfe0a7461680a6fdb405d3660188beb8df31c5c220eb440ef01f3`

```dockerfile
```

-	Layers:
	-	`sha256:ea222b18e43ed71da0dbe0388cdd9cb07f4e8de2913e67285ecee94a633170e2`  
		Last Modified: Tue, 17 Feb 2026 20:33:39 GMT  
		Size: 69.7 MB (69673302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104610d88431e289e46d0ce40fdfe4a344cc6acdeb459a354dfdfdcd72c1147f`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 27.3 KB (27257 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:2c4dcba075f803637fe24a9a72aaaf9bd9b3e1bf3f0fdf837f0f3c1788570d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.8 MB (715839703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903e2cacf280b7d6beb67e9da0b52b9628a7a91cde4b37336d7f62d7cb781c6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:57:56 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 17 Feb 2026 20:57:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 17 Feb 2026 20:57:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:57:56 GMT
ARG TARGETARCH=ppc64le
# Tue, 17 Feb 2026 20:57:56 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 17 Feb 2026 20:58:13 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 17 Feb 2026 20:58:15 GMT
ENV ODOO_VERSION=19.0
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_RELEASE=20260217
# Tue, 17 Feb 2026 20:58:15 GMT
ARG ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
# Tue, 17 Feb 2026 21:01:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 17 Feb 2026 21:01:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260217 ODOO_SHA=b303e9dc857329b1f91fd01f8944f25d4d53139e
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 17 Feb 2026 21:01:10 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 17 Feb 2026 21:01:10 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 17 Feb 2026 21:01:10 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 17 Feb 2026 21:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 17 Feb 2026 21:01:12 GMT
USER odoo
# Tue, 17 Feb 2026 21:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc0169bf586568d779da1131c69587cc539ba8404f5cf298d3606a68076b46e`  
		Last Modified: Tue, 17 Feb 2026 21:06:01 GMT  
		Size: 266.4 MB (266360265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7695e1dac687d4505fae48b4784af147d88ec0ed98b7a1fcb7cbddbaf5040b12`  
		Last Modified: Tue, 17 Feb 2026 21:05:50 GMT  
		Size: 14.9 MB (14888865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3648f2f1a7484f8b97f5992754300b1d623696d153b5c0b35c1f8b7854dd25a3`  
		Last Modified: Tue, 17 Feb 2026 21:05:49 GMT  
		Size: 480.1 KB (480061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abc00dea3b1a44d24e2c959706ec072eecf8164b932224145481b5a5fe7a036`  
		Last Modified: Tue, 17 Feb 2026 21:07:59 GMT  
		Size: 399.8 MB (399801159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed63c1bd8f28e2959998a5133afe15443980c8a9c332c56c624753e8a25c7ae6`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a4168953c7696577cd4cedd526477025830fa0f5d0a3f0b54376d3f263b193`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec75267b0c01eb6e303140016baea921805e9fa99e9b4e7455695a39da31b90`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b398406825a899163c58c76642b17ab0be9c525c13fa6b19a901458e79928e09`  
		Last Modified: Tue, 17 Feb 2026 21:07:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e882a1936fc80ddb238781ed5a6d0950b5d00eb1c06596e618e86dcaad4abec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69701559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7b9cd38a54e5f930d6e3f8abd8fa955a3c9b2fc34df37b4eb1ff8fb4fea091`

```dockerfile
```

-	Layers:
	-	`sha256:f3318899f2b4f37e8deac7df53e2836d54ff2e7f044745d00c5d3507cd6b3476`  
		Last Modified: Tue, 17 Feb 2026 21:07:39 GMT  
		Size: 69.7 MB (69674404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bd52fea9f1c05d467782122e6b245e08f812e1a6caecaffbfdafc00d18e4ce`  
		Last Modified: Tue, 17 Feb 2026 21:07:30 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
