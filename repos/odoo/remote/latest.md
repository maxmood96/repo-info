## `odoo:latest`

```console
$ docker pull odoo@sha256:11ec69d0d41a26b8ceaf7430637e556a226e4a35e5cce5511b53b86555350a2b
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
$ docker pull odoo@sha256:11915bf322efb5fa4371b1baabdac639c984e73c8d6fe076cde9f22f02000790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.9 MB (674938432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31294ed50b232a360d5052b9b8ac4b0f79b80e0bca8e6cfd0fd96c8b6f2ff047`
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
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=amd64
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6649e3d58a0d0b8784b9841145a38f28833c1e1843512168c5faf55063e49`  
		Last Modified: Tue, 01 Apr 2025 17:17:45 GMT  
		Size: 256.9 MB (256920087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7cdb5b6d46543dd0ae496333c3341fc26e1f7903ee205da7d0c7305aa5786`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 16.7 MB (16679841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4368ac54be95afda32beac0a5d938c2d22a44d7d4ffdb2d5288852e6433c38`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 478.6 KB (478631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b81e6dd4358e484db83bf7137711920744fa7ae817fb7b5aae821d2cd75115`  
		Last Modified: Tue, 01 Apr 2025 17:17:47 GMT  
		Size: 371.1 MB (371103144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b2ab46d8292b3e6e8656a6aa5f9d2022e99040eed1b6b692aa3da4ad9be223`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e51ac74ed12296ea5d0afcff54cf5dd9d235b6f5cc2a3d3d0a3a1258ac5855`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abff459f547feac64f046cf976feba44de557ffee0cebb6b37f798ce8e17109`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c5e89477b21c6c57e0daa68cd114e2c2828b5560be8e5139aef14bc084ce98`  
		Last Modified: Tue, 01 Apr 2025 17:17:43 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:0bc99842e9caccabba0b21955277d1521625d66bd4e627944de883af56fc16c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59211986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881845c37f6ef69622d56949434e3f93f0cb78c0af761e5df7eb8085f43fde41`

```dockerfile
```

-	Layers:
	-	`sha256:59706d74b4a7c1fcc1c5b321fe7152a1bc5ffd48fc4ce125ca224db9441eaf07`  
		Last Modified: Tue, 01 Apr 2025 17:17:42 GMT  
		Size: 59.2 MB (59184851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11c81002107ccfd779072a1f7a5f3dff323e3394218abad6a956cc86e1d7b40`  
		Last Modified: Tue, 01 Apr 2025 17:17:41 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6138adf199dce157a7b9ccb0f7ede6722a7209f2011dec46d7100a79edaeb922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.7 MB (670701306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd39fd06eba7900ac2a4f173c864b12804a8849128d54dbb678a90ddecd9ccf2`
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
# Thu, 20 Mar 2025 11:33:43 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 20 Mar 2025 11:33:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Mar 2025 11:33:43 GMT
ARG TARGETARCH=arm64
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_VERSION=18.0
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_RELEASE=20250320
# Thu, 20 Mar 2025 11:33:43 GMT
ARG ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250320 ODOO_SHA=f2b9056ce21821292062f3d753dc38dacc3afe4d
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 20 Mar 2025 11:33:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 20 Mar 2025 11:33:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 20 Mar 2025 11:33:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 20 Mar 2025 11:33:43 GMT
USER odoo
# Thu, 20 Mar 2025 11:33:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 20 Mar 2025 11:33:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8730f827b8b7817a0d4aa80fe57257039cd9098da1ac96e7c7eae75dcfc14d15`  
		Last Modified: Thu, 20 Mar 2025 17:19:11 GMT  
		Size: 254.2 MB (254156179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3cf7384512c28559c37404199f0662a7ae17ceb5ff872ae06a04b0b03f3cbc`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 16.6 MB (16621658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab85031777875a4a365d33aab4dc2c17d243e324e097d6f0e4f9d9bada5fad`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 478.6 KB (478605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d77f068fa67f17ced6f5216b2234e2912333dc124282e8afadf7dd23c73397`  
		Last Modified: Thu, 20 Mar 2025 17:19:12 GMT  
		Size: 370.5 MB (370548829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09246ae991ed7d432c1e88bbdc50ec8292f5276b8fe5a6ab9f4480c211f89984`  
		Last Modified: Thu, 20 Mar 2025 17:19:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d53e88c6c7f74c8281ae5b3457d77f12ead4038f0c72a735fda09fa0bfdd44`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ebe002e971520488811d202dfb62c61cf04b4648716544cd73f719dda09f63`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d90cdb34f68681d23720f704d47101a3e8a9503473370a98f353e63b8da472e`  
		Last Modified: Thu, 20 Mar 2025 17:19:07 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6ed1a95549d8dafc1b93c5f89b3f2b0fe75de5179261c6d6e639aadc2fee728d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59172966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533558d65bf86a325e5109360a3068e83e2b5bddaddaa678fec954e34b28584e`

```dockerfile
```

-	Layers:
	-	`sha256:e550d71a8de7750dc0ac2410ffea29403a1064db9af93fa6afbbe9a8be85d638`  
		Last Modified: Thu, 20 Mar 2025 17:19:06 GMT  
		Size: 59.1 MB (59145666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3974d4b5fe20ecc8f23483d86f84443d827077a1169798f7ad190012774a22d2`  
		Last Modified: Thu, 20 Mar 2025 17:19:04 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:e6359e6c77f001ceeb361efc63d07b6cd8fd9b402257c7aad09b1ffb6e836065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691583226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8641c36c1aace922eae6f8a576092797d9f7e981e66f3c4ab6ccaf1571fa87ec`
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
# Tue, 01 Apr 2025 13:33:26 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 01 Apr 2025 13:33:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 01 Apr 2025 13:33:26 GMT
ARG TARGETARCH=ppc64le
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_VERSION=18.0
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_RELEASE=20250401
# Tue, 01 Apr 2025 13:33:26 GMT
ARG ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250401 ODOO_SHA=e855a2ae12dd342571629c9e9e7e531bebff3fb2
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 01 Apr 2025 13:33:26 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 01 Apr 2025 13:33:26 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 01 Apr 2025 13:33:26 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 01 Apr 2025 13:33:26 GMT
USER odoo
# Tue, 01 Apr 2025 13:33:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Apr 2025 13:33:26 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b255a6cdf7bee77bd813b26e458404c51906e2c26ee33151f4494a4384cbbceb`  
		Last Modified: Thu, 20 Mar 2025 17:23:28 GMT  
		Size: 267.7 MB (267709874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266984176781c453c9676a0655e2600e985f7c298ed73730eba450762c46dc9e`  
		Last Modified: Thu, 20 Mar 2025 17:23:14 GMT  
		Size: 17.4 MB (17357354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fdec516c786264ba6ff83229ba8621ca81da021db675f524db6969367779215`  
		Last Modified: Thu, 20 Mar 2025 17:23:11 GMT  
		Size: 478.6 KB (478571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612e41278a9a3e9bbdbe7589c9b68e944ba6fb06be8b59373016da666817881c`  
		Last Modified: Tue, 01 Apr 2025 17:31:20 GMT  
		Size: 371.6 MB (371645163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e31cd8ee8b7a522177f93f796cdeaf41d295ec8d06d554d81a81f6f5b7cfc77`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b2f907bfb5a21e58d3ec64d6dcef4d8f8d6d63a2a9aa4a025bba0ac9710122`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e559a2d0c0cc1a7ac017e0cf846eb3bdcfa1ca2c06db9958a475cb04fab0dc3`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:048d34ebc171a7331741597ebdd77f2ea5d03fd9a0e0d6fc2293617a0efd1ea3`  
		Last Modified: Tue, 01 Apr 2025 17:31:11 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:a433252570c36776fd9d0bc8cdc75caae553ae927a9ab6d72b9b8ac5a930c7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ac41726d2a7dd9cc2661ed583418133b53ba912b5a2402b373d1e663744fbb`

```dockerfile
```

-	Layers:
	-	`sha256:cbe7a1280e2616c51f4871d9c148f3513a80c9afb3f879e1186817e39f90e36d`  
		Last Modified: Tue, 01 Apr 2025 17:31:12 GMT  
		Size: 59.2 MB (59192998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788016454f0a74828fbe2def6f9a0f308b4decbbd2ed7659d6fa5900e349c855`  
		Last Modified: Tue, 01 Apr 2025 17:31:10 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
