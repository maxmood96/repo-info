<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20251222`](#odoo170-20251222)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20251222`](#odoo180-20251222)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20251222`](#odoo190-20251222)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:8f3ff15073f1ef7d3aedf6464963b1a8394ac6416d37e1d8562d22d9e5df702b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:fbcc921644d551d0679e8bccac502013a44fbfa89e42f327cbd83a017b7e41dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.0 MB (607983277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d14f86fa825c8494f5d1469c49de64c9f767323fb6c94f149a78aa83448662`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:48 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:48 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:57 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:58 GMT
ENV ODOO_VERSION=17.0
# Wed, 24 Dec 2025 05:13:58 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:58 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Wed, 24 Dec 2025 05:14:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3dc70b2a3f7c29678d05adf7f9ed867bc040da5e2fc920afb742c9f8030be`  
		Last Modified: Wed, 24 Dec 2025 05:16:48 GMT  
		Size: 233.8 MB (233814084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e6b18d6b3c86ab31956c4f58bc613e10826066ff7981621a429744cc18a0c`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 2.6 MB (2597223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148589d145519d4a12a5ca1bdc8d630b49ac28b2663b0809a86331dd07dcd5ab`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 480.3 KB (480313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0969d876aad3bb7335d90eac67f895a2ac13862749ab609d1d19fa2556ef2eae`  
		Last Modified: Wed, 24 Dec 2025 05:16:54 GMT  
		Size: 341.6 MB (341552422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e6b35c79db206ee4db1647a4975f5884b362a08ad4fcb6252db3459402094`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d7a0e1cef690a8f642b0eda324dcc35363af28c4194d580f91705795b5068c`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bba1aeca0251a9feb6792c319258fb83256fb7c668c9720ade6904f5c410e69`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a4b8d58344c895ac9d0fef9f45bed84b8d55d1724271b37c4e6220a247d7d`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c31bad87053903a3b50e23b12b62fb3be78346ac3d6defa66cc39d7901325a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41889697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a6009113c8e9fd6de77e529fd707d0591cccda876883232482b68b8b8e71b4`

```dockerfile
```

-	Layers:
	-	`sha256:66c862fa09dae138e5b061c027584d9e8a3df7f7aa92121e2063f912ff8ad780`  
		Last Modified: Wed, 24 Dec 2025 08:12:25 GMT  
		Size: 41.9 MB (41862905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba5f8d10a8a997a71b85bad54065ec803d0fe799fb92e5c0e7a8ff168dabdb2`  
		Last Modified: Wed, 24 Dec 2025 08:12:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0845ac0c8d4f7ac943d059bff9bcd852468349f2a2afdcf4c68bc0a41a045f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 MB (602840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf240d51666298e7d8567d22644742297b0db5ab67f1bb7bab1cac921eda905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:16 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:27 GMT
ENV ODOO_VERSION=17.0
# Wed, 24 Dec 2025 05:13:27 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:27 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Wed, 24 Dec 2025 05:14:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87054dd4c107dd5036885036a8457c9f85d0047c2e2dbfd6e90e8b6e873ca054`  
		Last Modified: Wed, 24 Dec 2025 05:16:18 GMT  
		Size: 231.2 MB (231204816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85825c38ba4d62b57b70237150947fab18c2320445a4abefc9defd1245bebcdd`  
		Last Modified: Wed, 24 Dec 2025 05:16:09 GMT  
		Size: 2.6 MB (2592585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9221d52236be227978baebd522546569c98d629767b02579d51c3ba11987f5`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 480.3 KB (480314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e00d4494aa4286036eed92a37437d7d862fd8bad4157d23f05b1996a783678e`  
		Last Modified: Wed, 24 Dec 2025 05:16:19 GMT  
		Size: 341.2 MB (341176872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec358575f7073cd1aa5898b1b5955d127d2a53e5a4a9f7ccbc48a7cfd4b3308f`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff0fa86b4e3698cf35d27124b8ab406e3101fb913d7b02548fb97aa599cc0e7`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d786478767f740f15573fc06de9a174420316f8202eaa5f8f95073bf8d3279e`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea40755e929a938970c1255b7ce79c9df4c7ed68b00f4be1e76db130f28cb2e`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:3f150d1873b2add419468f872f28d36596e2d258b5a8a1ebf39cc88257e16a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e400ec04170f9348b7f6f6e76e3feef055f0dc6c7431e041585d471e874cb5d`

```dockerfile
```

-	Layers:
	-	`sha256:80c684400486c5f7075dea982d9a92cbbad721e6d210fb540eb27db31eb67624`  
		Last Modified: Wed, 24 Dec 2025 08:13:28 GMT  
		Size: 41.9 MB (41869412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:322eee282ad17841e366d2d9bf305f8f2b46f9be33617e0c2098d61f4fab5d5c`  
		Last Modified: Wed, 24 Dec 2025 08:13:29 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:8f3ff15073f1ef7d3aedf6464963b1a8394ac6416d37e1d8562d22d9e5df702b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:fbcc921644d551d0679e8bccac502013a44fbfa89e42f327cbd83a017b7e41dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.0 MB (607983277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d14f86fa825c8494f5d1469c49de64c9f767323fb6c94f149a78aa83448662`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:48 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:48 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:57 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:58 GMT
ENV ODOO_VERSION=17.0
# Wed, 24 Dec 2025 05:13:58 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:58 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Wed, 24 Dec 2025 05:14:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3dc70b2a3f7c29678d05adf7f9ed867bc040da5e2fc920afb742c9f8030be`  
		Last Modified: Wed, 24 Dec 2025 05:16:48 GMT  
		Size: 233.8 MB (233814084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e6b18d6b3c86ab31956c4f58bc613e10826066ff7981621a429744cc18a0c`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 2.6 MB (2597223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148589d145519d4a12a5ca1bdc8d630b49ac28b2663b0809a86331dd07dcd5ab`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 480.3 KB (480313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0969d876aad3bb7335d90eac67f895a2ac13862749ab609d1d19fa2556ef2eae`  
		Last Modified: Wed, 24 Dec 2025 05:16:54 GMT  
		Size: 341.6 MB (341552422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e6b35c79db206ee4db1647a4975f5884b362a08ad4fcb6252db3459402094`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d7a0e1cef690a8f642b0eda324dcc35363af28c4194d580f91705795b5068c`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bba1aeca0251a9feb6792c319258fb83256fb7c668c9720ade6904f5c410e69`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a4b8d58344c895ac9d0fef9f45bed84b8d55d1724271b37c4e6220a247d7d`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c31bad87053903a3b50e23b12b62fb3be78346ac3d6defa66cc39d7901325a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41889697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a6009113c8e9fd6de77e529fd707d0591cccda876883232482b68b8b8e71b4`

```dockerfile
```

-	Layers:
	-	`sha256:66c862fa09dae138e5b061c027584d9e8a3df7f7aa92121e2063f912ff8ad780`  
		Last Modified: Wed, 24 Dec 2025 08:12:25 GMT  
		Size: 41.9 MB (41862905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba5f8d10a8a997a71b85bad54065ec803d0fe799fb92e5c0e7a8ff168dabdb2`  
		Last Modified: Wed, 24 Dec 2025 08:12:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0845ac0c8d4f7ac943d059bff9bcd852468349f2a2afdcf4c68bc0a41a045f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 MB (602840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf240d51666298e7d8567d22644742297b0db5ab67f1bb7bab1cac921eda905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:16 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:27 GMT
ENV ODOO_VERSION=17.0
# Wed, 24 Dec 2025 05:13:27 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:27 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Wed, 24 Dec 2025 05:14:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87054dd4c107dd5036885036a8457c9f85d0047c2e2dbfd6e90e8b6e873ca054`  
		Last Modified: Wed, 24 Dec 2025 05:16:18 GMT  
		Size: 231.2 MB (231204816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85825c38ba4d62b57b70237150947fab18c2320445a4abefc9defd1245bebcdd`  
		Last Modified: Wed, 24 Dec 2025 05:16:09 GMT  
		Size: 2.6 MB (2592585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9221d52236be227978baebd522546569c98d629767b02579d51c3ba11987f5`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 480.3 KB (480314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e00d4494aa4286036eed92a37437d7d862fd8bad4157d23f05b1996a783678e`  
		Last Modified: Wed, 24 Dec 2025 05:16:19 GMT  
		Size: 341.2 MB (341176872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec358575f7073cd1aa5898b1b5955d127d2a53e5a4a9f7ccbc48a7cfd4b3308f`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff0fa86b4e3698cf35d27124b8ab406e3101fb913d7b02548fb97aa599cc0e7`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d786478767f740f15573fc06de9a174420316f8202eaa5f8f95073bf8d3279e`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea40755e929a938970c1255b7ce79c9df4c7ed68b00f4be1e76db130f28cb2e`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:3f150d1873b2add419468f872f28d36596e2d258b5a8a1ebf39cc88257e16a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e400ec04170f9348b7f6f6e76e3feef055f0dc6c7431e041585d471e874cb5d`

```dockerfile
```

-	Layers:
	-	`sha256:80c684400486c5f7075dea982d9a92cbbad721e6d210fb540eb27db31eb67624`  
		Last Modified: Wed, 24 Dec 2025 08:13:28 GMT  
		Size: 41.9 MB (41869412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:322eee282ad17841e366d2d9bf305f8f2b46f9be33617e0c2098d61f4fab5d5c`  
		Last Modified: Wed, 24 Dec 2025 08:13:29 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20251222`

```console
$ docker pull odoo@sha256:8f3ff15073f1ef7d3aedf6464963b1a8394ac6416d37e1d8562d22d9e5df702b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20251222` - linux; amd64

```console
$ docker pull odoo@sha256:fbcc921644d551d0679e8bccac502013a44fbfa89e42f327cbd83a017b7e41dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.0 MB (607983277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d14f86fa825c8494f5d1469c49de64c9f767323fb6c94f149a78aa83448662`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:48 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:48 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:48 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:48 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:13:48 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:57 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:58 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:58 GMT
ENV ODOO_VERSION=17.0
# Wed, 24 Dec 2025 05:13:58 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:58 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Wed, 24 Dec 2025 05:14:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:59 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3dc70b2a3f7c29678d05adf7f9ed867bc040da5e2fc920afb742c9f8030be`  
		Last Modified: Wed, 24 Dec 2025 05:16:48 GMT  
		Size: 233.8 MB (233814084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e6b18d6b3c86ab31956c4f58bc613e10826066ff7981621a429744cc18a0c`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 2.6 MB (2597223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148589d145519d4a12a5ca1bdc8d630b49ac28b2663b0809a86331dd07dcd5ab`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 480.3 KB (480313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0969d876aad3bb7335d90eac67f895a2ac13862749ab609d1d19fa2556ef2eae`  
		Last Modified: Wed, 24 Dec 2025 05:16:54 GMT  
		Size: 341.6 MB (341552422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878e6b35c79db206ee4db1647a4975f5884b362a08ad4fcb6252db3459402094`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d7a0e1cef690a8f642b0eda324dcc35363af28c4194d580f91705795b5068c`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bba1aeca0251a9feb6792c319258fb83256fb7c668c9720ade6904f5c410e69`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1a4b8d58344c895ac9d0fef9f45bed84b8d55d1724271b37c4e6220a247d7d`  
		Last Modified: Wed, 24 Dec 2025 05:16:33 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:c31bad87053903a3b50e23b12b62fb3be78346ac3d6defa66cc39d7901325a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41889697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a6009113c8e9fd6de77e529fd707d0591cccda876883232482b68b8b8e71b4`

```dockerfile
```

-	Layers:
	-	`sha256:66c862fa09dae138e5b061c027584d9e8a3df7f7aa92121e2063f912ff8ad780`  
		Last Modified: Wed, 24 Dec 2025 08:12:25 GMT  
		Size: 41.9 MB (41862905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba5f8d10a8a997a71b85bad54065ec803d0fe799fb92e5c0e7a8ff168dabdb2`  
		Last Modified: Wed, 24 Dec 2025 08:12:27 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20251222` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:0845ac0c8d4f7ac943d059bff9bcd852468349f2a2afdcf4c68bc0a41a045f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.8 MB (602840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf240d51666298e7d8567d22644742297b0db5ab67f1bb7bab1cac921eda905`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:16 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:16 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:16 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:16 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:26 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:27 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:27 GMT
ENV ODOO_VERSION=17.0
# Wed, 24 Dec 2025 05:13:27 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:27 GMT
ARG ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
# Wed, 24 Dec 2025 05:14:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=89bedfe72d8d35aac19b03135ba8e7064e6862ab
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:28 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87054dd4c107dd5036885036a8457c9f85d0047c2e2dbfd6e90e8b6e873ca054`  
		Last Modified: Wed, 24 Dec 2025 05:16:18 GMT  
		Size: 231.2 MB (231204816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85825c38ba4d62b57b70237150947fab18c2320445a4abefc9defd1245bebcdd`  
		Last Modified: Wed, 24 Dec 2025 05:16:09 GMT  
		Size: 2.6 MB (2592585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9221d52236be227978baebd522546569c98d629767b02579d51c3ba11987f5`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 480.3 KB (480314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e00d4494aa4286036eed92a37437d7d862fd8bad4157d23f05b1996a783678e`  
		Last Modified: Wed, 24 Dec 2025 05:16:19 GMT  
		Size: 341.2 MB (341176872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec358575f7073cd1aa5898b1b5955d127d2a53e5a4a9f7ccbc48a7cfd4b3308f`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff0fa86b4e3698cf35d27124b8ab406e3101fb913d7b02548fb97aa599cc0e7`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d786478767f740f15573fc06de9a174420316f8202eaa5f8f95073bf8d3279e`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea40755e929a938970c1255b7ce79c9df4c7ed68b00f4be1e76db130f28cb2e`  
		Last Modified: Wed, 24 Dec 2025 05:16:08 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:3f150d1873b2add419468f872f28d36596e2d258b5a8a1ebf39cc88257e16a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41896356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e400ec04170f9348b7f6f6e76e3feef055f0dc6c7431e041585d471e874cb5d`

```dockerfile
```

-	Layers:
	-	`sha256:80c684400486c5f7075dea982d9a92cbbad721e6d210fb540eb27db31eb67624`  
		Last Modified: Wed, 24 Dec 2025 08:13:28 GMT  
		Size: 41.9 MB (41869412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:322eee282ad17841e366d2d9bf305f8f2b46f9be33617e0c2098d61f4fab5d5c`  
		Last Modified: Wed, 24 Dec 2025 08:13:29 GMT  
		Size: 26.9 KB (26944 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:1ba7ab9783cd2b08a875077dc3c744b0dcbe7eb0f78ac354a1c7a658f5455749
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
$ docker pull odoo@sha256:69fcabd9ef3818440eb5300ae44e15076a77eda9925f8cd0641b24038dfeb4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680314103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbafce4c9a475e748d6033227380d8dbb8452876ec3eb4aa32db65fff6349d9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:57 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:13:57 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:14:07 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:14:08 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:14:08 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:14:08 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:15:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:15:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:15:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:15:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
USER odoo
# Wed, 24 Dec 2025 05:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:15:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f067bfe61f0cf0e3dc1268722b731044195fe086446a1547b64a0e687c3de52`  
		Last Modified: Wed, 24 Dec 2025 05:20:17 GMT  
		Size: 254.6 MB (254556968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd02c37bfe1dbfe524fe486baf03112d7b55551864232373bd232920c5643c`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 14.4 MB (14356622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735020f60fbf6f01a63f90f30d03345473ca0cb8a259e7335357d026d3e081e3`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 480.0 KB (479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0a262e7461c242b5ecc7365d62e32c0163031727c1c58c9324822a630ac48a`  
		Last Modified: Wed, 24 Dec 2025 05:20:20 GMT  
		Size: 381.2 MB (381193395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1914e0409c5edb8b81f4332fa9c2e97501607511829f0377255fc237ba8145`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d8b448bb52580a7f582939f6b94d89c337a8380a7649c6dc243d3401dfe074`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4febe640d26e3f3f4d2bfd850d54381e73689fcd1786a93a43887ae9cba200db`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865d3d125071e9c87ae911436047f6c7390f0fb242f2d7557995a818a9ee0ebb`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7417cac4a4176bb26bb15ccf9487458786cb85337e02a9c00bdab48103a663f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bc676acd8ca48973d99b8a456b39b23806b6de12271e89fbe0b2520b00e986`

```dockerfile
```

-	Layers:
	-	`sha256:4f1b46c60e9d2de606480240d70d872699b7fd384ca071995f168e6db8ba1367`  
		Last Modified: Wed, 24 Dec 2025 08:12:44 GMT  
		Size: 61.4 MB (61447207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7534f0d47ac70ab1a721326b60aa1adbe6116b081ca7eb9cbecb66b51f29df`  
		Last Modified: Wed, 24 Dec 2025 08:12:41 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e5df1eca650338a075257be65588d231d5b639cfc849a4b9849d361b6d082c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.7 MB (676695982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fb9d6c9a921c4c94d4c3c31831e32dd2cd51d2dd4b1b6a33253e57f2f6fa35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:39 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:39 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:51 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:13:51 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:51 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:14:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:52 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c6c4dd8728629dfae9e972f8ad8200102f169f31cc273197580c0df398d2c`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 252.0 MB (251956836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47200be7646f67b6fe04696e7257e66ddc69ad8cadd76c4b19ee6ae5f20bc796`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 14.3 MB (14334194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79bfa30f5723be9e79db439947a5fe3dab3d6ac2634abfab763afade32c996`  
		Last Modified: Wed, 24 Dec 2025 05:16:53 GMT  
		Size: 480.1 KB (480065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce21bf8d032b6b646d7f47c62ecca84a86ca083e3d050577d03aeba70177ba`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 381.1 MB (381060489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2507a0d6031b7387eaa644ae34f2b53bf896fea848f4df728e0c92bb0b41cebc`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08872a033ec07b149067502136b5056d42392a18223988e1041cc9951d6e7a`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2718713fdb0ae6d9388052cdd478d811e8157227f4a20d247ac7db6262b6d844`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da2532b90c10e56d5b2c66066cb8525eb8c3e329a362e71ae5a3bd4038a764`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:0f4aaf095b2a20b3c6189edeca52b8ece5446872f188494f18f6604aba3a8610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61481433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88399ec6273e8918c3cdfdb1788b09f226bebd77ea1724ae7fbe9a563943965`

```dockerfile
```

-	Layers:
	-	`sha256:059d7d9667e3b4cf8cfa9dfaed5ff580e0838a4aebe1968ce6537bcaff8b2c52`  
		Last Modified: Wed, 24 Dec 2025 08:14:58 GMT  
		Size: 61.5 MB (61454482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af647442717e509828bd3fb5a96b1b8c7314e47e0335b2c7c7106443b671c69`  
		Last Modified: Wed, 24 Dec 2025 08:14:59 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:413e69860943b9bc2436d7e78dd92622fecb385d40df7d8ebb61d2213b73473b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696487864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12add77d7cc557f5bfc6361d609b59ef214d5b528dfb5e881a8f06a11bf49a01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:15:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:15:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:15:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:15:49 GMT
ARG TARGETARCH=ppc64le
# Wed, 24 Dec 2025 05:15:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:18:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:18:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:18:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:18:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:18:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:18:43 GMT
USER odoo
# Wed, 24 Dec 2025 05:18:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceff955aaee4caea237c20301c4a641abd1ff7cfa6f6badf931348bced7c61`  
		Last Modified: Wed, 24 Dec 2025 05:24:12 GMT  
		Size: 265.1 MB (265086582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab10d7e4252bf6b6acd84ed974cacc270b5374aed5c27d772b77da5a47f225`  
		Last Modified: Wed, 24 Dec 2025 05:24:06 GMT  
		Size: 14.9 MB (14885504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fe9d208368cc6491c67f76d260cb902fa083d619b7564f06793764a524d6f6`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 480.1 KB (480063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b9f152040ff5ee81f990fd2fe15174344cede1c67e0ae8b945ecc59eff652`  
		Last Modified: Wed, 24 Dec 2025 05:24:20 GMT  
		Size: 381.7 MB (381728849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b5e36fc037f0bc056db0c3b276f596048d93e1342e5e083405ceb96746040`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7097faedda3790a63b4ef274315e4e2beaf1b27e11478e54fe86c129275e0f`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31a7d6d2708a987a0ffb311dca55261fccbdf3fc9b15d210bfe6868e2f53b8`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6698e9681d6cf1d0e2f2f3af566cee0641f73e9a24c35646543445fb81b6157`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:ee9ad11576440ae7a606861084ffddee3db260c1868699dabe661b3dffefa766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61482445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a61a660f2733d0bbb74b5a4966370d317d680920758af00254184a3396067e`

```dockerfile
```

-	Layers:
	-	`sha256:d013c931b2bfab06dc97253e883dec067436294b51b16bbf39b04255d9df58fe`  
		Last Modified: Wed, 24 Dec 2025 08:17:24 GMT  
		Size: 61.5 MB (61455590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae1a26b69e7105e4e6c76e8a5d44d3793afa05432664fadb8bdfb2476a92888`  
		Last Modified: Wed, 24 Dec 2025 08:17:26 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:1ba7ab9783cd2b08a875077dc3c744b0dcbe7eb0f78ac354a1c7a658f5455749
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
$ docker pull odoo@sha256:69fcabd9ef3818440eb5300ae44e15076a77eda9925f8cd0641b24038dfeb4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680314103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbafce4c9a475e748d6033227380d8dbb8452876ec3eb4aa32db65fff6349d9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:57 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:13:57 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:14:07 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:14:08 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:14:08 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:14:08 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:15:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:15:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:15:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:15:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
USER odoo
# Wed, 24 Dec 2025 05:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:15:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f067bfe61f0cf0e3dc1268722b731044195fe086446a1547b64a0e687c3de52`  
		Last Modified: Wed, 24 Dec 2025 05:20:17 GMT  
		Size: 254.6 MB (254556968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd02c37bfe1dbfe524fe486baf03112d7b55551864232373bd232920c5643c`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 14.4 MB (14356622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735020f60fbf6f01a63f90f30d03345473ca0cb8a259e7335357d026d3e081e3`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 480.0 KB (479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0a262e7461c242b5ecc7365d62e32c0163031727c1c58c9324822a630ac48a`  
		Last Modified: Wed, 24 Dec 2025 05:20:20 GMT  
		Size: 381.2 MB (381193395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1914e0409c5edb8b81f4332fa9c2e97501607511829f0377255fc237ba8145`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d8b448bb52580a7f582939f6b94d89c337a8380a7649c6dc243d3401dfe074`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4febe640d26e3f3f4d2bfd850d54381e73689fcd1786a93a43887ae9cba200db`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865d3d125071e9c87ae911436047f6c7390f0fb242f2d7557995a818a9ee0ebb`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7417cac4a4176bb26bb15ccf9487458786cb85337e02a9c00bdab48103a663f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bc676acd8ca48973d99b8a456b39b23806b6de12271e89fbe0b2520b00e986`

```dockerfile
```

-	Layers:
	-	`sha256:4f1b46c60e9d2de606480240d70d872699b7fd384ca071995f168e6db8ba1367`  
		Last Modified: Wed, 24 Dec 2025 08:12:44 GMT  
		Size: 61.4 MB (61447207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7534f0d47ac70ab1a721326b60aa1adbe6116b081ca7eb9cbecb66b51f29df`  
		Last Modified: Wed, 24 Dec 2025 08:12:41 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e5df1eca650338a075257be65588d231d5b639cfc849a4b9849d361b6d082c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.7 MB (676695982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fb9d6c9a921c4c94d4c3c31831e32dd2cd51d2dd4b1b6a33253e57f2f6fa35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:39 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:39 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:51 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:13:51 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:51 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:14:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:52 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c6c4dd8728629dfae9e972f8ad8200102f169f31cc273197580c0df398d2c`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 252.0 MB (251956836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47200be7646f67b6fe04696e7257e66ddc69ad8cadd76c4b19ee6ae5f20bc796`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 14.3 MB (14334194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79bfa30f5723be9e79db439947a5fe3dab3d6ac2634abfab763afade32c996`  
		Last Modified: Wed, 24 Dec 2025 05:16:53 GMT  
		Size: 480.1 KB (480065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce21bf8d032b6b646d7f47c62ecca84a86ca083e3d050577d03aeba70177ba`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 381.1 MB (381060489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2507a0d6031b7387eaa644ae34f2b53bf896fea848f4df728e0c92bb0b41cebc`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08872a033ec07b149067502136b5056d42392a18223988e1041cc9951d6e7a`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2718713fdb0ae6d9388052cdd478d811e8157227f4a20d247ac7db6262b6d844`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da2532b90c10e56d5b2c66066cb8525eb8c3e329a362e71ae5a3bd4038a764`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0f4aaf095b2a20b3c6189edeca52b8ece5446872f188494f18f6604aba3a8610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61481433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88399ec6273e8918c3cdfdb1788b09f226bebd77ea1724ae7fbe9a563943965`

```dockerfile
```

-	Layers:
	-	`sha256:059d7d9667e3b4cf8cfa9dfaed5ff580e0838a4aebe1968ce6537bcaff8b2c52`  
		Last Modified: Wed, 24 Dec 2025 08:14:58 GMT  
		Size: 61.5 MB (61454482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af647442717e509828bd3fb5a96b1b8c7314e47e0335b2c7c7106443b671c69`  
		Last Modified: Wed, 24 Dec 2025 08:14:59 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:413e69860943b9bc2436d7e78dd92622fecb385d40df7d8ebb61d2213b73473b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696487864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12add77d7cc557f5bfc6361d609b59ef214d5b528dfb5e881a8f06a11bf49a01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:15:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:15:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:15:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:15:49 GMT
ARG TARGETARCH=ppc64le
# Wed, 24 Dec 2025 05:15:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:18:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:18:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:18:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:18:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:18:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:18:43 GMT
USER odoo
# Wed, 24 Dec 2025 05:18:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceff955aaee4caea237c20301c4a641abd1ff7cfa6f6badf931348bced7c61`  
		Last Modified: Wed, 24 Dec 2025 05:24:12 GMT  
		Size: 265.1 MB (265086582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab10d7e4252bf6b6acd84ed974cacc270b5374aed5c27d772b77da5a47f225`  
		Last Modified: Wed, 24 Dec 2025 05:24:06 GMT  
		Size: 14.9 MB (14885504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fe9d208368cc6491c67f76d260cb902fa083d619b7564f06793764a524d6f6`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 480.1 KB (480063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b9f152040ff5ee81f990fd2fe15174344cede1c67e0ae8b945ecc59eff652`  
		Last Modified: Wed, 24 Dec 2025 05:24:20 GMT  
		Size: 381.7 MB (381728849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b5e36fc037f0bc056db0c3b276f596048d93e1342e5e083405ceb96746040`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7097faedda3790a63b4ef274315e4e2beaf1b27e11478e54fe86c129275e0f`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31a7d6d2708a987a0ffb311dca55261fccbdf3fc9b15d210bfe6868e2f53b8`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6698e9681d6cf1d0e2f2f3af566cee0641f73e9a24c35646543445fb81b6157`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ee9ad11576440ae7a606861084ffddee3db260c1868699dabe661b3dffefa766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61482445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a61a660f2733d0bbb74b5a4966370d317d680920758af00254184a3396067e`

```dockerfile
```

-	Layers:
	-	`sha256:d013c931b2bfab06dc97253e883dec067436294b51b16bbf39b04255d9df58fe`  
		Last Modified: Wed, 24 Dec 2025 08:17:24 GMT  
		Size: 61.5 MB (61455590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae1a26b69e7105e4e6c76e8a5d44d3793afa05432664fadb8bdfb2476a92888`  
		Last Modified: Wed, 24 Dec 2025 08:17:26 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20251222`

```console
$ docker pull odoo@sha256:1ba7ab9783cd2b08a875077dc3c744b0dcbe7eb0f78ac354a1c7a658f5455749
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20251222` - linux; amd64

```console
$ docker pull odoo@sha256:69fcabd9ef3818440eb5300ae44e15076a77eda9925f8cd0641b24038dfeb4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **680.3 MB (680314103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbafce4c9a475e748d6033227380d8dbb8452876ec3eb4aa32db65fff6349d9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:57 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:57 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:57 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:13:57 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:14:07 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:08 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:14:08 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:14:08 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:14:08 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:15:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:15:00 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:15:00 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:15:00 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:15:00 GMT
USER odoo
# Wed, 24 Dec 2025 05:15:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:15:00 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f067bfe61f0cf0e3dc1268722b731044195fe086446a1547b64a0e687c3de52`  
		Last Modified: Wed, 24 Dec 2025 05:20:17 GMT  
		Size: 254.6 MB (254556968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dd02c37bfe1dbfe524fe486baf03112d7b55551864232373bd232920c5643c`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 14.4 MB (14356622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735020f60fbf6f01a63f90f30d03345473ca0cb8a259e7335357d026d3e081e3`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 480.0 KB (479988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0a262e7461c242b5ecc7365d62e32c0163031727c1c58c9324822a630ac48a`  
		Last Modified: Wed, 24 Dec 2025 05:20:20 GMT  
		Size: 381.2 MB (381193395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1914e0409c5edb8b81f4332fa9c2e97501607511829f0377255fc237ba8145`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d8b448bb52580a7f582939f6b94d89c337a8380a7649c6dc243d3401dfe074`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4febe640d26e3f3f4d2bfd850d54381e73689fcd1786a93a43887ae9cba200db`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865d3d125071e9c87ae911436047f6c7390f0fb242f2d7557995a818a9ee0ebb`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:7417cac4a4176bb26bb15ccf9487458786cb85337e02a9c00bdab48103a663f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61474006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bc676acd8ca48973d99b8a456b39b23806b6de12271e89fbe0b2520b00e986`

```dockerfile
```

-	Layers:
	-	`sha256:4f1b46c60e9d2de606480240d70d872699b7fd384ca071995f168e6db8ba1367`  
		Last Modified: Wed, 24 Dec 2025 08:12:44 GMT  
		Size: 61.4 MB (61447207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7534f0d47ac70ab1a721326b60aa1adbe6116b081ca7eb9cbecb66b51f29df`  
		Last Modified: Wed, 24 Dec 2025 08:12:41 GMT  
		Size: 26.8 KB (26799 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251222` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:e5df1eca650338a075257be65588d231d5b639cfc849a4b9849d361b6d082c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.7 MB (676695982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fb9d6c9a921c4c94d4c3c31831e32dd2cd51d2dd4b1b6a33253e57f2f6fa35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:39 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:39 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:39 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:39 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:39 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:50 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:51 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:51 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:13:51 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:51 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:14:52 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:52 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:53 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42c6c4dd8728629dfae9e972f8ad8200102f169f31cc273197580c0df398d2c`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 252.0 MB (251956836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47200be7646f67b6fe04696e7257e66ddc69ad8cadd76c4b19ee6ae5f20bc796`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 14.3 MB (14334194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e79bfa30f5723be9e79db439947a5fe3dab3d6ac2634abfab763afade32c996`  
		Last Modified: Wed, 24 Dec 2025 05:16:53 GMT  
		Size: 480.1 KB (480065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce21bf8d032b6b646d7f47c62ecca84a86ca083e3d050577d03aeba70177ba`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 381.1 MB (381060489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2507a0d6031b7387eaa644ae34f2b53bf896fea848f4df728e0c92bb0b41cebc`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08872a033ec07b149067502136b5056d42392a18223988e1041cc9951d6e7a`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2718713fdb0ae6d9388052cdd478d811e8157227f4a20d247ac7db6262b6d844`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5da2532b90c10e56d5b2c66066cb8525eb8c3e329a362e71ae5a3bd4038a764`  
		Last Modified: Wed, 24 Dec 2025 05:17:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:0f4aaf095b2a20b3c6189edeca52b8ece5446872f188494f18f6604aba3a8610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61481433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88399ec6273e8918c3cdfdb1788b09f226bebd77ea1724ae7fbe9a563943965`

```dockerfile
```

-	Layers:
	-	`sha256:059d7d9667e3b4cf8cfa9dfaed5ff580e0838a4aebe1968ce6537bcaff8b2c52`  
		Last Modified: Wed, 24 Dec 2025 08:14:58 GMT  
		Size: 61.5 MB (61454482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af647442717e509828bd3fb5a96b1b8c7314e47e0335b2c7c7106443b671c69`  
		Last Modified: Wed, 24 Dec 2025 08:14:59 GMT  
		Size: 27.0 KB (26951 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20251222` - linux; ppc64le

```console
$ docker pull odoo@sha256:413e69860943b9bc2436d7e78dd92622fecb385d40df7d8ebb61d2213b73473b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.5 MB (696487864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12add77d7cc557f5bfc6361d609b59ef214d5b528dfb5e881a8f06a11bf49a01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:15:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:15:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:15:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:15:49 GMT
ARG TARGETARCH=ppc64le
# Wed, 24 Dec 2025 05:15:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
ENV ODOO_VERSION=18.0
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
# Wed, 24 Dec 2025 05:18:40 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:18:41 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=fc71ac3c039e84f1aa33ab2bf2a3922463eee889
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:18:42 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:18:42 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:18:42 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:18:43 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:18:43 GMT
USER odoo
# Wed, 24 Dec 2025 05:18:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:43 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceff955aaee4caea237c20301c4a641abd1ff7cfa6f6badf931348bced7c61`  
		Last Modified: Wed, 24 Dec 2025 05:24:12 GMT  
		Size: 265.1 MB (265086582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab10d7e4252bf6b6acd84ed974cacc270b5374aed5c27d772b77da5a47f225`  
		Last Modified: Wed, 24 Dec 2025 05:24:06 GMT  
		Size: 14.9 MB (14885504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fe9d208368cc6491c67f76d260cb902fa083d619b7564f06793764a524d6f6`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 480.1 KB (480063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1b9f152040ff5ee81f990fd2fe15174344cede1c67e0ae8b945ecc59eff652`  
		Last Modified: Wed, 24 Dec 2025 05:24:20 GMT  
		Size: 381.7 MB (381728849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b5e36fc037f0bc056db0c3b276f596048d93e1342e5e083405ceb96746040`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7097faedda3790a63b4ef274315e4e2beaf1b27e11478e54fe86c129275e0f`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd31a7d6d2708a987a0ffb311dca55261fccbdf3fc9b15d210bfe6868e2f53b8`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6698e9681d6cf1d0e2f2f3af566cee0641f73e9a24c35646543445fb81b6157`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:ee9ad11576440ae7a606861084ffddee3db260c1868699dabe661b3dffefa766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61482445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a61a660f2733d0bbb74b5a4966370d317d680920758af00254184a3396067e`

```dockerfile
```

-	Layers:
	-	`sha256:d013c931b2bfab06dc97253e883dec067436294b51b16bbf39b04255d9df58fe`  
		Last Modified: Wed, 24 Dec 2025 08:17:24 GMT  
		Size: 61.5 MB (61455590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae1a26b69e7105e4e6c76e8a5d44d3793afa05432664fadb8bdfb2476a92888`  
		Last Modified: Wed, 24 Dec 2025 08:17:26 GMT  
		Size: 26.9 KB (26855 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:34f57be597c45eebed1f0eeb71757a9d8eed6b7c512245632dfa2c9687968f2e
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
$ docker pull odoo@sha256:08aa92bc7870172b3d91f002176568ca77706551db21e613576e2d38940dcd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691610329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201187faf86c74219018efd5f8ddd842dce0fcfa856e1c4ec2e8c15a7d249256`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:14:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:14:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:14:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:14:07 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:14:07 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:15:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:15:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:15:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
USER odoo
# Wed, 24 Dec 2025 05:15:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:15:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d399bf55108070ede124f2b7dff4bdc8af4f215bd8e72b8eae96f478b6d5739`  
		Last Modified: Wed, 24 Dec 2025 05:18:02 GMT  
		Size: 254.6 MB (254557404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aec2b8a5a5314a546374dab3c5991bd5b52a10383c6f378bb218895a773bc0`  
		Last Modified: Wed, 24 Dec 2025 05:17:41 GMT  
		Size: 14.4 MB (14356532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c1cbc7fdcd4186ad9db8a56a6d1fd8358de8d8603182d8bb655423c69279d`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b4a7170802a2d146f763da24338d4452ad9861320ff7057e242a5f65d76b0`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 392.5 MB (392489279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1914e0409c5edb8b81f4332fa9c2e97501607511829f0377255fc237ba8145`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877e9f3f0a7705574fe2ab88ef16eb8f11609a6bf947e262bed38fa1f18e9c9`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1409ffa7fdb7d28110f668f3c753b63fb6b350e69c68523207614da134f34548`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9b605776b0b05d4f9c85a9572293b4768f4c26cb7f27175e85849a2026bbd`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:8ddba16ab762dc9ae22b940586262ff88b4c4897e76d2d5013101a3489fc33fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d504e9f3934eb745e90f33f873f9ed66f4b9960166c297725d7b00f6881a28ab`

```dockerfile
```

-	Layers:
	-	`sha256:92cccce5042f80212102f977ba0c3baba0d1d87b53a3490369a865c7e9f73f79`  
		Last Modified: Wed, 24 Dec 2025 08:13:01 GMT  
		Size: 68.9 MB (68856434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807747a1977978ba36c78913b6d9224c3cc37bb26805543e5075035a669c6f6`  
		Last Modified: Wed, 24 Dec 2025 08:13:03 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5879bea6770c7a87a1d9745cdb1273bde37899593298cef325916a09cd5a4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687957441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661b3b1a11bbf657c1138b72dbf70df47b84798bb7435f215e268a21911b0a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:38 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:38 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:14:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cad8acae719017b1b6f767064e1492f4c0ab45ef7b8c03320a11aef620f595`  
		Last Modified: Wed, 24 Dec 2025 05:18:13 GMT  
		Size: 252.0 MB (251957083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf6cb470b694b5569de0ce84d37c5bc103be710851386ca7313a687a1472cd5`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 14.3 MB (14334124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0bec9008867c7f0203ad6107b07b796d95fa3fcd57b7a70e8337565e9deb30`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcaa65ef14d78b5838f01db6cc18bf5e5c3657131f410a97093608f4999d72f`  
		Last Modified: Wed, 24 Dec 2025 05:18:52 GMT  
		Size: 392.3 MB (392321747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac84c235a987dd0a4718cb243a5dad2f8ad02ce78e30a5e78900372a3f0e9e61`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed3d0fdba17fdd66b92aeb88a76cde74a1bf194e245f4c90993a7cb22d46a`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b56f31ae57c02d9c4d8064af099b3f72c4841a1d6f71fa9f6d73873e4762f`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f122b9e7d38d4cd515b4b57785035924c2b46a55f545e13aca076e8d45b7543e`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:f07d4cd5ce9f4d09f49f422a814bc5df3afd74db5258b79360d2ac06ed709789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04142d5ff0159bfe56dd6b94a10222118d7a979a88a5462ea0a9e1be92a55c4`

```dockerfile
```

-	Layers:
	-	`sha256:a26646decd391b6962ae8d4e758b040a445849bc30246d930d12249ff8098ee5`  
		Last Modified: Wed, 24 Dec 2025 08:15:54 GMT  
		Size: 68.9 MB (68863721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7148824d0508577205414858a15b9d7175c145702ed7b28acf87a08e0711993f`  
		Last Modified: Wed, 24 Dec 2025 08:15:56 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:c3cd2fc05701e652dfc0a81e5ebf71f3921506ff1e9ebba58ee2e3de310b8cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707784246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfff713b8341f32c85fa6007defcbc00b1667728bbb7a4a5f38a11075484803c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:15:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:15:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:15:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:15:49 GMT
ARG TARGETARCH=ppc64le
# Wed, 24 Dec 2025 05:15:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:18:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:18:52 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:18:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:18:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:18:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:18:54 GMT
USER odoo
# Wed, 24 Dec 2025 05:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceff955aaee4caea237c20301c4a641abd1ff7cfa6f6badf931348bced7c61`  
		Last Modified: Wed, 24 Dec 2025 05:24:12 GMT  
		Size: 265.1 MB (265086582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab10d7e4252bf6b6acd84ed974cacc270b5374aed5c27d772b77da5a47f225`  
		Last Modified: Wed, 24 Dec 2025 05:24:06 GMT  
		Size: 14.9 MB (14885504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fe9d208368cc6491c67f76d260cb902fa083d619b7564f06793764a524d6f6`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 480.1 KB (480063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4578fffcfa426a37437ab2610b94c4d4e2934d48ff2b6d2c3c6ad4ecafde47dd`  
		Last Modified: Wed, 24 Dec 2025 05:26:11 GMT  
		Size: 393.0 MB (393025229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693981ab22a58d54cac34160b7a573d141198c14522f5bc63255b33ef75767db`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a788826e40f5d2f4025f90619f3e9be23a6545f64ba262260a9127ae71b2e`  
		Last Modified: Wed, 24 Dec 2025 05:24:58 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06e65979d75d6b3fdfb2c416b755606403f0913055fc0c8b3db20815c6ca1c`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f75f3d5dd086fa9bf349489064eedd3120201f15e2d808fc566aa7cccf0563`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:ea40ea5ad7f7ea928d9f7f325909cdd7e278fa81f5ab052daeffe1b61b2f7506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1249ad8f326e8ddfed0165a27ae64cb2842302769930e4d8980320d570411bfa`

```dockerfile
```

-	Layers:
	-	`sha256:85478b42735ce2b009c4cd3dbafaee3367afc08e5c0c58194a688614e0cffa6e`  
		Last Modified: Wed, 24 Dec 2025 08:18:51 GMT  
		Size: 68.9 MB (68864823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca7555814bbc2459b1a5962d10254c8d73787e6aae0d7a48001af712438caf8`  
		Last Modified: Wed, 24 Dec 2025 08:18:52 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:34f57be597c45eebed1f0eeb71757a9d8eed6b7c512245632dfa2c9687968f2e
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
$ docker pull odoo@sha256:08aa92bc7870172b3d91f002176568ca77706551db21e613576e2d38940dcd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691610329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201187faf86c74219018efd5f8ddd842dce0fcfa856e1c4ec2e8c15a7d249256`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:14:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:14:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:14:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:14:07 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:14:07 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:15:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:15:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:15:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
USER odoo
# Wed, 24 Dec 2025 05:15:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:15:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d399bf55108070ede124f2b7dff4bdc8af4f215bd8e72b8eae96f478b6d5739`  
		Last Modified: Wed, 24 Dec 2025 05:18:02 GMT  
		Size: 254.6 MB (254557404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aec2b8a5a5314a546374dab3c5991bd5b52a10383c6f378bb218895a773bc0`  
		Last Modified: Wed, 24 Dec 2025 05:17:41 GMT  
		Size: 14.4 MB (14356532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c1cbc7fdcd4186ad9db8a56a6d1fd8358de8d8603182d8bb655423c69279d`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b4a7170802a2d146f763da24338d4452ad9861320ff7057e242a5f65d76b0`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 392.5 MB (392489279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1914e0409c5edb8b81f4332fa9c2e97501607511829f0377255fc237ba8145`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877e9f3f0a7705574fe2ab88ef16eb8f11609a6bf947e262bed38fa1f18e9c9`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1409ffa7fdb7d28110f668f3c753b63fb6b350e69c68523207614da134f34548`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9b605776b0b05d4f9c85a9572293b4768f4c26cb7f27175e85849a2026bbd`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:8ddba16ab762dc9ae22b940586262ff88b4c4897e76d2d5013101a3489fc33fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d504e9f3934eb745e90f33f873f9ed66f4b9960166c297725d7b00f6881a28ab`

```dockerfile
```

-	Layers:
	-	`sha256:92cccce5042f80212102f977ba0c3baba0d1d87b53a3490369a865c7e9f73f79`  
		Last Modified: Wed, 24 Dec 2025 08:13:01 GMT  
		Size: 68.9 MB (68856434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807747a1977978ba36c78913b6d9224c3cc37bb26805543e5075035a669c6f6`  
		Last Modified: Wed, 24 Dec 2025 08:13:03 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5879bea6770c7a87a1d9745cdb1273bde37899593298cef325916a09cd5a4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687957441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661b3b1a11bbf657c1138b72dbf70df47b84798bb7435f215e268a21911b0a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:38 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:38 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:14:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cad8acae719017b1b6f767064e1492f4c0ab45ef7b8c03320a11aef620f595`  
		Last Modified: Wed, 24 Dec 2025 05:18:13 GMT  
		Size: 252.0 MB (251957083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf6cb470b694b5569de0ce84d37c5bc103be710851386ca7313a687a1472cd5`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 14.3 MB (14334124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0bec9008867c7f0203ad6107b07b796d95fa3fcd57b7a70e8337565e9deb30`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcaa65ef14d78b5838f01db6cc18bf5e5c3657131f410a97093608f4999d72f`  
		Last Modified: Wed, 24 Dec 2025 05:18:52 GMT  
		Size: 392.3 MB (392321747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac84c235a987dd0a4718cb243a5dad2f8ad02ce78e30a5e78900372a3f0e9e61`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed3d0fdba17fdd66b92aeb88a76cde74a1bf194e245f4c90993a7cb22d46a`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b56f31ae57c02d9c4d8064af099b3f72c4841a1d6f71fa9f6d73873e4762f`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f122b9e7d38d4cd515b4b57785035924c2b46a55f545e13aca076e8d45b7543e`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f07d4cd5ce9f4d09f49f422a814bc5df3afd74db5258b79360d2ac06ed709789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04142d5ff0159bfe56dd6b94a10222118d7a979a88a5462ea0a9e1be92a55c4`

```dockerfile
```

-	Layers:
	-	`sha256:a26646decd391b6962ae8d4e758b040a445849bc30246d930d12249ff8098ee5`  
		Last Modified: Wed, 24 Dec 2025 08:15:54 GMT  
		Size: 68.9 MB (68863721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7148824d0508577205414858a15b9d7175c145702ed7b28acf87a08e0711993f`  
		Last Modified: Wed, 24 Dec 2025 08:15:56 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:c3cd2fc05701e652dfc0a81e5ebf71f3921506ff1e9ebba58ee2e3de310b8cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707784246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfff713b8341f32c85fa6007defcbc00b1667728bbb7a4a5f38a11075484803c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:15:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:15:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:15:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:15:49 GMT
ARG TARGETARCH=ppc64le
# Wed, 24 Dec 2025 05:15:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:18:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:18:52 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:18:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:18:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:18:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:18:54 GMT
USER odoo
# Wed, 24 Dec 2025 05:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceff955aaee4caea237c20301c4a641abd1ff7cfa6f6badf931348bced7c61`  
		Last Modified: Wed, 24 Dec 2025 05:24:12 GMT  
		Size: 265.1 MB (265086582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab10d7e4252bf6b6acd84ed974cacc270b5374aed5c27d772b77da5a47f225`  
		Last Modified: Wed, 24 Dec 2025 05:24:06 GMT  
		Size: 14.9 MB (14885504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fe9d208368cc6491c67f76d260cb902fa083d619b7564f06793764a524d6f6`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 480.1 KB (480063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4578fffcfa426a37437ab2610b94c4d4e2934d48ff2b6d2c3c6ad4ecafde47dd`  
		Last Modified: Wed, 24 Dec 2025 05:26:11 GMT  
		Size: 393.0 MB (393025229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693981ab22a58d54cac34160b7a573d141198c14522f5bc63255b33ef75767db`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a788826e40f5d2f4025f90619f3e9be23a6545f64ba262260a9127ae71b2e`  
		Last Modified: Wed, 24 Dec 2025 05:24:58 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06e65979d75d6b3fdfb2c416b755606403f0913055fc0c8b3db20815c6ca1c`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f75f3d5dd086fa9bf349489064eedd3120201f15e2d808fc566aa7cccf0563`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ea40ea5ad7f7ea928d9f7f325909cdd7e278fa81f5ab052daeffe1b61b2f7506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1249ad8f326e8ddfed0165a27ae64cb2842302769930e4d8980320d570411bfa`

```dockerfile
```

-	Layers:
	-	`sha256:85478b42735ce2b009c4cd3dbafaee3367afc08e5c0c58194a688614e0cffa6e`  
		Last Modified: Wed, 24 Dec 2025 08:18:51 GMT  
		Size: 68.9 MB (68864823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca7555814bbc2459b1a5962d10254c8d73787e6aae0d7a48001af712438caf8`  
		Last Modified: Wed, 24 Dec 2025 08:18:52 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20251222`

```console
$ docker pull odoo@sha256:34f57be597c45eebed1f0eeb71757a9d8eed6b7c512245632dfa2c9687968f2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20251222` - linux; amd64

```console
$ docker pull odoo@sha256:08aa92bc7870172b3d91f002176568ca77706551db21e613576e2d38940dcd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691610329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201187faf86c74219018efd5f8ddd842dce0fcfa856e1c4ec2e8c15a7d249256`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:14:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:14:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:14:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:14:07 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:14:07 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:15:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:15:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:15:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
USER odoo
# Wed, 24 Dec 2025 05:15:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:15:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d399bf55108070ede124f2b7dff4bdc8af4f215bd8e72b8eae96f478b6d5739`  
		Last Modified: Wed, 24 Dec 2025 05:18:02 GMT  
		Size: 254.6 MB (254557404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aec2b8a5a5314a546374dab3c5991bd5b52a10383c6f378bb218895a773bc0`  
		Last Modified: Wed, 24 Dec 2025 05:17:41 GMT  
		Size: 14.4 MB (14356532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c1cbc7fdcd4186ad9db8a56a6d1fd8358de8d8603182d8bb655423c69279d`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b4a7170802a2d146f763da24338d4452ad9861320ff7057e242a5f65d76b0`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 392.5 MB (392489279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1914e0409c5edb8b81f4332fa9c2e97501607511829f0377255fc237ba8145`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877e9f3f0a7705574fe2ab88ef16eb8f11609a6bf947e262bed38fa1f18e9c9`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1409ffa7fdb7d28110f668f3c753b63fb6b350e69c68523207614da134f34548`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9b605776b0b05d4f9c85a9572293b4768f4c26cb7f27175e85849a2026bbd`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:8ddba16ab762dc9ae22b940586262ff88b4c4897e76d2d5013101a3489fc33fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d504e9f3934eb745e90f33f873f9ed66f4b9960166c297725d7b00f6881a28ab`

```dockerfile
```

-	Layers:
	-	`sha256:92cccce5042f80212102f977ba0c3baba0d1d87b53a3490369a865c7e9f73f79`  
		Last Modified: Wed, 24 Dec 2025 08:13:01 GMT  
		Size: 68.9 MB (68856434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807747a1977978ba36c78913b6d9224c3cc37bb26805543e5075035a669c6f6`  
		Last Modified: Wed, 24 Dec 2025 08:13:03 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251222` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5879bea6770c7a87a1d9745cdb1273bde37899593298cef325916a09cd5a4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687957441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661b3b1a11bbf657c1138b72dbf70df47b84798bb7435f215e268a21911b0a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:38 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:38 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:14:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cad8acae719017b1b6f767064e1492f4c0ab45ef7b8c03320a11aef620f595`  
		Last Modified: Wed, 24 Dec 2025 05:18:13 GMT  
		Size: 252.0 MB (251957083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf6cb470b694b5569de0ce84d37c5bc103be710851386ca7313a687a1472cd5`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 14.3 MB (14334124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0bec9008867c7f0203ad6107b07b796d95fa3fcd57b7a70e8337565e9deb30`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcaa65ef14d78b5838f01db6cc18bf5e5c3657131f410a97093608f4999d72f`  
		Last Modified: Wed, 24 Dec 2025 05:18:52 GMT  
		Size: 392.3 MB (392321747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac84c235a987dd0a4718cb243a5dad2f8ad02ce78e30a5e78900372a3f0e9e61`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed3d0fdba17fdd66b92aeb88a76cde74a1bf194e245f4c90993a7cb22d46a`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b56f31ae57c02d9c4d8064af099b3f72c4841a1d6f71fa9f6d73873e4762f`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f122b9e7d38d4cd515b4b57785035924c2b46a55f545e13aca076e8d45b7543e`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:f07d4cd5ce9f4d09f49f422a814bc5df3afd74db5258b79360d2ac06ed709789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04142d5ff0159bfe56dd6b94a10222118d7a979a88a5462ea0a9e1be92a55c4`

```dockerfile
```

-	Layers:
	-	`sha256:a26646decd391b6962ae8d4e758b040a445849bc30246d930d12249ff8098ee5`  
		Last Modified: Wed, 24 Dec 2025 08:15:54 GMT  
		Size: 68.9 MB (68863721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7148824d0508577205414858a15b9d7175c145702ed7b28acf87a08e0711993f`  
		Last Modified: Wed, 24 Dec 2025 08:15:56 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20251222` - linux; ppc64le

```console
$ docker pull odoo@sha256:c3cd2fc05701e652dfc0a81e5ebf71f3921506ff1e9ebba58ee2e3de310b8cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707784246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfff713b8341f32c85fa6007defcbc00b1667728bbb7a4a5f38a11075484803c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:15:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:15:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:15:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:15:49 GMT
ARG TARGETARCH=ppc64le
# Wed, 24 Dec 2025 05:15:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:18:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:18:52 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:18:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:18:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:18:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:18:54 GMT
USER odoo
# Wed, 24 Dec 2025 05:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceff955aaee4caea237c20301c4a641abd1ff7cfa6f6badf931348bced7c61`  
		Last Modified: Wed, 24 Dec 2025 05:24:12 GMT  
		Size: 265.1 MB (265086582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab10d7e4252bf6b6acd84ed974cacc270b5374aed5c27d772b77da5a47f225`  
		Last Modified: Wed, 24 Dec 2025 05:24:06 GMT  
		Size: 14.9 MB (14885504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fe9d208368cc6491c67f76d260cb902fa083d619b7564f06793764a524d6f6`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 480.1 KB (480063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4578fffcfa426a37437ab2610b94c4d4e2934d48ff2b6d2c3c6ad4ecafde47dd`  
		Last Modified: Wed, 24 Dec 2025 05:26:11 GMT  
		Size: 393.0 MB (393025229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693981ab22a58d54cac34160b7a573d141198c14522f5bc63255b33ef75767db`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a788826e40f5d2f4025f90619f3e9be23a6545f64ba262260a9127ae71b2e`  
		Last Modified: Wed, 24 Dec 2025 05:24:58 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06e65979d75d6b3fdfb2c416b755606403f0913055fc0c8b3db20815c6ca1c`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f75f3d5dd086fa9bf349489064eedd3120201f15e2d808fc566aa7cccf0563`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20251222` - unknown; unknown

```console
$ docker pull odoo@sha256:ea40ea5ad7f7ea928d9f7f325909cdd7e278fa81f5ab052daeffe1b61b2f7506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1249ad8f326e8ddfed0165a27ae64cb2842302769930e4d8980320d570411bfa`

```dockerfile
```

-	Layers:
	-	`sha256:85478b42735ce2b009c4cd3dbafaee3367afc08e5c0c58194a688614e0cffa6e`  
		Last Modified: Wed, 24 Dec 2025 08:18:51 GMT  
		Size: 68.9 MB (68864823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca7555814bbc2459b1a5962d10254c8d73787e6aae0d7a48001af712438caf8`  
		Last Modified: Wed, 24 Dec 2025 08:18:52 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:34f57be597c45eebed1f0eeb71757a9d8eed6b7c512245632dfa2c9687968f2e
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
$ docker pull odoo@sha256:08aa92bc7870172b3d91f002176568ca77706551db21e613576e2d38940dcd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **691.6 MB (691610329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201187faf86c74219018efd5f8ddd842dce0fcfa856e1c4ec2e8c15a7d249256`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:14:07 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:14:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:14:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:14:07 GMT
ARG TARGETARCH=amd64
# Wed, 24 Dec 2025 05:14:07 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:14:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:14:20 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:15:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:15:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:15:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:15:20 GMT
USER odoo
# Wed, 24 Dec 2025 05:15:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:15:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d399bf55108070ede124f2b7dff4bdc8af4f215bd8e72b8eae96f478b6d5739`  
		Last Modified: Wed, 24 Dec 2025 05:18:02 GMT  
		Size: 254.6 MB (254557404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aec2b8a5a5314a546374dab3c5991bd5b52a10383c6f378bb218895a773bc0`  
		Last Modified: Wed, 24 Dec 2025 05:17:41 GMT  
		Size: 14.4 MB (14356532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c1cbc7fdcd4186ad9db8a56a6d1fd8358de8d8603182d8bb655423c69279d`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b4a7170802a2d146f763da24338d4452ad9861320ff7057e242a5f65d76b0`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 392.5 MB (392489279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1914e0409c5edb8b81f4332fa9c2e97501607511829f0377255fc237ba8145`  
		Last Modified: Wed, 24 Dec 2025 05:17:10 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8877e9f3f0a7705574fe2ab88ef16eb8f11609a6bf947e262bed38fa1f18e9c9`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1409ffa7fdb7d28110f668f3c753b63fb6b350e69c68523207614da134f34548`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f9b605776b0b05d4f9c85a9572293b4768f4c26cb7f27175e85849a2026bbd`  
		Last Modified: Wed, 24 Dec 2025 05:17:40 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:8ddba16ab762dc9ae22b940586262ff88b4c4897e76d2d5013101a3489fc33fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68883527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d504e9f3934eb745e90f33f873f9ed66f4b9960166c297725d7b00f6881a28ab`

```dockerfile
```

-	Layers:
	-	`sha256:92cccce5042f80212102f977ba0c3baba0d1d87b53a3490369a865c7e9f73f79`  
		Last Modified: Wed, 24 Dec 2025 08:13:01 GMT  
		Size: 68.9 MB (68856434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1807747a1977978ba36c78913b6d9224c3cc37bb26805543e5075035a669c6f6`  
		Last Modified: Wed, 24 Dec 2025 08:13:03 GMT  
		Size: 27.1 KB (27093 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b5879bea6770c7a87a1d9745cdb1273bde37899593298cef325916a09cd5a4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.0 MB (687957441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661b3b1a11bbf657c1138b72dbf70df47b84798bb7435f215e268a21911b0a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:13:38 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:13:38 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:13:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:13:38 GMT
ARG TARGETARCH=arm64
# Wed, 24 Dec 2025 05:13:38 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:13:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:13:49 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:13:49 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:14:54 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:14:54 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:14:55 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:14:55 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:14:55 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:14:55 GMT
USER odoo
# Wed, 24 Dec 2025 05:14:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:55 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cad8acae719017b1b6f767064e1492f4c0ab45ef7b8c03320a11aef620f595`  
		Last Modified: Wed, 24 Dec 2025 05:18:13 GMT  
		Size: 252.0 MB (251957083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf6cb470b694b5569de0ce84d37c5bc103be710851386ca7313a687a1472cd5`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 14.3 MB (14334124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0bec9008867c7f0203ad6107b07b796d95fa3fcd57b7a70e8337565e9deb30`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 480.1 KB (480085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcaa65ef14d78b5838f01db6cc18bf5e5c3657131f410a97093608f4999d72f`  
		Last Modified: Wed, 24 Dec 2025 05:18:52 GMT  
		Size: 392.3 MB (392321747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac84c235a987dd0a4718cb243a5dad2f8ad02ce78e30a5e78900372a3f0e9e61`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142ed3d0fdba17fdd66b92aeb88a76cde74a1bf194e245f4c90993a7cb22d46a`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b56f31ae57c02d9c4d8064af099b3f72c4841a1d6f71fa9f6d73873e4762f`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f122b9e7d38d4cd515b4b57785035924c2b46a55f545e13aca076e8d45b7543e`  
		Last Modified: Wed, 24 Dec 2025 05:17:49 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f07d4cd5ce9f4d09f49f422a814bc5df3afd74db5258b79360d2ac06ed709789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68890977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04142d5ff0159bfe56dd6b94a10222118d7a979a88a5462ea0a9e1be92a55c4`

```dockerfile
```

-	Layers:
	-	`sha256:a26646decd391b6962ae8d4e758b040a445849bc30246d930d12249ff8098ee5`  
		Last Modified: Wed, 24 Dec 2025 08:15:54 GMT  
		Size: 68.9 MB (68863721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7148824d0508577205414858a15b9d7175c145702ed7b28acf87a08e0711993f`  
		Last Modified: Wed, 24 Dec 2025 08:15:56 GMT  
		Size: 27.3 KB (27256 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:c3cd2fc05701e652dfc0a81e5ebf71f3921506ff1e9ebba58ee2e3de310b8cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.8 MB (707784246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfff713b8341f32c85fa6007defcbc00b1667728bbb7a4a5f38a11075484803c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Wed, 24 Dec 2025 05:15:49 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 24 Dec 2025 05:15:49 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 24 Dec 2025 05:15:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 24 Dec 2025 05:15:49 GMT
ARG TARGETARCH=ppc64le
# Wed, 24 Dec 2025 05:15:49 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 24 Dec 2025 05:16:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 24 Dec 2025 05:16:05 GMT
ENV ODOO_VERSION=19.0
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_RELEASE=20251222
# Wed, 24 Dec 2025 05:16:05 GMT
ARG ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
# Wed, 24 Dec 2025 05:18:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 24 Dec 2025 05:18:52 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251222 ODOO_SHA=9e8816c0c76e1e89af884ce235032fb071d99510
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 24 Dec 2025 05:18:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 24 Dec 2025 05:18:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 24 Dec 2025 05:18:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 24 Dec 2025 05:18:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 24 Dec 2025 05:18:54 GMT
USER odoo
# Wed, 24 Dec 2025 05:18:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ceff955aaee4caea237c20301c4a641abd1ff7cfa6f6badf931348bced7c61`  
		Last Modified: Wed, 24 Dec 2025 05:24:12 GMT  
		Size: 265.1 MB (265086582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ab10d7e4252bf6b6acd84ed974cacc270b5374aed5c27d772b77da5a47f225`  
		Last Modified: Wed, 24 Dec 2025 05:24:06 GMT  
		Size: 14.9 MB (14885504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fe9d208368cc6491c67f76d260cb902fa083d619b7564f06793764a524d6f6`  
		Last Modified: Wed, 24 Dec 2025 05:24:05 GMT  
		Size: 480.1 KB (480063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4578fffcfa426a37437ab2610b94c4d4e2934d48ff2b6d2c3c6ad4ecafde47dd`  
		Last Modified: Wed, 24 Dec 2025 05:26:11 GMT  
		Size: 393.0 MB (393025229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693981ab22a58d54cac34160b7a573d141198c14522f5bc63255b33ef75767db`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912a788826e40f5d2f4025f90619f3e9be23a6545f64ba262260a9127ae71b2e`  
		Last Modified: Wed, 24 Dec 2025 05:24:58 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d06e65979d75d6b3fdfb2c416b755606403f0913055fc0c8b3db20815c6ca1c`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f75f3d5dd086fa9bf349489064eedd3120201f15e2d808fc566aa7cccf0563`  
		Last Modified: Wed, 24 Dec 2025 05:24:53 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:ea40ea5ad7f7ea928d9f7f325909cdd7e278fa81f5ab052daeffe1b61b2f7506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68891978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1249ad8f326e8ddfed0165a27ae64cb2842302769930e4d8980320d570411bfa`

```dockerfile
```

-	Layers:
	-	`sha256:85478b42735ce2b009c4cd3dbafaee3367afc08e5c0c58194a688614e0cffa6e`  
		Last Modified: Wed, 24 Dec 2025 08:18:51 GMT  
		Size: 68.9 MB (68864823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca7555814bbc2459b1a5962d10254c8d73787e6aae0d7a48001af712438caf8`  
		Last Modified: Wed, 24 Dec 2025 08:18:52 GMT  
		Size: 27.2 KB (27155 bytes)  
		MIME: application/vnd.in-toto+json
