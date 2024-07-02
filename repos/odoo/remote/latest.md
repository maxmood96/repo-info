## `odoo:latest`

```console
$ docker pull odoo@sha256:cfd904b5cbdfb3857709e65e13bfae204a635e4d1bf208ff27bbc88335d06f99
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
$ docker pull odoo@sha256:648f73f441f6c365796c85bd3c1c2981855dffbc2996efbd20885555dcc810c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 MB (594677171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a971c8e390d48f0f07140fed96db96d7963441919c74380f64f633ad020756c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 24 Jun 2024 09:13:48 GMT
ARG RELEASE
# Mon, 24 Jun 2024 09:13:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 24 Jun 2024 09:13:48 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 24 Jun 2024 09:13:48 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=amd64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f61ce99eb895f5f57f2e577ba92d82405da2518f1754c4bedeec5fa9e3515d`  
		Last Modified: Tue, 02 Jul 2024 03:23:26 GMT  
		Size: 233.7 MB (233723670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f296950c72ad7a88320aead36aa5339ae5f9339244ccfb62f6ce17854a3345fc`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 2.3 MB (2313751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1087908b082c60609c22ed2db4841f2fe1b534f767c75129f991a95a8ea2b7`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 460.2 KB (460217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cc2d985b0011a6433376d8c779e0f73df57334dc283e38b55967b7e40eee01`  
		Last Modified: Tue, 02 Jul 2024 03:23:28 GMT  
		Size: 328.6 MB (328643048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235871681e4bb561959bebc95dc884e102e8db333442971273762f9f3c87239`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5f8c48cc8c90b39e9c1f955ba04d288ff49a3760bdd127b98343f4ea99476f`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f249691be652760825dd298183e2a38338af4756b198657a04a6c72010ae85d`  
		Last Modified: Tue, 02 Jul 2024 03:23:24 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef67c5b9c03e47f2467df88506a11f9d2a516c49e3782ec79e6f4b3f5fda015`  
		Last Modified: Tue, 02 Jul 2024 03:23:25 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c929ee59788ba55a6268320ad4288ecfa84d68bbe1c1f9de26a42b81ac59a024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38667552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e779c9126971b3460a4247f1045fc333096220df484eeef1ddb915723581c6`

```dockerfile
```

-	Layers:
	-	`sha256:51efd760512e9b63b76ecb7cd5e5a3ac1351ef96ee157e9ed870f0e7ec9f80c9`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 38.6 MB (38640677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d16462c089873d7e5215598968921fd167d9517a2eb70d647aa28045c8d1d4`  
		Last Modified: Tue, 02 Jul 2024 03:23:23 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:52f02170ee855755e55921e11207233a9c973614fc48e8f533122814451a9499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 MB (589506044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7297ca0746061b2e6ea277b5742b6812557b79bd6d8ea316418d5c76ddd49a00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=arm64
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47c85e7c880a0b6a0829c41cdd1087784692d8fdbe4814d2a5ea6d83b6f3b5b`  
		Last Modified: Wed, 05 Jun 2024 16:47:36 GMT  
		Size: 231.1 MB (231129490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841be736c8c6adb83390654e12c5e97a2001d96c8d6a80f06b45ae6232d2244e`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 2.3 MB (2307615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd45dc8c7ace62c95b96ba7639f50653e7d4c4403ee4cd76b84b03a6a098c`  
		Last Modified: Wed, 05 Jun 2024 16:47:31 GMT  
		Size: 458.8 KB (458815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bfabac07be2024b8fccd8a3af3a59f3a7e09ff97be4ba2c865c11fdb0043d4`  
		Last Modified: Mon, 24 Jun 2024 18:29:46 GMT  
		Size: 328.2 MB (328245899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34314723ffd9e320fd561478044b50c27340c99b37eb43329ee689a4eb5429`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b518aa46a6ed6e075ea9b5a39a1a60d40f8a676a9678de5e68fbe936e8c1cc8e`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136e352ac21c2113b24b9a61063c2e7b22d0a8d2b8813d938b1b632e0694400c`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a97fa68e35c40e6ab7a5824874020d824108aec850e28d2097dd8c53e9e2e`  
		Last Modified: Mon, 24 Jun 2024 18:29:40 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:e3753d52d5a4d713fc351ed3d61e84b40b74ebf4dfd247844920534a4cb11cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38674378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41b0b10cdaeaa479067607a09d8713ea5a1ec05744340c3a7c7ac70115cf0d6`

```dockerfile
```

-	Layers:
	-	`sha256:2123ade5ac43e34b8bd186c470d9b1bc9662402a2ff5c4b1e85ea2b39d89bae1`  
		Last Modified: Mon, 24 Jun 2024 18:29:41 GMT  
		Size: 38.6 MB (38647202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340f4d6bb882266f1fa8bc5c6615fdfd5f43bf12ec40e02e984e1faef4ef64ed`  
		Last Modified: Mon, 24 Jun 2024 18:29:39 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:76a1170183ea3e1e614a3e76e10ad7de21f6e23ffa30d9cad9c07c35df584b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.2 MB (611177101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df0ae1009b13f5121c2bc2b2415a0e7f3f663ebd478133aa961c9017648be00`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 09:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 24 Jun 2024 09:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 09:13:48 GMT
ARG TARGETARCH=ppc64le
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_VERSION=17.0
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_RELEASE=20240624
# Mon, 24 Jun 2024 09:13:48 GMT
ARG ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240624 ODOO_SHA=76bba01e66368d00dc94c424f5f4964b8299f1b4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 24 Jun 2024 09:13:48 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 24 Jun 2024 09:13:48 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 24 Jun 2024 09:13:48 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 24 Jun 2024 09:13:48 GMT
USER odoo
# Mon, 24 Jun 2024 09:13:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 24 Jun 2024 09:13:48 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956fde24697c2bc63ebe0420d94352a09737c296dbd2b36955ee2062e9c0c770`  
		Last Modified: Wed, 05 Jun 2024 14:46:18 GMT  
		Size: 243.3 MB (243268694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ece47ec5864af7e8863954a92dd9f2fc7c049d58deae4e2b4860da85c7ffc64`  
		Last Modified: Wed, 05 Jun 2024 14:46:10 GMT  
		Size: 2.6 MB (2590044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490d2e7a7a95f94f8af2670a352815aca65e795ab1b0f1c0de54ac5c7d0c32a`  
		Last Modified: Wed, 05 Jun 2024 14:46:09 GMT  
		Size: 458.9 KB (458905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09df6db075a1a9dea80be197ad1d4dc2dc126691d190a41c4183938d85f3863e`  
		Last Modified: Mon, 24 Jun 2024 18:16:16 GMT  
		Size: 330.4 MB (330396320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282130baf4c896c22906d85c0838e337af019ad91416cfd9035440c48f60d3a8`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55709bb12b6c2542ae255950ca1e9610072f32e98e94fae28d07bdd5feccf972`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b6285537b99b839b789d323dcb1bbc9b06b26704d3d94ed3f8af28d6747eb4`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342e12641dba5f6ef33d3d8f36315ac2e79f20e3d3a8657a3ea103a515937e5f`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 587.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6d81886173938fb7968321b6254476c48c52a7e7c05db928f284c220be0ef270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38675920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9784ce9e348fbba540f04ab39c47b0b0e35acc076c0e3857e65ee93360ed561`

```dockerfile
```

-	Layers:
	-	`sha256:b05e653f8c0a61b63023a37e33469b1bc99acffdbe744ddb07b857ebe8fc9cef`  
		Last Modified: Mon, 24 Jun 2024 18:15:56 GMT  
		Size: 38.6 MB (38648990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85116f7f8a479bc882b5cc0775762ee661c883f2bae113d1d13ac6480a51d5c1`  
		Last Modified: Mon, 24 Jun 2024 18:15:55 GMT  
		Size: 26.9 KB (26930 bytes)  
		MIME: application/vnd.in-toto+json
