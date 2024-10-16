## `odoo:latest`

```console
$ docker pull odoo@sha256:e6f19e3f9d13ee9252cdc93891189ca71b0a8fb4a2635e29c85bf9610d323bb7
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
$ docker pull odoo@sha256:00fb918672b6087d3ca6bd5e6df975d8f4ee96f4c4720f6cd114cb6fc9a6f474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.7 MB (650742613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9817ec1524cfca5860f388c01421f07f419b14abff8c035a52bbd9c1f87c875`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c515723785c5cfc6b0d2f86579616e477dae56599b17d356f1421ab6b5d7ba50`  
		Last Modified: Sat, 12 Oct 2024 00:57:57 GMT  
		Size: 254.5 MB (254513796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a7c64c0d83ab297d6710da37f7d0fc47f5171043cc1a0fe2acd475161b8227`  
		Last Modified: Sat, 12 Oct 2024 00:57:54 GMT  
		Size: 14.1 MB (14141936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b06683cecc70f55c8e9d59b162f474b8d2c243a782a93fd2385c9e3be9f2ac0`  
		Last Modified: Sat, 12 Oct 2024 00:57:54 GMT  
		Size: 472.3 KB (472337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05df22d5330ab210e07c00cafc13c1acad7e29de6dd2c8cb1d61ac4b726114a`  
		Last Modified: Sat, 12 Oct 2024 00:57:59 GMT  
		Size: 351.9 MB (351861648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9731f49fa0fb40a5c9c1bbe5a75a4a179f080d85a70b8457a927f07ba42a8a46`  
		Last Modified: Sat, 12 Oct 2024 00:57:55 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e59423866c69f3ff07719d8ddfa65805d4e7b4eba35048474f9da1bb09f54`  
		Last Modified: Sat, 12 Oct 2024 00:57:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e104ed53e75d20f85c78e158a8c6490c8d93214bee44c652b26b0bbae860e1d8`  
		Last Modified: Sat, 12 Oct 2024 00:57:55 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ec8182ce88a22c697f81420fa6f080d66c3045739d4a08daa5cd966d733be`  
		Last Modified: Sat, 12 Oct 2024 00:57:55 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:140f02684fb0817d1f166de90906aed68ddcdedcd62cb42793e1e804f5a65468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55458320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b7d56cfa6af0cf6325bfe5a5acf0e069704200984c9cfaff529672fa7e900`

```dockerfile
```

-	Layers:
	-	`sha256:87708d51542fd988b793c7cf99d7fc196aa559ca2a36c3397841db370b6a2e1b`  
		Last Modified: Sat, 12 Oct 2024 00:57:54 GMT  
		Size: 55.4 MB (55431400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6f49554f0c4f0f6ba0a65d0bb77603924f09035615ba3f4efcf721ebd00032e`  
		Last Modified: Sat, 12 Oct 2024 00:57:54 GMT  
		Size: 26.9 KB (26920 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:469d874f139931a7f2a0a10a29dabfb0ae14b7412e9b1c32d89777162f4822d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.1 MB (647141072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bac0822ed93e36534f5e38d555a95fbd0b2549134011ed6dece9c0a27be413`
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
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
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
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd478e57a8c006cd475a198e624ceec42c46e24f93b4681c8d19079f361a6cb2`  
		Last Modified: Sat, 12 Oct 2024 02:07:57 GMT  
		Size: 251.9 MB (251942563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad40c07ba44630dc4544b7cb21470db681eee528d6360b12c38d002fff11d179`  
		Last Modified: Sat, 12 Oct 2024 02:07:53 GMT  
		Size: 14.1 MB (14113966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0360c03799a5b66a386223eaff9318abb98edc24820b425d49642ece662f843d`  
		Last Modified: Sat, 12 Oct 2024 02:07:52 GMT  
		Size: 472.4 KB (472357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6439155f942c7883b6f2a266c23586b0490f29c31a449da4c3fcb7a05b9c3894`  
		Last Modified: Sat, 12 Oct 2024 02:08:00 GMT  
		Size: 351.7 MB (351724139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec39b78cf6fb3269d18256b92f86ed2487fe8c136415407b30d2c9833109c7`  
		Last Modified: Sat, 12 Oct 2024 02:07:54 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f511d65a5aa0b191db261c54a98d538bc0e2f398316c6968504ede65393d2c`  
		Last Modified: Sat, 12 Oct 2024 02:07:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b99fe0c19d2405c180dba1fdb5ef9c67d69a505aabd82e44ebca982aad5098b`  
		Last Modified: Sat, 12 Oct 2024 02:07:55 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a1e27606dba3bded891a88f3cc9f7b50d416f92b72146f9f6fdbc2f8d1b3aa`  
		Last Modified: Sat, 12 Oct 2024 02:07:55 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e7a5296fb465fa91436a0df68dc6af2ae039893874abf950efb92719917417f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55465771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec7d1ca8082c239defc86d1942d6ba945a644da3b5af571c1117ee657cf8b2c`

```dockerfile
```

-	Layers:
	-	`sha256:bb0732abd77e9d1cc5e566197e59f911ad83da64db63dcd3224b9048e1a8278a`  
		Last Modified: Sat, 12 Oct 2024 02:07:54 GMT  
		Size: 55.4 MB (55438694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79384492f7899b4d90faf45abcc66300bdd7cf2b02d292c6a3e6ce7fbd402eaa`  
		Last Modified: Sat, 12 Oct 2024 02:07:52 GMT  
		Size: 27.1 KB (27077 bytes)  
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
