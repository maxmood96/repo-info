## `odoo:latest`

```console
$ docker pull odoo@sha256:58ebecde97869ec72b45b79983a79e0edd9985f4785cf04f66204144c58d3045
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
$ docker pull odoo@sha256:c266ed8754b7b75d0a1f1b593d0a37f74f222264ee0753d5080e8b9cea6b42b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **670.6 MB (670649328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8abb3b47c4f6002878a93d9d2cb61dc1ec6a17f4c51dade8bc4799dc8989d99b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=amd64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce721958af367d366bcbf4cc0ee90872028155903ecd43c32659de1f3d1c87b`  
		Last Modified: Mon, 05 May 2025 16:39:15 GMT  
		Size: 254.5 MB (254517355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2c29fb667652ad6c18d746e8ad288462540385972ecfac3323c6670c32521`  
		Last Modified: Mon, 05 May 2025 16:39:11 GMT  
		Size: 14.3 MB (14273576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb20087d90cdf7c10c8527376ceca2eda87c3f5bf4802f72f6e312924367fe2`  
		Last Modified: Mon, 05 May 2025 16:39:10 GMT  
		Size: 478.6 KB (478564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eaecfb9eced1f1c656dc186fcd04d20e440c92d3b48f9cc9c08a9cbfc1c305`  
		Last Modified: Mon, 05 May 2025 16:39:18 GMT  
		Size: 371.7 MB (371659858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e84e8cc1d541efd33200880edd3a36a9e5c23b409ee86e376dd8f2315a743`  
		Last Modified: Mon, 05 May 2025 16:38:33 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2b985cfc3bf52b8b4d1afab03f9cd1cdf41576682f9e0969cb9becc4309ac9`  
		Last Modified: Mon, 05 May 2025 16:39:11 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b37e640faa7bbf58b7769f2b2a1fe1c1dafd86649e10acf8623d3660bab2a`  
		Last Modified: Mon, 05 May 2025 16:39:12 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ad9dc624f13799cb91687a31bbf3de903abb7c0cbbe959fc69c48658d7819`  
		Last Modified: Mon, 05 May 2025 16:39:12 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6fd9f6f5ac437758f6678cadbf3d2de8731c772f5f2f82b0643f148435deb84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59248625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071c7f50279bcb3d1bfa31b7d6d8c500e1f671467784b514405197003988d968`

```dockerfile
```

-	Layers:
	-	`sha256:d0e3a0c9ab6eab2a44f2dc22c7f6123d1aab8a628cb44c6e444a5b4b1dede834`  
		Last Modified: Mon, 05 May 2025 16:39:11 GMT  
		Size: 59.2 MB (59221489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c4f60889b5258b26e4cee0b6ce615ba48b3e5420a9f63246b9201a03e067c1`  
		Last Modified: Mon, 05 May 2025 16:39:10 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:524adafe6d4f9a2c4e04c9cb482aaa789efeb8b80791c57a0ef976dec52a0227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.0 MB (667023965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bca2b47e1d7fe0110bcc62cbf0156b395be850c388ed97a4eeb1877df672ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=arm64
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cea12ad03e430fdf48d3d8940f180d90e8d3ab7751cd37cd03b42984aaf74`  
		Last Modified: Mon, 05 May 2025 17:55:36 GMT  
		Size: 251.9 MB (251942645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa0aced1c160ae538bf0ebec5077a1e8afbcaf5d03efbcbcb962ee3b221dc77`  
		Last Modified: Mon, 05 May 2025 17:55:31 GMT  
		Size: 14.2 MB (14248288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a45247f2759eee35efbf0f41226f028f4a4c0d102c16f95ecf5a6087605d4`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 478.6 KB (478561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210231a7018b03ca69d746792d72651afa53b651cc383a68db63af86715963b9`  
		Last Modified: Mon, 05 May 2025 17:55:38 GMT  
		Size: 371.5 MB (371505156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe1d153489f07da43b7fc6cb0fc2eb233b7562cc975f998ad71800f58e3651e`  
		Last Modified: Mon, 05 May 2025 17:55:31 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e03a48516d40c33711fd64f7d3d05b9fc34038d19b7150e15c861f438adb2`  
		Last Modified: Mon, 05 May 2025 17:55:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c0a7e0c7951e596f08fdcdb9df230e8921d3be05578cf3c2cbbaad968a1e34`  
		Last Modified: Mon, 05 May 2025 17:55:32 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2734564f9643c922eaf02ec63d2e4176e816ea393cfed731e3e25d2077228437`  
		Last Modified: Mon, 05 May 2025 17:55:33 GMT  
		Size: 584.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f6c9dce6407f2adb17aa0eb93ebfb7ef63fe3f0f7ac2d9482ad0e5a2d329fb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92e991458971cd9bc9201319f32960cf0f2de5e3a8c0463755ec29b62c6c41f`

```dockerfile
```

-	Layers:
	-	`sha256:4ab44bf49fd6495ea190b698e5d6af81147e405f7be32565e0e9aaa11eff112b`  
		Last Modified: Mon, 05 May 2025 17:55:32 GMT  
		Size: 59.2 MB (59228776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edeff0f6a890cb2df40a6a2ebc071f167c07333b7fd59fc1a1b87f6bdebe3a1`  
		Last Modified: Mon, 05 May 2025 17:55:30 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:186197d4e8c85b87ee28473f0d58cb36c850d385864b4fb8ea0ff8e8c9ecaf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.9 MB (686880694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad9d75d450cc063f86f0aaf3c01327181d786f418bb63f59cc3d3a932e6df2a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Mon, 28 Apr 2025 08:21:35 GMT
ARG RELEASE
# Mon, 28 Apr 2025 08:21:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 08:21:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Apr 2025 08:21:35 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["/bin/bash"]
# Mon, 28 Apr 2025 08:21:35 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 28 Apr 2025 08:21:35 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV LANG=en_US.UTF-8
# Mon, 28 Apr 2025 08:21:35 GMT
ARG TARGETARCH=ppc64le
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_VERSION=18.0
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_RELEASE=20250428
# Mon, 28 Apr 2025 08:21:35 GMT
ARG ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250428 ODOO_SHA=952a8f7148a7652809546ee7acdc2d66c09e04d9
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 28 Apr 2025 08:21:35 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 28 Apr 2025 08:21:35 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 28 Apr 2025 08:21:35 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 28 Apr 2025 08:21:35 GMT
USER odoo
# Mon, 28 Apr 2025 08:21:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Apr 2025 08:21:35 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a0cfd686d0bf7f2685e08e731f2256951d6fd010571255282341db491622f6`  
		Last Modified: Mon, 05 May 2025 17:46:12 GMT  
		Size: 265.1 MB (265077741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66b4970c3558e4f73623c9885fa8a1bddebb7ce9e44d6760e871a869602afee`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 14.8 MB (14797186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5152a85d6330f04722330a9eb18fa24c8dce960b2f2ac3ed34b33e74d5d8439`  
		Last Modified: Mon, 05 May 2025 17:45:55 GMT  
		Size: 478.6 KB (478615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d9fe1350f6e1b5a8c58ad71b50f7776c5fc07f2cc18a9726bb8dbdad6adc48`  
		Last Modified: Mon, 05 May 2025 17:46:24 GMT  
		Size: 372.2 MB (372183871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133719afd10b139102b254de89d3cde948dc05259b4c11a23e6cb4f0ab53a3cf`  
		Last Modified: Mon, 05 May 2025 17:45:56 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893719c4cb9d31f610adad2128cd7881aefea728b4ae9de563812c7c907c3f4`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928368c5b8efeead48bab993fbf849c634ac24968677095841b050752a0d7128`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6772dd4d24330136e0bb55571c1f9e8d02b559d2ba6c5fa8e9bf09b953d45ffd`  
		Last Modified: Mon, 05 May 2025 17:45:58 GMT  
		Size: 585.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:32ea24da4e1ccb1814f0cc149c8becd759cb599af8338dc954349087cb9839ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59256830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3917ea9097ba151e4a2945ce013933d556a4d0a56bc669ece0fda4e8ec02e20f`

```dockerfile
```

-	Layers:
	-	`sha256:72d8b734aa153d1f5bad70b1907e28540c6a8d324a7a4335bc0c12fa61200cd5`  
		Last Modified: Mon, 05 May 2025 17:45:57 GMT  
		Size: 59.2 MB (59229632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c8d19dd96517905493d8fb3a0abecc92e5d7a6c882725ca647a9a13b95eeaf`  
		Last Modified: Mon, 05 May 2025 17:45:54 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
