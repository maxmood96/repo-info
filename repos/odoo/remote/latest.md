## `odoo:latest`

```console
$ docker pull odoo@sha256:ffe1c549263d8b2f03a0b660cabe06226b3a1249078e18df6bfeac8c80bfdf2a
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
$ docker pull odoo@sha256:00b5ced774f37c6f8967c030655c806e17f2f0673f6af1646c89538108a1bf48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **710.6 MB (710591540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b8a191eb6bd7d2f0e532379789f47aa5e39fded619c8cf6ce5d2830662b935`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:34 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:34 GMT
ARG TARGETARCH=amd64
# Mon, 22 Jun 2026 18:09:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:41 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:42 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:42 GMT
ENV ODOO_VERSION=19.0
# Mon, 22 Jun 2026 18:09:42 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:42 GMT
ARG ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
# Mon, 22 Jun 2026 18:10:44 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:45 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:45 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:45 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:45 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:45 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:45 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:45 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:45 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:45 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a498b8754f43fc6f32463f149504d61e935ea2a2fb20b12769672041e12a76d`  
		Last Modified: Mon, 22 Jun 2026 18:13:11 GMT  
		Size: 257.1 MB (257064214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd8b834b79e4cfd8a3be6d64649279761c9491050069f0a618d1a31a2eb4ea7`  
		Last Modified: Mon, 22 Jun 2026 18:12:57 GMT  
		Size: 14.4 MB (14370815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d40773ba8111156ddf2c24e4909ad88e9cd79f8404d6ecd90bbfcd16c0143f`  
		Last Modified: Mon, 22 Jun 2026 18:12:55 GMT  
		Size: 481.5 KB (481493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c96cc2ddd9e7df12adf469a79dad1186393c58542e7b352c7f0747161d0c6f`  
		Last Modified: Mon, 22 Jun 2026 18:13:16 GMT  
		Size: 408.9 MB (408939467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec5e7f0c9a75b3e89357d085a0260903d5f6eae14adcd0a6c261e21ecec0be2`  
		Last Modified: Mon, 22 Jun 2026 18:12:57 GMT  
		Size: 716.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bb3e1a63d8921b18ff1f3346f717b03325d534a758862e1612b3d6e91bc37f`  
		Last Modified: Mon, 22 Jun 2026 18:12:58 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01811095191457c0c3bb3e457afc50b2b33587368eaa6a8e8e1f1868abd5c2d6`  
		Last Modified: Mon, 22 Jun 2026 18:12:59 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826709e1f3361c7852399623e3cd570c7f52e3bb856e44a36e8a6aa49d3874f6`  
		Last Modified: Mon, 22 Jun 2026 18:13:00 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:0b714edc83af8ac0a14a14b6b98bfa8ecdf92800c4586e07a03cdf515cd0b4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70808431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aee22680b1310f543cc5758c4dbd22a360fa6f239019481a07bc102fd6b035c`

```dockerfile
```

-	Layers:
	-	`sha256:9a772233cfa594b216490367713ab6477e62428f4def58e0dd02545661dc9155`  
		Last Modified: Mon, 22 Jun 2026 18:13:01 GMT  
		Size: 70.8 MB (70781326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17151e82c0f05ca62259ea5260b8f26fd9a058de597b6342b3974f60b9728137`  
		Last Modified: Mon, 22 Jun 2026 18:12:55 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:3277732b693104701b29a75004927eaa9d5fc6977dbb697e0f50d7a8a42407dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.8 MB (706806636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f638a3d0e56b02474ff84152659c869e1a0fb36d34a5bf855948a7d5da4543c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:09 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:09 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:09 GMT
ARG TARGETARCH=arm64
# Mon, 22 Jun 2026 18:09:09 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:15 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:16 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:16 GMT
ENV ODOO_VERSION=19.0
# Mon, 22 Jun 2026 18:09:16 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:16 GMT
ARG ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
# Mon, 22 Jun 2026 18:10:22 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:23 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:23 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:23 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:23 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:23 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:23 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:23 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:23 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:23 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6911c7ea9ec6caae65d47b87f46fcacb409a98f3d6457a28f5b7f252a5615e09`  
		Last Modified: Mon, 22 Jun 2026 18:13:02 GMT  
		Size: 254.3 MB (254280404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95499d7ed9dfdb50decf3cd50d0f14447ff6d121a6c5459d7945912e29fb5e45`  
		Last Modified: Mon, 22 Jun 2026 18:12:54 GMT  
		Size: 14.3 MB (14349233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab901ccea42be5d941eb8a8d294cea2a3df6194f07753ca50f94767a958cb65`  
		Last Modified: Mon, 22 Jun 2026 18:12:53 GMT  
		Size: 481.5 KB (481496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c61831efad87d1d2eeb21f02f823c3825f5ea8667d9b87b9b996a127c40e11`  
		Last Modified: Mon, 22 Jun 2026 18:13:06 GMT  
		Size: 408.8 MB (408816349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26525ee35175d00dbead13c1b1f89f751c0ef2797bed8c41fdc2e4e183e9fa0d`  
		Last Modified: Mon, 22 Jun 2026 18:12:54 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bbe8c16840e2938a8bd2c82971ef2d0e31c1021029111fca0910b4b7b400fc`  
		Last Modified: Mon, 22 Jun 2026 18:12:56 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b951cc5297c0c82c77156b099fdedceb8b25431fe1364c3e75bdff163f63061c`  
		Last Modified: Mon, 22 Jun 2026 18:12:56 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2eae2d3044c83a37089d1b272c4ed60c2a19fceeed743284ac42aa9c5e9a3`  
		Last Modified: Mon, 22 Jun 2026 18:12:57 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e56e01849ed34047d440b6afec6171bd84d1e3eefb63329e2080b4b1e395d1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70815882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96567a17b6e44ef4acaf0cf13a144a8af0d950b7d28df50009c09960c250dd22`

```dockerfile
```

-	Layers:
	-	`sha256:49ac6d4e814be48f27fb7cc560d5d8d7ba114bc72ebe98cac950e598190282c5`  
		Last Modified: Mon, 22 Jun 2026 18:12:57 GMT  
		Size: 70.8 MB (70788613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5463710b9f007956ead3ad43cc0aad408a8024c8fcd8bf45a3e531c4fd7e2b62`  
		Last Modified: Mon, 22 Jun 2026 18:12:53 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:4ab558a25055958a0268c5aa7c76d5404b6fede0c2d51b8d46a3846397b923e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.1 MB (727136282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7bf8cc64d5caee90abf6ae3ad72ef5de3885d6fc2fd6c7fdff38af46c4ca73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:30 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:15:30 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:15:30 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:15:30 GMT
ARG TARGETARCH=ppc64le
# Mon, 22 Jun 2026 18:15:30 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:15:41 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:15:44 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:15:44 GMT
ENV ODOO_VERSION=19.0
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
# Mon, 22 Jun 2026 18:18:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:18:08 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:18:08 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:18:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=9bee8d0dacd869ff673221960e5b77671d661abe
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:18:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:18:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:18:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:18:09 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:18:09 GMT
USER odoo
# Mon, 22 Jun 2026 18:18:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:18:09 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5506f792ec21667d7ee1ce73245b48165e88fc48a5b754ecb0e06a42f27cc917`  
		Last Modified: Mon, 22 Jun 2026 18:22:33 GMT  
		Size: 267.9 MB (267945849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5ae11f245759f238cd001999ba7611a8bc6ac2f4e319d4323c5d9208f6da29`  
		Last Modified: Mon, 22 Jun 2026 18:22:21 GMT  
		Size: 14.9 MB (14901269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a0f1ba1542858c557cbae4cd5e3a7a79f1c4499179414948b71819ae30196`  
		Last Modified: Mon, 22 Jun 2026 18:22:20 GMT  
		Size: 481.6 KB (481616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad96844e96aa181f3def05cd4a418ddb00643146cb8c0af3530cb8c98f6d961`  
		Last Modified: Mon, 22 Jun 2026 18:23:41 GMT  
		Size: 409.5 MB (409490695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5626199be7d69a2e553c3ca0835688460c4e3244d49024caa9ff0b67c9fd62fe`  
		Last Modified: Mon, 22 Jun 2026 18:23:30 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a13afdc277ffd8fd74fd3f8bc3a285997160d1df2032b0851a0a581afe4300`  
		Last Modified: Mon, 22 Jun 2026 18:23:30 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9caefa3952088073895d050bbc6662fca0cce72c0a4c33847750008f5dbbfc`  
		Last Modified: Mon, 22 Jun 2026 18:23:30 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cda394b91bb708262bf884c62854c4c6f8e202b0d80418f19a481a43ba57d4b`  
		Last Modified: Mon, 22 Jun 2026 18:23:31 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:410b7b861959f4ba92ff25e34069cba82fb997beb80dbdeccbd7f0fe130a8a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70816882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e870a1ccc1bec34d57ad75c9df2307a9498e2a8f3f286c1120e6d0aebcca9c`

```dockerfile
```

-	Layers:
	-	`sha256:6381c006c1cc6bb604aeb2ce87d48941ec89867a92e9b1ff76014c7b233f4668`  
		Last Modified: Mon, 22 Jun 2026 18:23:33 GMT  
		Size: 70.8 MB (70789715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d23f2699afea9bd88a3b4091710cbbc2371f027168599c5662b81a09cb523c`  
		Last Modified: Mon, 22 Jun 2026 18:23:29 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json
