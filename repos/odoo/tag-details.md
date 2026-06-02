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
$ docker pull odoo@sha256:6b91feb705472e3ef70e4683dee14b659edefa2179df7cc9ec9eb1bc78936b30
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
$ docker pull odoo@sha256:d44595948be404c27e45abf099b69108d5bb186e20f2fe28c5271191e247e42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686742448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c045b07e655ec4506037cbc054476e43d7ef09998bbb16cd2a1cc2919240711`
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
# Tue, 02 Jun 2026 08:20:57 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:20:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:20:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:20:57 GMT
ARG TARGETARCH=amd64
# Tue, 02 Jun 2026 08:20:57 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:05 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:21:05 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:05 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:21:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:21:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:21:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
USER odoo
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af3def404d362dfb63acf824b3ac22c88332608f438bce6a4acfbb52c13abf`  
		Last Modified: Tue, 02 Jun 2026 08:23:56 GMT  
		Size: 254.6 MB (254598559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d188877cbb051597a846f2effe02372b4aadb585d28a86a2e4579ad41ad965e8`  
		Last Modified: Tue, 02 Jun 2026 08:23:44 GMT  
		Size: 14.4 MB (14370716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99def91fc92fd9fcbb0e9d1d4374b66326592bdb6241a7548d5972cd9b9f26ee`  
		Last Modified: Tue, 02 Jun 2026 08:23:43 GMT  
		Size: 483.6 KB (483620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a7142174aa4c8cc6a25239e7df1ec3964083cd80ca48ed80a7ee0d5a818ee`  
		Last Modified: Tue, 02 Jun 2026 08:23:58 GMT  
		Size: 387.6 MB (387553954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863b22120565b8d7c0b1dcdfa4ba2045667ea70e15ac1a3f71503ae2738203cb`  
		Last Modified: Tue, 02 Jun 2026 08:23:44 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e741423ee6099a2b6337c6f094a1bc56fd8df8a439fb97a258c2bca229fdd6af`  
		Last Modified: Tue, 02 Jun 2026 08:23:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac333caa7bf9cc4b95dac303da584b8719de572be86c0824dc8185dc5ea3cbe4`  
		Last Modified: Tue, 02 Jun 2026 08:23:46 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad0af9d5f5ee661d7b51692775e8766c52872952849b1b99a6b28ed182bcf3`  
		Last Modified: Tue, 02 Jun 2026 08:23:47 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:7534a2231c0d88d2004986d0a2d9322ec855845a87cc7c55680c3a556a80c391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62509336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56b2a6ab230b72f230c1a3808b39be645708d7376eccabdbbb987ba0c61b67a`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d37dfe3544befe25ca39f3747e987469352235867ebd5df8eb8d42d173967`  
		Last Modified: Tue, 02 Jun 2026 08:23:47 GMT  
		Size: 62.5 MB (62482526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3570ca9a2d79ff93d1415b604fcce322b58fb2d4644ff8cecfc4c11186d533fa`  
		Last Modified: Tue, 02 Jun 2026 08:23:43 GMT  
		Size: 26.8 KB (26810 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b9d4cea7839cfc6e465345254a062221cc27311c4bceb0a5d9ffe882d401035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 MB (683112682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4870d877435fd470e3ae0913d477f570cc3b8598911c5da346dc57cbc503f2`
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
# Tue, 02 Jun 2026 08:21:09 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:21:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:21:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:21:09 GMT
ARG TARGETARCH=arm64
# Tue, 02 Jun 2026 08:21:09 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:17 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:21:17 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:17 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:22:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a7f7ec105c0400f6ed21c265f5994591b10c76caac46d214cd0a263241b6b4`  
		Last Modified: Tue, 02 Jun 2026 08:24:38 GMT  
		Size: 252.0 MB (252025329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98f81a4cea52780b97452edadbe2e5c45775470fc547c3749e71ec9d71726b9`  
		Last Modified: Tue, 02 Jun 2026 08:24:27 GMT  
		Size: 14.3 MB (14348961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04422e71694b8aad5a426963f3818e08a64d89e32ca238879c707e162dce04`  
		Last Modified: Tue, 02 Jun 2026 08:24:26 GMT  
		Size: 483.6 KB (483630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bd509b2ae76779bed1058d24f97823a49ee9837617ed2d34342874e16a7d9`  
		Last Modified: Tue, 02 Jun 2026 08:24:43 GMT  
		Size: 387.4 MB (387375560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f2f8a9641da666adcd759ec598f94ad8b133f5336bafc33c03f0b179ae5e0`  
		Last Modified: Tue, 02 Jun 2026 08:24:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c201893b81b872ad3a6353a22beae556a4a489affb7a9911a32b00c6a5aaac`  
		Last Modified: Tue, 02 Jun 2026 08:24:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7dfb194c5104e164619c9c8b7980d5c459485b50a9b91baaee92520b0184c6`  
		Last Modified: Tue, 02 Jun 2026 08:24:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbfe76c2e03e61388a219720867c3db5f1ef9e6d81b0aad27d58d81d90ae85`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:4762a1dcf5cf71a4481ccade6bea5a29b7a88c8dde8f1cb11a2bc444641fc380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62516764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabf1ada66bf6cab2cee336c92e4bcda7244c9047a9b9f5435e7cb1e26ebda9b`

```dockerfile
```

-	Layers:
	-	`sha256:f2c5fb991c9bb7aee8b486a8bdd7e40a44645139af599526c1fd8e160690bddf`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 62.5 MB (62489801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a8d08eea12917d2757dd2d0bd92a2ad2028c54b1e8260c6a9f0f8c88f7a8dc9`  
		Last Modified: Tue, 02 Jun 2026 08:24:26 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:b0fd072484a528cde804a4ddb0f3771966ab03cbc78f743889b042cdb18a9d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702889948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d1fb539cf64737c6b4abb0c2754491a8f0e2e8a38706e69bcde61aea2f5c17`
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
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:31:31 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:31:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:31:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:31:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:31:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
USER odoo
# Tue, 02 Jun 2026 08:31:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:31:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd15f2c34cf9d65c63042bb10b6d0a545a94094fa59bb5f6fd5b6df0d2478f6`  
		Last Modified: Tue, 02 Jun 2026 08:36:37 GMT  
		Size: 388.1 MB (388089267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e384f5236cb21389bb9bd1e06363a044f16f48a42c04ee0008493309b7814498`  
		Last Modified: Tue, 02 Jun 2026 08:36:20 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33daeec5c71b822cb2beb272a20df287ad2dc88b81ad4e8a8d622b5f075c713d`  
		Last Modified: Tue, 02 Jun 2026 08:36:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce25fc37d9399154d5b11450a32b8ecf50c536616b34771fe6aae2a19f7a04`  
		Last Modified: Tue, 02 Jun 2026 08:36:21 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce88476e7fbbdb0337c46057d7b7f806abe280412572365ba278ca279599330a`  
		Last Modified: Tue, 02 Jun 2026 08:36:22 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:2f2d69615a64da65baa794da2b080e194b8efe4d408fe7da1fb69686033a4191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62517776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e052ab6c1474b23c4aa1e881d6f45f677fbf435efb02958c0d4a092bfec313d6`

```dockerfile
```

-	Layers:
	-	`sha256:c6d4bdad67004d9b172068e05886e983cd5d76f3e2020dff109074304f507f1d`  
		Last Modified: Tue, 02 Jun 2026 08:36:23 GMT  
		Size: 62.5 MB (62490909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac55ab754a1600ebb42f0192d48d76be6feb9c08f8f75d2ea65e1149bf0acfd`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:6b91feb705472e3ef70e4683dee14b659edefa2179df7cc9ec9eb1bc78936b30
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
$ docker pull odoo@sha256:d44595948be404c27e45abf099b69108d5bb186e20f2fe28c5271191e247e42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686742448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c045b07e655ec4506037cbc054476e43d7ef09998bbb16cd2a1cc2919240711`
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
# Tue, 02 Jun 2026 08:20:57 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:20:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:20:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:20:57 GMT
ARG TARGETARCH=amd64
# Tue, 02 Jun 2026 08:20:57 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:05 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:21:05 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:05 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:21:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:21:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:21:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
USER odoo
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af3def404d362dfb63acf824b3ac22c88332608f438bce6a4acfbb52c13abf`  
		Last Modified: Tue, 02 Jun 2026 08:23:56 GMT  
		Size: 254.6 MB (254598559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d188877cbb051597a846f2effe02372b4aadb585d28a86a2e4579ad41ad965e8`  
		Last Modified: Tue, 02 Jun 2026 08:23:44 GMT  
		Size: 14.4 MB (14370716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99def91fc92fd9fcbb0e9d1d4374b66326592bdb6241a7548d5972cd9b9f26ee`  
		Last Modified: Tue, 02 Jun 2026 08:23:43 GMT  
		Size: 483.6 KB (483620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a7142174aa4c8cc6a25239e7df1ec3964083cd80ca48ed80a7ee0d5a818ee`  
		Last Modified: Tue, 02 Jun 2026 08:23:58 GMT  
		Size: 387.6 MB (387553954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863b22120565b8d7c0b1dcdfa4ba2045667ea70e15ac1a3f71503ae2738203cb`  
		Last Modified: Tue, 02 Jun 2026 08:23:44 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e741423ee6099a2b6337c6f094a1bc56fd8df8a439fb97a258c2bca229fdd6af`  
		Last Modified: Tue, 02 Jun 2026 08:23:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac333caa7bf9cc4b95dac303da584b8719de572be86c0824dc8185dc5ea3cbe4`  
		Last Modified: Tue, 02 Jun 2026 08:23:46 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad0af9d5f5ee661d7b51692775e8766c52872952849b1b99a6b28ed182bcf3`  
		Last Modified: Tue, 02 Jun 2026 08:23:47 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:7534a2231c0d88d2004986d0a2d9322ec855845a87cc7c55680c3a556a80c391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62509336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56b2a6ab230b72f230c1a3808b39be645708d7376eccabdbbb987ba0c61b67a`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d37dfe3544befe25ca39f3747e987469352235867ebd5df8eb8d42d173967`  
		Last Modified: Tue, 02 Jun 2026 08:23:47 GMT  
		Size: 62.5 MB (62482526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3570ca9a2d79ff93d1415b604fcce322b58fb2d4644ff8cecfc4c11186d533fa`  
		Last Modified: Tue, 02 Jun 2026 08:23:43 GMT  
		Size: 26.8 KB (26810 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b9d4cea7839cfc6e465345254a062221cc27311c4bceb0a5d9ffe882d401035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 MB (683112682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4870d877435fd470e3ae0913d477f570cc3b8598911c5da346dc57cbc503f2`
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
# Tue, 02 Jun 2026 08:21:09 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:21:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:21:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:21:09 GMT
ARG TARGETARCH=arm64
# Tue, 02 Jun 2026 08:21:09 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:17 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:21:17 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:17 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:22:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a7f7ec105c0400f6ed21c265f5994591b10c76caac46d214cd0a263241b6b4`  
		Last Modified: Tue, 02 Jun 2026 08:24:38 GMT  
		Size: 252.0 MB (252025329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98f81a4cea52780b97452edadbe2e5c45775470fc547c3749e71ec9d71726b9`  
		Last Modified: Tue, 02 Jun 2026 08:24:27 GMT  
		Size: 14.3 MB (14348961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04422e71694b8aad5a426963f3818e08a64d89e32ca238879c707e162dce04`  
		Last Modified: Tue, 02 Jun 2026 08:24:26 GMT  
		Size: 483.6 KB (483630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bd509b2ae76779bed1058d24f97823a49ee9837617ed2d34342874e16a7d9`  
		Last Modified: Tue, 02 Jun 2026 08:24:43 GMT  
		Size: 387.4 MB (387375560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f2f8a9641da666adcd759ec598f94ad8b133f5336bafc33c03f0b179ae5e0`  
		Last Modified: Tue, 02 Jun 2026 08:24:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c201893b81b872ad3a6353a22beae556a4a489affb7a9911a32b00c6a5aaac`  
		Last Modified: Tue, 02 Jun 2026 08:24:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7dfb194c5104e164619c9c8b7980d5c459485b50a9b91baaee92520b0184c6`  
		Last Modified: Tue, 02 Jun 2026 08:24:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbfe76c2e03e61388a219720867c3db5f1ef9e6d81b0aad27d58d81d90ae85`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:4762a1dcf5cf71a4481ccade6bea5a29b7a88c8dde8f1cb11a2bc444641fc380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62516764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabf1ada66bf6cab2cee336c92e4bcda7244c9047a9b9f5435e7cb1e26ebda9b`

```dockerfile
```

-	Layers:
	-	`sha256:f2c5fb991c9bb7aee8b486a8bdd7e40a44645139af599526c1fd8e160690bddf`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 62.5 MB (62489801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a8d08eea12917d2757dd2d0bd92a2ad2028c54b1e8260c6a9f0f8c88f7a8dc9`  
		Last Modified: Tue, 02 Jun 2026 08:24:26 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:b0fd072484a528cde804a4ddb0f3771966ab03cbc78f743889b042cdb18a9d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702889948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d1fb539cf64737c6b4abb0c2754491a8f0e2e8a38706e69bcde61aea2f5c17`
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
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:31:31 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:31:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:31:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:31:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:31:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
USER odoo
# Tue, 02 Jun 2026 08:31:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:31:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd15f2c34cf9d65c63042bb10b6d0a545a94094fa59bb5f6fd5b6df0d2478f6`  
		Last Modified: Tue, 02 Jun 2026 08:36:37 GMT  
		Size: 388.1 MB (388089267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e384f5236cb21389bb9bd1e06363a044f16f48a42c04ee0008493309b7814498`  
		Last Modified: Tue, 02 Jun 2026 08:36:20 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33daeec5c71b822cb2beb272a20df287ad2dc88b81ad4e8a8d622b5f075c713d`  
		Last Modified: Tue, 02 Jun 2026 08:36:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce25fc37d9399154d5b11450a32b8ecf50c536616b34771fe6aae2a19f7a04`  
		Last Modified: Tue, 02 Jun 2026 08:36:21 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce88476e7fbbdb0337c46057d7b7f806abe280412572365ba278ca279599330a`  
		Last Modified: Tue, 02 Jun 2026 08:36:22 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:2f2d69615a64da65baa794da2b080e194b8efe4d408fe7da1fb69686033a4191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62517776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e052ab6c1474b23c4aa1e881d6f45f677fbf435efb02958c0d4a092bfec313d6`

```dockerfile
```

-	Layers:
	-	`sha256:c6d4bdad67004d9b172068e05886e983cd5d76f3e2020dff109074304f507f1d`  
		Last Modified: Tue, 02 Jun 2026 08:36:23 GMT  
		Size: 62.5 MB (62490909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac55ab754a1600ebb42f0192d48d76be6feb9c08f8f75d2ea65e1149bf0acfd`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260528`

```console
$ docker pull odoo@sha256:6b91feb705472e3ef70e4683dee14b659edefa2179df7cc9ec9eb1bc78936b30
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
$ docker pull odoo@sha256:d44595948be404c27e45abf099b69108d5bb186e20f2fe28c5271191e247e42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **686.7 MB (686742448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c045b07e655ec4506037cbc054476e43d7ef09998bbb16cd2a1cc2919240711`
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
# Tue, 02 Jun 2026 08:20:57 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:20:57 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:20:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:20:57 GMT
ARG TARGETARCH=amd64
# Tue, 02 Jun 2026 08:20:57 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:05 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:05 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:21:05 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:05 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:21:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:21:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:21:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:21:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:21:53 GMT
USER odoo
# Tue, 02 Jun 2026 08:21:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:21:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af3def404d362dfb63acf824b3ac22c88332608f438bce6a4acfbb52c13abf`  
		Last Modified: Tue, 02 Jun 2026 08:23:56 GMT  
		Size: 254.6 MB (254598559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d188877cbb051597a846f2effe02372b4aadb585d28a86a2e4579ad41ad965e8`  
		Last Modified: Tue, 02 Jun 2026 08:23:44 GMT  
		Size: 14.4 MB (14370716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99def91fc92fd9fcbb0e9d1d4374b66326592bdb6241a7548d5972cd9b9f26ee`  
		Last Modified: Tue, 02 Jun 2026 08:23:43 GMT  
		Size: 483.6 KB (483620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a7142174aa4c8cc6a25239e7df1ec3964083cd80ca48ed80a7ee0d5a818ee`  
		Last Modified: Tue, 02 Jun 2026 08:23:58 GMT  
		Size: 387.6 MB (387553954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863b22120565b8d7c0b1dcdfa4ba2045667ea70e15ac1a3f71503ae2738203cb`  
		Last Modified: Tue, 02 Jun 2026 08:23:44 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e741423ee6099a2b6337c6f094a1bc56fd8df8a439fb97a258c2bca229fdd6af`  
		Last Modified: Tue, 02 Jun 2026 08:23:45 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac333caa7bf9cc4b95dac303da584b8719de572be86c0824dc8185dc5ea3cbe4`  
		Last Modified: Tue, 02 Jun 2026 08:23:46 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ad0af9d5f5ee661d7b51692775e8766c52872952849b1b99a6b28ed182bcf3`  
		Last Modified: Tue, 02 Jun 2026 08:23:47 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:7534a2231c0d88d2004986d0a2d9322ec855845a87cc7c55680c3a556a80c391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62509336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56b2a6ab230b72f230c1a3808b39be645708d7376eccabdbbb987ba0c61b67a`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d37dfe3544befe25ca39f3747e987469352235867ebd5df8eb8d42d173967`  
		Last Modified: Tue, 02 Jun 2026 08:23:47 GMT  
		Size: 62.5 MB (62482526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3570ca9a2d79ff93d1415b604fcce322b58fb2d4644ff8cecfc4c11186d533fa`  
		Last Modified: Tue, 02 Jun 2026 08:23:43 GMT  
		Size: 26.8 KB (26810 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260528` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:1b9d4cea7839cfc6e465345254a062221cc27311c4bceb0a5d9ffe882d401035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **683.1 MB (683112682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4870d877435fd470e3ae0913d477f570cc3b8598911c5da346dc57cbc503f2`
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
# Tue, 02 Jun 2026 08:21:09 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:21:09 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:21:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:21:09 GMT
ARG TARGETARCH=arm64
# Tue, 02 Jun 2026 08:21:09 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:16 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:17 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:17 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:21:17 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:17 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:22:14 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:15 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:15 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:15 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:15 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:15 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a7f7ec105c0400f6ed21c265f5994591b10c76caac46d214cd0a263241b6b4`  
		Last Modified: Tue, 02 Jun 2026 08:24:38 GMT  
		Size: 252.0 MB (252025329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98f81a4cea52780b97452edadbe2e5c45775470fc547c3749e71ec9d71726b9`  
		Last Modified: Tue, 02 Jun 2026 08:24:27 GMT  
		Size: 14.3 MB (14348961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc04422e71694b8aad5a426963f3818e08a64d89e32ca238879c707e162dce04`  
		Last Modified: Tue, 02 Jun 2026 08:24:26 GMT  
		Size: 483.6 KB (483630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bd509b2ae76779bed1058d24f97823a49ee9837617ed2d34342874e16a7d9`  
		Last Modified: Tue, 02 Jun 2026 08:24:43 GMT  
		Size: 387.4 MB (387375560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468f2f8a9641da666adcd759ec598f94ad8b133f5336bafc33c03f0b179ae5e0`  
		Last Modified: Tue, 02 Jun 2026 08:24:28 GMT  
		Size: 767.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c201893b81b872ad3a6353a22beae556a4a489affb7a9911a32b00c6a5aaac`  
		Last Modified: Tue, 02 Jun 2026 08:24:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7dfb194c5104e164619c9c8b7980d5c459485b50a9b91baaee92520b0184c6`  
		Last Modified: Tue, 02 Jun 2026 08:24:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bbfe76c2e03e61388a219720867c3db5f1ef9e6d81b0aad27d58d81d90ae85`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:4762a1dcf5cf71a4481ccade6bea5a29b7a88c8dde8f1cb11a2bc444641fc380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62516764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabf1ada66bf6cab2cee336c92e4bcda7244c9047a9b9f5435e7cb1e26ebda9b`

```dockerfile
```

-	Layers:
	-	`sha256:f2c5fb991c9bb7aee8b486a8bdd7e40a44645139af599526c1fd8e160690bddf`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 62.5 MB (62489801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a8d08eea12917d2757dd2d0bd92a2ad2028c54b1e8260c6a9f0f8c88f7a8dc9`  
		Last Modified: Tue, 02 Jun 2026 08:24:26 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260528` - linux; ppc64le

```console
$ docker pull odoo@sha256:b0fd072484a528cde804a4ddb0f3771966ab03cbc78f743889b042cdb18a9d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **702.9 MB (702889948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d1fb539cf64737c6b4abb0c2754491a8f0e2e8a38706e69bcde61aea2f5c17`
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
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=18.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
# Tue, 02 Jun 2026 08:31:31 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:31:32 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=298dc1c20c72db72d14fd60c8bbd68b4d711d1f4
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:31:33 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:31:33 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:31:33 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:31:33 GMT
USER odoo
# Tue, 02 Jun 2026 08:31:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:31:33 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd15f2c34cf9d65c63042bb10b6d0a545a94094fa59bb5f6fd5b6df0d2478f6`  
		Last Modified: Tue, 02 Jun 2026 08:36:37 GMT  
		Size: 388.1 MB (388089267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e384f5236cb21389bb9bd1e06363a044f16f48a42c04ee0008493309b7814498`  
		Last Modified: Tue, 02 Jun 2026 08:36:20 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33daeec5c71b822cb2beb272a20df287ad2dc88b81ad4e8a8d622b5f075c713d`  
		Last Modified: Tue, 02 Jun 2026 08:36:21 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dce25fc37d9399154d5b11450a32b8ecf50c536616b34771fe6aae2a19f7a04`  
		Last Modified: Tue, 02 Jun 2026 08:36:21 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce88476e7fbbdb0337c46057d7b7f806abe280412572365ba278ca279599330a`  
		Last Modified: Tue, 02 Jun 2026 08:36:22 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:2f2d69615a64da65baa794da2b080e194b8efe4d408fe7da1fb69686033a4191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62517776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e052ab6c1474b23c4aa1e881d6f45f677fbf435efb02958c0d4a092bfec313d6`

```dockerfile
```

-	Layers:
	-	`sha256:c6d4bdad67004d9b172068e05886e983cd5d76f3e2020dff109074304f507f1d`  
		Last Modified: Tue, 02 Jun 2026 08:36:23 GMT  
		Size: 62.5 MB (62490909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac55ab754a1600ebb42f0192d48d76be6feb9c08f8f75d2ea65e1149bf0acfd`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:b81c76750665681327f0193afcc8a54ed0348e8cac3bdaef1b7f4abea5471eed
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
$ docker pull odoo@sha256:b3f19bbe15f8608331f5530d04207e32b58ecf7ad74e6e21fed9f6f5ab2eef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705247887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6486b7fcb43de9176e3d674e8e4a3e9b0f9c350e9a4c4c4c57d60b2bfb5268`
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
# Tue, 02 Jun 2026 08:20:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:20:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:20:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:20:53 GMT
ARG TARGETARCH=amd64
# Tue, 02 Jun 2026 08:20:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:05 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:05 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ea211aef123987913f55b3e56db1129ba540618a9f796d72a9e53dd2186a6`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 254.6 MB (254599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46308feee278becd2169b5f37960a3d2b6b2a34cc3eb69091174e624341efc77`  
		Last Modified: Tue, 02 Jun 2026 08:24:21 GMT  
		Size: 14.4 MB (14370699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4f8b77136821a7b8d0a4974c81a9d4b061398bee0a616df80c17e3252762f`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 483.6 KB (483601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c396499eedbece332943b7536d1204e4d6d040517369e620cca1b752407f7f77`  
		Last Modified: Tue, 02 Jun 2026 08:24:34 GMT  
		Size: 406.1 MB (406058954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968ff0f7c7f262e9caa1f7b8f251b4b202e8c04281e9279b19a9d00e19ea6c1`  
		Last Modified: Tue, 02 Jun 2026 08:24:22 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b669d413d3c3795563adf658ad12c0e01d50373ce14c0a58beda71bf0431a`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c746e438768eaa85e9d51b4d7a7f04a29cff5ad9c35b13d72299b149f2a38f`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc590fa755ad5b9847a914efa7df935d30098ee6a8029829897f4353d598ff38`  
		Last Modified: Tue, 02 Jun 2026 08:24:24 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:f4a6198532bd9923c673c73ac05dffce4b0859360371a7067f1f1769a2250b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695582ab7cdaff097964a0a7c324143d0acede3cfbf5a234fe81786729c42721`

```dockerfile
```

-	Layers:
	-	`sha256:4268bdba9916a92463709db726ead3f9fceaef6019c3993d8df15f45b64fea31`  
		Last Modified: Tue, 02 Jun 2026 08:24:25 GMT  
		Size: 70.7 MB (70673274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41d0ca9bbcd530f48b01c5a4ca0822039f8715ebf4624986091e29de1d25ca7`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c381c001b8cf65caa97104f20e47ebf2861741c8d99031c2f2db71f9c5f50a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701618153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badf431ace2acc998e72a55a8286de39cd0d75898f03a1f4219641f005382d08`
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
# Tue, 02 Jun 2026 08:21:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:21:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:21:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:21:10 GMT
ARG TARGETARCH=arm64
# Tue, 02 Jun 2026 08:21:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bad4e770ea114436cde5b001b3edb388111df04c62d45c149f224e46ec5f77`  
		Last Modified: Tue, 02 Jun 2026 08:25:11 GMT  
		Size: 252.0 MB (252025476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2dadf9d33c224bb28665a42e43b1069e2e967b5ce0ba7cf3e29b910bae291`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 14.3 MB (14349033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95541986b405947875762d0437104a1d4877d394c92e15b864afecd36471fa28`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfddfeba8e6a09be03e995155a5950eba565d41a9013506aa7d72321fd73abe`  
		Last Modified: Tue, 02 Jun 2026 08:25:14 GMT  
		Size: 405.9 MB (405880866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6130fbfc457cb57088621636f61ab4c5621c7de9f2b88fd13aaa6abfcd19c`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c787a47086ac2b4b27812795bc0cdd5e892a38c4defd9ab791053e97f5f1b360`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9f67aa67164e087a2aacef790e25abd4da941b42a48945bf77c7f34be37429`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79d4a42c33ddf7e744d73e8fcdfc92dd6cbbb8ac894c9719fce8c6135ec19ce`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0d0e22e5cbaf8290cfa78fe81dc16570f7a460f381a1c4d30bcb671a046786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0f491449d1e06ea0ac1d1ea0377e2e8a297a025f2f8ea7c9c15c16ddf2edf9`

```dockerfile
```

-	Layers:
	-	`sha256:f2b6b351ada6f2a57d0a26743ceaa54de407b24386b50bf606ae24276d7a38df`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 70.7 MB (70680561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:998c494d95da0bb2b5bbffe6728f1c9222eeda73da4ae9558bf3934fbac733ff`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ff08ccc9336929c34be31bd8deb46f69fe646f72de5aac77fcf9374e0df6b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721391159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2802a6c783c52c33eb281162bc9bea19b010ec60579be80ec5298be2ea0347`
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
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:31:45 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:31:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:31:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:31:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
USER odoo
# Tue, 02 Jun 2026 08:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:31:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a47655c16a37b2e16d8e0a1f4b1af0731764de0cde980bac82443bcdaf2a1`  
		Last Modified: Tue, 02 Jun 2026 08:37:50 GMT  
		Size: 406.6 MB (406590522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34e3d7077f19a282c7197125b2c5e62fa63bc29fda85f75e6fab6db8754d0db`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110935a9e765f6c9be92ea7baaa87efc610107eee3bd3bcadf8d18ff7eb4e0aa`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b71339f4af483e577d53edc1ed078fa4cc839ca51b673f6ea50fd07a89456c`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f819eaec3f9d57a5fae2658b9385d2ebd5976cf06e183a81bf5a263beda6f2`  
		Last Modified: Tue, 02 Jun 2026 08:37:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:fa52a95dc93fc03b948e5bc010678b73a31a157e5d5924fbd5e6efac9528fb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be8fb7446f87e6f7b70c8e6354672603ea31dde4d15db0a0b453a08f16f96d6`

```dockerfile
```

-	Layers:
	-	`sha256:26768482c2d6be1096ddb67935c4b996c1677aa49ef55e21d1059a146d4ff6b7`  
		Last Modified: Tue, 02 Jun 2026 08:37:44 GMT  
		Size: 70.7 MB (70681663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d54bca6420ff21a70fb4a3b25e6b0d88f028d96c8e96800cb9baf0c9ce2c1271`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:b81c76750665681327f0193afcc8a54ed0348e8cac3bdaef1b7f4abea5471eed
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
$ docker pull odoo@sha256:b3f19bbe15f8608331f5530d04207e32b58ecf7ad74e6e21fed9f6f5ab2eef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705247887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6486b7fcb43de9176e3d674e8e4a3e9b0f9c350e9a4c4c4c57d60b2bfb5268`
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
# Tue, 02 Jun 2026 08:20:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:20:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:20:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:20:53 GMT
ARG TARGETARCH=amd64
# Tue, 02 Jun 2026 08:20:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:05 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:05 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ea211aef123987913f55b3e56db1129ba540618a9f796d72a9e53dd2186a6`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 254.6 MB (254599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46308feee278becd2169b5f37960a3d2b6b2a34cc3eb69091174e624341efc77`  
		Last Modified: Tue, 02 Jun 2026 08:24:21 GMT  
		Size: 14.4 MB (14370699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4f8b77136821a7b8d0a4974c81a9d4b061398bee0a616df80c17e3252762f`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 483.6 KB (483601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c396499eedbece332943b7536d1204e4d6d040517369e620cca1b752407f7f77`  
		Last Modified: Tue, 02 Jun 2026 08:24:34 GMT  
		Size: 406.1 MB (406058954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968ff0f7c7f262e9caa1f7b8f251b4b202e8c04281e9279b19a9d00e19ea6c1`  
		Last Modified: Tue, 02 Jun 2026 08:24:22 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b669d413d3c3795563adf658ad12c0e01d50373ce14c0a58beda71bf0431a`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c746e438768eaa85e9d51b4d7a7f04a29cff5ad9c35b13d72299b149f2a38f`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc590fa755ad5b9847a914efa7df935d30098ee6a8029829897f4353d598ff38`  
		Last Modified: Tue, 02 Jun 2026 08:24:24 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:f4a6198532bd9923c673c73ac05dffce4b0859360371a7067f1f1769a2250b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695582ab7cdaff097964a0a7c324143d0acede3cfbf5a234fe81786729c42721`

```dockerfile
```

-	Layers:
	-	`sha256:4268bdba9916a92463709db726ead3f9fceaef6019c3993d8df15f45b64fea31`  
		Last Modified: Tue, 02 Jun 2026 08:24:25 GMT  
		Size: 70.7 MB (70673274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41d0ca9bbcd530f48b01c5a4ca0822039f8715ebf4624986091e29de1d25ca7`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c381c001b8cf65caa97104f20e47ebf2861741c8d99031c2f2db71f9c5f50a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701618153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badf431ace2acc998e72a55a8286de39cd0d75898f03a1f4219641f005382d08`
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
# Tue, 02 Jun 2026 08:21:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:21:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:21:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:21:10 GMT
ARG TARGETARCH=arm64
# Tue, 02 Jun 2026 08:21:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bad4e770ea114436cde5b001b3edb388111df04c62d45c149f224e46ec5f77`  
		Last Modified: Tue, 02 Jun 2026 08:25:11 GMT  
		Size: 252.0 MB (252025476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2dadf9d33c224bb28665a42e43b1069e2e967b5ce0ba7cf3e29b910bae291`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 14.3 MB (14349033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95541986b405947875762d0437104a1d4877d394c92e15b864afecd36471fa28`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfddfeba8e6a09be03e995155a5950eba565d41a9013506aa7d72321fd73abe`  
		Last Modified: Tue, 02 Jun 2026 08:25:14 GMT  
		Size: 405.9 MB (405880866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6130fbfc457cb57088621636f61ab4c5621c7de9f2b88fd13aaa6abfcd19c`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c787a47086ac2b4b27812795bc0cdd5e892a38c4defd9ab791053e97f5f1b360`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9f67aa67164e087a2aacef790e25abd4da941b42a48945bf77c7f34be37429`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79d4a42c33ddf7e744d73e8fcdfc92dd6cbbb8ac894c9719fce8c6135ec19ce`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0d0e22e5cbaf8290cfa78fe81dc16570f7a460f381a1c4d30bcb671a046786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0f491449d1e06ea0ac1d1ea0377e2e8a297a025f2f8ea7c9c15c16ddf2edf9`

```dockerfile
```

-	Layers:
	-	`sha256:f2b6b351ada6f2a57d0a26743ceaa54de407b24386b50bf606ae24276d7a38df`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 70.7 MB (70680561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:998c494d95da0bb2b5bbffe6728f1c9222eeda73da4ae9558bf3934fbac733ff`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ff08ccc9336929c34be31bd8deb46f69fe646f72de5aac77fcf9374e0df6b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721391159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2802a6c783c52c33eb281162bc9bea19b010ec60579be80ec5298be2ea0347`
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
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:31:45 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:31:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:31:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:31:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
USER odoo
# Tue, 02 Jun 2026 08:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:31:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a47655c16a37b2e16d8e0a1f4b1af0731764de0cde980bac82443bcdaf2a1`  
		Last Modified: Tue, 02 Jun 2026 08:37:50 GMT  
		Size: 406.6 MB (406590522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34e3d7077f19a282c7197125b2c5e62fa63bc29fda85f75e6fab6db8754d0db`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110935a9e765f6c9be92ea7baaa87efc610107eee3bd3bcadf8d18ff7eb4e0aa`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b71339f4af483e577d53edc1ed078fa4cc839ca51b673f6ea50fd07a89456c`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f819eaec3f9d57a5fae2658b9385d2ebd5976cf06e183a81bf5a263beda6f2`  
		Last Modified: Tue, 02 Jun 2026 08:37:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:fa52a95dc93fc03b948e5bc010678b73a31a157e5d5924fbd5e6efac9528fb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be8fb7446f87e6f7b70c8e6354672603ea31dde4d15db0a0b453a08f16f96d6`

```dockerfile
```

-	Layers:
	-	`sha256:26768482c2d6be1096ddb67935c4b996c1677aa49ef55e21d1059a146d4ff6b7`  
		Last Modified: Tue, 02 Jun 2026 08:37:44 GMT  
		Size: 70.7 MB (70681663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d54bca6420ff21a70fb4a3b25e6b0d88f028d96c8e96800cb9baf0c9ce2c1271`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260528`

```console
$ docker pull odoo@sha256:b81c76750665681327f0193afcc8a54ed0348e8cac3bdaef1b7f4abea5471eed
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
$ docker pull odoo@sha256:b3f19bbe15f8608331f5530d04207e32b58ecf7ad74e6e21fed9f6f5ab2eef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705247887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6486b7fcb43de9176e3d674e8e4a3e9b0f9c350e9a4c4c4c57d60b2bfb5268`
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
# Tue, 02 Jun 2026 08:20:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:20:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:20:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:20:53 GMT
ARG TARGETARCH=amd64
# Tue, 02 Jun 2026 08:20:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:05 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:05 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ea211aef123987913f55b3e56db1129ba540618a9f796d72a9e53dd2186a6`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 254.6 MB (254599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46308feee278becd2169b5f37960a3d2b6b2a34cc3eb69091174e624341efc77`  
		Last Modified: Tue, 02 Jun 2026 08:24:21 GMT  
		Size: 14.4 MB (14370699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4f8b77136821a7b8d0a4974c81a9d4b061398bee0a616df80c17e3252762f`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 483.6 KB (483601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c396499eedbece332943b7536d1204e4d6d040517369e620cca1b752407f7f77`  
		Last Modified: Tue, 02 Jun 2026 08:24:34 GMT  
		Size: 406.1 MB (406058954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968ff0f7c7f262e9caa1f7b8f251b4b202e8c04281e9279b19a9d00e19ea6c1`  
		Last Modified: Tue, 02 Jun 2026 08:24:22 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b669d413d3c3795563adf658ad12c0e01d50373ce14c0a58beda71bf0431a`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c746e438768eaa85e9d51b4d7a7f04a29cff5ad9c35b13d72299b149f2a38f`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc590fa755ad5b9847a914efa7df935d30098ee6a8029829897f4353d598ff38`  
		Last Modified: Tue, 02 Jun 2026 08:24:24 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:f4a6198532bd9923c673c73ac05dffce4b0859360371a7067f1f1769a2250b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695582ab7cdaff097964a0a7c324143d0acede3cfbf5a234fe81786729c42721`

```dockerfile
```

-	Layers:
	-	`sha256:4268bdba9916a92463709db726ead3f9fceaef6019c3993d8df15f45b64fea31`  
		Last Modified: Tue, 02 Jun 2026 08:24:25 GMT  
		Size: 70.7 MB (70673274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41d0ca9bbcd530f48b01c5a4ca0822039f8715ebf4624986091e29de1d25ca7`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260528` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c381c001b8cf65caa97104f20e47ebf2861741c8d99031c2f2db71f9c5f50a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701618153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badf431ace2acc998e72a55a8286de39cd0d75898f03a1f4219641f005382d08`
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
# Tue, 02 Jun 2026 08:21:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:21:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:21:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:21:10 GMT
ARG TARGETARCH=arm64
# Tue, 02 Jun 2026 08:21:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bad4e770ea114436cde5b001b3edb388111df04c62d45c149f224e46ec5f77`  
		Last Modified: Tue, 02 Jun 2026 08:25:11 GMT  
		Size: 252.0 MB (252025476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2dadf9d33c224bb28665a42e43b1069e2e967b5ce0ba7cf3e29b910bae291`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 14.3 MB (14349033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95541986b405947875762d0437104a1d4877d394c92e15b864afecd36471fa28`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfddfeba8e6a09be03e995155a5950eba565d41a9013506aa7d72321fd73abe`  
		Last Modified: Tue, 02 Jun 2026 08:25:14 GMT  
		Size: 405.9 MB (405880866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6130fbfc457cb57088621636f61ab4c5621c7de9f2b88fd13aaa6abfcd19c`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c787a47086ac2b4b27812795bc0cdd5e892a38c4defd9ab791053e97f5f1b360`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9f67aa67164e087a2aacef790e25abd4da941b42a48945bf77c7f34be37429`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79d4a42c33ddf7e744d73e8fcdfc92dd6cbbb8ac894c9719fce8c6135ec19ce`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0d0e22e5cbaf8290cfa78fe81dc16570f7a460f381a1c4d30bcb671a046786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0f491449d1e06ea0ac1d1ea0377e2e8a297a025f2f8ea7c9c15c16ddf2edf9`

```dockerfile
```

-	Layers:
	-	`sha256:f2b6b351ada6f2a57d0a26743ceaa54de407b24386b50bf606ae24276d7a38df`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 70.7 MB (70680561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:998c494d95da0bb2b5bbffe6728f1c9222eeda73da4ae9558bf3934fbac733ff`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260528` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ff08ccc9336929c34be31bd8deb46f69fe646f72de5aac77fcf9374e0df6b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721391159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2802a6c783c52c33eb281162bc9bea19b010ec60579be80ec5298be2ea0347`
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
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:31:45 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:31:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:31:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:31:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
USER odoo
# Tue, 02 Jun 2026 08:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:31:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a47655c16a37b2e16d8e0a1f4b1af0731764de0cde980bac82443bcdaf2a1`  
		Last Modified: Tue, 02 Jun 2026 08:37:50 GMT  
		Size: 406.6 MB (406590522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34e3d7077f19a282c7197125b2c5e62fa63bc29fda85f75e6fab6db8754d0db`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110935a9e765f6c9be92ea7baaa87efc610107eee3bd3bcadf8d18ff7eb4e0aa`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b71339f4af483e577d53edc1ed078fa4cc839ca51b673f6ea50fd07a89456c`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f819eaec3f9d57a5fae2658b9385d2ebd5976cf06e183a81bf5a263beda6f2`  
		Last Modified: Tue, 02 Jun 2026 08:37:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260528` - unknown; unknown

```console
$ docker pull odoo@sha256:fa52a95dc93fc03b948e5bc010678b73a31a157e5d5924fbd5e6efac9528fb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be8fb7446f87e6f7b70c8e6354672603ea31dde4d15db0a0b453a08f16f96d6`

```dockerfile
```

-	Layers:
	-	`sha256:26768482c2d6be1096ddb67935c4b996c1677aa49ef55e21d1059a146d4ff6b7`  
		Last Modified: Tue, 02 Jun 2026 08:37:44 GMT  
		Size: 70.7 MB (70681663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d54bca6420ff21a70fb4a3b25e6b0d88f028d96c8e96800cb9baf0c9ce2c1271`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:b81c76750665681327f0193afcc8a54ed0348e8cac3bdaef1b7f4abea5471eed
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
$ docker pull odoo@sha256:b3f19bbe15f8608331f5530d04207e32b58ecf7ad74e6e21fed9f6f5ab2eef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **705.2 MB (705247887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6486b7fcb43de9176e3d674e8e4a3e9b0f9c350e9a4c4c4c57d60b2bfb5268`
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
# Tue, 02 Jun 2026 08:20:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:20:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:20:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:20:53 GMT
ARG TARGETARCH=amd64
# Tue, 02 Jun 2026 08:20:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:02 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:04 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:05 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:05 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:05 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:05 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:05 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ea211aef123987913f55b3e56db1129ba540618a9f796d72a9e53dd2186a6`  
		Last Modified: Tue, 02 Jun 2026 08:24:31 GMT  
		Size: 254.6 MB (254599084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46308feee278becd2169b5f37960a3d2b6b2a34cc3eb69091174e624341efc77`  
		Last Modified: Tue, 02 Jun 2026 08:24:21 GMT  
		Size: 14.4 MB (14370699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4f8b77136821a7b8d0a4974c81a9d4b061398bee0a616df80c17e3252762f`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 483.6 KB (483601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c396499eedbece332943b7536d1204e4d6d040517369e620cca1b752407f7f77`  
		Last Modified: Tue, 02 Jun 2026 08:24:34 GMT  
		Size: 406.1 MB (406058954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2968ff0f7c7f262e9caa1f7b8f251b4b202e8c04281e9279b19a9d00e19ea6c1`  
		Last Modified: Tue, 02 Jun 2026 08:24:22 GMT  
		Size: 717.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979b669d413d3c3795563adf658ad12c0e01d50373ce14c0a58beda71bf0431a`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c746e438768eaa85e9d51b4d7a7f04a29cff5ad9c35b13d72299b149f2a38f`  
		Last Modified: Tue, 02 Jun 2026 08:24:23 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc590fa755ad5b9847a914efa7df935d30098ee6a8029829897f4353d598ff38`  
		Last Modified: Tue, 02 Jun 2026 08:24:24 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f4a6198532bd9923c673c73ac05dffce4b0859360371a7067f1f1769a2250b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70700379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695582ab7cdaff097964a0a7c324143d0acede3cfbf5a234fe81786729c42721`

```dockerfile
```

-	Layers:
	-	`sha256:4268bdba9916a92463709db726ead3f9fceaef6019c3993d8df15f45b64fea31`  
		Last Modified: Tue, 02 Jun 2026 08:24:25 GMT  
		Size: 70.7 MB (70673274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41d0ca9bbcd530f48b01c5a4ca0822039f8715ebf4624986091e29de1d25ca7`  
		Last Modified: Tue, 02 Jun 2026 08:24:20 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:c381c001b8cf65caa97104f20e47ebf2861741c8d99031c2f2db71f9c5f50a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **701.6 MB (701618153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badf431ace2acc998e72a55a8286de39cd0d75898f03a1f4219641f005382d08`
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
# Tue, 02 Jun 2026 08:21:10 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:21:10 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:21:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:21:10 GMT
ARG TARGETARCH=arm64
# Tue, 02 Jun 2026 08:21:10 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:21:18 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:21:19 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:21:19 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:22:25 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:22:25 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:22:25 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:22:25 GMT
USER odoo
# Tue, 02 Jun 2026 08:22:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:22:25 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bad4e770ea114436cde5b001b3edb388111df04c62d45c149f224e46ec5f77`  
		Last Modified: Tue, 02 Jun 2026 08:25:11 GMT  
		Size: 252.0 MB (252025476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f2dadf9d33c224bb28665a42e43b1069e2e967b5ce0ba7cf3e29b910bae291`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 14.3 MB (14349033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95541986b405947875762d0437104a1d4877d394c92e15b864afecd36471fa28`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 483.6 KB (483626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfddfeba8e6a09be03e995155a5950eba565d41a9013506aa7d72321fd73abe`  
		Last Modified: Tue, 02 Jun 2026 08:25:14 GMT  
		Size: 405.9 MB (405880866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6130fbfc457cb57088621636f61ab4c5621c7de9f2b88fd13aaa6abfcd19c`  
		Last Modified: Tue, 02 Jun 2026 08:25:02 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c787a47086ac2b4b27812795bc0cdd5e892a38c4defd9ab791053e97f5f1b360`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9f67aa67164e087a2aacef790e25abd4da941b42a48945bf77c7f34be37429`  
		Last Modified: Tue, 02 Jun 2026 08:25:04 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79d4a42c33ddf7e744d73e8fcdfc92dd6cbbb8ac894c9719fce8c6135ec19ce`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:aa0d0e22e5cbaf8290cfa78fe81dc16570f7a460f381a1c4d30bcb671a046786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70707830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0f491449d1e06ea0ac1d1ea0377e2e8a297a025f2f8ea7c9c15c16ddf2edf9`

```dockerfile
```

-	Layers:
	-	`sha256:f2b6b351ada6f2a57d0a26743ceaa54de407b24386b50bf606ae24276d7a38df`  
		Last Modified: Tue, 02 Jun 2026 08:25:05 GMT  
		Size: 70.7 MB (70680561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:998c494d95da0bb2b5bbffe6728f1c9222eeda73da4ae9558bf3934fbac733ff`  
		Last Modified: Tue, 02 Jun 2026 08:25:01 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:6ff08ccc9336929c34be31bd8deb46f69fe646f72de5aac77fcf9374e0df6b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.4 MB (721391159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2802a6c783c52c33eb281162bc9bea19b010ec60579be80ec5298be2ea0347`
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
# Tue, 02 Jun 2026 08:29:03 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 02 Jun 2026 08:29:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 02 Jun 2026 08:29:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 02 Jun 2026 08:29:03 GMT
ARG TARGETARCH=ppc64le
# Tue, 02 Jun 2026 08:29:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 02 Jun 2026 08:29:18 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 02 Jun 2026 08:29:20 GMT
ENV ODOO_VERSION=19.0
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_RELEASE=20260528
# Tue, 02 Jun 2026 08:29:20 GMT
ARG ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
# Tue, 02 Jun 2026 08:31:45 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 02 Jun 2026 08:31:46 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260528 ODOO_SHA=2c6fb64ea1535dabb039e78760c8f21284a3c990
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 02 Jun 2026 08:31:47 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 02 Jun 2026 08:31:47 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 02 Jun 2026 08:31:47 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 02 Jun 2026 08:31:47 GMT
USER odoo
# Tue, 02 Jun 2026 08:31:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 02 Jun 2026 08:31:47 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f45bd0c99c8dc652a2ed4e93fef926ae28157022f9d6fda42a3adfd4ed85ab`  
		Last Modified: Tue, 02 Jun 2026 08:36:32 GMT  
		Size: 265.1 MB (265099073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb49d5267f9bf7ed206d8bfba6dd8c44f7d40d83f7af8ec07161bbb78d7180`  
		Last Modified: Tue, 02 Jun 2026 08:36:19 GMT  
		Size: 14.9 MB (14900963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c5c2fd41355ecffaf8fc63e9894e6b9e89ae3ef861a39d4dea859b0f5c2d6`  
		Last Modified: Tue, 02 Jun 2026 08:36:18 GMT  
		Size: 483.7 KB (483748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741a47655c16a37b2e16d8e0a1f4b1af0731764de0cde980bac82443bcdaf2a1`  
		Last Modified: Tue, 02 Jun 2026 08:37:50 GMT  
		Size: 406.6 MB (406590522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34e3d7077f19a282c7197125b2c5e62fa63bc29fda85f75e6fab6db8754d0db`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110935a9e765f6c9be92ea7baaa87efc610107eee3bd3bcadf8d18ff7eb4e0aa`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b71339f4af483e577d53edc1ed078fa4cc839ca51b673f6ea50fd07a89456c`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 599.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f819eaec3f9d57a5fae2658b9385d2ebd5976cf06e183a81bf5a263beda6f2`  
		Last Modified: Tue, 02 Jun 2026 08:37:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:fa52a95dc93fc03b948e5bc010678b73a31a157e5d5924fbd5e6efac9528fb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70708830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be8fb7446f87e6f7b70c8e6354672603ea31dde4d15db0a0b453a08f16f96d6`

```dockerfile
```

-	Layers:
	-	`sha256:26768482c2d6be1096ddb67935c4b996c1677aa49ef55e21d1059a146d4ff6b7`  
		Last Modified: Tue, 02 Jun 2026 08:37:44 GMT  
		Size: 70.7 MB (70681663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d54bca6420ff21a70fb4a3b25e6b0d88f028d96c8e96800cb9baf0c9ce2c1271`  
		Last Modified: Tue, 02 Jun 2026 08:37:40 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json
