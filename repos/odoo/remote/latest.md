## `odoo:latest`

```console
$ docker pull odoo@sha256:15a1e852727e2e9952a1e8b138f5bd0a2234c012684f4fff6124563a54e8bd0f
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
$ docker pull odoo@sha256:36da9378d08bfec1f42f975ffa53bd2e10928b7ecf8a778806b74b1994d298d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.3 MB (678341469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2e59f5c2b599195f9377997858b3c78588120f358e991cc89e9fa4c591fbb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=amd64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78717648042f04d1bc55296335cdfd48309babd6d29ee245d8994c9eb6bfaa2e`  
		Last Modified: Wed, 01 Oct 2025 16:13:24 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e662152c908a8e728eefe42676ce8f7a1c2c98bc14462d1915f0acda428398`  
		Last Modified: Wed, 01 Oct 2025 05:10:08 GMT  
		Size: 14.3 MB (14339116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e8b0d104998320a5f4e08c7d94523fa8fd70bdae5ace26960207267cc45d4`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 480.0 KB (479985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c290470ff834642941deb9bfd3cb197eaa3bfad5ee4e190334c647ea7189c72`  
		Last Modified: Wed, 01 Oct 2025 16:13:53 GMT  
		Size: 379.2 MB (379238542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67cf444b63eb2547b2204d181e763a34da5f6068d4ca21659793e60010e1661`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 703.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581327cc3459dbcd9847df406a552ad459447a4597e980c608ff70c5d205e28`  
		Last Modified: Tue, 30 Sep 2025 17:58:09 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b6f8015343e394ad0a2efc552051c9f9c6853292461b15b2c598f2edd8b6d`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123b01163d7f3be00d9fcb082594052820d6997b08b311d209bfe0df01b99302`  
		Last Modified: Tue, 30 Sep 2025 17:58:10 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f800547caf96d0a22ada9a6a31715bbdcca06d9d9b0c92cca9a0e97775916ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67733546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add45288c9f74d7603471ef18cbc35065bf010e42ea23ab850930f04cae3e4a7`

```dockerfile
```

-	Layers:
	-	`sha256:84ff58b3695834647b23762d73cd8ffd7a6a74e479f4e9b55335860ead281be0`  
		Last Modified: Wed, 01 Oct 2025 16:12:43 GMT  
		Size: 67.7 MB (67706411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23dd0dc27c53023978fd555939620d6626540546d861c75cafd8ebb1aeecd9b`  
		Last Modified: Wed, 01 Oct 2025 16:12:45 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:161ef89df3d75ff0fdca79e2b94355414a533bf4c62188e36bc646c7eb2b7fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a7d31b3862ab8b0808b8b57a18c3b537754030473b4a15d4fe393ed50ad4e0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=arm64
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e5d2339a6059bc3c7a4ec252d57decfde3f20a6b77c2c8c1ca609e7f3c5947`  
		Last Modified: Thu, 02 Oct 2025 02:29:42 GMT  
		Size: 254.2 MB (254200999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5a203e7a483a9058423564f960e03a3fe532b12a62e27ff8d7825cde41429a`  
		Last Modified: Thu, 02 Oct 2025 01:33:23 GMT  
		Size: 14.3 MB (14320410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d18b1f6c0ff4014074f3b23f243269a39c595fe392c33a14c5e4a90e8ae86e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 480.0 KB (480001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf9f3a7b503dfe098b051887c35aba98d19a665729c8eb69a95289a145c72a1`  
		Last Modified: Thu, 02 Oct 2025 02:29:26 GMT  
		Size: 379.1 MB (379077904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256405c69c1fc96c4dd7de63cffefbe6780d3471751c4c287595b0907825dfe`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7695771ca09b4d8fecb368b5db9e5a0527560dbcbd4c1ceb08c8445facd3547`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835258a0402b4e8e31ad4d60f996a15d9591115b874535d8d858f2462446906f`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5f792e3ee7d0096b53edab4e87067ee725d5d5f438a4dc0ffb001ca5b2145e`  
		Last Modified: Thu, 02 Oct 2025 01:33:22 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:00df3783cd21e5005ac760b5a30caba31833cdb80961a4955ae88dc2c6023da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ead6c1c40247a474d98f48604150ce2164a028270de61f269b24315da699414`

```dockerfile
```

-	Layers:
	-	`sha256:2701eb48c73194f1e1ff74af919c9358d718977a70b0ec2a3232dc519b98b6b4`  
		Last Modified: Thu, 02 Oct 2025 04:14:35 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4db4bcfc15543405629d87c49a4c5f9c63ab41b3978a63c54c0760ea816f39`  
		Last Modified: Thu, 02 Oct 2025 04:14:36 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:526d3afb0efcd7fd170175d06cccebbcbea9fe75fd6efc3ceb23e5f3b27aa495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697159051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d365d96782efcbadf4b83fabfc795d2c1877848af8266085364ebb504613e87d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 30 Sep 2025 08:05:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 08:05:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 08:05:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 08:05:28 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 08:05:28 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Tue, 30 Sep 2025 08:05:28 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Sep 2025 08:05:28 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e52a931c56e47595ae3578fc689562f7305a74f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Sep 2025 08:05:28 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Sep 2025 08:05:28 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
USER odoo
# Tue, 30 Sep 2025 08:05:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Sep 2025 08:05:28 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf1a1b8677cff444b9e317e1467774c91615249c599ee42edfb6ab1c4cf486d`  
		Last Modified: Thu, 02 Oct 2025 03:45:21 GMT  
		Size: 267.7 MB (267727312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac6de21a3054ad275003707ff584683bd495c1bbeb99acd7e54f3eea2860c67`  
		Last Modified: Thu, 02 Oct 2025 03:37:15 GMT  
		Size: 14.9 MB (14868184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06776cbd1a8b5a25f42620e8af3ae9792dee52ae04ca4bac5ab5f9f99e575a73`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 480.1 KB (480122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46792139f3c25fcd8010c37c4c037fc7f55941b626ba2139006b08486259db5b`  
		Last Modified: Thu, 02 Oct 2025 04:13:11 GMT  
		Size: 379.8 MB (379777442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2f2d9aa482942688bf3fb37fa6a67276a69da6439c60f7d216ad7678e7665d`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9f0c67d1977eda0e36d267d5dabb868eb94902c15eef84ef83191a14e70d70`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4159ac72157fbae13b6c612dbe75b29766ee70bc3f38b2191fdf9c06f3b850`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c7eb819eae59eb5b07081ad059f0337a075f2c76f6746f59263a733b15c7c6`  
		Last Modified: Thu, 02 Oct 2025 03:37:12 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:78716b9f097b4776f69f1f752584fbcb23361957947b881a707c5914d2306e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a52a5c3dba67d56befc991c4e41258c4045a3a797a06307950dd5ecc85a4fe`

```dockerfile
```

-	Layers:
	-	`sha256:babaad4a2f86d393e73d58abccbc2095e201e366890f97f7055f32f76468f4c7`  
		Last Modified: Thu, 02 Oct 2025 04:16:17 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f8da8184b442e0ef106f055139b568b90d7facd537c49987639eff0a55b205b`  
		Last Modified: Thu, 02 Oct 2025 04:16:18 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
