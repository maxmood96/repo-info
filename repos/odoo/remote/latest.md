## `odoo:latest`

```console
$ docker pull odoo@sha256:b080d2048d06ced509d149f83a48bc60bb285e7b762e16c1a5a81836469b9dd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:latest` - linux; amd64

```console
$ docker pull odoo@sha256:880603abbe06a44c0cd522924857a658fc21ce86d113c0f8513d87b8ad7c29af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.8 MB (601790743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb407f383e179f9f6e1e0d9c44597c604d13c0d10fc0e9fdfb3d8d221ec850dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d916741f1f15fd5069b649299933cc5887d10a2ccbb056811c2c4a87acf80b5b`  
		Last Modified: Wed, 29 May 2024 20:01:59 GMT  
		Size: 233.7 MB (233721257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f06bd7631d24e69aecd8d9789ceec3d9a73f5e57bc98964519c6badb5c3744f`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 2.3 MB (2313388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d17ac75ffa51eb8632be5539b2bf8ffcd6c708f292b54dc43bba1ec5b47c46`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 458.9 KB (458948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53d0ba3a7a498f6eba11623e9fe798536c07a5ddb5fa4bf9ee29f4a9c1d3627`  
		Last Modified: Wed, 29 May 2024 20:02:02 GMT  
		Size: 335.8 MB (335760757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d361c9543ce6de2c209aafc6951969c55e6e1b5d9fe8a8e9bfcda1e302005bb0`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f508a43736c0d8168da81a39a40a7f700e6f3b860182f0998f5fe695643a8d`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aa690bba6acc686036cf68b1f27112eb0538d528561b48a5e9a80172317c64`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b942dcae61c8bc9ef20b19bba778e33b8c40a0bccd1245805ad818fa5790900`  
		Last Modified: Wed, 29 May 2024 20:01:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:bd522790584ce055e0d3362dcaa26dab82a4ba7b5bcea928370caa05dcc7fb2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b49525727a5bc9bd79a82747a0e82891b76a59ac0a41d981eb1ad77153cf942`

```dockerfile
```

-	Layers:
	-	`sha256:af80ce5281b9ca2eb24d41ebfdbf5fdbfe51adf6f0b3f4040a5d222ef3123cc4`  
		Last Modified: Wed, 29 May 2024 20:01:57 GMT  
		Size: 39.2 MB (39192841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1da4c12ad03bb3f5c42d2a171ff670838020c8f004033fd315e8f8b307e47e3`  
		Last Modified: Wed, 29 May 2024 20:01:56 GMT  
		Size: 26.5 KB (26517 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:576a3ca2d18d74f5aee91d26921573b84805b6a1e4edf8447c650ae0becc3734
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.1 MB (598088280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3418aa89ab7b164589c9602211aaacaee64319124d8cda9d93e537427ded844`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:28:33 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 02 May 2024 01:28:33 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 02 May 2024 01:28:33 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 01:28:33 GMT
ARG TARGETARCH
# Thu, 02 May 2024 01:30:55 GMT
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb
# Thu, 02 May 2024 01:31:10 GMT
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 01:31:11 GMT
RUN npm install -g rtlcss
# Thu, 02 May 2024 01:31:11 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 19:58:58 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 19:58:58 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 20:01:20 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb
# Wed, 22 May 2024 20:01:29 GMT
COPY file:cbe34bc5236465e4ed439e0c8f6504d2d221f79f7c70b37fe62b56662bd0ab6d in / 
# Wed, 22 May 2024 20:01:29 GMT
COPY file:1e7209cce5525d270c422815db614f496d4d0da4820de1ab0000e9e592223235 in /etc/odoo/ 
# Wed, 22 May 2024 20:01:30 GMT
# ARGS: ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons
# Wed, 22 May 2024 20:01:30 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 20:01:30 GMT
EXPOSE 8069 8071 8072
# Wed, 22 May 2024 20:01:30 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 20:01:30 GMT
COPY file:0bc771c66dfeb517d19d13ea2699a0d3cbbbba684c8851640e6b87fe85b40619 in /usr/local/bin/wait-for-psql.py 
# Wed, 22 May 2024 20:01:30 GMT
USER odoo
# Wed, 22 May 2024 20:01:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 20:01:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d5983fdb42d6e446c61ffd23ea73a31d297eb116faab716b0a05982385aef7`  
		Last Modified: Thu, 02 May 2024 01:33:56 GMT  
		Size: 231.1 MB (231130596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf51c84c847e95593779366fe62fbfc47376ab1cbb6b6a2891c096fbce365476`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 2.5 MB (2523315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4821493b21fb69aad8b99473d2e8c6fbc2c2ef7b66fe8255b0856b3929182b80`  
		Last Modified: Thu, 02 May 2024 01:33:37 GMT  
		Size: 459.4 KB (459401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395097b419f1653ad2f1bd560801bd7445fbfa6b5fa3cf4058aaf2dd117314e6`  
		Last Modified: Wed, 22 May 2024 20:03:53 GMT  
		Size: 335.6 MB (335571319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3022d74fcd3ee7b048231cd8d267a277018b56628a0e82e9831a071924143e9`  
		Last Modified: Wed, 22 May 2024 20:03:21 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef30f983608477172c69e8c399ea1488d8771405243a0ad20dd3e18c7852d17a`  
		Last Modified: Wed, 22 May 2024 20:03:22 GMT  
		Size: 554.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6db5452f9e3e9c79377e441f5c2b65ba5ebf66766f3f63a9a8587fdebfd440`  
		Last Modified: Wed, 22 May 2024 20:03:21 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9703cbc51fd3a98443851c5003332ca3191290e461fe9b5c7a82cffddf28ffa9`  
		Last Modified: Wed, 22 May 2024 20:03:21 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:22fb44ee0617d2c2287729c9d4cc063ba01cdbeb7d5fe17e14c2ed41eebd7eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.3 MB (618293001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041b490a3825dc5ac99cd47662bcd5e7bc09bd32fd2e81adeb84b31c967542ce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 12:05:22 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 22 May 2024 12:05:22 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 22 May 2024 12:05:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 22 May 2024 12:05:22 GMT
ARG TARGETARCH
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_VERSION=17.0
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_RELEASE=20240522
# Wed, 22 May 2024 12:05:22 GMT
ARG ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 22 May 2024 12:05:22 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 22 May 2024 12:05:22 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240522 ODOO_SHA=cc1b723a48b09ba80ee737dc10b4b08572811746
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 22 May 2024 12:05:22 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 22 May 2024 12:05:22 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 22 May 2024 12:05:22 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 22 May 2024 12:05:22 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 22 May 2024 12:05:22 GMT
USER odoo
# Wed, 22 May 2024 12:05:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 May 2024 12:05:22 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff62be6f5f65b553b61acf7267ff22918d248665ec3ec9a1b313b03ef217c4f9`  
		Last Modified: Wed, 29 May 2024 20:30:00 GMT  
		Size: 243.3 MB (243268541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5dbca549a03a5cbe2117251a21b070881d53c88f09c1ae04e307816c15136c`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 2.6 MB (2590095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18644e0e4b87df08e7c9adbfb8deb6d4a17e18bbfceb5bb2df6011fe530c58cd`  
		Last Modified: Wed, 29 May 2024 20:29:51 GMT  
		Size: 458.9 KB (458899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eb8100fed10d012faa8008015da5b511f60b8dee46440760ea3dd082dc88a4`  
		Last Modified: Wed, 29 May 2024 20:30:14 GMT  
		Size: 337.5 MB (337511798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050412ca59e9ada9ba40c8b96cc3d4b7b0d1a1d174b088c26ff8846d8ca17c07`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e450bf62e071223d4dfbbed16ae7bc09ef0c67bc771207b6b59c4d5287f608`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2e81751ebfab0458d5faa9cb865296a292023d86b365c8456c41931e3dd101`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72170a90d094a9b391380c725a24c3e1fbfa0f50ced61c68c949d26c8fd6f0c3`  
		Last Modified: Wed, 29 May 2024 20:29:53 GMT  
		Size: 586.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b7898e5ae60c55e5fda5148bf636cfcc902fc5cda1e59080a9ab29a6882c78ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39227716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa32bd721966b5b7a264d2b1376c3fe9d77a3a37dbca4b390a7604df7b52fed`

```dockerfile
```

-	Layers:
	-	`sha256:b0b003291c88e1b96a175acc1435e1dc71a766409583a95204d735e96b98b75a`  
		Last Modified: Wed, 29 May 2024 20:29:52 GMT  
		Size: 39.2 MB (39201148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebd75b346477b649ce59cccca1278fb9423e9d85f895202c526d18d0cce9bbc`  
		Last Modified: Wed, 29 May 2024 20:29:50 GMT  
		Size: 26.6 KB (26568 bytes)  
		MIME: application/vnd.in-toto+json
