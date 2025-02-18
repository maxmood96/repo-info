## `odoo:latest`

```console
$ docker pull odoo@sha256:e984296ff633ad1c41d5b2ce099e9c75727a330a2fcda60cb4724d3dfe00587e
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
$ docker pull odoo@sha256:ed3e0573d8dc50a7f0d8a874b9e0dcdb42510f2f491f783cb3a9c7fc3d85f0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.8 MB (668821858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5549291bfd3cb5580386caf6e6cbecbfe6e75147fb39a08b857f776ba870ce60`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=amd64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 03 Feb 2025 23:00:26 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93c8457230a63c5fefa8a18a55154a4d9e66501ea9798169b1c202be5870e64`  
		Last Modified: Mon, 10 Feb 2025 20:13:11 GMT  
		Size: 254.5 MB (254514665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d65c04e02a60a679132af7431d0de40543254188f4388470d5a270764bff527`  
		Last Modified: Mon, 10 Feb 2025 20:12:51 GMT  
		Size: 16.6 MB (16634870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e32a3c71a37305f330e98d26d05f4813c2c3db9e6491f1de9e2c08853e931`  
		Last Modified: Mon, 10 Feb 2025 20:12:55 GMT  
		Size: 485.7 KB (485725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ffdf7ada3d25bc89191e5ab5ed201fc562e0357359cb5a57e71042a35faa99`  
		Last Modified: Mon, 10 Feb 2025 20:13:08 GMT  
		Size: 367.4 MB (367429874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a02c62c359d99d7749234c7dbc7ea7ba86e12d9234f7413a0af21333ee0d5d`  
		Last Modified: Mon, 10 Feb 2025 20:12:32 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2fb41ec4dfebf94ae4caeb265eebe9141bce36c484ca20f2c8ffe94a298d1e`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec91224c0307bdc867bbd18a3867c214e7ac92aff1b326e10520c817997e9a4`  
		Last Modified: Mon, 10 Feb 2025 20:12:57 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3b87f359ce03e621bd093d9c62c2c21bc913f9f78dd786abb6cd76aa2c14e9`  
		Last Modified: Mon, 10 Feb 2025 20:12:58 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d6dea5db3797508ad116f48e44d8db4a86507e00ddba7b55343ec2e69a792227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58502815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4ae0831eae72c2bb41b56ffe25e7e7b22ef73e148a9581b0dd95449ccd287d`

```dockerfile
```

-	Layers:
	-	`sha256:2c72ce9fa2d675776ea4f1d90eeb1a6d55e6ac52cf6f53f6b311d1734f34db4c`  
		Last Modified: Tue, 11 Feb 2025 10:02:47 GMT  
		Size: 58.5 MB (58475679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769c881a6e94e403056206373113ed66c5cf22e0c6a6a7e902620745b4997963`  
		Last Modified: Tue, 11 Feb 2025 10:02:42 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a62bd3145fc5c753e4fcd2d8c30eec4afa4cbfbdcea6a2e2257b6f00c9d080c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.2 MB (665205895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81af33182b1229b54babc7d46ac4a8db7b86c8f3eb2678d1ff52d31e285e8e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=arm64
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Tue, 04 Feb 2025 06:04:53 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4423ae3417994b02e28e725cf3fc1fbb074aba9d094ffeb5dbce79bb54e0f8b`  
		Last Modified: Mon, 10 Feb 2025 20:19:59 GMT  
		Size: 251.9 MB (251943363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1572c494925a5dc1301929c70510c4fddbc44dc821e6c485bf3c660b9332bc39`  
		Last Modified: Mon, 10 Feb 2025 20:19:48 GMT  
		Size: 16.6 MB (16581015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bba4c4196ec9c1a655094047ad1675b7e3cce5bd2735fe164bd0586d2471128`  
		Last Modified: Mon, 10 Feb 2025 20:56:29 GMT  
		Size: 485.7 KB (485723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c170fc6f3a93f27a45563edadd842fccfa276908110f763a5c925fda6ec1ca4c`  
		Last Modified: Mon, 10 Feb 2025 20:19:58 GMT  
		Size: 367.3 MB (367299757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfae44fbb129501505113d1e98aa82cc0012c80cbba4e9480b5f5ede8d9f5178`  
		Last Modified: Mon, 10 Feb 2025 20:19:49 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36565f0b254fe5085e6637cf18b71ecdff18aceccb4f701a38a81420c228d79`  
		Last Modified: Mon, 10 Feb 2025 20:19:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad0d7729a69ffae57421fc62aabba7b44213db3a99dfc556d4459b98068e329`  
		Last Modified: Mon, 10 Feb 2025 20:19:51 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35be8019f78f6aeeed2353b8b526f1dd15df9939de788076eef3c70a08e6b1d1`  
		Last Modified: Mon, 10 Feb 2025 20:25:56 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:59ccc0584a4a870b931ab3ec2af0fe87bb92e165ada2a52e62054d615da7c7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58510270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71051e33e0a726f5b2b6981e7042ac5504d75c8e9f0e8939043e8c1151d127d`

```dockerfile
```

-	Layers:
	-	`sha256:f575e9c1a9ac1b41123a687b20ad6d8cd3b5aa009b0ab3595ef98d6d4828fb2d`  
		Last Modified: Mon, 17 Feb 2025 08:12:36 GMT  
		Size: 58.5 MB (58482970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd59be01d2a10a58f34db4d5f1ff9ee63bd876e295ac01bc9ee47d9a89d609b`  
		Last Modified: Tue, 11 Feb 2025 10:03:49 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:d5a9b7740facb0f73384c72fe37478836d7d6f3be8dff8ee07b8c7f6bd44b516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **685.2 MB (685228926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ce4e1a930429c3a87189a3c10030f98850d5f109952c5cc8fa3489a9e8db82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 10:52:51 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Fri, 07 Feb 2025 10:52:51 GMT
SHELL [/bin/bash -xo pipefail -c]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 10:52:51 GMT
ARG TARGETARCH=ppc64le
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_VERSION=18.0
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_RELEASE=20250207
# Fri, 07 Feb 2025 10:52:51 GMT
ARG ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./entrypoint.sh / # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250207 ODOO_SHA=5658df4949b61e3b910aaa1000ec2b14c2b565c9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Fri, 07 Feb 2025 10:52:51 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Fri, 07 Feb 2025 10:52:51 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Fri, 07 Feb 2025 10:52:51 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Fri, 07 Feb 2025 10:52:51 GMT
USER odoo
# Fri, 07 Feb 2025 10:52:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Feb 2025 10:52:51 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Tue, 04 Feb 2025 07:01:00 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8455c54b495abb021f3ea0c5c47e4cc801d26c3f5b4f623f88a5ba88b4181458`  
		Last Modified: Tue, 11 Feb 2025 10:04:05 GMT  
		Size: 265.1 MB (265074206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0aa37e025c7ccd816c72a6cf91884a71817e56a69b066240616f7a2ae1537`  
		Last Modified: Tue, 11 Feb 2025 10:05:22 GMT  
		Size: 17.3 MB (17306456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a84f231b270cb999af35933efb7b7de7e00f97622369b26ac2dc6fec5558d7`  
		Last Modified: Tue, 11 Feb 2025 10:03:56 GMT  
		Size: 485.7 KB (485744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516ebdfd5cae90e665bc71c3b7d9d9c22c23f9250b65886700ff84958ca60188`  
		Last Modified: Tue, 11 Feb 2025 10:04:09 GMT  
		Size: 368.0 MB (367970253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db94ad5e4581072bac30b1f283b3bc048bce683f7ca053367d9d120d991ecc4`  
		Last Modified: Tue, 11 Feb 2025 06:06:44 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a28c04c6e61973e5fec7cca066fa13d7307f4ced12163423b98e9d253bcb6`  
		Last Modified: Tue, 11 Feb 2025 10:03:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38722995d30c6e2d4be74ac5fc9b2aa8b4e9150f0a02354d5bd256145c7d3133`  
		Last Modified: Thu, 13 Feb 2025 18:23:50 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372cd5fbdde7a18b51116b89d043b2ca11d9156e29347b9b7397625aa89c13d`  
		Last Modified: Tue, 11 Feb 2025 06:06:47 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c653f00151186ce57500a66373bbf59853f49b78c0baf99f098f56110748b1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58511040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646e1861ab8ab4e07f770835468c074727dd94e048aee7697ba88ad5be79852f`

```dockerfile
```

-	Layers:
	-	`sha256:2907c1ff3ac8deeedf25cd92fe2c9f6e92274fad98df7dab14597bcdea953fa8`  
		Last Modified: Tue, 11 Feb 2025 10:05:35 GMT  
		Size: 58.5 MB (58483842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c31ecbd9f32c3486ef587e4763db0650fbe21afee1a24bb28c561f837cdd0ca`  
		Last Modified: Tue, 11 Feb 2025 10:05:31 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
