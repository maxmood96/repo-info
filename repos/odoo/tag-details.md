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
$ docker pull odoo@sha256:80c068394bfcbc7911369fe33c6eff81408d99b7837b19b6d27e91e69072f15e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:7c0ecdf48d03918c85ff1dffa4fc1a7f2da8a05e093e02d66dd8c7faa5bb8bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.2 MB (605230305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa365d62466e4fe099f81e953678d32975520f832593e0fc5d36010ef5b7cb95`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a75641d85647092644e7c1c160b11cebfa6f5c862fcaa7421f1caaa3b5beddb`  
		Last Modified: Tue, 21 Oct 2025 22:12:32 GMT  
		Size: 233.8 MB (233821017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5e90676fc60a4060d8c7238ba870e1c52e20d572fdbc495ac8a3ab470672c9`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 2.6 MB (2595053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80567abe16ca66a0dceff3a475751861fac321f3d8c3d0085f29b6e9aa48585c`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 480.3 KB (480259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5867ed48d6d13e0f4cace1e914578bbbe4f7e3ab7c094f46f588eed5650994`  
		Last Modified: Tue, 21 Oct 2025 22:12:55 GMT  
		Size: 338.8 MB (338794720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2d5cec672f05a83a6f403c10d32a7e83cc8ae1b16723ff6355ef37bd8040b4`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835b443fa5595cd1760ac66bfb38297ac40ec15932729df41afea7a1b03e24f6`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5b6c328025b4f4db7de27fcddf4ac438bb5c4ec2d2fd632d8b9d7ef226302b`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5128826e579b6e36cf394ad96b6c1ff5a9dad9307c2a63b91ae05d3d46b8ae`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:d932968db68308ee30b6fe5506377ec7a6460477afaf1208c25309077d2f4df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41516041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223b9fedd32bf6847039e5917b54bf3449291767cd457c066bef1b60606aa8ef`

```dockerfile
```

-	Layers:
	-	`sha256:67456cc86b2208e92248087c47942b5113c973ffa178547d5aa723051adb2cc0`  
		Last Modified: Tue, 21 Oct 2025 22:12:25 GMT  
		Size: 41.5 MB (41489206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da50173f78775efc42968c64c1add6d5e0ccbdd941797bdb5074baedce80aeb`  
		Last Modified: Tue, 21 Oct 2025 22:12:27 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ee30ddbfb4dacf04821cb41bc94ca568aa8351cab4f4b0590660dfd5ac96514c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (600045111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138e94962fee9ee6496e2b9899a46acb7996dfdce2c0e3f742a5ffa63ece1582`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a565c1e8b1cecbafd07db30cb7a76e47ad38b4f4f11df6e04bab6d4d8b5f1b`  
		Last Modified: Tue, 21 Oct 2025 22:13:55 GMT  
		Size: 231.2 MB (231194292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aabf496327000cdd5542d54506f711afe44581a02bcd17ad05c49a44b29d94c`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 2.6 MB (2590510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0aa06a45a67b4905b3efa30a4d6e0a3a4eed9476eb4418c41efa52ba1a5e18`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 480.4 KB (480362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832a094b2e645ddd0e788a8e784ae1ebae274bb86de514ffdc7dd16fca854024`  
		Last Modified: Tue, 21 Oct 2025 22:14:05 GMT  
		Size: 338.4 MB (338394404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c0956bded4745ac63221e7515f1fe5788da5520065ebc7bb969d7e529d4a7`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571004864b97715352028418d871152abf752a3c918d9c55a70abfa0eebb2394`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af37cbea3168a3888c3a90f8c959053ea82b8c557e882fffad781912173cba5`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a77a84bf740f09e310f60e44ba9514d1bdf66c095f1e112e437f863ed279e`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c84400024dcba2f4011c3b360a6707b4522f871e3ecfd0982a27d4da1677b5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41522700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1026fe0855d912aa845c043d2d58c23951e5d71fae319f214f0053356499836f`

```dockerfile
```

-	Layers:
	-	`sha256:6816e4979cea2822e9e340f5a368d0e9db20c05a113c8f155f3926e01f9d0255`  
		Last Modified: Tue, 21 Oct 2025 22:13:21 GMT  
		Size: 41.5 MB (41495713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1bf611b2eb385d1ce63f2476525e9ab2189cc4c5a4f5a54032ef1a1fef4269`  
		Last Modified: Tue, 21 Oct 2025 22:13:22 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:80c068394bfcbc7911369fe33c6eff81408d99b7837b19b6d27e91e69072f15e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:7c0ecdf48d03918c85ff1dffa4fc1a7f2da8a05e093e02d66dd8c7faa5bb8bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.2 MB (605230305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa365d62466e4fe099f81e953678d32975520f832593e0fc5d36010ef5b7cb95`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a75641d85647092644e7c1c160b11cebfa6f5c862fcaa7421f1caaa3b5beddb`  
		Last Modified: Tue, 21 Oct 2025 22:12:32 GMT  
		Size: 233.8 MB (233821017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5e90676fc60a4060d8c7238ba870e1c52e20d572fdbc495ac8a3ab470672c9`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 2.6 MB (2595053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80567abe16ca66a0dceff3a475751861fac321f3d8c3d0085f29b6e9aa48585c`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 480.3 KB (480259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5867ed48d6d13e0f4cace1e914578bbbe4f7e3ab7c094f46f588eed5650994`  
		Last Modified: Tue, 21 Oct 2025 22:12:55 GMT  
		Size: 338.8 MB (338794720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2d5cec672f05a83a6f403c10d32a7e83cc8ae1b16723ff6355ef37bd8040b4`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835b443fa5595cd1760ac66bfb38297ac40ec15932729df41afea7a1b03e24f6`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5b6c328025b4f4db7de27fcddf4ac438bb5c4ec2d2fd632d8b9d7ef226302b`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5128826e579b6e36cf394ad96b6c1ff5a9dad9307c2a63b91ae05d3d46b8ae`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d932968db68308ee30b6fe5506377ec7a6460477afaf1208c25309077d2f4df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41516041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223b9fedd32bf6847039e5917b54bf3449291767cd457c066bef1b60606aa8ef`

```dockerfile
```

-	Layers:
	-	`sha256:67456cc86b2208e92248087c47942b5113c973ffa178547d5aa723051adb2cc0`  
		Last Modified: Tue, 21 Oct 2025 22:12:25 GMT  
		Size: 41.5 MB (41489206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da50173f78775efc42968c64c1add6d5e0ccbdd941797bdb5074baedce80aeb`  
		Last Modified: Tue, 21 Oct 2025 22:12:27 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ee30ddbfb4dacf04821cb41bc94ca568aa8351cab4f4b0590660dfd5ac96514c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (600045111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138e94962fee9ee6496e2b9899a46acb7996dfdce2c0e3f742a5ffa63ece1582`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a565c1e8b1cecbafd07db30cb7a76e47ad38b4f4f11df6e04bab6d4d8b5f1b`  
		Last Modified: Tue, 21 Oct 2025 22:13:55 GMT  
		Size: 231.2 MB (231194292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aabf496327000cdd5542d54506f711afe44581a02bcd17ad05c49a44b29d94c`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 2.6 MB (2590510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0aa06a45a67b4905b3efa30a4d6e0a3a4eed9476eb4418c41efa52ba1a5e18`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 480.4 KB (480362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832a094b2e645ddd0e788a8e784ae1ebae274bb86de514ffdc7dd16fca854024`  
		Last Modified: Tue, 21 Oct 2025 22:14:05 GMT  
		Size: 338.4 MB (338394404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c0956bded4745ac63221e7515f1fe5788da5520065ebc7bb969d7e529d4a7`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571004864b97715352028418d871152abf752a3c918d9c55a70abfa0eebb2394`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af37cbea3168a3888c3a90f8c959053ea82b8c557e882fffad781912173cba5`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a77a84bf740f09e310f60e44ba9514d1bdf66c095f1e112e437f863ed279e`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c84400024dcba2f4011c3b360a6707b4522f871e3ecfd0982a27d4da1677b5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41522700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1026fe0855d912aa845c043d2d58c23951e5d71fae319f214f0053356499836f`

```dockerfile
```

-	Layers:
	-	`sha256:6816e4979cea2822e9e340f5a368d0e9db20c05a113c8f155f3926e01f9d0255`  
		Last Modified: Tue, 21 Oct 2025 22:13:21 GMT  
		Size: 41.5 MB (41495713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1bf611b2eb385d1ce63f2476525e9ab2189cc4c5a4f5a54032ef1a1fef4269`  
		Last Modified: Tue, 21 Oct 2025 22:13:22 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20251021`

```console
$ docker pull odoo@sha256:80c068394bfcbc7911369fe33c6eff81408d99b7837b19b6d27e91e69072f15e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20251021` - linux; amd64

```console
$ docker pull odoo@sha256:7c0ecdf48d03918c85ff1dffa4fc1a7f2da8a05e093e02d66dd8c7faa5bb8bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.2 MB (605230305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa365d62466e4fe099f81e953678d32975520f832593e0fc5d36010ef5b7cb95`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a75641d85647092644e7c1c160b11cebfa6f5c862fcaa7421f1caaa3b5beddb`  
		Last Modified: Tue, 21 Oct 2025 22:12:32 GMT  
		Size: 233.8 MB (233821017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5e90676fc60a4060d8c7238ba870e1c52e20d572fdbc495ac8a3ab470672c9`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 2.6 MB (2595053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80567abe16ca66a0dceff3a475751861fac321f3d8c3d0085f29b6e9aa48585c`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 480.3 KB (480259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5867ed48d6d13e0f4cace1e914578bbbe4f7e3ab7c094f46f588eed5650994`  
		Last Modified: Tue, 21 Oct 2025 22:12:55 GMT  
		Size: 338.8 MB (338794720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2d5cec672f05a83a6f403c10d32a7e83cc8ae1b16723ff6355ef37bd8040b4`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835b443fa5595cd1760ac66bfb38297ac40ec15932729df41afea7a1b03e24f6`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5b6c328025b4f4db7de27fcddf4ac438bb5c4ec2d2fd632d8b9d7ef226302b`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5128826e579b6e36cf394ad96b6c1ff5a9dad9307c2a63b91ae05d3d46b8ae`  
		Last Modified: Tue, 21 Oct 2025 20:23:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:d932968db68308ee30b6fe5506377ec7a6460477afaf1208c25309077d2f4df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41516041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223b9fedd32bf6847039e5917b54bf3449291767cd457c066bef1b60606aa8ef`

```dockerfile
```

-	Layers:
	-	`sha256:67456cc86b2208e92248087c47942b5113c973ffa178547d5aa723051adb2cc0`  
		Last Modified: Tue, 21 Oct 2025 22:12:25 GMT  
		Size: 41.5 MB (41489206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da50173f78775efc42968c64c1add6d5e0ccbdd941797bdb5074baedce80aeb`  
		Last Modified: Tue, 21 Oct 2025 22:12:27 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20251021` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ee30ddbfb4dacf04821cb41bc94ca568aa8351cab4f4b0590660dfd5ac96514c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.0 MB (600045111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138e94962fee9ee6496e2b9899a46acb7996dfdce2c0e3f742a5ffa63ece1582`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=17.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=d8c3f991cc028a6c9022d8b16d3a790da7ca8952
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a565c1e8b1cecbafd07db30cb7a76e47ad38b4f4f11df6e04bab6d4d8b5f1b`  
		Last Modified: Tue, 21 Oct 2025 22:13:55 GMT  
		Size: 231.2 MB (231194292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aabf496327000cdd5542d54506f711afe44581a02bcd17ad05c49a44b29d94c`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 2.6 MB (2590510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0aa06a45a67b4905b3efa30a4d6e0a3a4eed9476eb4418c41efa52ba1a5e18`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 480.4 KB (480362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832a094b2e645ddd0e788a8e784ae1ebae274bb86de514ffdc7dd16fca854024`  
		Last Modified: Tue, 21 Oct 2025 22:14:05 GMT  
		Size: 338.4 MB (338394404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c0956bded4745ac63221e7515f1fe5788da5520065ebc7bb969d7e529d4a7`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571004864b97715352028418d871152abf752a3c918d9c55a70abfa0eebb2394`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af37cbea3168a3888c3a90f8c959053ea82b8c557e882fffad781912173cba5`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453a77a84bf740f09e310f60e44ba9514d1bdf66c095f1e112e437f863ed279e`  
		Last Modified: Tue, 21 Oct 2025 19:56:44 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:c84400024dcba2f4011c3b360a6707b4522f871e3ecfd0982a27d4da1677b5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41522700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1026fe0855d912aa845c043d2d58c23951e5d71fae319f214f0053356499836f`

```dockerfile
```

-	Layers:
	-	`sha256:6816e4979cea2822e9e340f5a368d0e9db20c05a113c8f155f3926e01f9d0255`  
		Last Modified: Tue, 21 Oct 2025 22:13:21 GMT  
		Size: 41.5 MB (41495713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b1bf611b2eb385d1ce63f2476525e9ab2189cc4c5a4f5a54032ef1a1fef4269`  
		Last Modified: Tue, 21 Oct 2025 22:13:22 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:5ba70ff950b461c2caaeb15b43e4b879935afaa9762da8034beae7facfe6df20
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
$ docker pull odoo@sha256:88f041650885cac6d139c5bd9fe4f978528ee4bf0136222dcd97294c40385fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.6 MB (677605989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b265adae93c91a30e0882e5572ff747d951ae3f0c103c706dcb5ebe51b2418aa`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9dd5db5ee75c65d415533124aec3497ea6cfe7728de5f89d89fb1fcb4d9fec`  
		Last Modified: Tue, 21 Oct 2025 22:13:18 GMT  
		Size: 254.6 MB (254558334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f61a3f793676c616ca646fbb5b34a13f47c0c4a4513777cade48586f3dc5af`  
		Last Modified: Tue, 21 Oct 2025 22:12:35 GMT  
		Size: 14.4 MB (14355860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3732c206b5a236e0323004f885ae0097c2fb967ba8704773f196efc9d45d9609`  
		Last Modified: Tue, 21 Oct 2025 20:24:17 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa2e8d88c6f62dbeaf4402ed65fbb0a19d3e9f0b85a32b280102e40cbd2cf5e`  
		Last Modified: Tue, 21 Oct 2025 22:12:45 GMT  
		Size: 378.5 MB (378486201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471402e95017dd2c0b18762d6906b3db5892ee394970c5056475b78c269a64c2`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82261e23706e3cc03d60ee6a6f01e6040245f97a206497eb0fea4bc92d14e5f4`  
		Last Modified: Tue, 21 Oct 2025 20:24:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23be812d141190b6cb961262fb5e9ce197fd24671d9017b2008ffad73794b488`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4873efd9c94b6611332e41a224823a2cb4a5254ffdbf0763f5b104cc0350bf`  
		Last Modified: Tue, 21 Oct 2025 20:24:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:279730dbbab9071b8f403a2cffaa8992f953136b120ea3fa1eafd29e6ecb130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61147988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f75e7221ceb3b379a4c51d5983095da13ee2fe735d8740320d548814117add`

```dockerfile
```

-	Layers:
	-	`sha256:dbba5b1ef6887c3aad08db42c26d5066829ecdd2987ed17882d7f90757099926`  
		Last Modified: Tue, 21 Oct 2025 22:12:39 GMT  
		Size: 61.1 MB (61121146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe151a020702b51fdbf815edd5bc13b03756b999f985083736d7955ed4ab25bb`  
		Last Modified: Tue, 21 Oct 2025 22:12:41 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:da71ccf94726713d385b8ec9624ccc7da55273f82fdfd0fc26a3a8c6847ded57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (673963797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d933c4f3b5042bb2782c775fd61334f34dae60181f4756508fded7fba1b917`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c54a63595205df680cc62caf76cd95a0d9b0f0002f5b26ce14b9db049693a8b`  
		Last Modified: Tue, 21 Oct 2025 22:13:15 GMT  
		Size: 252.0 MB (251960055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c49c49e27117fadc00f07697a96106539d20d575130a17a26ab90e382150fe`  
		Last Modified: Tue, 21 Oct 2025 19:57:26 GMT  
		Size: 14.3 MB (14333975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215225848a0cdc06f81f9570c13feaffe201463ad1d22ac343f54f26a5ea851f`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 480.0 KB (480002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec5e8cfbdca99baa3539ed0b967e041ca1b8b97712993d772c6f8b9fd17f683`  
		Last Modified: Tue, 21 Oct 2025 22:13:07 GMT  
		Size: 378.3 MB (378325611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af75e214bc33a94f915e7a0e4f13de46d9024c5f2e40dc4d040750960856ba0`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f42319f7a8dc6de5231c76c1f28d16af39a1892f69fc2402e366ad8e52f8ec`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f92858d7deae355be8c705ad8693b359c42dd87d43455c4f60bfae7e5d6e55`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ffb8b8e7f9cba4b932b447f5afe7007df11b0e45b7a97e472b127fde1be09b`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:01f89a1bf5ec8809d5400d310ee7e8f0436283fd170163bfd7725ec8d95d84e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61155415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8c652354ea3fe53cac5f9ba1e0ea12b98f567837e91ec60613d764f9567285`

```dockerfile
```

-	Layers:
	-	`sha256:a5fdab1d31211377a5d8ba5f2f0e4942c02b8644c0bd78f39574e05d6a738801`  
		Last Modified: Tue, 21 Oct 2025 22:14:20 GMT  
		Size: 61.1 MB (61128421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c63454c6caf99288085965a261e98b0f290794e231395578001fc023598b531`  
		Last Modified: Tue, 21 Oct 2025 22:14:22 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:58c64b20f8b2500dde5bd664acffe9d5f1e64682d9b93267190f716cdaa2d855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.8 MB (693770725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5046a17225dc94a888d42e1fa9745c487439da34c7e9a4cf4c885b08092c5fd1`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=ppc64le
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
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
	-	`sha256:ac0a27b08d5b9780c7d719b380d0e62a2876e87a5645202c2eb916107849db85`  
		Last Modified: Tue, 21 Oct 2025 23:57:26 GMT  
		Size: 379.0 MB (379021406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b430615140aac450924ea0e0a88bc155eadcc9ddf601b27847e0fe6fc6e73a4`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53804ece2c4ca306dff7cb8396cf69b054b386ecf50faa7badfa42f98c11e66`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b325cd7dcf4e35f386ab8039f7472949ce1d53af8a84ec643030ffaba687af`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a8a013adeb16cb6e1de6d3a8efe22489cc9a0a134eb7040104ddbea809cb21`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:35760a9d878fa046973781090b45e4b88096e355c6b879d3a5f373cff21ea8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61156373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e01baf8fcb6ab20345a7e9e10636d8845b1cf7fd0c11f3bc89a777ae54f636f`

```dockerfile
```

-	Layers:
	-	`sha256:5bdc3a5bf6febf658cd8ce0db8db83de76f098299f358d56398fcde7386330bc`  
		Last Modified: Wed, 22 Oct 2025 01:16:24 GMT  
		Size: 61.1 MB (61129475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f58ded0c1a59a3704a7de4b90b11f1bcbc3aaf0938039eeac18b5892f2bd48b8`  
		Last Modified: Wed, 22 Oct 2025 01:16:26 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:5ba70ff950b461c2caaeb15b43e4b879935afaa9762da8034beae7facfe6df20
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
$ docker pull odoo@sha256:88f041650885cac6d139c5bd9fe4f978528ee4bf0136222dcd97294c40385fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.6 MB (677605989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b265adae93c91a30e0882e5572ff747d951ae3f0c103c706dcb5ebe51b2418aa`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9dd5db5ee75c65d415533124aec3497ea6cfe7728de5f89d89fb1fcb4d9fec`  
		Last Modified: Tue, 21 Oct 2025 22:13:18 GMT  
		Size: 254.6 MB (254558334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f61a3f793676c616ca646fbb5b34a13f47c0c4a4513777cade48586f3dc5af`  
		Last Modified: Tue, 21 Oct 2025 22:12:35 GMT  
		Size: 14.4 MB (14355860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3732c206b5a236e0323004f885ae0097c2fb967ba8704773f196efc9d45d9609`  
		Last Modified: Tue, 21 Oct 2025 20:24:17 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa2e8d88c6f62dbeaf4402ed65fbb0a19d3e9f0b85a32b280102e40cbd2cf5e`  
		Last Modified: Tue, 21 Oct 2025 22:12:45 GMT  
		Size: 378.5 MB (378486201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471402e95017dd2c0b18762d6906b3db5892ee394970c5056475b78c269a64c2`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82261e23706e3cc03d60ee6a6f01e6040245f97a206497eb0fea4bc92d14e5f4`  
		Last Modified: Tue, 21 Oct 2025 20:24:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23be812d141190b6cb961262fb5e9ce197fd24671d9017b2008ffad73794b488`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4873efd9c94b6611332e41a224823a2cb4a5254ffdbf0763f5b104cc0350bf`  
		Last Modified: Tue, 21 Oct 2025 20:24:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:279730dbbab9071b8f403a2cffaa8992f953136b120ea3fa1eafd29e6ecb130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61147988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f75e7221ceb3b379a4c51d5983095da13ee2fe735d8740320d548814117add`

```dockerfile
```

-	Layers:
	-	`sha256:dbba5b1ef6887c3aad08db42c26d5066829ecdd2987ed17882d7f90757099926`  
		Last Modified: Tue, 21 Oct 2025 22:12:39 GMT  
		Size: 61.1 MB (61121146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe151a020702b51fdbf815edd5bc13b03756b999f985083736d7955ed4ab25bb`  
		Last Modified: Tue, 21 Oct 2025 22:12:41 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:da71ccf94726713d385b8ec9624ccc7da55273f82fdfd0fc26a3a8c6847ded57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (673963797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d933c4f3b5042bb2782c775fd61334f34dae60181f4756508fded7fba1b917`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c54a63595205df680cc62caf76cd95a0d9b0f0002f5b26ce14b9db049693a8b`  
		Last Modified: Tue, 21 Oct 2025 22:13:15 GMT  
		Size: 252.0 MB (251960055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c49c49e27117fadc00f07697a96106539d20d575130a17a26ab90e382150fe`  
		Last Modified: Tue, 21 Oct 2025 19:57:26 GMT  
		Size: 14.3 MB (14333975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215225848a0cdc06f81f9570c13feaffe201463ad1d22ac343f54f26a5ea851f`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 480.0 KB (480002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec5e8cfbdca99baa3539ed0b967e041ca1b8b97712993d772c6f8b9fd17f683`  
		Last Modified: Tue, 21 Oct 2025 22:13:07 GMT  
		Size: 378.3 MB (378325611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af75e214bc33a94f915e7a0e4f13de46d9024c5f2e40dc4d040750960856ba0`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f42319f7a8dc6de5231c76c1f28d16af39a1892f69fc2402e366ad8e52f8ec`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f92858d7deae355be8c705ad8693b359c42dd87d43455c4f60bfae7e5d6e55`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ffb8b8e7f9cba4b932b447f5afe7007df11b0e45b7a97e472b127fde1be09b`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:01f89a1bf5ec8809d5400d310ee7e8f0436283fd170163bfd7725ec8d95d84e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61155415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8c652354ea3fe53cac5f9ba1e0ea12b98f567837e91ec60613d764f9567285`

```dockerfile
```

-	Layers:
	-	`sha256:a5fdab1d31211377a5d8ba5f2f0e4942c02b8644c0bd78f39574e05d6a738801`  
		Last Modified: Tue, 21 Oct 2025 22:14:20 GMT  
		Size: 61.1 MB (61128421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c63454c6caf99288085965a261e98b0f290794e231395578001fc023598b531`  
		Last Modified: Tue, 21 Oct 2025 22:14:22 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:58c64b20f8b2500dde5bd664acffe9d5f1e64682d9b93267190f716cdaa2d855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.8 MB (693770725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5046a17225dc94a888d42e1fa9745c487439da34c7e9a4cf4c885b08092c5fd1`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=ppc64le
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
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
	-	`sha256:ac0a27b08d5b9780c7d719b380d0e62a2876e87a5645202c2eb916107849db85`  
		Last Modified: Tue, 21 Oct 2025 23:57:26 GMT  
		Size: 379.0 MB (379021406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b430615140aac450924ea0e0a88bc155eadcc9ddf601b27847e0fe6fc6e73a4`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53804ece2c4ca306dff7cb8396cf69b054b386ecf50faa7badfa42f98c11e66`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b325cd7dcf4e35f386ab8039f7472949ce1d53af8a84ec643030ffaba687af`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a8a013adeb16cb6e1de6d3a8efe22489cc9a0a134eb7040104ddbea809cb21`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:35760a9d878fa046973781090b45e4b88096e355c6b879d3a5f373cff21ea8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61156373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e01baf8fcb6ab20345a7e9e10636d8845b1cf7fd0c11f3bc89a777ae54f636f`

```dockerfile
```

-	Layers:
	-	`sha256:5bdc3a5bf6febf658cd8ce0db8db83de76f098299f358d56398fcde7386330bc`  
		Last Modified: Wed, 22 Oct 2025 01:16:24 GMT  
		Size: 61.1 MB (61129475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f58ded0c1a59a3704a7de4b90b11f1bcbc3aaf0938039eeac18b5892f2bd48b8`  
		Last Modified: Wed, 22 Oct 2025 01:16:26 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251021`

```console
$ docker pull odoo@sha256:5ba70ff950b461c2caaeb15b43e4b879935afaa9762da8034beae7facfe6df20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20251021` - linux; amd64

```console
$ docker pull odoo@sha256:88f041650885cac6d139c5bd9fe4f978528ee4bf0136222dcd97294c40385fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.6 MB (677605989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b265adae93c91a30e0882e5572ff747d951ae3f0c103c706dcb5ebe51b2418aa`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9dd5db5ee75c65d415533124aec3497ea6cfe7728de5f89d89fb1fcb4d9fec`  
		Last Modified: Tue, 21 Oct 2025 22:13:18 GMT  
		Size: 254.6 MB (254558334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f61a3f793676c616ca646fbb5b34a13f47c0c4a4513777cade48586f3dc5af`  
		Last Modified: Tue, 21 Oct 2025 22:12:35 GMT  
		Size: 14.4 MB (14355860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3732c206b5a236e0323004f885ae0097c2fb967ba8704773f196efc9d45d9609`  
		Last Modified: Tue, 21 Oct 2025 20:24:17 GMT  
		Size: 480.0 KB (480009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa2e8d88c6f62dbeaf4402ed65fbb0a19d3e9f0b85a32b280102e40cbd2cf5e`  
		Last Modified: Tue, 21 Oct 2025 22:12:45 GMT  
		Size: 378.5 MB (378486201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471402e95017dd2c0b18762d6906b3db5892ee394970c5056475b78c269a64c2`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82261e23706e3cc03d60ee6a6f01e6040245f97a206497eb0fea4bc92d14e5f4`  
		Last Modified: Tue, 21 Oct 2025 20:24:17 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23be812d141190b6cb961262fb5e9ce197fd24671d9017b2008ffad73794b488`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4873efd9c94b6611332e41a224823a2cb4a5254ffdbf0763f5b104cc0350bf`  
		Last Modified: Tue, 21 Oct 2025 20:24:14 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:279730dbbab9071b8f403a2cffaa8992f953136b120ea3fa1eafd29e6ecb130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61147988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f75e7221ceb3b379a4c51d5983095da13ee2fe735d8740320d548814117add`

```dockerfile
```

-	Layers:
	-	`sha256:dbba5b1ef6887c3aad08db42c26d5066829ecdd2987ed17882d7f90757099926`  
		Last Modified: Tue, 21 Oct 2025 22:12:39 GMT  
		Size: 61.1 MB (61121146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe151a020702b51fdbf815edd5bc13b03756b999f985083736d7955ed4ab25bb`  
		Last Modified: Tue, 21 Oct 2025 22:12:41 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251021` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:da71ccf94726713d385b8ec9624ccc7da55273f82fdfd0fc26a3a8c6847ded57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.0 MB (673963797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d933c4f3b5042bb2782c775fd61334f34dae60181f4756508fded7fba1b917`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c54a63595205df680cc62caf76cd95a0d9b0f0002f5b26ce14b9db049693a8b`  
		Last Modified: Tue, 21 Oct 2025 22:13:15 GMT  
		Size: 252.0 MB (251960055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c49c49e27117fadc00f07697a96106539d20d575130a17a26ab90e382150fe`  
		Last Modified: Tue, 21 Oct 2025 19:57:26 GMT  
		Size: 14.3 MB (14333975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215225848a0cdc06f81f9570c13feaffe201463ad1d22ac343f54f26a5ea851f`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 480.0 KB (480002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec5e8cfbdca99baa3539ed0b967e041ca1b8b97712993d772c6f8b9fd17f683`  
		Last Modified: Tue, 21 Oct 2025 22:13:07 GMT  
		Size: 378.3 MB (378325611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af75e214bc33a94f915e7a0e4f13de46d9024c5f2e40dc4d040750960856ba0`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f42319f7a8dc6de5231c76c1f28d16af39a1892f69fc2402e366ad8e52f8ec`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f92858d7deae355be8c705ad8693b359c42dd87d43455c4f60bfae7e5d6e55`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ffb8b8e7f9cba4b932b447f5afe7007df11b0e45b7a97e472b127fde1be09b`  
		Last Modified: Tue, 21 Oct 2025 19:57:24 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:01f89a1bf5ec8809d5400d310ee7e8f0436283fd170163bfd7725ec8d95d84e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61155415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8c652354ea3fe53cac5f9ba1e0ea12b98f567837e91ec60613d764f9567285`

```dockerfile
```

-	Layers:
	-	`sha256:a5fdab1d31211377a5d8ba5f2f0e4942c02b8644c0bd78f39574e05d6a738801`  
		Last Modified: Tue, 21 Oct 2025 22:14:20 GMT  
		Size: 61.1 MB (61128421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c63454c6caf99288085965a261e98b0f290794e231395578001fc023598b531`  
		Last Modified: Tue, 21 Oct 2025 22:14:22 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251021` - linux; ppc64le

```console
$ docker pull odoo@sha256:58c64b20f8b2500dde5bd664acffe9d5f1e64682d9b93267190f716cdaa2d855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **693.8 MB (693770725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5046a17225dc94a888d42e1fa9745c487439da34c7e9a4cf4c885b08092c5fd1`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=ppc64le
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=18.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=29dcdb90f62464d7de48eead12df402ab85c132c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
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
	-	`sha256:ac0a27b08d5b9780c7d719b380d0e62a2876e87a5645202c2eb916107849db85`  
		Last Modified: Tue, 21 Oct 2025 23:57:26 GMT  
		Size: 379.0 MB (379021406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b430615140aac450924ea0e0a88bc155eadcc9ddf601b27847e0fe6fc6e73a4`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53804ece2c4ca306dff7cb8396cf69b054b386ecf50faa7badfa42f98c11e66`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b325cd7dcf4e35f386ab8039f7472949ce1d53af8a84ec643030ffaba687af`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a8a013adeb16cb6e1de6d3a8efe22489cc9a0a134eb7040104ddbea809cb21`  
		Last Modified: Tue, 21 Oct 2025 23:57:32 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:35760a9d878fa046973781090b45e4b88096e355c6b879d3a5f373cff21ea8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61156373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e01baf8fcb6ab20345a7e9e10636d8845b1cf7fd0c11f3bc89a777ae54f636f`

```dockerfile
```

-	Layers:
	-	`sha256:5bdc3a5bf6febf658cd8ce0db8db83de76f098299f358d56398fcde7386330bc`  
		Last Modified: Wed, 22 Oct 2025 01:16:24 GMT  
		Size: 61.1 MB (61129475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f58ded0c1a59a3704a7de4b90b11f1bcbc3aaf0938039eeac18b5892f2bd48b8`  
		Last Modified: Wed, 22 Oct 2025 01:16:26 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:28457d4c74b2861a56feb38fe7a74107110a66af7627bbec54099a1f5deeede0
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
$ docker pull odoo@sha256:3543b8a8ce8bb2fd90a5798b909d93a96b56b057e7b535982cb576a477973155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.5 MB (682514827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4956f45f43d834a1bf8369f2fcba4f6338b10afceecfe9988a570fbb33a6844`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883995ffbfadee83082d89b7a8faead2d18beb6ca21da5aad31077b8f123fa89`  
		Last Modified: Tue, 21 Oct 2025 22:13:51 GMT  
		Size: 254.6 MB (254557915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b6081310e7cf6a7fd841d3a483e1a3aaba3c3e4eee17230974db51d002285`  
		Last Modified: Tue, 21 Oct 2025 20:24:18 GMT  
		Size: 14.4 MB (14355749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b859646dd41c973c652fc2b04f39a621d5b48719d30850a54522c38327b3ac1d`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 480.0 KB (480015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df96018c5d095084fa9018f9eadb26ea0884637546d36c9e3a73fbe770ff381`  
		Last Modified: Tue, 21 Oct 2025 22:13:13 GMT  
		Size: 383.4 MB (383395566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20262af59a5fa8847b1e3538d38968a268bf64fa38be65d22341068617ab74eb`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70319edc0e99800f8031a477035b873eef57ff6daa2e56d61e1d83b146938012`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7b7c010c92195b7ed5f4ca846dd3907676eb696c2801f53d9d65dad697d7c`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8c82846fadfdc40be1d16e766c7ea7bf7893cf1bf02074d876b2d96d77e57`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:b1f131bf97c2bfd0d58851913d04cafdbd087f48a056e60379b39b49be299048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67859461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b61dcdf93b0cb6da4338c358da14474ae9c4f2ef1c6f80057125e52858f196`

```dockerfile
```

-	Layers:
	-	`sha256:fa15a3ad0447c3c45bf1a1c1f15fc748c5cbc41044716a5257ebe1660e235b29`  
		Last Modified: Tue, 21 Oct 2025 22:12:53 GMT  
		Size: 67.8 MB (67832326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c782dc2393232c7d6c930dfb54320d7f3c5127e3d398439527d4065637944f`  
		Last Modified: Tue, 21 Oct 2025 22:12:55 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7e534274c0e03c1e28986385122715f65bab3df9fd3b925b2c693298b76f7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.9 MB (678867371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d8f042fc15acaed7eb3c8bd45ad043c25181a31a6f8a49a439e09f9d6a4e4e`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ce2ab9e0e9cf3c5ae8236ed055fc513518faa29bcd51ce736a20085990a44`  
		Last Modified: Tue, 21 Oct 2025 22:15:38 GMT  
		Size: 252.0 MB (251959729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7789c2c262e2374a0f7549ff6399bed5e2fd4794ba28f5e53446c43b9e4e02`  
		Last Modified: Tue, 21 Oct 2025 19:57:53 GMT  
		Size: 14.3 MB (14333960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfded980a75f3045b5138811e896ac387c7ca4cdf545aa15ca354e3eab63f90`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 480.0 KB (480014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec89e226fc9bd25095e0f23cce987c88bbfb59738ff4f691e39cf32fcf50762`  
		Last Modified: Tue, 21 Oct 2025 22:15:50 GMT  
		Size: 383.2 MB (383229517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20999f36a80a8a3c77e5d6f370c04f6dcea75dd349b53f54c5ba0bfd38c093`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269dbd32081dbd7226a81102344a3e00bc811215d354c2aa50a4a233ba99eea2`  
		Last Modified: Tue, 21 Oct 2025 19:57:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a051a99f82ada1e3342e4bee4c541e379c3d1c93a8554ddd47d8080429c34b52`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5681f91ce105f11be6337c65f846174e68aed65ddf61912c96480cfe88ccf`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:9731bada9ffc47f8539bc9b348d75696b92ff0a3269cb087d88d753de21e7310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7b3ced07bea6af37eab6069740db8daf9357c823324c3a5983d43ad14f215c`

```dockerfile
```

-	Layers:
	-	`sha256:aa67b1d82cd033b5aa9b50ef5f884f30d1201bb9ea1e30e2cb3076c302e1cd5a`  
		Last Modified: Tue, 21 Oct 2025 22:14:59 GMT  
		Size: 67.8 MB (67839613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4974e812b2001ddc83d5bbb177e35a90a90c3f7f5fb3d40a41851d1efe2fee`  
		Last Modified: Tue, 21 Oct 2025 22:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:8465dde008ba902488efc7027cd6017ff5c05b11c8cff3837e4093ece9fa4f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.7 MB (698678685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3efac6cdd8f8d1885af589355974d849fdade958395360d4f5b96a47ec3f65`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=ppc64le
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
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
	-	`sha256:fb5814ea53b18e9c5b0f1363392b080a4a2e18f42f5605a36fa8ae272d6fb054`  
		Last Modified: Tue, 21 Oct 2025 23:50:37 GMT  
		Size: 383.9 MB (383929359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bfe0ddf6502e432cf6c5f3c270e9117dd29ef625290bbdeb5cae52330b7089`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7d7ceeb0ec778c9b615a9bda964056189eeca4cee526d16c6057ae6437961`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c171b72f46cd0d2c2e8e7a97f72444450b2ca25cf83081e10240b56e4c6d5cb9`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac8d9a58534e5f00feb39b29922e4f34b9a1d17f6e064799e1c34dbaa872ac`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:7296b3b8c5cf0e170097454fd704e2767f7c9c94c13bff5d6841ebd987296df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67867859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb893d96926384ff2fd7ce6af19e80af4943a41d40b0214babf22daa5f7c5e0`

```dockerfile
```

-	Layers:
	-	`sha256:006889b71d13ae7143c491cfd83e84b784c5620239659b0a306ac9a5fb9dc136`  
		Last Modified: Wed, 22 Oct 2025 01:16:34 GMT  
		Size: 67.8 MB (67840661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aac6901f92cc48ee2eb9bae4478077b639dd09209febfdba00619267a1ffd85`  
		Last Modified: Wed, 22 Oct 2025 01:16:35 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:28457d4c74b2861a56feb38fe7a74107110a66af7627bbec54099a1f5deeede0
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
$ docker pull odoo@sha256:3543b8a8ce8bb2fd90a5798b909d93a96b56b057e7b535982cb576a477973155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.5 MB (682514827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4956f45f43d834a1bf8369f2fcba4f6338b10afceecfe9988a570fbb33a6844`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883995ffbfadee83082d89b7a8faead2d18beb6ca21da5aad31077b8f123fa89`  
		Last Modified: Tue, 21 Oct 2025 22:13:51 GMT  
		Size: 254.6 MB (254557915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b6081310e7cf6a7fd841d3a483e1a3aaba3c3e4eee17230974db51d002285`  
		Last Modified: Tue, 21 Oct 2025 20:24:18 GMT  
		Size: 14.4 MB (14355749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b859646dd41c973c652fc2b04f39a621d5b48719d30850a54522c38327b3ac1d`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 480.0 KB (480015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df96018c5d095084fa9018f9eadb26ea0884637546d36c9e3a73fbe770ff381`  
		Last Modified: Tue, 21 Oct 2025 22:13:13 GMT  
		Size: 383.4 MB (383395566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20262af59a5fa8847b1e3538d38968a268bf64fa38be65d22341068617ab74eb`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70319edc0e99800f8031a477035b873eef57ff6daa2e56d61e1d83b146938012`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7b7c010c92195b7ed5f4ca846dd3907676eb696c2801f53d9d65dad697d7c`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8c82846fadfdc40be1d16e766c7ea7bf7893cf1bf02074d876b2d96d77e57`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b1f131bf97c2bfd0d58851913d04cafdbd087f48a056e60379b39b49be299048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67859461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b61dcdf93b0cb6da4338c358da14474ae9c4f2ef1c6f80057125e52858f196`

```dockerfile
```

-	Layers:
	-	`sha256:fa15a3ad0447c3c45bf1a1c1f15fc748c5cbc41044716a5257ebe1660e235b29`  
		Last Modified: Tue, 21 Oct 2025 22:12:53 GMT  
		Size: 67.8 MB (67832326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c782dc2393232c7d6c930dfb54320d7f3c5127e3d398439527d4065637944f`  
		Last Modified: Tue, 21 Oct 2025 22:12:55 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7e534274c0e03c1e28986385122715f65bab3df9fd3b925b2c693298b76f7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.9 MB (678867371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d8f042fc15acaed7eb3c8bd45ad043c25181a31a6f8a49a439e09f9d6a4e4e`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ce2ab9e0e9cf3c5ae8236ed055fc513518faa29bcd51ce736a20085990a44`  
		Last Modified: Tue, 21 Oct 2025 22:15:38 GMT  
		Size: 252.0 MB (251959729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7789c2c262e2374a0f7549ff6399bed5e2fd4794ba28f5e53446c43b9e4e02`  
		Last Modified: Tue, 21 Oct 2025 19:57:53 GMT  
		Size: 14.3 MB (14333960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfded980a75f3045b5138811e896ac387c7ca4cdf545aa15ca354e3eab63f90`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 480.0 KB (480014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec89e226fc9bd25095e0f23cce987c88bbfb59738ff4f691e39cf32fcf50762`  
		Last Modified: Tue, 21 Oct 2025 22:15:50 GMT  
		Size: 383.2 MB (383229517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20999f36a80a8a3c77e5d6f370c04f6dcea75dd349b53f54c5ba0bfd38c093`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269dbd32081dbd7226a81102344a3e00bc811215d354c2aa50a4a233ba99eea2`  
		Last Modified: Tue, 21 Oct 2025 19:57:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a051a99f82ada1e3342e4bee4c541e379c3d1c93a8554ddd47d8080429c34b52`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5681f91ce105f11be6337c65f846174e68aed65ddf61912c96480cfe88ccf`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9731bada9ffc47f8539bc9b348d75696b92ff0a3269cb087d88d753de21e7310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7b3ced07bea6af37eab6069740db8daf9357c823324c3a5983d43ad14f215c`

```dockerfile
```

-	Layers:
	-	`sha256:aa67b1d82cd033b5aa9b50ef5f884f30d1201bb9ea1e30e2cb3076c302e1cd5a`  
		Last Modified: Tue, 21 Oct 2025 22:14:59 GMT  
		Size: 67.8 MB (67839613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4974e812b2001ddc83d5bbb177e35a90a90c3f7f5fb3d40a41851d1efe2fee`  
		Last Modified: Tue, 21 Oct 2025 22:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:8465dde008ba902488efc7027cd6017ff5c05b11c8cff3837e4093ece9fa4f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.7 MB (698678685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3efac6cdd8f8d1885af589355974d849fdade958395360d4f5b96a47ec3f65`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=ppc64le
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
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
	-	`sha256:fb5814ea53b18e9c5b0f1363392b080a4a2e18f42f5605a36fa8ae272d6fb054`  
		Last Modified: Tue, 21 Oct 2025 23:50:37 GMT  
		Size: 383.9 MB (383929359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bfe0ddf6502e432cf6c5f3c270e9117dd29ef625290bbdeb5cae52330b7089`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7d7ceeb0ec778c9b615a9bda964056189eeca4cee526d16c6057ae6437961`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c171b72f46cd0d2c2e8e7a97f72444450b2ca25cf83081e10240b56e4c6d5cb9`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac8d9a58534e5f00feb39b29922e4f34b9a1d17f6e064799e1c34dbaa872ac`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7296b3b8c5cf0e170097454fd704e2767f7c9c94c13bff5d6841ebd987296df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67867859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb893d96926384ff2fd7ce6af19e80af4943a41d40b0214babf22daa5f7c5e0`

```dockerfile
```

-	Layers:
	-	`sha256:006889b71d13ae7143c491cfd83e84b784c5620239659b0a306ac9a5fb9dc136`  
		Last Modified: Wed, 22 Oct 2025 01:16:34 GMT  
		Size: 67.8 MB (67840661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aac6901f92cc48ee2eb9bae4478077b639dd09209febfdba00619267a1ffd85`  
		Last Modified: Wed, 22 Oct 2025 01:16:35 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251021`

```console
$ docker pull odoo@sha256:28457d4c74b2861a56feb38fe7a74107110a66af7627bbec54099a1f5deeede0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20251021` - linux; amd64

```console
$ docker pull odoo@sha256:3543b8a8ce8bb2fd90a5798b909d93a96b56b057e7b535982cb576a477973155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.5 MB (682514827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4956f45f43d834a1bf8369f2fcba4f6338b10afceecfe9988a570fbb33a6844`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883995ffbfadee83082d89b7a8faead2d18beb6ca21da5aad31077b8f123fa89`  
		Last Modified: Tue, 21 Oct 2025 22:13:51 GMT  
		Size: 254.6 MB (254557915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b6081310e7cf6a7fd841d3a483e1a3aaba3c3e4eee17230974db51d002285`  
		Last Modified: Tue, 21 Oct 2025 20:24:18 GMT  
		Size: 14.4 MB (14355749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b859646dd41c973c652fc2b04f39a621d5b48719d30850a54522c38327b3ac1d`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 480.0 KB (480015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df96018c5d095084fa9018f9eadb26ea0884637546d36c9e3a73fbe770ff381`  
		Last Modified: Tue, 21 Oct 2025 22:13:13 GMT  
		Size: 383.4 MB (383395566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20262af59a5fa8847b1e3538d38968a268bf64fa38be65d22341068617ab74eb`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70319edc0e99800f8031a477035b873eef57ff6daa2e56d61e1d83b146938012`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7b7c010c92195b7ed5f4ca846dd3907676eb696c2801f53d9d65dad697d7c`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8c82846fadfdc40be1d16e766c7ea7bf7893cf1bf02074d876b2d96d77e57`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:b1f131bf97c2bfd0d58851913d04cafdbd087f48a056e60379b39b49be299048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67859461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b61dcdf93b0cb6da4338c358da14474ae9c4f2ef1c6f80057125e52858f196`

```dockerfile
```

-	Layers:
	-	`sha256:fa15a3ad0447c3c45bf1a1c1f15fc748c5cbc41044716a5257ebe1660e235b29`  
		Last Modified: Tue, 21 Oct 2025 22:12:53 GMT  
		Size: 67.8 MB (67832326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c782dc2393232c7d6c930dfb54320d7f3c5127e3d398439527d4065637944f`  
		Last Modified: Tue, 21 Oct 2025 22:12:55 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251021` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7e534274c0e03c1e28986385122715f65bab3df9fd3b925b2c693298b76f7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.9 MB (678867371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d8f042fc15acaed7eb3c8bd45ad043c25181a31a6f8a49a439e09f9d6a4e4e`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ce2ab9e0e9cf3c5ae8236ed055fc513518faa29bcd51ce736a20085990a44`  
		Last Modified: Tue, 21 Oct 2025 22:15:38 GMT  
		Size: 252.0 MB (251959729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7789c2c262e2374a0f7549ff6399bed5e2fd4794ba28f5e53446c43b9e4e02`  
		Last Modified: Tue, 21 Oct 2025 19:57:53 GMT  
		Size: 14.3 MB (14333960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfded980a75f3045b5138811e896ac387c7ca4cdf545aa15ca354e3eab63f90`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 480.0 KB (480014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec89e226fc9bd25095e0f23cce987c88bbfb59738ff4f691e39cf32fcf50762`  
		Last Modified: Tue, 21 Oct 2025 22:15:50 GMT  
		Size: 383.2 MB (383229517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20999f36a80a8a3c77e5d6f370c04f6dcea75dd349b53f54c5ba0bfd38c093`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269dbd32081dbd7226a81102344a3e00bc811215d354c2aa50a4a233ba99eea2`  
		Last Modified: Tue, 21 Oct 2025 19:57:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a051a99f82ada1e3342e4bee4c541e379c3d1c93a8554ddd47d8080429c34b52`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5681f91ce105f11be6337c65f846174e68aed65ddf61912c96480cfe88ccf`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:9731bada9ffc47f8539bc9b348d75696b92ff0a3269cb087d88d753de21e7310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7b3ced07bea6af37eab6069740db8daf9357c823324c3a5983d43ad14f215c`

```dockerfile
```

-	Layers:
	-	`sha256:aa67b1d82cd033b5aa9b50ef5f884f30d1201bb9ea1e30e2cb3076c302e1cd5a`  
		Last Modified: Tue, 21 Oct 2025 22:14:59 GMT  
		Size: 67.8 MB (67839613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4974e812b2001ddc83d5bbb177e35a90a90c3f7f5fb3d40a41851d1efe2fee`  
		Last Modified: Tue, 21 Oct 2025 22:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251021` - linux; ppc64le

```console
$ docker pull odoo@sha256:8465dde008ba902488efc7027cd6017ff5c05b11c8cff3837e4093ece9fa4f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.7 MB (698678685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3efac6cdd8f8d1885af589355974d849fdade958395360d4f5b96a47ec3f65`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=ppc64le
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
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
	-	`sha256:fb5814ea53b18e9c5b0f1363392b080a4a2e18f42f5605a36fa8ae272d6fb054`  
		Last Modified: Tue, 21 Oct 2025 23:50:37 GMT  
		Size: 383.9 MB (383929359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bfe0ddf6502e432cf6c5f3c270e9117dd29ef625290bbdeb5cae52330b7089`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7d7ceeb0ec778c9b615a9bda964056189eeca4cee526d16c6057ae6437961`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c171b72f46cd0d2c2e8e7a97f72444450b2ca25cf83081e10240b56e4c6d5cb9`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac8d9a58534e5f00feb39b29922e4f34b9a1d17f6e064799e1c34dbaa872ac`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251021` - unknown; unknown

```console
$ docker pull odoo@sha256:7296b3b8c5cf0e170097454fd704e2767f7c9c94c13bff5d6841ebd987296df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67867859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb893d96926384ff2fd7ce6af19e80af4943a41d40b0214babf22daa5f7c5e0`

```dockerfile
```

-	Layers:
	-	`sha256:006889b71d13ae7143c491cfd83e84b784c5620239659b0a306ac9a5fb9dc136`  
		Last Modified: Wed, 22 Oct 2025 01:16:34 GMT  
		Size: 67.8 MB (67840661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aac6901f92cc48ee2eb9bae4478077b639dd09209febfdba00619267a1ffd85`  
		Last Modified: Wed, 22 Oct 2025 01:16:35 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:28457d4c74b2861a56feb38fe7a74107110a66af7627bbec54099a1f5deeede0
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
$ docker pull odoo@sha256:3543b8a8ce8bb2fd90a5798b909d93a96b56b057e7b535982cb576a477973155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.5 MB (682514827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4956f45f43d834a1bf8369f2fcba4f6338b10afceecfe9988a570fbb33a6844`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=amd64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883995ffbfadee83082d89b7a8faead2d18beb6ca21da5aad31077b8f123fa89`  
		Last Modified: Tue, 21 Oct 2025 22:13:51 GMT  
		Size: 254.6 MB (254557915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379b6081310e7cf6a7fd841d3a483e1a3aaba3c3e4eee17230974db51d002285`  
		Last Modified: Tue, 21 Oct 2025 20:24:18 GMT  
		Size: 14.4 MB (14355749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b859646dd41c973c652fc2b04f39a621d5b48719d30850a54522c38327b3ac1d`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 480.0 KB (480015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df96018c5d095084fa9018f9eadb26ea0884637546d36c9e3a73fbe770ff381`  
		Last Modified: Tue, 21 Oct 2025 22:13:13 GMT  
		Size: 383.4 MB (383395566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20262af59a5fa8847b1e3538d38968a268bf64fa38be65d22341068617ab74eb`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70319edc0e99800f8031a477035b873eef57ff6daa2e56d61e1d83b146938012`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b7b7c010c92195b7ed5f4ca846dd3907676eb696c2801f53d9d65dad697d7c`  
		Last Modified: Tue, 21 Oct 2025 20:24:16 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8c82846fadfdc40be1d16e766c7ea7bf7893cf1bf02074d876b2d96d77e57`  
		Last Modified: Tue, 21 Oct 2025 20:24:15 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b1f131bf97c2bfd0d58851913d04cafdbd087f48a056e60379b39b49be299048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67859461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b61dcdf93b0cb6da4338c358da14474ae9c4f2ef1c6f80057125e52858f196`

```dockerfile
```

-	Layers:
	-	`sha256:fa15a3ad0447c3c45bf1a1c1f15fc748c5cbc41044716a5257ebe1660e235b29`  
		Last Modified: Tue, 21 Oct 2025 22:12:53 GMT  
		Size: 67.8 MB (67832326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22c782dc2393232c7d6c930dfb54320d7f3c5127e3d398439527d4065637944f`  
		Last Modified: Tue, 21 Oct 2025 22:12:55 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c7e534274c0e03c1e28986385122715f65bab3df9fd3b925b2c693298b76f7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.9 MB (678867371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d8f042fc15acaed7eb3c8bd45ad043c25181a31a6f8a49a439e09f9d6a4e4e`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=arm64
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ce2ab9e0e9cf3c5ae8236ed055fc513518faa29bcd51ce736a20085990a44`  
		Last Modified: Tue, 21 Oct 2025 22:15:38 GMT  
		Size: 252.0 MB (251959729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7789c2c262e2374a0f7549ff6399bed5e2fd4794ba28f5e53446c43b9e4e02`  
		Last Modified: Tue, 21 Oct 2025 19:57:53 GMT  
		Size: 14.3 MB (14333960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfded980a75f3045b5138811e896ac387c7ca4cdf545aa15ca354e3eab63f90`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 480.0 KB (480014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec89e226fc9bd25095e0f23cce987c88bbfb59738ff4f691e39cf32fcf50762`  
		Last Modified: Tue, 21 Oct 2025 22:15:50 GMT  
		Size: 383.2 MB (383229517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20999f36a80a8a3c77e5d6f370c04f6dcea75dd349b53f54c5ba0bfd38c093`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269dbd32081dbd7226a81102344a3e00bc811215d354c2aa50a4a233ba99eea2`  
		Last Modified: Tue, 21 Oct 2025 19:57:51 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a051a99f82ada1e3342e4bee4c541e379c3d1c93a8554ddd47d8080429c34b52`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f5681f91ce105f11be6337c65f846174e68aed65ddf61912c96480cfe88ccf`  
		Last Modified: Tue, 21 Oct 2025 19:57:50 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:9731bada9ffc47f8539bc9b348d75696b92ff0a3269cb087d88d753de21e7310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67866913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7b3ced07bea6af37eab6069740db8daf9357c823324c3a5983d43ad14f215c`

```dockerfile
```

-	Layers:
	-	`sha256:aa67b1d82cd033b5aa9b50ef5f884f30d1201bb9ea1e30e2cb3076c302e1cd5a`  
		Last Modified: Tue, 21 Oct 2025 22:14:59 GMT  
		Size: 67.8 MB (67839613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c4974e812b2001ddc83d5bbb177e35a90a90c3f7f5fb3d40a41851d1efe2fee`  
		Last Modified: Tue, 21 Oct 2025 22:15:00 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:8465dde008ba902488efc7027cd6017ff5c05b11c8cff3837e4093ece9fa4f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **698.7 MB (698678685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3efac6cdd8f8d1885af589355974d849fdade958395360d4f5b96a47ec3f65`
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
# Tue, 21 Oct 2025 11:42:44 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 21 Oct 2025 11:42:44 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Oct 2025 11:42:44 GMT
ARG TARGETARCH=ppc64le
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_VERSION=19.0
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_RELEASE=20251021
# Tue, 21 Oct 2025 11:42:44 GMT
ARG ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251021 ODOO_SHA=eeba5130e7d34caa1c8459df926f1a207c314857
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 21 Oct 2025 11:42:44 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 21 Oct 2025 11:42:44 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 21 Oct 2025 11:42:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 21 Oct 2025 11:42:44 GMT
USER odoo
# Tue, 21 Oct 2025 11:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 21 Oct 2025 11:42:44 GMT
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
	-	`sha256:fb5814ea53b18e9c5b0f1363392b080a4a2e18f42f5605a36fa8ae272d6fb054`  
		Last Modified: Tue, 21 Oct 2025 23:50:37 GMT  
		Size: 383.9 MB (383929359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19bfe0ddf6502e432cf6c5f3c270e9117dd29ef625290bbdeb5cae52330b7089`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7d7ceeb0ec778c9b615a9bda964056189eeca4cee526d16c6057ae6437961`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c171b72f46cd0d2c2e8e7a97f72444450b2ca25cf83081e10240b56e4c6d5cb9`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ac8d9a58534e5f00feb39b29922e4f34b9a1d17f6e064799e1c34dbaa872ac`  
		Last Modified: Tue, 21 Oct 2025 23:50:43 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7296b3b8c5cf0e170097454fd704e2767f7c9c94c13bff5d6841ebd987296df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67867859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb893d96926384ff2fd7ce6af19e80af4943a41d40b0214babf22daa5f7c5e0`

```dockerfile
```

-	Layers:
	-	`sha256:006889b71d13ae7143c491cfd83e84b784c5620239659b0a306ac9a5fb9dc136`  
		Last Modified: Wed, 22 Oct 2025 01:16:34 GMT  
		Size: 67.8 MB (67840661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aac6901f92cc48ee2eb9bae4478077b639dd09209febfdba00619267a1ffd85`  
		Last Modified: Wed, 22 Oct 2025 01:16:35 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
