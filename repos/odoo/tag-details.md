<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260619`](#odoo170-20260619)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260619`](#odoo180-20260619)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260619`](#odoo190-20260619)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:736fa781c5c86cb0e0c5cf87e570bcad8842130711457e4408e1c703a8c9b566
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:9c309b1d7574aed20ad891524736e4f735f421601beff17a61a7057800c07ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614309669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a948cdf12f8cdaa55fade9dffad181ff03d360c56fbbab379e896997373db4d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:32 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:32 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:32 GMT
ARG TARGETARCH=amd64
# Mon, 22 Jun 2026 18:09:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
ENV ODOO_VERSION=17.0
# Mon, 22 Jun 2026 18:09:38 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:38 GMT
ARG ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
# Mon, 22 Jun 2026 18:10:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109468b0e7d237a825867c5eb4282683c81780435b57b108b69d583b5caaf747`  
		Last Modified: Mon, 22 Jun 2026 18:12:03 GMT  
		Size: 236.1 MB (236066948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bac2ecd212cbe470caf5516b0a4095b65ba3608abe3f8d61777711cfd19761`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 2.6 MB (2611733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ff671091e8fe029933354b2d35921ae4516f5508a31dd233fda61a1d796184`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 481.7 KB (481718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6ee520ba230d9b5a404d99559933f227a3c87d4a343d54e81baae2040f38bc`  
		Last Modified: Mon, 22 Jun 2026 18:12:05 GMT  
		Size: 345.4 MB (345409791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b867587a5ba7ed80427c6a36ce27ddb2ffad4810c7afbfeef2c82b5afa7c43f6`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eecf974d13b1cd8651e60aa02aeaaf2eb05ac089fb3bea9dd99d7a66c87cd5`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca9fbc64f0a1d88322b3ebc466b330b436722aad853721f91ad5155733b337`  
		Last Modified: Mon, 22 Jun 2026 18:11:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db48b7d272e6531a84edba60d636bc0891391f9769543cf93fa482da0b79c12`  
		Last Modified: Mon, 22 Jun 2026 18:11:51 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:00e428a9ec8079d1090dd79c58a361611f07399365455b5583862d5794f0a45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43085700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f630bdb8fd3625abcd533d9fcc88eac2d8cf13dfcd1b0244ba0564df0ffc2f2`

```dockerfile
```

-	Layers:
	-	`sha256:4a62e0168d0b98727eec2281a816e2f9e5f14450bcc623d8d5bacd1d50635a29`  
		Last Modified: Mon, 22 Jun 2026 18:11:52 GMT  
		Size: 43.1 MB (43058896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6efd16e700a2880a15ded64228e2c86c148d1742f731b4215ad8d9d23ca26c4`  
		Last Modified: Mon, 22 Jun 2026 18:11:46 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:626407fb58fc1703fc1cb920cfe2a3b1fea3a6659e4c6901559068abc2cdda42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (609035662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa26c8ae19097cf11086fc2e45c561371a09cd5109c00ad66e4feb0a746824`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:00 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:00 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:00 GMT
ARG TARGETARCH=arm64
# Mon, 22 Jun 2026 18:09:00 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:07 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:08 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:08 GMT
ENV ODOO_VERSION=17.0
# Mon, 22 Jun 2026 18:09:08 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:08 GMT
ARG ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
# Mon, 22 Jun 2026 18:10:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2063924646b9f533bbf9be04d411baf28504eaf2d1ab6c99fe9e6c9b63ed56`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 233.3 MB (233300737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be46a929ff061234568d1a5877654bd66b3cd1a227b619a8b410107ca3dfab`  
		Last Modified: Mon, 22 Jun 2026 18:11:38 GMT  
		Size: 2.6 MB (2606854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe7225d9566a03d49589d8343239b6118342fa4607e78b720bb4948465b97c5`  
		Last Modified: Mon, 22 Jun 2026 18:11:38 GMT  
		Size: 481.7 KB (481724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f5ccb03e19184c26301b957ac1b5bb455a747cbeeaa22adb82311e7c67ad3b`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 345.0 MB (345036929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9695129bf55e61d00746ad379308e62b19acb16a78ed44de09599889669aef`  
		Last Modified: Mon, 22 Jun 2026 18:11:39 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd895f55902e24b663777f9753dd365fff085d9388b9b40a085d47e96cce0125`  
		Last Modified: Mon, 22 Jun 2026 18:11:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba9a64c6c82ba4895dcb3ab843ff0762d1a42968fca50996ad42e3a09fdeb9f`  
		Last Modified: Mon, 22 Jun 2026 18:11:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab3b20c9b832ebecc23ba2620d8e1d729e5f5be59b876083379dcaaa11c468f`  
		Last Modified: Mon, 22 Jun 2026 18:11:41 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1b748072ca91bae223da1f2090067b069386ea6c2da0f1088061bdf89fb6d203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43092359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6995ad3c7c0afb66a7e653b303ce9d8e47fb520e96298014c8a9f9ddd39d7bf7`

```dockerfile
```

-	Layers:
	-	`sha256:9d7f27b24f1d3e3c23ac2c44d6e9cea06644637a818f246323908ae37ca23399`  
		Last Modified: Mon, 22 Jun 2026 18:11:40 GMT  
		Size: 43.1 MB (43065403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2aa2403f96065d9e4478f8e0e697fcfcb2dcb5a14ee55bcea338711a649b96`  
		Last Modified: Mon, 22 Jun 2026 18:11:37 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:736fa781c5c86cb0e0c5cf87e570bcad8842130711457e4408e1c703a8c9b566
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:9c309b1d7574aed20ad891524736e4f735f421601beff17a61a7057800c07ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614309669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a948cdf12f8cdaa55fade9dffad181ff03d360c56fbbab379e896997373db4d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:32 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:32 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:32 GMT
ARG TARGETARCH=amd64
# Mon, 22 Jun 2026 18:09:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
ENV ODOO_VERSION=17.0
# Mon, 22 Jun 2026 18:09:38 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:38 GMT
ARG ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
# Mon, 22 Jun 2026 18:10:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109468b0e7d237a825867c5eb4282683c81780435b57b108b69d583b5caaf747`  
		Last Modified: Mon, 22 Jun 2026 18:12:03 GMT  
		Size: 236.1 MB (236066948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bac2ecd212cbe470caf5516b0a4095b65ba3608abe3f8d61777711cfd19761`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 2.6 MB (2611733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ff671091e8fe029933354b2d35921ae4516f5508a31dd233fda61a1d796184`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 481.7 KB (481718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6ee520ba230d9b5a404d99559933f227a3c87d4a343d54e81baae2040f38bc`  
		Last Modified: Mon, 22 Jun 2026 18:12:05 GMT  
		Size: 345.4 MB (345409791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b867587a5ba7ed80427c6a36ce27ddb2ffad4810c7afbfeef2c82b5afa7c43f6`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eecf974d13b1cd8651e60aa02aeaaf2eb05ac089fb3bea9dd99d7a66c87cd5`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca9fbc64f0a1d88322b3ebc466b330b436722aad853721f91ad5155733b337`  
		Last Modified: Mon, 22 Jun 2026 18:11:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db48b7d272e6531a84edba60d636bc0891391f9769543cf93fa482da0b79c12`  
		Last Modified: Mon, 22 Jun 2026 18:11:51 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:00e428a9ec8079d1090dd79c58a361611f07399365455b5583862d5794f0a45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43085700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f630bdb8fd3625abcd533d9fcc88eac2d8cf13dfcd1b0244ba0564df0ffc2f2`

```dockerfile
```

-	Layers:
	-	`sha256:4a62e0168d0b98727eec2281a816e2f9e5f14450bcc623d8d5bacd1d50635a29`  
		Last Modified: Mon, 22 Jun 2026 18:11:52 GMT  
		Size: 43.1 MB (43058896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6efd16e700a2880a15ded64228e2c86c148d1742f731b4215ad8d9d23ca26c4`  
		Last Modified: Mon, 22 Jun 2026 18:11:46 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:626407fb58fc1703fc1cb920cfe2a3b1fea3a6659e4c6901559068abc2cdda42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (609035662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa26c8ae19097cf11086fc2e45c561371a09cd5109c00ad66e4feb0a746824`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:00 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:00 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:00 GMT
ARG TARGETARCH=arm64
# Mon, 22 Jun 2026 18:09:00 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:07 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:08 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:08 GMT
ENV ODOO_VERSION=17.0
# Mon, 22 Jun 2026 18:09:08 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:08 GMT
ARG ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
# Mon, 22 Jun 2026 18:10:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2063924646b9f533bbf9be04d411baf28504eaf2d1ab6c99fe9e6c9b63ed56`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 233.3 MB (233300737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be46a929ff061234568d1a5877654bd66b3cd1a227b619a8b410107ca3dfab`  
		Last Modified: Mon, 22 Jun 2026 18:11:38 GMT  
		Size: 2.6 MB (2606854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe7225d9566a03d49589d8343239b6118342fa4607e78b720bb4948465b97c5`  
		Last Modified: Mon, 22 Jun 2026 18:11:38 GMT  
		Size: 481.7 KB (481724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f5ccb03e19184c26301b957ac1b5bb455a747cbeeaa22adb82311e7c67ad3b`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 345.0 MB (345036929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9695129bf55e61d00746ad379308e62b19acb16a78ed44de09599889669aef`  
		Last Modified: Mon, 22 Jun 2026 18:11:39 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd895f55902e24b663777f9753dd365fff085d9388b9b40a085d47e96cce0125`  
		Last Modified: Mon, 22 Jun 2026 18:11:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba9a64c6c82ba4895dcb3ab843ff0762d1a42968fca50996ad42e3a09fdeb9f`  
		Last Modified: Mon, 22 Jun 2026 18:11:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab3b20c9b832ebecc23ba2620d8e1d729e5f5be59b876083379dcaaa11c468f`  
		Last Modified: Mon, 22 Jun 2026 18:11:41 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1b748072ca91bae223da1f2090067b069386ea6c2da0f1088061bdf89fb6d203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43092359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6995ad3c7c0afb66a7e653b303ce9d8e47fb520e96298014c8a9f9ddd39d7bf7`

```dockerfile
```

-	Layers:
	-	`sha256:9d7f27b24f1d3e3c23ac2c44d6e9cea06644637a818f246323908ae37ca23399`  
		Last Modified: Mon, 22 Jun 2026 18:11:40 GMT  
		Size: 43.1 MB (43065403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2aa2403f96065d9e4478f8e0e697fcfcb2dcb5a14ee55bcea338711a649b96`  
		Last Modified: Mon, 22 Jun 2026 18:11:37 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260619`

```console
$ docker pull odoo@sha256:736fa781c5c86cb0e0c5cf87e570bcad8842130711457e4408e1c703a8c9b566
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260619` - linux; amd64

```console
$ docker pull odoo@sha256:9c309b1d7574aed20ad891524736e4f735f421601beff17a61a7057800c07ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.3 MB (614309669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a948cdf12f8cdaa55fade9dffad181ff03d360c56fbbab379e896997373db4d3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:32 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:32 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:32 GMT
ARG TARGETARCH=amd64
# Mon, 22 Jun 2026 18:09:32 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:38 GMT
ENV ODOO_VERSION=17.0
# Mon, 22 Jun 2026 18:09:38 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:38 GMT
ARG ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
# Mon, 22 Jun 2026 18:10:33 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:34 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109468b0e7d237a825867c5eb4282683c81780435b57b108b69d583b5caaf747`  
		Last Modified: Mon, 22 Jun 2026 18:12:03 GMT  
		Size: 236.1 MB (236066948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bac2ecd212cbe470caf5516b0a4095b65ba3608abe3f8d61777711cfd19761`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 2.6 MB (2611733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ff671091e8fe029933354b2d35921ae4516f5508a31dd233fda61a1d796184`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 481.7 KB (481718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6ee520ba230d9b5a404d99559933f227a3c87d4a343d54e81baae2040f38bc`  
		Last Modified: Mon, 22 Jun 2026 18:12:05 GMT  
		Size: 345.4 MB (345409791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b867587a5ba7ed80427c6a36ce27ddb2ffad4810c7afbfeef2c82b5afa7c43f6`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eecf974d13b1cd8651e60aa02aeaaf2eb05ac089fb3bea9dd99d7a66c87cd5`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca9fbc64f0a1d88322b3ebc466b330b436722aad853721f91ad5155733b337`  
		Last Modified: Mon, 22 Jun 2026 18:11:51 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db48b7d272e6531a84edba60d636bc0891391f9769543cf93fa482da0b79c12`  
		Last Modified: Mon, 22 Jun 2026 18:11:51 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260619` - unknown; unknown

```console
$ docker pull odoo@sha256:00e428a9ec8079d1090dd79c58a361611f07399365455b5583862d5794f0a45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43085700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f630bdb8fd3625abcd533d9fcc88eac2d8cf13dfcd1b0244ba0564df0ffc2f2`

```dockerfile
```

-	Layers:
	-	`sha256:4a62e0168d0b98727eec2281a816e2f9e5f14450bcc623d8d5bacd1d50635a29`  
		Last Modified: Mon, 22 Jun 2026 18:11:52 GMT  
		Size: 43.1 MB (43058896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6efd16e700a2880a15ded64228e2c86c148d1742f731b4215ad8d9d23ca26c4`  
		Last Modified: Mon, 22 Jun 2026 18:11:46 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260619` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:626407fb58fc1703fc1cb920cfe2a3b1fea3a6659e4c6901559068abc2cdda42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **609.0 MB (609035662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa26c8ae19097cf11086fc2e45c561371a09cd5109c00ad66e4feb0a746824`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:09:00 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:00 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:00 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:00 GMT
ARG TARGETARCH=arm64
# Mon, 22 Jun 2026 18:09:00 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:07 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:08 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:08 GMT
ENV ODOO_VERSION=17.0
# Mon, 22 Jun 2026 18:09:08 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:08 GMT
ARG ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
# Mon, 22 Jun 2026 18:10:19 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=f97cf2f11738a1690b3ced0d4708b97c290a7932
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:20 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2063924646b9f533bbf9be04d411baf28504eaf2d1ab6c99fe9e6c9b63ed56`  
		Last Modified: Mon, 22 Jun 2026 18:11:47 GMT  
		Size: 233.3 MB (233300737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be46a929ff061234568d1a5877654bd66b3cd1a227b619a8b410107ca3dfab`  
		Last Modified: Mon, 22 Jun 2026 18:11:38 GMT  
		Size: 2.6 MB (2606854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe7225d9566a03d49589d8343239b6118342fa4607e78b720bb4948465b97c5`  
		Last Modified: Mon, 22 Jun 2026 18:11:38 GMT  
		Size: 481.7 KB (481724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f5ccb03e19184c26301b957ac1b5bb455a747cbeeaa22adb82311e7c67ad3b`  
		Last Modified: Mon, 22 Jun 2026 18:11:49 GMT  
		Size: 345.0 MB (345036929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9695129bf55e61d00746ad379308e62b19acb16a78ed44de09599889669aef`  
		Last Modified: Mon, 22 Jun 2026 18:11:39 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd895f55902e24b663777f9753dd365fff085d9388b9b40a085d47e96cce0125`  
		Last Modified: Mon, 22 Jun 2026 18:11:39 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba9a64c6c82ba4895dcb3ab843ff0762d1a42968fca50996ad42e3a09fdeb9f`  
		Last Modified: Mon, 22 Jun 2026 18:11:41 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab3b20c9b832ebecc23ba2620d8e1d729e5f5be59b876083379dcaaa11c468f`  
		Last Modified: Mon, 22 Jun 2026 18:11:41 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260619` - unknown; unknown

```console
$ docker pull odoo@sha256:1b748072ca91bae223da1f2090067b069386ea6c2da0f1088061bdf89fb6d203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43092359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6995ad3c7c0afb66a7e653b303ce9d8e47fb520e96298014c8a9f9ddd39d7bf7`

```dockerfile
```

-	Layers:
	-	`sha256:9d7f27b24f1d3e3c23ac2c44d6e9cea06644637a818f246323908ae37ca23399`  
		Last Modified: Mon, 22 Jun 2026 18:11:40 GMT  
		Size: 43.1 MB (43065403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2aa2403f96065d9e4478f8e0e697fcfcb2dcb5a14ee55bcea338711a649b96`  
		Last Modified: Mon, 22 Jun 2026 18:11:37 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:d263921105082f1793e6598b73779fc9fa4463fbe6add0278e469efaf0b9f7f0
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
$ docker pull odoo@sha256:a08f5636ed99b19bd78d02470fccfadcaa3ebb86fc02db4c8f10130417b73a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.1 MB (690112002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df1bf3d086d61368aa19f8fcf01cbcb2ccf68e6e39d58a355e3a8fda2a179f`
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
# Mon, 22 Jun 2026 18:09:43 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:43 GMT
ARG TARGETARCH=amd64
# Mon, 22 Jun 2026 18:09:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:49 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:49 GMT
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:09:49 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:49 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:10:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:42 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0c8bc9e35cdaee2c8f6796ba1a7cf6f3e94fbd81ce04f5b50a519b8c4ea5e1`  
		Last Modified: Mon, 22 Jun 2026 18:12:39 GMT  
		Size: 257.1 MB (257064727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc269a438732938a872e19201683126ed13faa7108149358b1bda3a183004d22`  
		Last Modified: Mon, 22 Jun 2026 18:12:27 GMT  
		Size: 14.4 MB (14370956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1a47888c903f18bd8cf3813464b680c2468a4718729e7dde0f9903ff6c34cd`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 481.5 KB (481538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd49a003df35c66a05e556acb6c3e4e4396250569dc0d3a36885f74b8476eea`  
		Last Modified: Mon, 22 Jun 2026 18:12:43 GMT  
		Size: 388.5 MB (388459178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a05b2ba00f056fe39e34d8f44d558860c94bed98c1073dc3c2ac47676b5631`  
		Last Modified: Mon, 22 Jun 2026 18:12:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65f7d40a2a3d88daab30a93a9147be964420cf2c0d1971561579570566b812`  
		Last Modified: Mon, 22 Jun 2026 18:12:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aff5f43a4008a2faa681eea3a33d3d236bc02ad5f64329572a593f571374c06`  
		Last Modified: Mon, 22 Jun 2026 18:12:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a448a206286a3d04b0a84fdbf11037e62fb019667637edd988311c9a3c70d52`  
		Last Modified: Mon, 22 Jun 2026 18:12:31 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:1a357f29fcfe1ef67bb10d2c84e2cea847f6b5759b48c9a4719d2028f29bcff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62556947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c78bc056eee9fe7548e4a8e61ae73a6e055ed63ac3facff55279fa0a2a35537`

```dockerfile
```

-	Layers:
	-	`sha256:d37d4391f48e9a34d080c701d5abf9a655b714ea4b5cd65aec4f76a13bc0aa4c`  
		Last Modified: Mon, 22 Jun 2026 18:12:30 GMT  
		Size: 62.5 MB (62530136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1aabfce38940b83a42955d54957274478866c39388420e9e8c29a7bb11de07`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:85bce4c080759e0c675a2615a42dce86f1b3649d8bcc4a0b6dbf9215af8d2bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 MB (686289297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4032ec4d3b2a64fab1cd233fa1560ff1f97d023c4dc75ec54b21f430a6be243f`
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
# Mon, 22 Jun 2026 18:09:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:10 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:10 GMT
ARG TARGETARCH=arm64
# Mon, 22 Jun 2026 18:09:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:17 GMT
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:09:17 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:17 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:10:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e86000fd660a73009b49cd0b11b1930e592229bc60bd3851160ee0e999f56`  
		Last Modified: Mon, 22 Jun 2026 18:12:33 GMT  
		Size: 254.3 MB (254280804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2751a1e1c3f4820e4d4f9dc18782326837349983abb5cdcf4607087ab3c6d33`  
		Last Modified: Mon, 22 Jun 2026 18:12:23 GMT  
		Size: 14.3 MB (14349314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a469d0cc596e8c0c88d790fd1b5a671835aa2b7e9344f9e5147ded799b5361`  
		Last Modified: Mon, 22 Jun 2026 18:12:22 GMT  
		Size: 481.5 KB (481501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239611cb92dd6f920911a33e27688856be51cb4e8ff97411313a918cf9424b8d`  
		Last Modified: Mon, 22 Jun 2026 18:12:36 GMT  
		Size: 388.3 MB (388298474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83513265a04c9c536b1ce44005b3e98861014a0f375d1844b122ff65893f8b6a`  
		Last Modified: Mon, 22 Jun 2026 18:12:24 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf485a84f8c8d16638f019670bfee1796dc122ca1b16f4ec03075b94c028f663`  
		Last Modified: Mon, 22 Jun 2026 18:12:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5ddcc5ef78a01f0d7de9e369d8edf93ef6824aeb9cc2d1c0e82c0159212d69`  
		Last Modified: Mon, 22 Jun 2026 18:12:25 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b3efee3012c9acdcbb08d0c7e89f2f882a34049c0b1bd45e46556bc171819a`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:66a8014e18568321eed8a1ebe937f6e2bbda5a61086dbd31793df0b174c8d63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62564374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ceb21a68a46bef7907aeedc9f64e9bdcfd28d2ec154ec72b85bdd65011edd86`

```dockerfile
```

-	Layers:
	-	`sha256:9297a6a6ff750163f8869ecbf67b2eaabd9d5ac8025472cdca8daeefe576ca15`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 62.5 MB (62537411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd625498ae232a3a8ca82817dee8c043072e45313c09fcf16883991ef043c49`  
		Last Modified: Mon, 22 Jun 2026 18:12:22 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:25de7cb7f08a71afc837fe1ba5b5461212cd082c22ea1d2e2661865a36cf8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706634076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808c513a0e1349f748d2b8130756ea78c72b960ff83781472dcfc5cde0ce7f9e`
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
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:17:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:17:52 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:17:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:17:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:17:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:17:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
USER odoo
# Mon, 22 Jun 2026 18:17:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:17:53 GMT
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
	-	`sha256:d515890ab146672e31138b2f0d0006f5791d9ab9cabab0d0a91cf721587044e5`  
		Last Modified: Mon, 22 Jun 2026 18:22:35 GMT  
		Size: 389.0 MB (388988439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac0c5fe5c28231718a590cc75ab315d417be0c045460b3e7cb7887fccdf35e9`  
		Last Modified: Mon, 22 Jun 2026 18:22:22 GMT  
		Size: 768.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adc50bb78012e98e28b6357efbbcc7f5977386970565b1bd35393899c94ee20`  
		Last Modified: Mon, 22 Jun 2026 18:22:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f72962bbd09c70f0721b8a00921a918cfa796cb96ba4ed7dc98223cf92bf11d`  
		Last Modified: Mon, 22 Jun 2026 18:22:24 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb168e93206c476adf654b6ff544a429170af148f7e159f6b3740aff2021cbd`  
		Last Modified: Mon, 22 Jun 2026 18:22:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:0520a77309a79f75bc70ada53ad33f617baac87a6d64f5a5fa6299bfd98ceb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62565386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e80f72207b0268b50ac16be8c1d81011f16b8cd09d959735e9fb1d7ec8b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:023ed1bdbadc8ea708196947afd751f060ef48480cb6f97111a4d29e16723c7b`  
		Last Modified: Mon, 22 Jun 2026 18:22:26 GMT  
		Size: 62.5 MB (62538519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79a66d4056e0ae060435a6fb3b716dd71d07effb3e29dc076e40ab4985a92a9`  
		Last Modified: Mon, 22 Jun 2026 18:22:20 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:d263921105082f1793e6598b73779fc9fa4463fbe6add0278e469efaf0b9f7f0
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
$ docker pull odoo@sha256:a08f5636ed99b19bd78d02470fccfadcaa3ebb86fc02db4c8f10130417b73a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.1 MB (690112002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df1bf3d086d61368aa19f8fcf01cbcb2ccf68e6e39d58a355e3a8fda2a179f`
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
# Mon, 22 Jun 2026 18:09:43 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:43 GMT
ARG TARGETARCH=amd64
# Mon, 22 Jun 2026 18:09:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:49 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:49 GMT
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:09:49 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:49 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:10:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:42 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0c8bc9e35cdaee2c8f6796ba1a7cf6f3e94fbd81ce04f5b50a519b8c4ea5e1`  
		Last Modified: Mon, 22 Jun 2026 18:12:39 GMT  
		Size: 257.1 MB (257064727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc269a438732938a872e19201683126ed13faa7108149358b1bda3a183004d22`  
		Last Modified: Mon, 22 Jun 2026 18:12:27 GMT  
		Size: 14.4 MB (14370956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1a47888c903f18bd8cf3813464b680c2468a4718729e7dde0f9903ff6c34cd`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 481.5 KB (481538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd49a003df35c66a05e556acb6c3e4e4396250569dc0d3a36885f74b8476eea`  
		Last Modified: Mon, 22 Jun 2026 18:12:43 GMT  
		Size: 388.5 MB (388459178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a05b2ba00f056fe39e34d8f44d558860c94bed98c1073dc3c2ac47676b5631`  
		Last Modified: Mon, 22 Jun 2026 18:12:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65f7d40a2a3d88daab30a93a9147be964420cf2c0d1971561579570566b812`  
		Last Modified: Mon, 22 Jun 2026 18:12:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aff5f43a4008a2faa681eea3a33d3d236bc02ad5f64329572a593f571374c06`  
		Last Modified: Mon, 22 Jun 2026 18:12:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a448a206286a3d04b0a84fdbf11037e62fb019667637edd988311c9a3c70d52`  
		Last Modified: Mon, 22 Jun 2026 18:12:31 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1a357f29fcfe1ef67bb10d2c84e2cea847f6b5759b48c9a4719d2028f29bcff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62556947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c78bc056eee9fe7548e4a8e61ae73a6e055ed63ac3facff55279fa0a2a35537`

```dockerfile
```

-	Layers:
	-	`sha256:d37d4391f48e9a34d080c701d5abf9a655b714ea4b5cd65aec4f76a13bc0aa4c`  
		Last Modified: Mon, 22 Jun 2026 18:12:30 GMT  
		Size: 62.5 MB (62530136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1aabfce38940b83a42955d54957274478866c39388420e9e8c29a7bb11de07`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:85bce4c080759e0c675a2615a42dce86f1b3649d8bcc4a0b6dbf9215af8d2bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 MB (686289297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4032ec4d3b2a64fab1cd233fa1560ff1f97d023c4dc75ec54b21f430a6be243f`
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
# Mon, 22 Jun 2026 18:09:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:10 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:10 GMT
ARG TARGETARCH=arm64
# Mon, 22 Jun 2026 18:09:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:17 GMT
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:09:17 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:17 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:10:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e86000fd660a73009b49cd0b11b1930e592229bc60bd3851160ee0e999f56`  
		Last Modified: Mon, 22 Jun 2026 18:12:33 GMT  
		Size: 254.3 MB (254280804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2751a1e1c3f4820e4d4f9dc18782326837349983abb5cdcf4607087ab3c6d33`  
		Last Modified: Mon, 22 Jun 2026 18:12:23 GMT  
		Size: 14.3 MB (14349314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a469d0cc596e8c0c88d790fd1b5a671835aa2b7e9344f9e5147ded799b5361`  
		Last Modified: Mon, 22 Jun 2026 18:12:22 GMT  
		Size: 481.5 KB (481501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239611cb92dd6f920911a33e27688856be51cb4e8ff97411313a918cf9424b8d`  
		Last Modified: Mon, 22 Jun 2026 18:12:36 GMT  
		Size: 388.3 MB (388298474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83513265a04c9c536b1ce44005b3e98861014a0f375d1844b122ff65893f8b6a`  
		Last Modified: Mon, 22 Jun 2026 18:12:24 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf485a84f8c8d16638f019670bfee1796dc122ca1b16f4ec03075b94c028f663`  
		Last Modified: Mon, 22 Jun 2026 18:12:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5ddcc5ef78a01f0d7de9e369d8edf93ef6824aeb9cc2d1c0e82c0159212d69`  
		Last Modified: Mon, 22 Jun 2026 18:12:25 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b3efee3012c9acdcbb08d0c7e89f2f882a34049c0b1bd45e46556bc171819a`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:66a8014e18568321eed8a1ebe937f6e2bbda5a61086dbd31793df0b174c8d63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62564374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ceb21a68a46bef7907aeedc9f64e9bdcfd28d2ec154ec72b85bdd65011edd86`

```dockerfile
```

-	Layers:
	-	`sha256:9297a6a6ff750163f8869ecbf67b2eaabd9d5ac8025472cdca8daeefe576ca15`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 62.5 MB (62537411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd625498ae232a3a8ca82817dee8c043072e45313c09fcf16883991ef043c49`  
		Last Modified: Mon, 22 Jun 2026 18:12:22 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:25de7cb7f08a71afc837fe1ba5b5461212cd082c22ea1d2e2661865a36cf8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706634076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808c513a0e1349f748d2b8130756ea78c72b960ff83781472dcfc5cde0ce7f9e`
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
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:17:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:17:52 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:17:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:17:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:17:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:17:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
USER odoo
# Mon, 22 Jun 2026 18:17:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:17:53 GMT
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
	-	`sha256:d515890ab146672e31138b2f0d0006f5791d9ab9cabab0d0a91cf721587044e5`  
		Last Modified: Mon, 22 Jun 2026 18:22:35 GMT  
		Size: 389.0 MB (388988439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac0c5fe5c28231718a590cc75ab315d417be0c045460b3e7cb7887fccdf35e9`  
		Last Modified: Mon, 22 Jun 2026 18:22:22 GMT  
		Size: 768.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adc50bb78012e98e28b6357efbbcc7f5977386970565b1bd35393899c94ee20`  
		Last Modified: Mon, 22 Jun 2026 18:22:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f72962bbd09c70f0721b8a00921a918cfa796cb96ba4ed7dc98223cf92bf11d`  
		Last Modified: Mon, 22 Jun 2026 18:22:24 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb168e93206c476adf654b6ff544a429170af148f7e159f6b3740aff2021cbd`  
		Last Modified: Mon, 22 Jun 2026 18:22:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:0520a77309a79f75bc70ada53ad33f617baac87a6d64f5a5fa6299bfd98ceb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62565386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e80f72207b0268b50ac16be8c1d81011f16b8cd09d959735e9fb1d7ec8b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:023ed1bdbadc8ea708196947afd751f060ef48480cb6f97111a4d29e16723c7b`  
		Last Modified: Mon, 22 Jun 2026 18:22:26 GMT  
		Size: 62.5 MB (62538519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79a66d4056e0ae060435a6fb3b716dd71d07effb3e29dc076e40ab4985a92a9`  
		Last Modified: Mon, 22 Jun 2026 18:22:20 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260619`

```console
$ docker pull odoo@sha256:d263921105082f1793e6598b73779fc9fa4463fbe6add0278e469efaf0b9f7f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260619` - linux; amd64

```console
$ docker pull odoo@sha256:a08f5636ed99b19bd78d02470fccfadcaa3ebb86fc02db4c8f10130417b73a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **690.1 MB (690112002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91df1bf3d086d61368aa19f8fcf01cbcb2ccf68e6e39d58a355e3a8fda2a179f`
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
# Mon, 22 Jun 2026 18:09:43 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:43 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:43 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:43 GMT
ARG TARGETARCH=amd64
# Mon, 22 Jun 2026 18:09:43 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:48 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:49 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:49 GMT
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:09:49 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:49 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:10:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:41 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:41 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:41 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:42 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:42 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:42 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0c8bc9e35cdaee2c8f6796ba1a7cf6f3e94fbd81ce04f5b50a519b8c4ea5e1`  
		Last Modified: Mon, 22 Jun 2026 18:12:39 GMT  
		Size: 257.1 MB (257064727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc269a438732938a872e19201683126ed13faa7108149358b1bda3a183004d22`  
		Last Modified: Mon, 22 Jun 2026 18:12:27 GMT  
		Size: 14.4 MB (14370956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1a47888c903f18bd8cf3813464b680c2468a4718729e7dde0f9903ff6c34cd`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 481.5 KB (481538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd49a003df35c66a05e556acb6c3e4e4396250569dc0d3a36885f74b8476eea`  
		Last Modified: Mon, 22 Jun 2026 18:12:43 GMT  
		Size: 388.5 MB (388459178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a05b2ba00f056fe39e34d8f44d558860c94bed98c1073dc3c2ac47676b5631`  
		Last Modified: Mon, 22 Jun 2026 18:12:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee65f7d40a2a3d88daab30a93a9147be964420cf2c0d1971561579570566b812`  
		Last Modified: Mon, 22 Jun 2026 18:12:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aff5f43a4008a2faa681eea3a33d3d236bc02ad5f64329572a593f571374c06`  
		Last Modified: Mon, 22 Jun 2026 18:12:29 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a448a206286a3d04b0a84fdbf11037e62fb019667637edd988311c9a3c70d52`  
		Last Modified: Mon, 22 Jun 2026 18:12:31 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260619` - unknown; unknown

```console
$ docker pull odoo@sha256:1a357f29fcfe1ef67bb10d2c84e2cea847f6b5759b48c9a4719d2028f29bcff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62556947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c78bc056eee9fe7548e4a8e61ae73a6e055ed63ac3facff55279fa0a2a35537`

```dockerfile
```

-	Layers:
	-	`sha256:d37d4391f48e9a34d080c701d5abf9a655b714ea4b5cd65aec4f76a13bc0aa4c`  
		Last Modified: Mon, 22 Jun 2026 18:12:30 GMT  
		Size: 62.5 MB (62530136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1aabfce38940b83a42955d54957274478866c39388420e9e8c29a7bb11de07`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260619` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:85bce4c080759e0c675a2615a42dce86f1b3649d8bcc4a0b6dbf9215af8d2bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.3 MB (686289297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4032ec4d3b2a64fab1cd233fa1560ff1f97d023c4dc75ec54b21f430a6be243f`
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
# Mon, 22 Jun 2026 18:09:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Mon, 22 Jun 2026 18:09:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 22 Jun 2026 18:09:10 GMT
ENV LANG=en_US.UTF-8
# Mon, 22 Jun 2026 18:09:10 GMT
ARG TARGETARCH=arm64
# Mon, 22 Jun 2026 18:09:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 22 Jun 2026 18:09:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 18:09:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 22 Jun 2026 18:09:17 GMT
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:09:17 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:09:17 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:10:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:10:16 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:10:16 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:10:16 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:10:16 GMT
USER odoo
# Mon, 22 Jun 2026 18:10:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:10:16 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e86000fd660a73009b49cd0b11b1930e592229bc60bd3851160ee0e999f56`  
		Last Modified: Mon, 22 Jun 2026 18:12:33 GMT  
		Size: 254.3 MB (254280804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2751a1e1c3f4820e4d4f9dc18782326837349983abb5cdcf4607087ab3c6d33`  
		Last Modified: Mon, 22 Jun 2026 18:12:23 GMT  
		Size: 14.3 MB (14349314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a469d0cc596e8c0c88d790fd1b5a671835aa2b7e9344f9e5147ded799b5361`  
		Last Modified: Mon, 22 Jun 2026 18:12:22 GMT  
		Size: 481.5 KB (481501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239611cb92dd6f920911a33e27688856be51cb4e8ff97411313a918cf9424b8d`  
		Last Modified: Mon, 22 Jun 2026 18:12:36 GMT  
		Size: 388.3 MB (388298474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83513265a04c9c536b1ce44005b3e98861014a0f375d1844b122ff65893f8b6a`  
		Last Modified: Mon, 22 Jun 2026 18:12:24 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf485a84f8c8d16638f019670bfee1796dc122ca1b16f4ec03075b94c028f663`  
		Last Modified: Mon, 22 Jun 2026 18:12:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5ddcc5ef78a01f0d7de9e369d8edf93ef6824aeb9cc2d1c0e82c0159212d69`  
		Last Modified: Mon, 22 Jun 2026 18:12:25 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b3efee3012c9acdcbb08d0c7e89f2f882a34049c0b1bd45e46556bc171819a`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260619` - unknown; unknown

```console
$ docker pull odoo@sha256:66a8014e18568321eed8a1ebe937f6e2bbda5a61086dbd31793df0b174c8d63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62564374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ceb21a68a46bef7907aeedc9f64e9bdcfd28d2ec154ec72b85bdd65011edd86`

```dockerfile
```

-	Layers:
	-	`sha256:9297a6a6ff750163f8869ecbf67b2eaabd9d5ac8025472cdca8daeefe576ca15`  
		Last Modified: Mon, 22 Jun 2026 18:12:26 GMT  
		Size: 62.5 MB (62537411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fd625498ae232a3a8ca82817dee8c043072e45313c09fcf16883991ef043c49`  
		Last Modified: Mon, 22 Jun 2026 18:12:22 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260619` - linux; ppc64le

```console
$ docker pull odoo@sha256:25de7cb7f08a71afc837fe1ba5b5461212cd082c22ea1d2e2661865a36cf8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.6 MB (706634076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808c513a0e1349f748d2b8130756ea78c72b960ff83781472dcfc5cde0ce7f9e`
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
ENV ODOO_VERSION=18.0
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_RELEASE=20260619
# Mon, 22 Jun 2026 18:15:44 GMT
ARG ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
# Mon, 22 Jun 2026 18:17:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 22 Jun 2026 18:17:52 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 22 Jun 2026 18:17:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260619 ODOO_SHA=28e5e1186040594e9f44b4988b006f1782f4718c
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 22 Jun 2026 18:17:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 22 Jun 2026 18:17:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 22 Jun 2026 18:17:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 22 Jun 2026 18:17:53 GMT
USER odoo
# Mon, 22 Jun 2026 18:17:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 18:17:53 GMT
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
	-	`sha256:d515890ab146672e31138b2f0d0006f5791d9ab9cabab0d0a91cf721587044e5`  
		Last Modified: Mon, 22 Jun 2026 18:22:35 GMT  
		Size: 389.0 MB (388988439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac0c5fe5c28231718a590cc75ab315d417be0c045460b3e7cb7887fccdf35e9`  
		Last Modified: Mon, 22 Jun 2026 18:22:22 GMT  
		Size: 768.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adc50bb78012e98e28b6357efbbcc7f5977386970565b1bd35393899c94ee20`  
		Last Modified: Mon, 22 Jun 2026 18:22:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f72962bbd09c70f0721b8a00921a918cfa796cb96ba4ed7dc98223cf92bf11d`  
		Last Modified: Mon, 22 Jun 2026 18:22:24 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb168e93206c476adf654b6ff544a429170af148f7e159f6b3740aff2021cbd`  
		Last Modified: Mon, 22 Jun 2026 18:22:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260619` - unknown; unknown

```console
$ docker pull odoo@sha256:0520a77309a79f75bc70ada53ad33f617baac87a6d64f5a5fa6299bfd98ceb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62565386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e80f72207b0268b50ac16be8c1d81011f16b8cd09d959735e9fb1d7ec8b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:023ed1bdbadc8ea708196947afd751f060ef48480cb6f97111a4d29e16723c7b`  
		Last Modified: Mon, 22 Jun 2026 18:22:26 GMT  
		Size: 62.5 MB (62538519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a79a66d4056e0ae060435a6fb3b716dd71d07effb3e29dc076e40ab4985a92a9`  
		Last Modified: Mon, 22 Jun 2026 18:22:20 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

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

### `odoo:19` - linux; amd64

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

### `odoo:19` - unknown; unknown

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

### `odoo:19` - linux; arm64 variant v8

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

### `odoo:19` - unknown; unknown

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

### `odoo:19` - linux; ppc64le

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

### `odoo:19` - unknown; unknown

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

## `odoo:19.0`

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

### `odoo:19.0` - linux; amd64

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

### `odoo:19.0` - unknown; unknown

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

### `odoo:19.0` - linux; arm64 variant v8

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

### `odoo:19.0` - unknown; unknown

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

### `odoo:19.0` - linux; ppc64le

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

### `odoo:19.0` - unknown; unknown

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

## `odoo:19.0-20260619`

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

### `odoo:19.0-20260619` - linux; amd64

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

### `odoo:19.0-20260619` - unknown; unknown

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

### `odoo:19.0-20260619` - linux; arm64 variant v8

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

### `odoo:19.0-20260619` - unknown; unknown

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

### `odoo:19.0-20260619` - linux; ppc64le

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

### `odoo:19.0-20260619` - unknown; unknown

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
