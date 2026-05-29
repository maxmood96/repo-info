<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260528`](#odoo170-20260528)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260528`](#odoo180-20260528)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260528`](#odoo190-20260528)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:a6815d43d76d91d4d76ace77e9718b9d0cff98359a6cee8dfb192fae6fda98be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:be76328bd7233c8f860c7a18449d463769f2ce3ce9613700ff71835d6b8af100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.4 MB (611397696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad671c35671b1f60639aace57aaa83d9de4ec6d272f8e3e8f459669948bf7137`
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
# Thu, 28 May 2026 21:19:19 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:19:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:19:19 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:19:19 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:19:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:19:25 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:19:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:19:26 GMT
ENV ODOO_VERSION=17.0
# Thu, 28 May 2026 21:19:26 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:19:26 GMT
ARG ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
# Thu, 28 May 2026 21:20:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:20:19 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:20:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:20:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:20:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:20:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:20:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:20:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:20:19 GMT
USER odoo
# Thu, 28 May 2026 21:20:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:20:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c9a908bec59e30bfaf775d660c1e2d842d2e623d9e148d601912432054cabe`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 233.8 MB (233835058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a508392171167ceea13d67af3f889dbaad9ae0380e4f7d19f470047c37a74f`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 2.6 MB (2611499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7039c17552a3fbb50e23d5b33f57c8ccbd3e3bd381f2f06915074af188e16bf8`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 483.8 KB (483836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729ed212720627eb9cbc61fcbe0a7a5c36d8bce22c16d869c77d910ac972983`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 344.7 MB (344727824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c068be46d027f4772b6adb2f2178af0c6e542bf6068133bff8525648d75b1`  
		Last Modified: Thu, 28 May 2026 21:21:35 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fef691daf4995b7ca513880b0c5d32dcfbce9b77286604a994cc51dd3b66ae`  
		Last Modified: Thu, 28 May 2026 21:21:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9a2f2d0e4d1ea325a20044e0b8a63a7331ba25facf8b9acf80d9ce63a279f8`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf21c048a3356215d713ba74804e535c5fd86ce7324db0621b8f817bf7915722`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a0391fb37ae6eae0f333415f9efd59091d1618276364632c1fd19d1fbd59a4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd221811040d1e6702dbec3577a97ceab660396eb7cbcf9160eb0b3d523dddcd`

```dockerfile
```

-	Layers:
	-	`sha256:17b94913b49c61cdff5a03f74e05dba79bad209ddbba352d22fc8078a1f8a23b`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 43.1 MB (43070412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea733b81f45944ce6e391fa4e6a846a3803bd5a3d031ecbbd94e9b2139b23b9`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4300e35f5a072ef4613f08c1b4ede9e47f3d32d35b4430bc9eb4cca1f1df534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.2 MB (606220669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0e28cb1621a2b206bd9321b162ae95f8d706c3f2215130625a0d77354c784`
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
# Thu, 28 May 2026 21:18:54 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:18:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:18:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:18:54 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:18:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:19:01 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:19:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:19:02 GMT
ENV ODOO_VERSION=17.0
# Thu, 28 May 2026 21:19:02 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:19:02 GMT
ARG ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
# Thu, 28 May 2026 21:20:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:20:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:20:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:20:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:20:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:20:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:20:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:20:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:20:21 GMT
USER odoo
# Thu, 28 May 2026 21:20:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:20:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96968d3c732bb4f8a4b07b9e4dad0a50a1f509bfb1385526709c2f11bc27c574`  
		Last Modified: Thu, 28 May 2026 21:21:52 GMT  
		Size: 231.2 MB (231203414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a750e77e0cca983dfe49d7a3bf0135a1e885741a4cb37f365300346e70a931`  
		Last Modified: Thu, 28 May 2026 21:21:43 GMT  
		Size: 2.6 MB (2606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce19193af6f3912bce4ce62a7c603b5e6a03806bf0fd7d32565892b03372347`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 483.9 KB (483918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea30d33ed982ae9286ce0a6715b94f5cc16759e450ffb4de4958a52977e400`  
		Last Modified: Thu, 28 May 2026 21:21:54 GMT  
		Size: 344.3 MB (344317178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07202d9571a7340265f7fabc470c929556725a61def88a4a001039833608ad`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b124d113ac7637177caefbaedd70244d8bc07750639b0488e7fa4f9abc94fc`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44cd8c930605b9751b51de25d7219d236371d7aeb6808130ac2b74f547224a`  
		Last Modified: Thu, 28 May 2026 21:21:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f120c863e452dda70f5fefd377e50fffb51294890b7924bd00eb69bdece3f7c`  
		Last Modified: Thu, 28 May 2026 21:21:46 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:1b2287fd6cc0cf338c179003f2340bead66c926a9e85f2c30af46960b1841093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43103875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd5743f2d4894c0491cd514aedf162efa665e76bde0d367b4b1d56feae92f8`

```dockerfile
```

-	Layers:
	-	`sha256:86a1214d467e056c033702a527de33eaed63c081dcc4fb9085cffc74b8634d68`  
		Last Modified: Thu, 28 May 2026 21:21:45 GMT  
		Size: 43.1 MB (43076919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be28950497bf83d0bbda0391cd710348100b5a82b8a767502f6994336d6e0fd2`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:a6815d43d76d91d4d76ace77e9718b9d0cff98359a6cee8dfb192fae6fda98be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:be76328bd7233c8f860c7a18449d463769f2ce3ce9613700ff71835d6b8af100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.4 MB (611397696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad671c35671b1f60639aace57aaa83d9de4ec6d272f8e3e8f459669948bf7137`
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
# Thu, 28 May 2026 21:19:19 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:19:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:19:19 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:19:19 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:19:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:19:25 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:19:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:19:26 GMT
ENV ODOO_VERSION=17.0
# Thu, 28 May 2026 21:19:26 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:19:26 GMT
ARG ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
# Thu, 28 May 2026 21:20:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:20:19 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:20:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:20:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:20:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:20:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:20:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:20:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:20:19 GMT
USER odoo
# Thu, 28 May 2026 21:20:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:20:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c9a908bec59e30bfaf775d660c1e2d842d2e623d9e148d601912432054cabe`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 233.8 MB (233835058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a508392171167ceea13d67af3f889dbaad9ae0380e4f7d19f470047c37a74f`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 2.6 MB (2611499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7039c17552a3fbb50e23d5b33f57c8ccbd3e3bd381f2f06915074af188e16bf8`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 483.8 KB (483836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729ed212720627eb9cbc61fcbe0a7a5c36d8bce22c16d869c77d910ac972983`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 344.7 MB (344727824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c068be46d027f4772b6adb2f2178af0c6e542bf6068133bff8525648d75b1`  
		Last Modified: Thu, 28 May 2026 21:21:35 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fef691daf4995b7ca513880b0c5d32dcfbce9b77286604a994cc51dd3b66ae`  
		Last Modified: Thu, 28 May 2026 21:21:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9a2f2d0e4d1ea325a20044e0b8a63a7331ba25facf8b9acf80d9ce63a279f8`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf21c048a3356215d713ba74804e535c5fd86ce7324db0621b8f817bf7915722`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a0391fb37ae6eae0f333415f9efd59091d1618276364632c1fd19d1fbd59a4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd221811040d1e6702dbec3577a97ceab660396eb7cbcf9160eb0b3d523dddcd`

```dockerfile
```

-	Layers:
	-	`sha256:17b94913b49c61cdff5a03f74e05dba79bad209ddbba352d22fc8078a1f8a23b`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 43.1 MB (43070412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea733b81f45944ce6e391fa4e6a846a3803bd5a3d031ecbbd94e9b2139b23b9`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4300e35f5a072ef4613f08c1b4ede9e47f3d32d35b4430bc9eb4cca1f1df534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.2 MB (606220669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0e28cb1621a2b206bd9321b162ae95f8d706c3f2215130625a0d77354c784`
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
# Thu, 28 May 2026 21:18:54 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:18:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:18:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:18:54 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:18:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:19:01 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:19:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:19:02 GMT
ENV ODOO_VERSION=17.0
# Thu, 28 May 2026 21:19:02 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:19:02 GMT
ARG ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
# Thu, 28 May 2026 21:20:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:20:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:20:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:20:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:20:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:20:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:20:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:20:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:20:21 GMT
USER odoo
# Thu, 28 May 2026 21:20:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:20:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96968d3c732bb4f8a4b07b9e4dad0a50a1f509bfb1385526709c2f11bc27c574`  
		Last Modified: Thu, 28 May 2026 21:21:52 GMT  
		Size: 231.2 MB (231203414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a750e77e0cca983dfe49d7a3bf0135a1e885741a4cb37f365300346e70a931`  
		Last Modified: Thu, 28 May 2026 21:21:43 GMT  
		Size: 2.6 MB (2606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce19193af6f3912bce4ce62a7c603b5e6a03806bf0fd7d32565892b03372347`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 483.9 KB (483918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea30d33ed982ae9286ce0a6715b94f5cc16759e450ffb4de4958a52977e400`  
		Last Modified: Thu, 28 May 2026 21:21:54 GMT  
		Size: 344.3 MB (344317178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07202d9571a7340265f7fabc470c929556725a61def88a4a001039833608ad`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b124d113ac7637177caefbaedd70244d8bc07750639b0488e7fa4f9abc94fc`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44cd8c930605b9751b51de25d7219d236371d7aeb6808130ac2b74f547224a`  
		Last Modified: Thu, 28 May 2026 21:21:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f120c863e452dda70f5fefd377e50fffb51294890b7924bd00eb69bdece3f7c`  
		Last Modified: Thu, 28 May 2026 21:21:46 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1b2287fd6cc0cf338c179003f2340bead66c926a9e85f2c30af46960b1841093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43103875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd5743f2d4894c0491cd514aedf162efa665e76bde0d367b4b1d56feae92f8`

```dockerfile
```

-	Layers:
	-	`sha256:86a1214d467e056c033702a527de33eaed63c081dcc4fb9085cffc74b8634d68`  
		Last Modified: Thu, 28 May 2026 21:21:45 GMT  
		Size: 43.1 MB (43076919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be28950497bf83d0bbda0391cd710348100b5a82b8a767502f6994336d6e0fd2`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260528`

```console
$ docker pull odoo@sha256:a6815d43d76d91d4d76ace77e9718b9d0cff98359a6cee8dfb192fae6fda98be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260528` - linux; amd64

```console
$ docker pull odoo@sha256:be76328bd7233c8f860c7a18449d463769f2ce3ce9613700ff71835d6b8af100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.4 MB (611397696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad671c35671b1f60639aace57aaa83d9de4ec6d272f8e3e8f459669948bf7137`
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
# Thu, 28 May 2026 21:19:19 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:19:19 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:19:19 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:19:19 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:19:19 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:19:25 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:19:26 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:19:26 GMT
ENV ODOO_VERSION=17.0
# Thu, 28 May 2026 21:19:26 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:19:26 GMT
ARG ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
# Thu, 28 May 2026 21:20:18 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:20:19 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:20:19 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:20:19 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:20:19 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:20:19 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:20:19 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:20:19 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:20:19 GMT
USER odoo
# Thu, 28 May 2026 21:20:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:20:19 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c9a908bec59e30bfaf775d660c1e2d842d2e623d9e148d601912432054cabe`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 233.8 MB (233835058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a508392171167ceea13d67af3f889dbaad9ae0380e4f7d19f470047c37a74f`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 2.6 MB (2611499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7039c17552a3fbb50e23d5b33f57c8ccbd3e3bd381f2f06915074af188e16bf8`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 483.8 KB (483836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2729ed212720627eb9cbc61fcbe0a7a5c36d8bce22c16d869c77d910ac972983`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 344.7 MB (344727824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3c068be46d027f4772b6adb2f2178af0c6e542bf6068133bff8525648d75b1`  
		Last Modified: Thu, 28 May 2026 21:21:35 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fef691daf4995b7ca513880b0c5d32dcfbce9b77286604a994cc51dd3b66ae`  
		Last Modified: Thu, 28 May 2026 21:21:35 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9a2f2d0e4d1ea325a20044e0b8a63a7331ba25facf8b9acf80d9ce63a279f8`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf21c048a3356215d713ba74804e535c5fd86ce7324db0621b8f817bf7915722`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:a0391fb37ae6eae0f333415f9efd59091d1618276364632c1fd19d1fbd59a4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43097216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd221811040d1e6702dbec3577a97ceab660396eb7cbcf9160eb0b3d523dddcd`

```dockerfile
```

-	Layers:
	-	`sha256:17b94913b49c61cdff5a03f74e05dba79bad209ddbba352d22fc8078a1f8a23b`  
		Last Modified: Thu, 28 May 2026 21:21:36 GMT  
		Size: 43.1 MB (43070412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea733b81f45944ce6e391fa4e6a846a3803bd5a3d031ecbbd94e9b2139b23b9`  
		Last Modified: Thu, 28 May 2026 21:21:33 GMT  
		Size: 26.8 KB (26804 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260528` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:4300e35f5a072ef4613f08c1b4ede9e47f3d32d35b4430bc9eb4cca1f1df534f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.2 MB (606220669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0e28cb1621a2b206bd9321b162ae95f8d706c3f2215130625a0d77354c784`
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
# Thu, 28 May 2026 21:18:54 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:18:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:18:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:18:54 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:18:54 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:19:01 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:19:02 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:19:02 GMT
ENV ODOO_VERSION=17.0
# Thu, 28 May 2026 21:19:02 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:19:02 GMT
ARG ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
# Thu, 28 May 2026 21:20:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:20:21 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:20:21 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:20:21 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=8795e338a1ac6a5a72fffd4837c52054157602e0
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:20:21 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:20:21 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:20:21 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:20:21 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:20:21 GMT
USER odoo
# Thu, 28 May 2026 21:20:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:20:21 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96968d3c732bb4f8a4b07b9e4dad0a50a1f509bfb1385526709c2f11bc27c574`  
		Last Modified: Thu, 28 May 2026 21:21:52 GMT  
		Size: 231.2 MB (231203414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a750e77e0cca983dfe49d7a3bf0135a1e885741a4cb37f365300346e70a931`  
		Last Modified: Thu, 28 May 2026 21:21:43 GMT  
		Size: 2.6 MB (2606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce19193af6f3912bce4ce62a7c603b5e6a03806bf0fd7d32565892b03372347`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 483.9 KB (483918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea30d33ed982ae9286ce0a6715b94f5cc16759e450ffb4de4958a52977e400`  
		Last Modified: Thu, 28 May 2026 21:21:54 GMT  
		Size: 344.3 MB (344317178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec07202d9571a7340265f7fabc470c929556725a61def88a4a001039833608ad`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b124d113ac7637177caefbaedd70244d8bc07750639b0488e7fa4f9abc94fc`  
		Last Modified: Thu, 28 May 2026 21:21:44 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de44cd8c930605b9751b51de25d7219d236371d7aeb6808130ac2b74f547224a`  
		Last Modified: Thu, 28 May 2026 21:21:45 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f120c863e452dda70f5fefd377e50fffb51294890b7924bd00eb69bdece3f7c`  
		Last Modified: Thu, 28 May 2026 21:21:46 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:1b2287fd6cc0cf338c179003f2340bead66c926a9e85f2c30af46960b1841093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43103875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd5743f2d4894c0491cd514aedf162efa665e76bde0d367b4b1d56feae92f8`

```dockerfile
```

-	Layers:
	-	`sha256:86a1214d467e056c033702a527de33eaed63c081dcc4fb9085cffc74b8634d68`  
		Last Modified: Thu, 28 May 2026 21:21:45 GMT  
		Size: 43.1 MB (43076919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be28950497bf83d0bbda0391cd710348100b5a82b8a767502f6994336d6e0fd2`  
		Last Modified: Thu, 28 May 2026 21:21:42 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:98bc8790bd0147b4cd1eb668e2ac655b65434d8eb5165c1650f2f6b4a5b4d2e4
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
$ docker pull odoo@sha256:d9597f624f8731cd62c28c77b37eab40bbf1807f0910ad7df0e9b4c1aa92fe5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686737647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c375d0b69af7074a0b21e39c68220b719ca0bdf18b0134097025b48fbd539710`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:16:54 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:16:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:16:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:16:54 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:16:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:17:00 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:17:01 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:17:01 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:17:01 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:17:01 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:18:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:37 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:37 GMT
USER odoo
# Thu, 28 May 2026 21:18:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c89c7ca4209071a5ec570dadb75593672e30e62d3b984473be644a5b4863694`  
		Last Modified: Thu, 28 May 2026 21:20:32 GMT  
		Size: 254.6 MB (254598307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b517c4236772f2301d8a72c8035219d853327413669d9bfdc24d176db2a5f385`  
		Last Modified: Thu, 28 May 2026 21:20:24 GMT  
		Size: 14.4 MB (14370474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8f101ed9c64c45f5363f620de7ef0dc7003d3c98fbf621080d1e66fc3f4ea`  
		Last Modified: Thu, 28 May 2026 21:20:23 GMT  
		Size: 483.6 KB (483611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9ff5dae8684e61de52387e2c3236a9cdaff9817db56cf65a332db9d2d8889f`  
		Last Modified: Thu, 28 May 2026 21:20:35 GMT  
		Size: 387.5 MB (387549479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30ec3a2292245575390bf9b3bcef106149cb1bc4e515528f259517d83199a8a`  
		Last Modified: Thu, 28 May 2026 21:20:24 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70238d5d7c298d1c361d8588679f174cc17a204368a1e0b1a38ec4a704b5145`  
		Last Modified: Thu, 28 May 2026 21:20:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eb95e455a52af61d7dcc352ae0a934d51b83e4857164dded96fad713a57cad`  
		Last Modified: Thu, 28 May 2026 21:20:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8043c2b95ad6d4a5ec95c0ab18b4b593e3ffb4ed1a213c62ca704a40b70ee70`  
		Last Modified: Thu, 28 May 2026 21:20:27 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:9618d0ea10ff284555425b6714b4529dae9e17009294a7cdb466227a44622435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62509319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157b7b7cf735f4feb7f2c88fe38a0a3457cfc5703cf6e55dd63b068f0c0a73b`

```dockerfile
```

-	Layers:
	-	`sha256:95ea2c7105fa83593fb4b65b92b9aa43ebb787c0db0324c763ec6c85f9bca406`  
		Last Modified: Thu, 28 May 2026 21:20:26 GMT  
		Size: 62.5 MB (62482508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74734130552a96c643f0071e903bb297b112fe578b59219bdb668240b0bb5733`  
		Last Modified: Thu, 28 May 2026 21:20:23 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d059becabec264363d435277357ecb7b2fee1b35bbca06cd678dea782f10fa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 MB (683114604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26b43332eccfe140c5233cfe38eccb850a69457744af0cdffc1c59d08f76f27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:16:26 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:16:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:16:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:16:26 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:16:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:35 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:16:35 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:35 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:17:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:17:29 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:17:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:17:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:17:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:17:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:17:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:17:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:17:30 GMT
USER odoo
# Thu, 28 May 2026 21:17:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:17:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f70a91118831730337d99ab01a633194ef75a9adcea688d0c95e127b0cd991`  
		Last Modified: Thu, 28 May 2026 21:19:47 GMT  
		Size: 252.0 MB (252026618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e95b59b997937f6f4f5c344a60b62aa0d594a753822a32ec267c1606590e18a`  
		Last Modified: Thu, 28 May 2026 21:19:38 GMT  
		Size: 14.3 MB (14348858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212a9216e2e5e5f6ede20929ce7b1e936d145803ac5bceb5404f78490831ab48`  
		Last Modified: Thu, 28 May 2026 21:19:37 GMT  
		Size: 483.6 KB (483635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30123eb04ceb0154fac0b25136ece38a0325d3e06f64076af3d330c7f1392b1`  
		Last Modified: Thu, 28 May 2026 21:19:51 GMT  
		Size: 387.4 MB (387376912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7f0a8b692e9473b74e60437cba741fca53395cef0fe6996ca1e6f6011ce82f`  
		Last Modified: Thu, 28 May 2026 21:19:38 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ce4f3d886a11ce22289be8011df4ac422c3c71408696f148c1bfe861a8d2fe`  
		Last Modified: Thu, 28 May 2026 21:19:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecefd75f0eb04c675fb89b5a9b27cfc48ee07b9902435f99090297c6257808f`  
		Last Modified: Thu, 28 May 2026 21:19:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c50bfcb59a988769e08facc5f561f94dcf31cd7fdc8972f64acf30fc9fccad`  
		Last Modified: Thu, 28 May 2026 21:19:41 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:4cecea56f18f833e267654cc357fb3894794c524b31530494391784e917bf83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62516746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920124f01c7d58e9e31c1e87b8983c1140514c8981d08eea9a44b1c6ae04e06a`

```dockerfile
```

-	Layers:
	-	`sha256:ffaf7c31ce6f876f1199a997ced84b324a5fb442f7d25e51cae9a9a15ff53a0b`  
		Last Modified: Thu, 28 May 2026 21:19:41 GMT  
		Size: 62.5 MB (62489783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0b6056e5bbe6cfb90ce0053622f56afc073d912d00a5d779addc48f62d507b`  
		Last Modified: Thu, 28 May 2026 21:19:37 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:f20fce102e463b19eb25afdfe82e01ea93cbe09ed123ab4e2c728f88555a049b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702893471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaecd20b6441eac231521e3320700108fd2b10362b50858a61b08aa722a16ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:53 GMT
ARG TARGETARCH=ppc64le
# Thu, 28 May 2026 21:15:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:08 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:18:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:42 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:44 GMT
USER odoo
# Thu, 28 May 2026 21:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29150aebfcc08323e7fdcc0c134cedcad1519ca845ec21434e3a6e85df35d3`  
		Last Modified: Thu, 28 May 2026 21:23:33 GMT  
		Size: 265.1 MB (265100862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a36948866ea2ac317fd1be2db3843982f24b522111f210a3744bc359b1a36e`  
		Last Modified: Thu, 28 May 2026 21:23:22 GMT  
		Size: 14.9 MB (14900865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39faf04fb4343c25724c49e209e6d6709156436c8e6d057e03a248f3eff5d`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 483.7 KB (483671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3865628fa667ab809b8b109a281c43d580d61c2e2f1ce68d8af90c9da5b6a92`  
		Last Modified: Thu, 28 May 2026 21:23:36 GMT  
		Size: 388.1 MB (388091091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6609d10e2110df629388b1f10950c05aaacfffe955aeb3c066eb74e07c14db67`  
		Last Modified: Thu, 28 May 2026 21:23:23 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4564653c255a0e1b399754288d8913cfb47e2b7cbe387c2d1b9bb5e375655e47`  
		Last Modified: Thu, 28 May 2026 21:23:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cafa4cfcc929c1c8d05c94e41ad1ed241c4f1e974f0e670683a0f599f98f1e`  
		Last Modified: Thu, 28 May 2026 21:23:24 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a18879fbb68df8f6f704c1aa5194c91a2ef459d122e1725148eb31273b435fc`  
		Last Modified: Thu, 28 May 2026 21:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:eaeb21e460413a61c63e2fd3badb233dcff2d9061ed917cb165a69cd2a42c6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62517758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635d65d0d23e36312c8f0289203d7977c88da679a234e59250d45f69336051d3`

```dockerfile
```

-	Layers:
	-	`sha256:9a546551e7881dfaf5bba44b5ffcb937bd0685de03fb423ce7332678cf182063`  
		Last Modified: Thu, 28 May 2026 21:23:25 GMT  
		Size: 62.5 MB (62490891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea52638be7c4c81eb08ac00c1f1b304eb5d1d49a6f67eb0c2d3505c56458200`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:98bc8790bd0147b4cd1eb668e2ac655b65434d8eb5165c1650f2f6b4a5b4d2e4
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
$ docker pull odoo@sha256:d9597f624f8731cd62c28c77b37eab40bbf1807f0910ad7df0e9b4c1aa92fe5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686737647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c375d0b69af7074a0b21e39c68220b719ca0bdf18b0134097025b48fbd539710`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:16:54 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:16:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:16:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:16:54 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:16:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:17:00 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:17:01 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:17:01 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:17:01 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:17:01 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:18:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:37 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:37 GMT
USER odoo
# Thu, 28 May 2026 21:18:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c89c7ca4209071a5ec570dadb75593672e30e62d3b984473be644a5b4863694`  
		Last Modified: Thu, 28 May 2026 21:20:32 GMT  
		Size: 254.6 MB (254598307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b517c4236772f2301d8a72c8035219d853327413669d9bfdc24d176db2a5f385`  
		Last Modified: Thu, 28 May 2026 21:20:24 GMT  
		Size: 14.4 MB (14370474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8f101ed9c64c45f5363f620de7ef0dc7003d3c98fbf621080d1e66fc3f4ea`  
		Last Modified: Thu, 28 May 2026 21:20:23 GMT  
		Size: 483.6 KB (483611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9ff5dae8684e61de52387e2c3236a9cdaff9817db56cf65a332db9d2d8889f`  
		Last Modified: Thu, 28 May 2026 21:20:35 GMT  
		Size: 387.5 MB (387549479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30ec3a2292245575390bf9b3bcef106149cb1bc4e515528f259517d83199a8a`  
		Last Modified: Thu, 28 May 2026 21:20:24 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70238d5d7c298d1c361d8588679f174cc17a204368a1e0b1a38ec4a704b5145`  
		Last Modified: Thu, 28 May 2026 21:20:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eb95e455a52af61d7dcc352ae0a934d51b83e4857164dded96fad713a57cad`  
		Last Modified: Thu, 28 May 2026 21:20:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8043c2b95ad6d4a5ec95c0ab18b4b593e3ffb4ed1a213c62ca704a40b70ee70`  
		Last Modified: Thu, 28 May 2026 21:20:27 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:9618d0ea10ff284555425b6714b4529dae9e17009294a7cdb466227a44622435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62509319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157b7b7cf735f4feb7f2c88fe38a0a3457cfc5703cf6e55dd63b068f0c0a73b`

```dockerfile
```

-	Layers:
	-	`sha256:95ea2c7105fa83593fb4b65b92b9aa43ebb787c0db0324c763ec6c85f9bca406`  
		Last Modified: Thu, 28 May 2026 21:20:26 GMT  
		Size: 62.5 MB (62482508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74734130552a96c643f0071e903bb297b112fe578b59219bdb668240b0bb5733`  
		Last Modified: Thu, 28 May 2026 21:20:23 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d059becabec264363d435277357ecb7b2fee1b35bbca06cd678dea782f10fa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 MB (683114604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26b43332eccfe140c5233cfe38eccb850a69457744af0cdffc1c59d08f76f27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:16:26 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:16:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:16:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:16:26 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:16:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:35 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:16:35 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:35 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:17:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:17:29 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:17:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:17:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:17:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:17:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:17:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:17:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:17:30 GMT
USER odoo
# Thu, 28 May 2026 21:17:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:17:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f70a91118831730337d99ab01a633194ef75a9adcea688d0c95e127b0cd991`  
		Last Modified: Thu, 28 May 2026 21:19:47 GMT  
		Size: 252.0 MB (252026618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e95b59b997937f6f4f5c344a60b62aa0d594a753822a32ec267c1606590e18a`  
		Last Modified: Thu, 28 May 2026 21:19:38 GMT  
		Size: 14.3 MB (14348858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212a9216e2e5e5f6ede20929ce7b1e936d145803ac5bceb5404f78490831ab48`  
		Last Modified: Thu, 28 May 2026 21:19:37 GMT  
		Size: 483.6 KB (483635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30123eb04ceb0154fac0b25136ece38a0325d3e06f64076af3d330c7f1392b1`  
		Last Modified: Thu, 28 May 2026 21:19:51 GMT  
		Size: 387.4 MB (387376912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7f0a8b692e9473b74e60437cba741fca53395cef0fe6996ca1e6f6011ce82f`  
		Last Modified: Thu, 28 May 2026 21:19:38 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ce4f3d886a11ce22289be8011df4ac422c3c71408696f148c1bfe861a8d2fe`  
		Last Modified: Thu, 28 May 2026 21:19:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecefd75f0eb04c675fb89b5a9b27cfc48ee07b9902435f99090297c6257808f`  
		Last Modified: Thu, 28 May 2026 21:19:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c50bfcb59a988769e08facc5f561f94dcf31cd7fdc8972f64acf30fc9fccad`  
		Last Modified: Thu, 28 May 2026 21:19:41 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4cecea56f18f833e267654cc357fb3894794c524b31530494391784e917bf83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62516746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920124f01c7d58e9e31c1e87b8983c1140514c8981d08eea9a44b1c6ae04e06a`

```dockerfile
```

-	Layers:
	-	`sha256:ffaf7c31ce6f876f1199a997ced84b324a5fb442f7d25e51cae9a9a15ff53a0b`  
		Last Modified: Thu, 28 May 2026 21:19:41 GMT  
		Size: 62.5 MB (62489783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0b6056e5bbe6cfb90ce0053622f56afc073d912d00a5d779addc48f62d507b`  
		Last Modified: Thu, 28 May 2026 21:19:37 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:f20fce102e463b19eb25afdfe82e01ea93cbe09ed123ab4e2c728f88555a049b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702893471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaecd20b6441eac231521e3320700108fd2b10362b50858a61b08aa722a16ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:53 GMT
ARG TARGETARCH=ppc64le
# Thu, 28 May 2026 21:15:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:08 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:18:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:42 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:44 GMT
USER odoo
# Thu, 28 May 2026 21:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29150aebfcc08323e7fdcc0c134cedcad1519ca845ec21434e3a6e85df35d3`  
		Last Modified: Thu, 28 May 2026 21:23:33 GMT  
		Size: 265.1 MB (265100862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a36948866ea2ac317fd1be2db3843982f24b522111f210a3744bc359b1a36e`  
		Last Modified: Thu, 28 May 2026 21:23:22 GMT  
		Size: 14.9 MB (14900865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39faf04fb4343c25724c49e209e6d6709156436c8e6d057e03a248f3eff5d`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 483.7 KB (483671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3865628fa667ab809b8b109a281c43d580d61c2e2f1ce68d8af90c9da5b6a92`  
		Last Modified: Thu, 28 May 2026 21:23:36 GMT  
		Size: 388.1 MB (388091091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6609d10e2110df629388b1f10950c05aaacfffe955aeb3c066eb74e07c14db67`  
		Last Modified: Thu, 28 May 2026 21:23:23 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4564653c255a0e1b399754288d8913cfb47e2b7cbe387c2d1b9bb5e375655e47`  
		Last Modified: Thu, 28 May 2026 21:23:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cafa4cfcc929c1c8d05c94e41ad1ed241c4f1e974f0e670683a0f599f98f1e`  
		Last Modified: Thu, 28 May 2026 21:23:24 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a18879fbb68df8f6f704c1aa5194c91a2ef459d122e1725148eb31273b435fc`  
		Last Modified: Thu, 28 May 2026 21:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:eaeb21e460413a61c63e2fd3badb233dcff2d9061ed917cb165a69cd2a42c6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62517758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635d65d0d23e36312c8f0289203d7977c88da679a234e59250d45f69336051d3`

```dockerfile
```

-	Layers:
	-	`sha256:9a546551e7881dfaf5bba44b5ffcb937bd0685de03fb423ce7332678cf182063`  
		Last Modified: Thu, 28 May 2026 21:23:25 GMT  
		Size: 62.5 MB (62490891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea52638be7c4c81eb08ac00c1f1b304eb5d1d49a6f67eb0c2d3505c56458200`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260528`

```console
$ docker pull odoo@sha256:98bc8790bd0147b4cd1eb668e2ac655b65434d8eb5165c1650f2f6b4a5b4d2e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260528` - linux; amd64

```console
$ docker pull odoo@sha256:d9597f624f8731cd62c28c77b37eab40bbf1807f0910ad7df0e9b4c1aa92fe5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686737647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c375d0b69af7074a0b21e39c68220b719ca0bdf18b0134097025b48fbd539710`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:16:54 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:16:54 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:16:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:16:54 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:16:54 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:17:00 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:17:01 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:17:01 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:17:01 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:17:01 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:18:36 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:37 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:37 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:37 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:37 GMT
USER odoo
# Thu, 28 May 2026 21:18:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c89c7ca4209071a5ec570dadb75593672e30e62d3b984473be644a5b4863694`  
		Last Modified: Thu, 28 May 2026 21:20:32 GMT  
		Size: 254.6 MB (254598307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b517c4236772f2301d8a72c8035219d853327413669d9bfdc24d176db2a5f385`  
		Last Modified: Thu, 28 May 2026 21:20:24 GMT  
		Size: 14.4 MB (14370474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8f101ed9c64c45f5363f620de7ef0dc7003d3c98fbf621080d1e66fc3f4ea`  
		Last Modified: Thu, 28 May 2026 21:20:23 GMT  
		Size: 483.6 KB (483611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9ff5dae8684e61de52387e2c3236a9cdaff9817db56cf65a332db9d2d8889f`  
		Last Modified: Thu, 28 May 2026 21:20:35 GMT  
		Size: 387.5 MB (387549479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30ec3a2292245575390bf9b3bcef106149cb1bc4e515528f259517d83199a8a`  
		Last Modified: Thu, 28 May 2026 21:20:24 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70238d5d7c298d1c361d8588679f174cc17a204368a1e0b1a38ec4a704b5145`  
		Last Modified: Thu, 28 May 2026 21:20:25 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eb95e455a52af61d7dcc352ae0a934d51b83e4857164dded96fad713a57cad`  
		Last Modified: Thu, 28 May 2026 21:20:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8043c2b95ad6d4a5ec95c0ab18b4b593e3ffb4ed1a213c62ca704a40b70ee70`  
		Last Modified: Thu, 28 May 2026 21:20:27 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:9618d0ea10ff284555425b6714b4529dae9e17009294a7cdb466227a44622435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62509319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157b7b7cf735f4feb7f2c88fe38a0a3457cfc5703cf6e55dd63b068f0c0a73b`

```dockerfile
```

-	Layers:
	-	`sha256:95ea2c7105fa83593fb4b65b92b9aa43ebb787c0db0324c763ec6c85f9bca406`  
		Last Modified: Thu, 28 May 2026 21:20:26 GMT  
		Size: 62.5 MB (62482508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74734130552a96c643f0071e903bb297b112fe578b59219bdb668240b0bb5733`  
		Last Modified: Thu, 28 May 2026 21:20:23 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260528` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:d059becabec264363d435277357ecb7b2fee1b35bbca06cd678dea782f10fa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 MB (683114604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26b43332eccfe140c5233cfe38eccb850a69457744af0cdffc1c59d08f76f27`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:16:26 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:16:26 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:16:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:16:26 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:16:26 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:35 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:35 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:16:35 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:35 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:17:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:17:29 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:17:29 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:17:29 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:17:29 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:17:29 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:17:29 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:17:30 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:17:30 GMT
USER odoo
# Thu, 28 May 2026 21:17:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:17:30 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f70a91118831730337d99ab01a633194ef75a9adcea688d0c95e127b0cd991`  
		Last Modified: Thu, 28 May 2026 21:19:47 GMT  
		Size: 252.0 MB (252026618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e95b59b997937f6f4f5c344a60b62aa0d594a753822a32ec267c1606590e18a`  
		Last Modified: Thu, 28 May 2026 21:19:38 GMT  
		Size: 14.3 MB (14348858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212a9216e2e5e5f6ede20929ce7b1e936d145803ac5bceb5404f78490831ab48`  
		Last Modified: Thu, 28 May 2026 21:19:37 GMT  
		Size: 483.6 KB (483635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30123eb04ceb0154fac0b25136ece38a0325d3e06f64076af3d330c7f1392b1`  
		Last Modified: Thu, 28 May 2026 21:19:51 GMT  
		Size: 387.4 MB (387376912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7f0a8b692e9473b74e60437cba741fca53395cef0fe6996ca1e6f6011ce82f`  
		Last Modified: Thu, 28 May 2026 21:19:38 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ce4f3d886a11ce22289be8011df4ac422c3c71408696f148c1bfe861a8d2fe`  
		Last Modified: Thu, 28 May 2026 21:19:39 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecefd75f0eb04c675fb89b5a9b27cfc48ee07b9902435f99090297c6257808f`  
		Last Modified: Thu, 28 May 2026 21:19:40 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c50bfcb59a988769e08facc5f561f94dcf31cd7fdc8972f64acf30fc9fccad`  
		Last Modified: Thu, 28 May 2026 21:19:41 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:4cecea56f18f833e267654cc357fb3894794c524b31530494391784e917bf83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62516746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920124f01c7d58e9e31c1e87b8983c1140514c8981d08eea9a44b1c6ae04e06a`

```dockerfile
```

-	Layers:
	-	`sha256:ffaf7c31ce6f876f1199a997ced84b324a5fb442f7d25e51cae9a9a15ff53a0b`  
		Last Modified: Thu, 28 May 2026 21:19:41 GMT  
		Size: 62.5 MB (62489783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0b6056e5bbe6cfb90ce0053622f56afc073d912d00a5d779addc48f62d507b`  
		Last Modified: Thu, 28 May 2026 21:19:37 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260528` - linux; ppc64le

```console
$ docker pull odoo@sha256:f20fce102e463b19eb25afdfe82e01ea93cbe09ed123ab4e2c728f88555a049b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702893471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaaecd20b6441eac231521e3320700108fd2b10362b50858a61b08aa722a16ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:53 GMT
ARG TARGETARCH=ppc64le
# Thu, 28 May 2026 21:15:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:08 GMT
ENV ODOO_VERSION=18.0
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Thu, 28 May 2026 21:18:41 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:42 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:43 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:43 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:43 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:43 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:43 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:44 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:44 GMT
USER odoo
# Thu, 28 May 2026 21:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:44 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29150aebfcc08323e7fdcc0c134cedcad1519ca845ec21434e3a6e85df35d3`  
		Last Modified: Thu, 28 May 2026 21:23:33 GMT  
		Size: 265.1 MB (265100862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a36948866ea2ac317fd1be2db3843982f24b522111f210a3744bc359b1a36e`  
		Last Modified: Thu, 28 May 2026 21:23:22 GMT  
		Size: 14.9 MB (14900865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39faf04fb4343c25724c49e209e6d6709156436c8e6d057e03a248f3eff5d`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 483.7 KB (483671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3865628fa667ab809b8b109a281c43d580d61c2e2f1ce68d8af90c9da5b6a92`  
		Last Modified: Thu, 28 May 2026 21:23:36 GMT  
		Size: 388.1 MB (388091091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6609d10e2110df629388b1f10950c05aaacfffe955aeb3c066eb74e07c14db67`  
		Last Modified: Thu, 28 May 2026 21:23:23 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4564653c255a0e1b399754288d8913cfb47e2b7cbe387c2d1b9bb5e375655e47`  
		Last Modified: Thu, 28 May 2026 21:23:23 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cafa4cfcc929c1c8d05c94e41ad1ed241c4f1e974f0e670683a0f599f98f1e`  
		Last Modified: Thu, 28 May 2026 21:23:24 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a18879fbb68df8f6f704c1aa5194c91a2ef459d122e1725148eb31273b435fc`  
		Last Modified: Thu, 28 May 2026 21:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:eaeb21e460413a61c63e2fd3badb233dcff2d9061ed917cb165a69cd2a42c6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62517758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635d65d0d23e36312c8f0289203d7977c88da679a234e59250d45f69336051d3`

```dockerfile
```

-	Layers:
	-	`sha256:9a546551e7881dfaf5bba44b5ffcb937bd0685de03fb423ce7332678cf182063`  
		Last Modified: Thu, 28 May 2026 21:23:25 GMT  
		Size: 62.5 MB (62490891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea52638be7c4c81eb08ac00c1f1b304eb5d1d49a6f67eb0c2d3505c56458200`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:59e9031dddd179ef0138483bac20e391c3e39bb1173dc0be70c7a944ed532487
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
$ docker pull odoo@sha256:55b0bb3dd8ee451ea39e508e604f34cdbd0cd4e954a458534a49f0bc79334fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705245477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed137bec4d66a8ba94632055f965327b5c21c1381828414a2ce61004154b99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:03 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:15:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:10 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:11 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:15 GMT
USER odoo
# Thu, 28 May 2026 21:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d101d2b00fe118bd945707d66e8778f27a33a633a21fd19d3e8380578380df2`  
		Last Modified: Thu, 28 May 2026 21:18:34 GMT  
		Size: 254.6 MB (254597720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0dac29446c76c06544f82fb71d82fbc99cfba16fc2ca628b30706edd3a6bee`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 14.4 MB (14370420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9f1fbe37dd1b8a56b21866723a47ba4c77930c3340f703c038c8299df20d1`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 483.7 KB (483664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499289b0963d3b81aacd59e63f66b61b5bbf459586950e2078e23dfdd8d5764`  
		Last Modified: Thu, 28 May 2026 21:18:41 GMT  
		Size: 406.1 MB (406057948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f98c0ee3f0249bf5727bcabf78e0e97bdb348859ea21457b1aa655f122002f`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eec0baa569902e43c84b1cec83124e42d43cea961296ba36b7da500886406e`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167b9f0fe1119cab5ff7c4633619e84553014f75931fa5b0498f780d6082c920`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:f7562e650dd7ad498045b1e8a0fa9b7c1be076391b22f4d6675eee415ca7fe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8776a08cdb09658cba90fcb311d114542d7ebc4f99e926af2b1f77665ce221e6`

```dockerfile
```

-	Layers:
	-	`sha256:08fd13edde1d950271887e146d560b71e73d76cb8427d9c117292232e6365c3e`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 70.7 MB (70673256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4f7e05785bc9e886fe2590276d2339e56f7e1a31aec9e7e231c6fd8804b9be`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5c43fe77e8c4af2c496afd511af68b7014ed95e6cf4219d78d11fd4b700b4713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701614831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fa96fb678d9f0493fb78a49d9bc43a39870487772cd8e9318e97eb81cc65ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:07 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:07 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:15:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:15 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:25 GMT
USER odoo
# Thu, 28 May 2026 21:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad0f83ef124c3a8b0a66fa96de3c1dd7ef623051c0dd912b8b5440fb886d047`  
		Last Modified: Thu, 28 May 2026 21:19:20 GMT  
		Size: 252.0 MB (252027005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1854407fd02a3c3fdbfb3aeb62bee81378239f01a7727276797b7fbbaef6f8b`  
		Last Modified: Thu, 28 May 2026 21:19:12 GMT  
		Size: 14.3 MB (14348830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8226e5e72dbdea19a8cd45329e6c22761bb00307e82bdb5ed89e7c084f02c293`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 483.6 KB (483617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f7dffc443fa56e846e54fbb456beb8c9141e8bbfb9aa45e7fddb7f32543010`  
		Last Modified: Thu, 28 May 2026 21:19:28 GMT  
		Size: 405.9 MB (405876844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34b88b7ce7a2d78f8ae8611cc87742934608e72dafa73774494a4ba95f4877c`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404adfd6c5dbc559c07e98056aada695c9434296a1ce9b66f1afda76ec1a2ed`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5898fbac2a61dc9149b653e5b6d31a9498cb4a1dc9b46bf2a828a4fd1ad8a76b`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:d50a48b53493574e2a3c0e427b7fdcfe53ad6bf8aff24ed38dbccb8e11b31b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a986a5365de493eb7b07124c4448fcc63c4e3ddaaaacd5d1a93c41a6665876f6`

```dockerfile
```

-	Layers:
	-	`sha256:521b5b097e5c52cd4ddd94aad142695736017d5bbced3d6e097d750b53e8bcc6`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 70.7 MB (70680543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b020873f4e2621f1d5740a675f11e847c7f9390466d7de420e99983f2eab9cb`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:1a0577918b515a086480c22f248de53bbca42d1e00d11d85a512fa1b1bc2a3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721394078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c60d1913f3ca297ea41a8dd7312cf2a7a2ac6113fffe949e821e5a36ff48ae7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:53 GMT
ARG TARGETARCH=ppc64le
# Thu, 28 May 2026 21:15:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:08 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:18:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:59 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:59 GMT
USER odoo
# Thu, 28 May 2026 21:18:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29150aebfcc08323e7fdcc0c134cedcad1519ca845ec21434e3a6e85df35d3`  
		Last Modified: Thu, 28 May 2026 21:23:33 GMT  
		Size: 265.1 MB (265100862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a36948866ea2ac317fd1be2db3843982f24b522111f210a3744bc359b1a36e`  
		Last Modified: Thu, 28 May 2026 21:23:22 GMT  
		Size: 14.9 MB (14900865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39faf04fb4343c25724c49e209e6d6709156436c8e6d057e03a248f3eff5d`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 483.7 KB (483671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a18548ac7ededa9575d497acaf6913681cf1522fa238fb156b3f6bc99ff80`  
		Last Modified: Thu, 28 May 2026 21:25:05 GMT  
		Size: 406.6 MB (406591746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f88be2111530fcbe7f9937f3eb30a98c2f784fa0cec28698e7453a3a939b9c`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2780fddf75d95ca5e5d68b26f80020173c96206a3cee55f00013dcb2f26e9`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176fefe67793953740695f03079d840b92f19277a7aec9e74a76453f6c1a8da6`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1e55f99fb56f634e540924a2a0a14a679bef36c7886085153883b75b7780c`  
		Last Modified: Thu, 28 May 2026 21:24:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:1f61b2f6f4d154bebaa47abe4479400a2797e5beccf96970b2be411497c8c312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3611cfe45554bc47c2b4c052bda0433c5cb495d643f5b4b0db0bfae642c4cdcc`

```dockerfile
```

-	Layers:
	-	`sha256:f33c47f4274ded9b83db68673229189d5c754f55903ad15bb300198969ebafbd`  
		Last Modified: Thu, 28 May 2026 21:24:57 GMT  
		Size: 70.7 MB (70681645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e94554c621255d0e66e003cc6d95abf4659b3584fb22dd4c6abb2f883761c39`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:59e9031dddd179ef0138483bac20e391c3e39bb1173dc0be70c7a944ed532487
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
$ docker pull odoo@sha256:55b0bb3dd8ee451ea39e508e604f34cdbd0cd4e954a458534a49f0bc79334fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705245477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed137bec4d66a8ba94632055f965327b5c21c1381828414a2ce61004154b99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:03 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:15:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:10 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:11 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:15 GMT
USER odoo
# Thu, 28 May 2026 21:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d101d2b00fe118bd945707d66e8778f27a33a633a21fd19d3e8380578380df2`  
		Last Modified: Thu, 28 May 2026 21:18:34 GMT  
		Size: 254.6 MB (254597720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0dac29446c76c06544f82fb71d82fbc99cfba16fc2ca628b30706edd3a6bee`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 14.4 MB (14370420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9f1fbe37dd1b8a56b21866723a47ba4c77930c3340f703c038c8299df20d1`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 483.7 KB (483664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499289b0963d3b81aacd59e63f66b61b5bbf459586950e2078e23dfdd8d5764`  
		Last Modified: Thu, 28 May 2026 21:18:41 GMT  
		Size: 406.1 MB (406057948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f98c0ee3f0249bf5727bcabf78e0e97bdb348859ea21457b1aa655f122002f`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eec0baa569902e43c84b1cec83124e42d43cea961296ba36b7da500886406e`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167b9f0fe1119cab5ff7c4633619e84553014f75931fa5b0498f780d6082c920`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f7562e650dd7ad498045b1e8a0fa9b7c1be076391b22f4d6675eee415ca7fe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8776a08cdb09658cba90fcb311d114542d7ebc4f99e926af2b1f77665ce221e6`

```dockerfile
```

-	Layers:
	-	`sha256:08fd13edde1d950271887e146d560b71e73d76cb8427d9c117292232e6365c3e`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 70.7 MB (70673256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4f7e05785bc9e886fe2590276d2339e56f7e1a31aec9e7e231c6fd8804b9be`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5c43fe77e8c4af2c496afd511af68b7014ed95e6cf4219d78d11fd4b700b4713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701614831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fa96fb678d9f0493fb78a49d9bc43a39870487772cd8e9318e97eb81cc65ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:07 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:07 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:15:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:15 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:25 GMT
USER odoo
# Thu, 28 May 2026 21:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad0f83ef124c3a8b0a66fa96de3c1dd7ef623051c0dd912b8b5440fb886d047`  
		Last Modified: Thu, 28 May 2026 21:19:20 GMT  
		Size: 252.0 MB (252027005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1854407fd02a3c3fdbfb3aeb62bee81378239f01a7727276797b7fbbaef6f8b`  
		Last Modified: Thu, 28 May 2026 21:19:12 GMT  
		Size: 14.3 MB (14348830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8226e5e72dbdea19a8cd45329e6c22761bb00307e82bdb5ed89e7c084f02c293`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 483.6 KB (483617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f7dffc443fa56e846e54fbb456beb8c9141e8bbfb9aa45e7fddb7f32543010`  
		Last Modified: Thu, 28 May 2026 21:19:28 GMT  
		Size: 405.9 MB (405876844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34b88b7ce7a2d78f8ae8611cc87742934608e72dafa73774494a4ba95f4877c`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404adfd6c5dbc559c07e98056aada695c9434296a1ce9b66f1afda76ec1a2ed`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5898fbac2a61dc9149b653e5b6d31a9498cb4a1dc9b46bf2a828a4fd1ad8a76b`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d50a48b53493574e2a3c0e427b7fdcfe53ad6bf8aff24ed38dbccb8e11b31b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a986a5365de493eb7b07124c4448fcc63c4e3ddaaaacd5d1a93c41a6665876f6`

```dockerfile
```

-	Layers:
	-	`sha256:521b5b097e5c52cd4ddd94aad142695736017d5bbced3d6e097d750b53e8bcc6`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 70.7 MB (70680543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b020873f4e2621f1d5740a675f11e847c7f9390466d7de420e99983f2eab9cb`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:1a0577918b515a086480c22f248de53bbca42d1e00d11d85a512fa1b1bc2a3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721394078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c60d1913f3ca297ea41a8dd7312cf2a7a2ac6113fffe949e821e5a36ff48ae7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:53 GMT
ARG TARGETARCH=ppc64le
# Thu, 28 May 2026 21:15:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:08 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:18:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:59 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:59 GMT
USER odoo
# Thu, 28 May 2026 21:18:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29150aebfcc08323e7fdcc0c134cedcad1519ca845ec21434e3a6e85df35d3`  
		Last Modified: Thu, 28 May 2026 21:23:33 GMT  
		Size: 265.1 MB (265100862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a36948866ea2ac317fd1be2db3843982f24b522111f210a3744bc359b1a36e`  
		Last Modified: Thu, 28 May 2026 21:23:22 GMT  
		Size: 14.9 MB (14900865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39faf04fb4343c25724c49e209e6d6709156436c8e6d057e03a248f3eff5d`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 483.7 KB (483671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a18548ac7ededa9575d497acaf6913681cf1522fa238fb156b3f6bc99ff80`  
		Last Modified: Thu, 28 May 2026 21:25:05 GMT  
		Size: 406.6 MB (406591746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f88be2111530fcbe7f9937f3eb30a98c2f784fa0cec28698e7453a3a939b9c`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2780fddf75d95ca5e5d68b26f80020173c96206a3cee55f00013dcb2f26e9`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176fefe67793953740695f03079d840b92f19277a7aec9e74a76453f6c1a8da6`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1e55f99fb56f634e540924a2a0a14a679bef36c7886085153883b75b7780c`  
		Last Modified: Thu, 28 May 2026 21:24:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:1f61b2f6f4d154bebaa47abe4479400a2797e5beccf96970b2be411497c8c312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3611cfe45554bc47c2b4c052bda0433c5cb495d643f5b4b0db0bfae642c4cdcc`

```dockerfile
```

-	Layers:
	-	`sha256:f33c47f4274ded9b83db68673229189d5c754f55903ad15bb300198969ebafbd`  
		Last Modified: Thu, 28 May 2026 21:24:57 GMT  
		Size: 70.7 MB (70681645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e94554c621255d0e66e003cc6d95abf4659b3584fb22dd4c6abb2f883761c39`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260528`

```console
$ docker pull odoo@sha256:59e9031dddd179ef0138483bac20e391c3e39bb1173dc0be70c7a944ed532487
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260528` - linux; amd64

```console
$ docker pull odoo@sha256:55b0bb3dd8ee451ea39e508e604f34cdbd0cd4e954a458534a49f0bc79334fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705245477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed137bec4d66a8ba94632055f965327b5c21c1381828414a2ce61004154b99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:03 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:15:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:10 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:11 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:15 GMT
USER odoo
# Thu, 28 May 2026 21:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d101d2b00fe118bd945707d66e8778f27a33a633a21fd19d3e8380578380df2`  
		Last Modified: Thu, 28 May 2026 21:18:34 GMT  
		Size: 254.6 MB (254597720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0dac29446c76c06544f82fb71d82fbc99cfba16fc2ca628b30706edd3a6bee`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 14.4 MB (14370420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9f1fbe37dd1b8a56b21866723a47ba4c77930c3340f703c038c8299df20d1`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 483.7 KB (483664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499289b0963d3b81aacd59e63f66b61b5bbf459586950e2078e23dfdd8d5764`  
		Last Modified: Thu, 28 May 2026 21:18:41 GMT  
		Size: 406.1 MB (406057948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f98c0ee3f0249bf5727bcabf78e0e97bdb348859ea21457b1aa655f122002f`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eec0baa569902e43c84b1cec83124e42d43cea961296ba36b7da500886406e`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167b9f0fe1119cab5ff7c4633619e84553014f75931fa5b0498f780d6082c920`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:f7562e650dd7ad498045b1e8a0fa9b7c1be076391b22f4d6675eee415ca7fe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8776a08cdb09658cba90fcb311d114542d7ebc4f99e926af2b1f77665ce221e6`

```dockerfile
```

-	Layers:
	-	`sha256:08fd13edde1d950271887e146d560b71e73d76cb8427d9c117292232e6365c3e`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 70.7 MB (70673256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4f7e05785bc9e886fe2590276d2339e56f7e1a31aec9e7e231c6fd8804b9be`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260528` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5c43fe77e8c4af2c496afd511af68b7014ed95e6cf4219d78d11fd4b700b4713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701614831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fa96fb678d9f0493fb78a49d9bc43a39870487772cd8e9318e97eb81cc65ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:07 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:07 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:15:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:15 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:25 GMT
USER odoo
# Thu, 28 May 2026 21:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad0f83ef124c3a8b0a66fa96de3c1dd7ef623051c0dd912b8b5440fb886d047`  
		Last Modified: Thu, 28 May 2026 21:19:20 GMT  
		Size: 252.0 MB (252027005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1854407fd02a3c3fdbfb3aeb62bee81378239f01a7727276797b7fbbaef6f8b`  
		Last Modified: Thu, 28 May 2026 21:19:12 GMT  
		Size: 14.3 MB (14348830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8226e5e72dbdea19a8cd45329e6c22761bb00307e82bdb5ed89e7c084f02c293`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 483.6 KB (483617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f7dffc443fa56e846e54fbb456beb8c9141e8bbfb9aa45e7fddb7f32543010`  
		Last Modified: Thu, 28 May 2026 21:19:28 GMT  
		Size: 405.9 MB (405876844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34b88b7ce7a2d78f8ae8611cc87742934608e72dafa73774494a4ba95f4877c`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404adfd6c5dbc559c07e98056aada695c9434296a1ce9b66f1afda76ec1a2ed`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5898fbac2a61dc9149b653e5b6d31a9498cb4a1dc9b46bf2a828a4fd1ad8a76b`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:d50a48b53493574e2a3c0e427b7fdcfe53ad6bf8aff24ed38dbccb8e11b31b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a986a5365de493eb7b07124c4448fcc63c4e3ddaaaacd5d1a93c41a6665876f6`

```dockerfile
```

-	Layers:
	-	`sha256:521b5b097e5c52cd4ddd94aad142695736017d5bbced3d6e097d750b53e8bcc6`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 70.7 MB (70680543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b020873f4e2621f1d5740a675f11e847c7f9390466d7de420e99983f2eab9cb`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260528` - linux; ppc64le

```console
$ docker pull odoo@sha256:1a0577918b515a086480c22f248de53bbca42d1e00d11d85a512fa1b1bc2a3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721394078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c60d1913f3ca297ea41a8dd7312cf2a7a2ac6113fffe949e821e5a36ff48ae7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:53 GMT
ARG TARGETARCH=ppc64le
# Thu, 28 May 2026 21:15:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:08 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:18:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:59 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:59 GMT
USER odoo
# Thu, 28 May 2026 21:18:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29150aebfcc08323e7fdcc0c134cedcad1519ca845ec21434e3a6e85df35d3`  
		Last Modified: Thu, 28 May 2026 21:23:33 GMT  
		Size: 265.1 MB (265100862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a36948866ea2ac317fd1be2db3843982f24b522111f210a3744bc359b1a36e`  
		Last Modified: Thu, 28 May 2026 21:23:22 GMT  
		Size: 14.9 MB (14900865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39faf04fb4343c25724c49e209e6d6709156436c8e6d057e03a248f3eff5d`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 483.7 KB (483671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a18548ac7ededa9575d497acaf6913681cf1522fa238fb156b3f6bc99ff80`  
		Last Modified: Thu, 28 May 2026 21:25:05 GMT  
		Size: 406.6 MB (406591746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f88be2111530fcbe7f9937f3eb30a98c2f784fa0cec28698e7453a3a939b9c`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2780fddf75d95ca5e5d68b26f80020173c96206a3cee55f00013dcb2f26e9`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176fefe67793953740695f03079d840b92f19277a7aec9e74a76453f6c1a8da6`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1e55f99fb56f634e540924a2a0a14a679bef36c7886085153883b75b7780c`  
		Last Modified: Thu, 28 May 2026 21:24:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:1f61b2f6f4d154bebaa47abe4479400a2797e5beccf96970b2be411497c8c312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3611cfe45554bc47c2b4c052bda0433c5cb495d643f5b4b0db0bfae642c4cdcc`

```dockerfile
```

-	Layers:
	-	`sha256:f33c47f4274ded9b83db68673229189d5c754f55903ad15bb300198969ebafbd`  
		Last Modified: Thu, 28 May 2026 21:24:57 GMT  
		Size: 70.7 MB (70681645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e94554c621255d0e66e003cc6d95abf4659b3584fb22dd4c6abb2f883761c39`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:59e9031dddd179ef0138483bac20e391c3e39bb1173dc0be70c7a944ed532487
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
$ docker pull odoo@sha256:55b0bb3dd8ee451ea39e508e604f34cdbd0cd4e954a458534a49f0bc79334fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705245477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ed137bec4d66a8ba94632055f965327b5c21c1381828414a2ce61004154b99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:03 GMT
ARG TARGETARCH=amd64
# Thu, 28 May 2026 21:15:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:10 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:11 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:11 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:11 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:14 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:15 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:15 GMT
USER odoo
# Thu, 28 May 2026 21:16:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d101d2b00fe118bd945707d66e8778f27a33a633a21fd19d3e8380578380df2`  
		Last Modified: Thu, 28 May 2026 21:18:34 GMT  
		Size: 254.6 MB (254597720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0dac29446c76c06544f82fb71d82fbc99cfba16fc2ca628b30706edd3a6bee`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 14.4 MB (14370420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9f1fbe37dd1b8a56b21866723a47ba4c77930c3340f703c038c8299df20d1`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 483.7 KB (483664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9499289b0963d3b81aacd59e63f66b61b5bbf459586950e2078e23dfdd8d5764`  
		Last Modified: Thu, 28 May 2026 21:18:41 GMT  
		Size: 406.1 MB (406057948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f98c0ee3f0249bf5727bcabf78e0e97bdb348859ea21457b1aa655f122002f`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eec0baa569902e43c84b1cec83124e42d43cea961296ba36b7da500886406e`  
		Last Modified: Thu, 28 May 2026 21:18:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167b9f0fe1119cab5ff7c4633619e84553014f75931fa5b0498f780d6082c920`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f7562e650dd7ad498045b1e8a0fa9b7c1be076391b22f4d6675eee415ca7fe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8776a08cdb09658cba90fcb311d114542d7ebc4f99e926af2b1f77665ce221e6`

```dockerfile
```

-	Layers:
	-	`sha256:08fd13edde1d950271887e146d560b71e73d76cb8427d9c117292232e6365c3e`  
		Last Modified: Thu, 28 May 2026 21:18:29 GMT  
		Size: 70.7 MB (70673256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4f7e05785bc9e886fe2590276d2339e56f7e1a31aec9e7e231c6fd8804b9be`  
		Last Modified: Thu, 28 May 2026 21:18:25 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:5c43fe77e8c4af2c496afd511af68b7014ed95e6cf4219d78d11fd4b700b4713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701614831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fa96fb678d9f0493fb78a49d9bc43a39870487772cd8e9318e97eb81cc65ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:07 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:07 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:07 GMT
ARG TARGETARCH=arm64
# Thu, 28 May 2026 21:15:07 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:15:14 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:15:15 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:15:15 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:15:15 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:16:24 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:16:24 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:16:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:16:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:16:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:16:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:16:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:16:25 GMT
USER odoo
# Thu, 28 May 2026 21:16:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:16:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad0f83ef124c3a8b0a66fa96de3c1dd7ef623051c0dd912b8b5440fb886d047`  
		Last Modified: Thu, 28 May 2026 21:19:20 GMT  
		Size: 252.0 MB (252027005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1854407fd02a3c3fdbfb3aeb62bee81378239f01a7727276797b7fbbaef6f8b`  
		Last Modified: Thu, 28 May 2026 21:19:12 GMT  
		Size: 14.3 MB (14348830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8226e5e72dbdea19a8cd45329e6c22761bb00307e82bdb5ed89e7c084f02c293`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 483.6 KB (483617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f7dffc443fa56e846e54fbb456beb8c9141e8bbfb9aa45e7fddb7f32543010`  
		Last Modified: Thu, 28 May 2026 21:19:28 GMT  
		Size: 405.9 MB (405876844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858044c253b3dd18a71484e121d57ca399370828a3d90711ba646966c070ced`  
		Last Modified: Thu, 28 May 2026 21:18:26 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34b88b7ce7a2d78f8ae8611cc87742934608e72dafa73774494a4ba95f4877c`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404adfd6c5dbc559c07e98056aada695c9434296a1ce9b66f1afda76ec1a2ed`  
		Last Modified: Thu, 28 May 2026 21:19:13 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5898fbac2a61dc9149b653e5b6d31a9498cb4a1dc9b46bf2a828a4fd1ad8a76b`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d50a48b53493574e2a3c0e427b7fdcfe53ad6bf8aff24ed38dbccb8e11b31b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a986a5365de493eb7b07124c4448fcc63c4e3ddaaaacd5d1a93c41a6665876f6`

```dockerfile
```

-	Layers:
	-	`sha256:521b5b097e5c52cd4ddd94aad142695736017d5bbced3d6e097d750b53e8bcc6`  
		Last Modified: Thu, 28 May 2026 21:19:14 GMT  
		Size: 70.7 MB (70680543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b020873f4e2621f1d5740a675f11e847c7f9390466d7de420e99983f2eab9cb`  
		Last Modified: Thu, 28 May 2026 21:19:10 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:1a0577918b515a086480c22f248de53bbca42d1e00d11d85a512fa1b1bc2a3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721394078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c60d1913f3ca297ea41a8dd7312cf2a7a2ac6113fffe949e821e5a36ff48ae7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Thu, 28 May 2026 21:15:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Thu, 28 May 2026 21:15:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 28 May 2026 21:15:53 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 May 2026 21:15:53 GMT
ARG TARGETARCH=ppc64le
# Thu, 28 May 2026 21:15:53 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 28 May 2026 21:16:05 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 21:16:08 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 28 May 2026 21:16:08 GMT
ENV ODOO_VERSION=19.0
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_RELEASE=20260528
# Thu, 28 May 2026 21:16:08 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Thu, 28 May 2026 21:18:57 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 28 May 2026 21:18:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 28 May 2026 21:18:59 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 28 May 2026 21:18:59 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 28 May 2026 21:18:59 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 28 May 2026 21:18:59 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 28 May 2026 21:18:59 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 28 May 2026 21:18:59 GMT
USER odoo
# Thu, 28 May 2026 21:18:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 May 2026 21:18:59 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce29150aebfcc08323e7fdcc0c134cedcad1519ca845ec21434e3a6e85df35d3`  
		Last Modified: Thu, 28 May 2026 21:23:33 GMT  
		Size: 265.1 MB (265100862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a36948866ea2ac317fd1be2db3843982f24b522111f210a3744bc359b1a36e`  
		Last Modified: Thu, 28 May 2026 21:23:22 GMT  
		Size: 14.9 MB (14900865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b39faf04fb4343c25724c49e209e6d6709156436c8e6d057e03a248f3eff5d`  
		Last Modified: Thu, 28 May 2026 21:23:21 GMT  
		Size: 483.7 KB (483671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a18548ac7ededa9575d497acaf6913681cf1522fa238fb156b3f6bc99ff80`  
		Last Modified: Thu, 28 May 2026 21:25:05 GMT  
		Size: 406.6 MB (406591746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f88be2111530fcbe7f9937f3eb30a98c2f784fa0cec28698e7453a3a939b9c`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae2780fddf75d95ca5e5d68b26f80020173c96206a3cee55f00013dcb2f26e9`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176fefe67793953740695f03079d840b92f19277a7aec9e74a76453f6c1a8da6`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1e55f99fb56f634e540924a2a0a14a679bef36c7886085153883b75b7780c`  
		Last Modified: Thu, 28 May 2026 21:24:55 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:1f61b2f6f4d154bebaa47abe4479400a2797e5beccf96970b2be411497c8c312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3611cfe45554bc47c2b4c052bda0433c5cb495d643f5b4b0db0bfae642c4cdcc`

```dockerfile
```

-	Layers:
	-	`sha256:f33c47f4274ded9b83db68673229189d5c754f55903ad15bb300198969ebafbd`  
		Last Modified: Thu, 28 May 2026 21:24:57 GMT  
		Size: 70.7 MB (70681645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e94554c621255d0e66e003cc6d95abf4659b3584fb22dd4c6abb2f883761c39`  
		Last Modified: Thu, 28 May 2026 21:24:54 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json
