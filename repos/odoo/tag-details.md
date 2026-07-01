<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20260630`](#odoo170-20260630)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20260630`](#odoo180-20260630)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20260630`](#odoo190-20260630)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:f210a19a0e1301e02a2b860a9745da1ba0e2522f48fc26a70dfdef6cb48866ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:5bfda275c8ca6cc25f063751a11a2751492438c6148f467b299b9f2b2a59fca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616894332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bad06fdef8a46e28e3d43c2ce4d7969a0f2cb9a3fda2d07ca64975ab034dff`
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
# Tue, 30 Jun 2026 23:37:50 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:50 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jun 2026 23:37:56 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:37:56 GMT
ARG ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:38:52 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:38:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:38:52 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
USER odoo
# Tue, 30 Jun 2026 23:38:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:38:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4dc009fcb52162f88b61048bb265128eb415230c05f908fed68e732893515`  
		Last Modified: Tue, 30 Jun 2026 23:40:21 GMT  
		Size: 238.4 MB (238372188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1006fd5c64994d2b344066b5f35d2ec3534aa4b2fd4c7f386cc980a8379bf72f`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 2.6 MB (2611783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5671eed01885bb857789c558d9820246c6f30160ac2e0e692d101b99355f9645`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 482.9 KB (482939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2491feff5b0506ad945ed5129c3fc6200b73b202e5aafdbb07cf884fade79`  
		Last Modified: Tue, 30 Jun 2026 23:40:25 GMT  
		Size: 345.7 MB (345687949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f39b8671dbf0a3c8abfb5610e5f3cca9ae8f1bd5fffc2f7bff3cb0e0d1cbd55`  
		Last Modified: Tue, 30 Jun 2026 23:40:09 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8076ddd15f0625ba0f505a680a4375a1189f8cd5c11bc03a37a3b06dc39db721`  
		Last Modified: Tue, 30 Jun 2026 23:40:09 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140c9924aedc5375de4b5b2fdc25dd6a121243aa70495f87cb9bfee1c30a6d7`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d739cafe3631a70aa45b66405b7ee3c318201f80e4730c1ec0b677a6577ef`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:c2f46fb827de375ade02134d850c6e1ca8f28eda09392e50ea12ab93adf58ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43086382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691d36fb75bfe85cc9e08510e653c352b47199165460bd76bd8dedc771305e7c`

```dockerfile
```

-	Layers:
	-	`sha256:156c2092564616f60ea62c966c6d52214afbba47e1ae926492b5ef5b0694d848`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 43.1 MB (43059579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f143d04d23bed1c62d2c17a3c39fd4d1453dc80b11d55cb41f37d548bf358dc9`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 26.8 KB (26803 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:05844f5df9e69c3c4b7505c52d7b77631a21330530056181c77322ee92dc978a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.6 MB (611612504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45293f73bfdfd88ad9677e7d017732c2350363861f4c75f309091c3bb65c3d7e`
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
# Tue, 30 Jun 2026 23:35:32 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:32 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:39 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jun 2026 23:35:40 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:40 GMT
ARG ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
# Tue, 30 Jun 2026 23:36:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9fe9ef32a47ca7a4dd03e8f7b210bbb2ad5dc1995e156cf19025a73247b3e8`  
		Last Modified: Tue, 30 Jun 2026 23:38:09 GMT  
		Size: 235.6 MB (235593116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7d6ed60e7e8909f7ae436d484aeb14bee7c1d8fd70069b39b83690cc7fe820`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 2.6 MB (2606995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0106341e845feca5e7d1f809c21ba5b19add71725b380cea9fe9ed2033174`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 483.0 KB (482985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2d0712e5a0d3c23d29f8056bec57871bcf0dd5c7f4270138640296bf8b10de`  
		Last Modified: Tue, 30 Jun 2026 23:38:11 GMT  
		Size: 345.3 MB (345319986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64150a62fccc80de8f8b81cb6f30dca1dc7de620b16855d9df6d97ebbb97cdb8`  
		Last Modified: Tue, 30 Jun 2026 23:38:01 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ca390359aac4cddfbede1b45f5a138bd140809be01d653ab404b3fcaf159da`  
		Last Modified: Tue, 30 Jun 2026 23:38:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81145ce39bfb50cf3ee811c481907a1da3cd68b5f4c0a07c8c1579c23ba1b4cd`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746e6c21d8778c893fc0f3af330ae13c1fd6d2b309e7ccfc3157eae1f8f82cdf`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:014caf0459351b121bda60d3ea3c1b95f873d99c25ec8b206d8855b1301ec204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43093042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27291e55d3df0eebdf1e3ccf9d07a71e5c66d1b7b255fe7de091888eff4a4ca5`

```dockerfile
```

-	Layers:
	-	`sha256:d251012a990c371c9d62650062f6a73386e1a1319ac18cb94263275ba7181cf6`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 43.1 MB (43066086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5194937257dceec6f71f7d81fdde936c568fa4f939d0248ecaf7e653d1895d9`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:f210a19a0e1301e02a2b860a9745da1ba0e2522f48fc26a70dfdef6cb48866ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:5bfda275c8ca6cc25f063751a11a2751492438c6148f467b299b9f2b2a59fca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616894332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bad06fdef8a46e28e3d43c2ce4d7969a0f2cb9a3fda2d07ca64975ab034dff`
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
# Tue, 30 Jun 2026 23:37:50 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:50 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jun 2026 23:37:56 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:37:56 GMT
ARG ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:38:52 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:38:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:38:52 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
USER odoo
# Tue, 30 Jun 2026 23:38:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:38:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4dc009fcb52162f88b61048bb265128eb415230c05f908fed68e732893515`  
		Last Modified: Tue, 30 Jun 2026 23:40:21 GMT  
		Size: 238.4 MB (238372188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1006fd5c64994d2b344066b5f35d2ec3534aa4b2fd4c7f386cc980a8379bf72f`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 2.6 MB (2611783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5671eed01885bb857789c558d9820246c6f30160ac2e0e692d101b99355f9645`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 482.9 KB (482939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2491feff5b0506ad945ed5129c3fc6200b73b202e5aafdbb07cf884fade79`  
		Last Modified: Tue, 30 Jun 2026 23:40:25 GMT  
		Size: 345.7 MB (345687949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f39b8671dbf0a3c8abfb5610e5f3cca9ae8f1bd5fffc2f7bff3cb0e0d1cbd55`  
		Last Modified: Tue, 30 Jun 2026 23:40:09 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8076ddd15f0625ba0f505a680a4375a1189f8cd5c11bc03a37a3b06dc39db721`  
		Last Modified: Tue, 30 Jun 2026 23:40:09 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140c9924aedc5375de4b5b2fdc25dd6a121243aa70495f87cb9bfee1c30a6d7`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d739cafe3631a70aa45b66405b7ee3c318201f80e4730c1ec0b677a6577ef`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c2f46fb827de375ade02134d850c6e1ca8f28eda09392e50ea12ab93adf58ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43086382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691d36fb75bfe85cc9e08510e653c352b47199165460bd76bd8dedc771305e7c`

```dockerfile
```

-	Layers:
	-	`sha256:156c2092564616f60ea62c966c6d52214afbba47e1ae926492b5ef5b0694d848`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 43.1 MB (43059579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f143d04d23bed1c62d2c17a3c39fd4d1453dc80b11d55cb41f37d548bf358dc9`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 26.8 KB (26803 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:05844f5df9e69c3c4b7505c52d7b77631a21330530056181c77322ee92dc978a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.6 MB (611612504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45293f73bfdfd88ad9677e7d017732c2350363861f4c75f309091c3bb65c3d7e`
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
# Tue, 30 Jun 2026 23:35:32 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:32 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:39 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jun 2026 23:35:40 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:40 GMT
ARG ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
# Tue, 30 Jun 2026 23:36:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9fe9ef32a47ca7a4dd03e8f7b210bbb2ad5dc1995e156cf19025a73247b3e8`  
		Last Modified: Tue, 30 Jun 2026 23:38:09 GMT  
		Size: 235.6 MB (235593116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7d6ed60e7e8909f7ae436d484aeb14bee7c1d8fd70069b39b83690cc7fe820`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 2.6 MB (2606995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0106341e845feca5e7d1f809c21ba5b19add71725b380cea9fe9ed2033174`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 483.0 KB (482985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2d0712e5a0d3c23d29f8056bec57871bcf0dd5c7f4270138640296bf8b10de`  
		Last Modified: Tue, 30 Jun 2026 23:38:11 GMT  
		Size: 345.3 MB (345319986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64150a62fccc80de8f8b81cb6f30dca1dc7de620b16855d9df6d97ebbb97cdb8`  
		Last Modified: Tue, 30 Jun 2026 23:38:01 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ca390359aac4cddfbede1b45f5a138bd140809be01d653ab404b3fcaf159da`  
		Last Modified: Tue, 30 Jun 2026 23:38:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81145ce39bfb50cf3ee811c481907a1da3cd68b5f4c0a07c8c1579c23ba1b4cd`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746e6c21d8778c893fc0f3af330ae13c1fd6d2b309e7ccfc3157eae1f8f82cdf`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:014caf0459351b121bda60d3ea3c1b95f873d99c25ec8b206d8855b1301ec204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43093042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27291e55d3df0eebdf1e3ccf9d07a71e5c66d1b7b255fe7de091888eff4a4ca5`

```dockerfile
```

-	Layers:
	-	`sha256:d251012a990c371c9d62650062f6a73386e1a1319ac18cb94263275ba7181cf6`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 43.1 MB (43066086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5194937257dceec6f71f7d81fdde936c568fa4f939d0248ecaf7e653d1895d9`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20260630`

```console
$ docker pull odoo@sha256:f210a19a0e1301e02a2b860a9745da1ba0e2522f48fc26a70dfdef6cb48866ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20260630` - linux; amd64

```console
$ docker pull odoo@sha256:5bfda275c8ca6cc25f063751a11a2751492438c6148f467b299b9f2b2a59fca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **616.9 MB (616894332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bad06fdef8a46e28e3d43c2ce4d7969a0f2cb9a3fda2d07ca64975ab034dff`
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
# Tue, 30 Jun 2026 23:37:50 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:50 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:50 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:50 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:50 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:37:56 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jun 2026 23:37:56 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:37:56 GMT
ARG ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:38:52 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:38:52 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:38:52 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:38:52 GMT
USER odoo
# Tue, 30 Jun 2026 23:38:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:38:52 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c4dc009fcb52162f88b61048bb265128eb415230c05f908fed68e732893515`  
		Last Modified: Tue, 30 Jun 2026 23:40:21 GMT  
		Size: 238.4 MB (238372188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1006fd5c64994d2b344066b5f35d2ec3534aa4b2fd4c7f386cc980a8379bf72f`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 2.6 MB (2611783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5671eed01885bb857789c558d9820246c6f30160ac2e0e692d101b99355f9645`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 482.9 KB (482939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2491feff5b0506ad945ed5129c3fc6200b73b202e5aafdbb07cf884fade79`  
		Last Modified: Tue, 30 Jun 2026 23:40:25 GMT  
		Size: 345.7 MB (345687949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f39b8671dbf0a3c8abfb5610e5f3cca9ae8f1bd5fffc2f7bff3cb0e0d1cbd55`  
		Last Modified: Tue, 30 Jun 2026 23:40:09 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8076ddd15f0625ba0f505a680a4375a1189f8cd5c11bc03a37a3b06dc39db721`  
		Last Modified: Tue, 30 Jun 2026 23:40:09 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140c9924aedc5375de4b5b2fdc25dd6a121243aa70495f87cb9bfee1c30a6d7`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d739cafe3631a70aa45b66405b7ee3c318201f80e4730c1ec0b677a6577ef`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:c2f46fb827de375ade02134d850c6e1ca8f28eda09392e50ea12ab93adf58ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43086382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691d36fb75bfe85cc9e08510e653c352b47199165460bd76bd8dedc771305e7c`

```dockerfile
```

-	Layers:
	-	`sha256:156c2092564616f60ea62c966c6d52214afbba47e1ae926492b5ef5b0694d848`  
		Last Modified: Tue, 30 Jun 2026 23:40:10 GMT  
		Size: 43.1 MB (43059579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f143d04d23bed1c62d2c17a3c39fd4d1453dc80b11d55cb41f37d548bf358dc9`  
		Last Modified: Tue, 30 Jun 2026 23:40:07 GMT  
		Size: 26.8 KB (26803 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20260630` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:05844f5df9e69c3c4b7505c52d7b77631a21330530056181c77322ee92dc978a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.6 MB (611612504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45293f73bfdfd88ad9677e7d017732c2350363861f4c75f309091c3bb65c3d7e`
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
# Tue, 30 Jun 2026 23:35:32 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:32 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:32 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:32 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:39 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:40 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:40 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Jun 2026 23:35:40 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:40 GMT
ARG ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
# Tue, 30 Jun 2026 23:36:36 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:36 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:36 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=51a6dfb4165c0b9b90c0033192074e3efa585a2f
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:37 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:37 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:37 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:37 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:37 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9fe9ef32a47ca7a4dd03e8f7b210bbb2ad5dc1995e156cf19025a73247b3e8`  
		Last Modified: Tue, 30 Jun 2026 23:38:09 GMT  
		Size: 235.6 MB (235593116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7d6ed60e7e8909f7ae436d484aeb14bee7c1d8fd70069b39b83690cc7fe820`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 2.6 MB (2606995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab0106341e845feca5e7d1f809c21ba5b19add71725b380cea9fe9ed2033174`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 483.0 KB (482985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2d0712e5a0d3c23d29f8056bec57871bcf0dd5c7f4270138640296bf8b10de`  
		Last Modified: Tue, 30 Jun 2026 23:38:11 GMT  
		Size: 345.3 MB (345319986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64150a62fccc80de8f8b81cb6f30dca1dc7de620b16855d9df6d97ebbb97cdb8`  
		Last Modified: Tue, 30 Jun 2026 23:38:01 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ca390359aac4cddfbede1b45f5a138bd140809be01d653ab404b3fcaf159da`  
		Last Modified: Tue, 30 Jun 2026 23:38:01 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81145ce39bfb50cf3ee811c481907a1da3cd68b5f4c0a07c8c1579c23ba1b4cd`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746e6c21d8778c893fc0f3af330ae13c1fd6d2b309e7ccfc3157eae1f8f82cdf`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:014caf0459351b121bda60d3ea3c1b95f873d99c25ec8b206d8855b1301ec204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43093042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27291e55d3df0eebdf1e3ccf9d07a71e5c66d1b7b255fe7de091888eff4a4ca5`

```dockerfile
```

-	Layers:
	-	`sha256:d251012a990c371c9d62650062f6a73386e1a1319ac18cb94263275ba7181cf6`  
		Last Modified: Tue, 30 Jun 2026 23:38:03 GMT  
		Size: 43.1 MB (43066086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5194937257dceec6f71f7d81fdde936c568fa4f939d0248ecaf7e653d1895d9`  
		Last Modified: Tue, 30 Jun 2026 23:38:00 GMT  
		Size: 27.0 KB (26956 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:b9da278bc64c41e22a2e30fcf32e87fc3ba1c82f6154cd22bf4336a7f0a4bcf5
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
$ docker pull odoo@sha256:010494207792d203a723feacf2c199167f146085aae0632e848b5434fdb7cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.9 MB (692865041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed8899269ce05d9fddd5f44e82cf449fa29901977ca3aea4f91e02e6a0f123d`
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
# Tue, 30 Jun 2026 23:37:56 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:56 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:38:04 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:38:04 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:38:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:38:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:38:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
USER odoo
# Tue, 30 Jun 2026 23:38:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:38:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e958ce98eaeb5b906c5b11fb3487baf925f05a75f680f23877c1a9b8981a4d`  
		Last Modified: Tue, 30 Jun 2026 23:40:47 GMT  
		Size: 257.1 MB (257063701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebc79b623e73a1d98d0fd81d12b3276c9922c2e9789937a39bdefec7d027661`  
		Last Modified: Tue, 30 Jun 2026 23:40:38 GMT  
		Size: 16.8 MB (16779696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78605a7beffed8ad2c167f99e2c203622b2ceb7a94e365a2cb7bd3884880a2`  
		Last Modified: Tue, 30 Jun 2026 23:40:37 GMT  
		Size: 482.6 KB (482626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff5760762511580378e747e4196d93f7795500a166be2b3fa4f2da2823b2d92`  
		Last Modified: Tue, 30 Jun 2026 23:40:49 GMT  
		Size: 388.8 MB (388803421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fead65f0ed0fcd52870a1a57c9290bcf1f7bdf9357282976bca7c7bfe99601`  
		Last Modified: Tue, 30 Jun 2026 23:40:38 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341460c6f2599c38728cd28bc9f93050ff12cef4a276b4e43538633710c9827e`  
		Last Modified: Tue, 30 Jun 2026 23:40:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6b5d569c492cbfec98e2e472eccfb25d2abee3a24bc4ea4950bf4f59fb2672`  
		Last Modified: Tue, 30 Jun 2026 23:40:39 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb79b6897611c7039eed3b9d922e911c0ab106585fe7e6f220ff22b4d463b25`  
		Last Modified: Tue, 30 Jun 2026 23:40:41 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:6bc3dcf3904cd1044022d145d089e2045361e35e850f2967dd4808f3fcba353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62587035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f3ef7a7b92a87e038dc59a4972a09c70c4636b06d9cb09f5162150db9b1a9e`

```dockerfile
```

-	Layers:
	-	`sha256:003813cef9069cb28c1d04fd1ac8332949541d651e43ed8673cea68d545b9001`  
		Last Modified: Tue, 30 Jun 2026 23:40:41 GMT  
		Size: 62.6 MB (62560224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cf1329ca3d1f87d691f03f6f63e38cb1011c5d3884417ce89d6d69ab439fdf4`  
		Last Modified: Tue, 30 Jun 2026 23:40:37 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f3f7aa25a645a09d050620f98255ccaa8ef5e947b70a540da0ff7c0cae04bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 MB (689011977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af0feb1277d98ce924cc1c71ace56b8a9464693122de1efab1f66ec963712e`
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
# Tue, 30 Jun 2026 23:35:45 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:45 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:45 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:45 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:56 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:56 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:35:56 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:56 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:36:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:49 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:49 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c28c51c5f775ada3f4f20572efd0d5ddb0f436485efcf1af7ea1f5c25985cd`  
		Last Modified: Tue, 30 Jun 2026 23:39:02 GMT  
		Size: 254.3 MB (254282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e5c73d15d81189fad22bc7c478576383e733ffd2783626bbb012e7fa20bb81`  
		Last Modified: Tue, 30 Jun 2026 23:38:52 GMT  
		Size: 16.7 MB (16719084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d472d67f4217fafb7659f5ec83592880081cff5a96fa382ccb719189a78f45`  
		Last Modified: Tue, 30 Jun 2026 23:38:51 GMT  
		Size: 482.6 KB (482633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d71f675900f996fb2031eebabf675510b7220dc30f73dfb6ee85b478c631d1`  
		Last Modified: Tue, 30 Jun 2026 23:39:04 GMT  
		Size: 388.6 MB (388648682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0caacfc3fcb97e2f7657a7e304580a6ca2235385a3e76412a7748e9c48d57e1`  
		Last Modified: Tue, 30 Jun 2026 23:38:52 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0191af9bf21278dc6f69eb69f7f3b12f3a0220944b43935b0527b3009c352c`  
		Last Modified: Tue, 30 Jun 2026 23:38:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553df1537b2a53e7d23ddd8b8b14986abfc00635e44bbf18f4a409a88fd016f1`  
		Last Modified: Tue, 30 Jun 2026 23:38:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606bca78b9e839334c6020ff5e7f0bbbdd278062b328160a3d9565e7fa918b86`  
		Last Modified: Tue, 30 Jun 2026 23:38:55 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:ef56616746f116c43a99f45dbc676ea327e898ae1143c9c5d0df8bdbb8dac9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62594466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c7fe8be912531809e39a90fbf8feb7aebac3927ec833a0fb41d84a10664327`

```dockerfile
```

-	Layers:
	-	`sha256:6e0c9ef71cfa9213c2b0579315fa7ceb2fdd11f7f39afe49cf07998e731b7f94`  
		Last Modified: Tue, 30 Jun 2026 23:38:55 GMT  
		Size: 62.6 MB (62567503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a439822333bae292837939af35636cf36c7fcdb369c9f997199ec794ff2944`  
		Last Modified: Tue, 30 Jun 2026 23:38:51 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:2ea25ffc2876d12404762f1410d1aaf25ae6f672f3cea360140067b659a67ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.5 MB (709542612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183326c2c681cb65c21b21dd446aef335550e7443c05e377b9ee75a452253a58`
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
# Tue, 30 Jun 2026 23:32:42 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:32:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:32:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jun 2026 23:32:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:33:01 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:34:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:34:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:34:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:34:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:34:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:34:54 GMT
USER odoo
# Tue, 30 Jun 2026 23:34:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:34:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e83db4c0f91c3a2b071bba1ef13204b2a8125ff767668895631b827c30d5e`  
		Last Modified: Tue, 30 Jun 2026 23:39:35 GMT  
		Size: 267.9 MB (267946018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b578ec0bb2e72240c01425d3256e7be25da85c765a9d9d1fa382334dd97e8de`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 17.5 MB (17456519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b81fe9abe408f00b0d14e8786a827cbacf8b5da70d10d5f56708741d46b96b`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 482.7 KB (482666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2ed05a918fed5ddb7dbcf46d9cdce7b24838232ba544586d06d945919fac32`  
		Last Modified: Tue, 30 Jun 2026 23:39:37 GMT  
		Size: 389.3 MB (389340513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec102b1e45c20f72293eeb8cf5bd46f07555caaaf457e9c108bf63c6873579d1`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6699604d4a39670f5c45a920b36eee0140efbc97fc1ddcb94effc28128ccca61`  
		Last Modified: Tue, 30 Jun 2026 23:39:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d9856844a7e9f21283be9fd9491aeb05dfcfe6efad9defa63894d37867e35a`  
		Last Modified: Tue, 30 Jun 2026 23:39:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355d2a6c8d6144a530b97f7a62d725e4ac8a34807a6103c84cfe031aa6f8c48b`  
		Last Modified: Tue, 30 Jun 2026 23:39:27 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:5e84c87dc4e01a37598a50269f1e1d41c1587f23655881881519d5635cf12600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04161f51dc880c7cbd2a6da206287455b4494debcd04184a32eeeaeb651a1b7c`

```dockerfile
```

-	Layers:
	-	`sha256:db5accb07b3d0fba90a1c0fcf2eb0d6d44cb77be319c0a95846095400f6fcc93`  
		Last Modified: Tue, 30 Jun 2026 23:39:28 GMT  
		Size: 62.6 MB (62568607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a7487faa5b2d720aa404972ed683118daff79552301678eae6dcfb25440962`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:b9da278bc64c41e22a2e30fcf32e87fc3ba1c82f6154cd22bf4336a7f0a4bcf5
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
$ docker pull odoo@sha256:010494207792d203a723feacf2c199167f146085aae0632e848b5434fdb7cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.9 MB (692865041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed8899269ce05d9fddd5f44e82cf449fa29901977ca3aea4f91e02e6a0f123d`
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
# Tue, 30 Jun 2026 23:37:56 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:56 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:38:04 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:38:04 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:38:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:38:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:38:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
USER odoo
# Tue, 30 Jun 2026 23:38:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:38:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e958ce98eaeb5b906c5b11fb3487baf925f05a75f680f23877c1a9b8981a4d`  
		Last Modified: Tue, 30 Jun 2026 23:40:47 GMT  
		Size: 257.1 MB (257063701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebc79b623e73a1d98d0fd81d12b3276c9922c2e9789937a39bdefec7d027661`  
		Last Modified: Tue, 30 Jun 2026 23:40:38 GMT  
		Size: 16.8 MB (16779696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78605a7beffed8ad2c167f99e2c203622b2ceb7a94e365a2cb7bd3884880a2`  
		Last Modified: Tue, 30 Jun 2026 23:40:37 GMT  
		Size: 482.6 KB (482626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff5760762511580378e747e4196d93f7795500a166be2b3fa4f2da2823b2d92`  
		Last Modified: Tue, 30 Jun 2026 23:40:49 GMT  
		Size: 388.8 MB (388803421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fead65f0ed0fcd52870a1a57c9290bcf1f7bdf9357282976bca7c7bfe99601`  
		Last Modified: Tue, 30 Jun 2026 23:40:38 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341460c6f2599c38728cd28bc9f93050ff12cef4a276b4e43538633710c9827e`  
		Last Modified: Tue, 30 Jun 2026 23:40:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6b5d569c492cbfec98e2e472eccfb25d2abee3a24bc4ea4950bf4f59fb2672`  
		Last Modified: Tue, 30 Jun 2026 23:40:39 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb79b6897611c7039eed3b9d922e911c0ab106585fe7e6f220ff22b4d463b25`  
		Last Modified: Tue, 30 Jun 2026 23:40:41 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6bc3dcf3904cd1044022d145d089e2045361e35e850f2967dd4808f3fcba353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62587035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f3ef7a7b92a87e038dc59a4972a09c70c4636b06d9cb09f5162150db9b1a9e`

```dockerfile
```

-	Layers:
	-	`sha256:003813cef9069cb28c1d04fd1ac8332949541d651e43ed8673cea68d545b9001`  
		Last Modified: Tue, 30 Jun 2026 23:40:41 GMT  
		Size: 62.6 MB (62560224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cf1329ca3d1f87d691f03f6f63e38cb1011c5d3884417ce89d6d69ab439fdf4`  
		Last Modified: Tue, 30 Jun 2026 23:40:37 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f3f7aa25a645a09d050620f98255ccaa8ef5e947b70a540da0ff7c0cae04bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 MB (689011977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af0feb1277d98ce924cc1c71ace56b8a9464693122de1efab1f66ec963712e`
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
# Tue, 30 Jun 2026 23:35:45 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:45 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:45 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:45 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:56 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:56 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:35:56 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:56 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:36:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:49 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:49 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c28c51c5f775ada3f4f20572efd0d5ddb0f436485efcf1af7ea1f5c25985cd`  
		Last Modified: Tue, 30 Jun 2026 23:39:02 GMT  
		Size: 254.3 MB (254282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e5c73d15d81189fad22bc7c478576383e733ffd2783626bbb012e7fa20bb81`  
		Last Modified: Tue, 30 Jun 2026 23:38:52 GMT  
		Size: 16.7 MB (16719084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d472d67f4217fafb7659f5ec83592880081cff5a96fa382ccb719189a78f45`  
		Last Modified: Tue, 30 Jun 2026 23:38:51 GMT  
		Size: 482.6 KB (482633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d71f675900f996fb2031eebabf675510b7220dc30f73dfb6ee85b478c631d1`  
		Last Modified: Tue, 30 Jun 2026 23:39:04 GMT  
		Size: 388.6 MB (388648682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0caacfc3fcb97e2f7657a7e304580a6ca2235385a3e76412a7748e9c48d57e1`  
		Last Modified: Tue, 30 Jun 2026 23:38:52 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0191af9bf21278dc6f69eb69f7f3b12f3a0220944b43935b0527b3009c352c`  
		Last Modified: Tue, 30 Jun 2026 23:38:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553df1537b2a53e7d23ddd8b8b14986abfc00635e44bbf18f4a409a88fd016f1`  
		Last Modified: Tue, 30 Jun 2026 23:38:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606bca78b9e839334c6020ff5e7f0bbbdd278062b328160a3d9565e7fa918b86`  
		Last Modified: Tue, 30 Jun 2026 23:38:55 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:ef56616746f116c43a99f45dbc676ea327e898ae1143c9c5d0df8bdbb8dac9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62594466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c7fe8be912531809e39a90fbf8feb7aebac3927ec833a0fb41d84a10664327`

```dockerfile
```

-	Layers:
	-	`sha256:6e0c9ef71cfa9213c2b0579315fa7ceb2fdd11f7f39afe49cf07998e731b7f94`  
		Last Modified: Tue, 30 Jun 2026 23:38:55 GMT  
		Size: 62.6 MB (62567503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a439822333bae292837939af35636cf36c7fcdb369c9f997199ec794ff2944`  
		Last Modified: Tue, 30 Jun 2026 23:38:51 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:2ea25ffc2876d12404762f1410d1aaf25ae6f672f3cea360140067b659a67ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.5 MB (709542612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183326c2c681cb65c21b21dd446aef335550e7443c05e377b9ee75a452253a58`
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
# Tue, 30 Jun 2026 23:32:42 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:32:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:32:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jun 2026 23:32:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:33:01 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:34:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:34:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:34:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:34:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:34:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:34:54 GMT
USER odoo
# Tue, 30 Jun 2026 23:34:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:34:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e83db4c0f91c3a2b071bba1ef13204b2a8125ff767668895631b827c30d5e`  
		Last Modified: Tue, 30 Jun 2026 23:39:35 GMT  
		Size: 267.9 MB (267946018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b578ec0bb2e72240c01425d3256e7be25da85c765a9d9d1fa382334dd97e8de`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 17.5 MB (17456519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b81fe9abe408f00b0d14e8786a827cbacf8b5da70d10d5f56708741d46b96b`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 482.7 KB (482666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2ed05a918fed5ddb7dbcf46d9cdce7b24838232ba544586d06d945919fac32`  
		Last Modified: Tue, 30 Jun 2026 23:39:37 GMT  
		Size: 389.3 MB (389340513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec102b1e45c20f72293eeb8cf5bd46f07555caaaf457e9c108bf63c6873579d1`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6699604d4a39670f5c45a920b36eee0140efbc97fc1ddcb94effc28128ccca61`  
		Last Modified: Tue, 30 Jun 2026 23:39:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d9856844a7e9f21283be9fd9491aeb05dfcfe6efad9defa63894d37867e35a`  
		Last Modified: Tue, 30 Jun 2026 23:39:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355d2a6c8d6144a530b97f7a62d725e4ac8a34807a6103c84cfe031aa6f8c48b`  
		Last Modified: Tue, 30 Jun 2026 23:39:27 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:5e84c87dc4e01a37598a50269f1e1d41c1587f23655881881519d5635cf12600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04161f51dc880c7cbd2a6da206287455b4494debcd04184a32eeeaeb651a1b7c`

```dockerfile
```

-	Layers:
	-	`sha256:db5accb07b3d0fba90a1c0fcf2eb0d6d44cb77be319c0a95846095400f6fcc93`  
		Last Modified: Tue, 30 Jun 2026 23:39:28 GMT  
		Size: 62.6 MB (62568607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a7487faa5b2d720aa404972ed683118daff79552301678eae6dcfb25440962`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20260630`

```console
$ docker pull odoo@sha256:b9da278bc64c41e22a2e30fcf32e87fc3ba1c82f6154cd22bf4336a7f0a4bcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20260630` - linux; amd64

```console
$ docker pull odoo@sha256:010494207792d203a723feacf2c199167f146085aae0632e848b5434fdb7cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **692.9 MB (692865041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed8899269ce05d9fddd5f44e82cf449fa29901977ca3aea4f91e02e6a0f123d`
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
# Tue, 30 Jun 2026 23:37:56 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:56 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:56 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:56 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:56 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:38:04 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:38:04 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:38:04 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:38:52 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:38:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:38:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:38:53 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:38:53 GMT
USER odoo
# Tue, 30 Jun 2026 23:38:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:38:53 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e958ce98eaeb5b906c5b11fb3487baf925f05a75f680f23877c1a9b8981a4d`  
		Last Modified: Tue, 30 Jun 2026 23:40:47 GMT  
		Size: 257.1 MB (257063701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebc79b623e73a1d98d0fd81d12b3276c9922c2e9789937a39bdefec7d027661`  
		Last Modified: Tue, 30 Jun 2026 23:40:38 GMT  
		Size: 16.8 MB (16779696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78605a7beffed8ad2c167f99e2c203622b2ceb7a94e365a2cb7bd3884880a2`  
		Last Modified: Tue, 30 Jun 2026 23:40:37 GMT  
		Size: 482.6 KB (482626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff5760762511580378e747e4196d93f7795500a166be2b3fa4f2da2823b2d92`  
		Last Modified: Tue, 30 Jun 2026 23:40:49 GMT  
		Size: 388.8 MB (388803421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fead65f0ed0fcd52870a1a57c9290bcf1f7bdf9357282976bca7c7bfe99601`  
		Last Modified: Tue, 30 Jun 2026 23:40:38 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341460c6f2599c38728cd28bc9f93050ff12cef4a276b4e43538633710c9827e`  
		Last Modified: Tue, 30 Jun 2026 23:40:39 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6b5d569c492cbfec98e2e472eccfb25d2abee3a24bc4ea4950bf4f59fb2672`  
		Last Modified: Tue, 30 Jun 2026 23:40:39 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb79b6897611c7039eed3b9d922e911c0ab106585fe7e6f220ff22b4d463b25`  
		Last Modified: Tue, 30 Jun 2026 23:40:41 GMT  
		Size: 877.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:6bc3dcf3904cd1044022d145d089e2045361e35e850f2967dd4808f3fcba353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62587035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f3ef7a7b92a87e038dc59a4972a09c70c4636b06d9cb09f5162150db9b1a9e`

```dockerfile
```

-	Layers:
	-	`sha256:003813cef9069cb28c1d04fd1ac8332949541d651e43ed8673cea68d545b9001`  
		Last Modified: Tue, 30 Jun 2026 23:40:41 GMT  
		Size: 62.6 MB (62560224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cf1329ca3d1f87d691f03f6f63e38cb1011c5d3884417ce89d6d69ab439fdf4`  
		Last Modified: Tue, 30 Jun 2026 23:40:37 GMT  
		Size: 26.8 KB (26811 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260630` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:f3f7aa25a645a09d050620f98255ccaa8ef5e947b70a540da0ff7c0cae04bebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **689.0 MB (689011977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4af0feb1277d98ce924cc1c71ace56b8a9464693122de1efab1f66ec963712e`
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
# Tue, 30 Jun 2026 23:35:45 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:45 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:45 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:45 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:45 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:55 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:56 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:56 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:35:56 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:56 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:36:48 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:49 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:49 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:49 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:49 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:49 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c28c51c5f775ada3f4f20572efd0d5ddb0f436485efcf1af7ea1f5c25985cd`  
		Last Modified: Tue, 30 Jun 2026 23:39:02 GMT  
		Size: 254.3 MB (254282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e5c73d15d81189fad22bc7c478576383e733ffd2783626bbb012e7fa20bb81`  
		Last Modified: Tue, 30 Jun 2026 23:38:52 GMT  
		Size: 16.7 MB (16719084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d472d67f4217fafb7659f5ec83592880081cff5a96fa382ccb719189a78f45`  
		Last Modified: Tue, 30 Jun 2026 23:38:51 GMT  
		Size: 482.6 KB (482633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d71f675900f996fb2031eebabf675510b7220dc30f73dfb6ee85b478c631d1`  
		Last Modified: Tue, 30 Jun 2026 23:39:04 GMT  
		Size: 388.6 MB (388648682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0caacfc3fcb97e2f7657a7e304580a6ca2235385a3e76412a7748e9c48d57e1`  
		Last Modified: Tue, 30 Jun 2026 23:38:52 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0191af9bf21278dc6f69eb69f7f3b12f3a0220944b43935b0527b3009c352c`  
		Last Modified: Tue, 30 Jun 2026 23:38:54 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553df1537b2a53e7d23ddd8b8b14986abfc00635e44bbf18f4a409a88fd016f1`  
		Last Modified: Tue, 30 Jun 2026 23:38:54 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606bca78b9e839334c6020ff5e7f0bbbdd278062b328160a3d9565e7fa918b86`  
		Last Modified: Tue, 30 Jun 2026 23:38:55 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:ef56616746f116c43a99f45dbc676ea327e898ae1143c9c5d0df8bdbb8dac9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62594466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c7fe8be912531809e39a90fbf8feb7aebac3927ec833a0fb41d84a10664327`

```dockerfile
```

-	Layers:
	-	`sha256:6e0c9ef71cfa9213c2b0579315fa7ceb2fdd11f7f39afe49cf07998e731b7f94`  
		Last Modified: Tue, 30 Jun 2026 23:38:55 GMT  
		Size: 62.6 MB (62567503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2a439822333bae292837939af35636cf36c7fcdb369c9f997199ec794ff2944`  
		Last Modified: Tue, 30 Jun 2026 23:38:51 GMT  
		Size: 27.0 KB (26963 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20260630` - linux; ppc64le

```console
$ docker pull odoo@sha256:2ea25ffc2876d12404762f1410d1aaf25ae6f672f3cea360140067b659a67ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.5 MB (709542612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183326c2c681cb65c21b21dd446aef335550e7443c05e377b9ee75a452253a58`
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
# Tue, 30 Jun 2026 23:32:42 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:32:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:32:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jun 2026 23:32:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:33:01 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
ENV ODOO_VERSION=18.0
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
# Tue, 30 Jun 2026 23:34:51 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:34:52 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=a6a0989209a2d98fd6c9a8fdc9b3b37c43ac73ae
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:34:53 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:34:53 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:34:53 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:34:54 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:34:54 GMT
USER odoo
# Tue, 30 Jun 2026 23:34:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:34:54 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e83db4c0f91c3a2b071bba1ef13204b2a8125ff767668895631b827c30d5e`  
		Last Modified: Tue, 30 Jun 2026 23:39:35 GMT  
		Size: 267.9 MB (267946018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b578ec0bb2e72240c01425d3256e7be25da85c765a9d9d1fa382334dd97e8de`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 17.5 MB (17456519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b81fe9abe408f00b0d14e8786a827cbacf8b5da70d10d5f56708741d46b96b`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 482.7 KB (482666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2ed05a918fed5ddb7dbcf46d9cdce7b24838232ba544586d06d945919fac32`  
		Last Modified: Tue, 30 Jun 2026 23:39:37 GMT  
		Size: 389.3 MB (389340513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec102b1e45c20f72293eeb8cf5bd46f07555caaaf457e9c108bf63c6873579d1`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 766.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6699604d4a39670f5c45a920b36eee0140efbc97fc1ddcb94effc28128ccca61`  
		Last Modified: Tue, 30 Jun 2026 23:39:26 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d9856844a7e9f21283be9fd9491aeb05dfcfe6efad9defa63894d37867e35a`  
		Last Modified: Tue, 30 Jun 2026 23:39:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355d2a6c8d6144a530b97f7a62d725e4ac8a34807a6103c84cfe031aa6f8c48b`  
		Last Modified: Tue, 30 Jun 2026 23:39:27 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:5e84c87dc4e01a37598a50269f1e1d41c1587f23655881881519d5635cf12600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62595474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04161f51dc880c7cbd2a6da206287455b4494debcd04184a32eeeaeb651a1b7c`

```dockerfile
```

-	Layers:
	-	`sha256:db5accb07b3d0fba90a1c0fcf2eb0d6d44cb77be319c0a95846095400f6fcc93`  
		Last Modified: Tue, 30 Jun 2026 23:39:28 GMT  
		Size: 62.6 MB (62568607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a7487faa5b2d720aa404972ed683118daff79552301678eae6dcfb25440962`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:957d6b8a68a035154c682732780272e89b13dc3604d855bcaa2653bdea2d372b
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
$ docker pull odoo@sha256:d45f808cf08accbac383c14fea99da4f72e651aa99d3ae6dc4d1022570870b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.7 MB (713689871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d3a5cf9a7642951b89e457f68039001329c4cd53d44964e650cc0f5f06d5fc`
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
# Tue, 30 Jun 2026 23:37:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:53 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:38:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:39:01 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:39:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:39:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:39:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
USER odoo
# Tue, 30 Jun 2026 23:39:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:39:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e3d3d553f901dedafccf7adf8259846d966d7cf3dab2575984a4126f016cdb`  
		Last Modified: Tue, 30 Jun 2026 23:41:16 GMT  
		Size: 257.1 MB (257063783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa4341931c2942d6d02c72750d021c156cb981fa3ee4d76ed01f2e81765ae55`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 16.8 MB (16779757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7c7fb49ce8a177639e1d8d46569e710f12b57120316785b7ded934e00a27f4`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 482.6 KB (482639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac8325105ae39155ea58732e60421fee9155267e024938b2c8c3cb6efc5cf03`  
		Last Modified: Tue, 30 Jun 2026 23:41:19 GMT  
		Size: 409.6 MB (409628139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a5485e5ef960ca082d5bb15a34c1d5085f1a5da5eab361f7c56f2e96c2d2da`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c94c77677dfa1825591a63f73ca6f5cefbf6e3dfac7606b79da0ba225170a`  
		Last Modified: Tue, 30 Jun 2026 23:41:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b58bc9a47643fa96017ab5cd8f1e1bb3d58b930b5dcf41a8178b0824b70b2`  
		Last Modified: Tue, 30 Jun 2026 23:41:07 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c1bbeadfea29b830d1613d8cdce740f3b45b3a548a9c0564b8d97d9ca014b6`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:6873644659807dfdb10eb545113d249d93b98d3e17d0dd388a9f4b699dc16a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70858086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d068fad4331999ff59a2f5900530a1390f4e31d6f4b8620d261b967cba047`

```dockerfile
```

-	Layers:
	-	`sha256:4dee7414d35a03008ddcc38ac88eae33d9ad9ba83aec60eb988e9118304ca1d3`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 70.8 MB (70830981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6d1ec07ffa7d8ab12f9167672067792c310c42159fcf72a278b15e41e0b7b8`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ca88b278631c86851d073878de9f827d38a92905ac1b5ee1e99fa41ec5d6dbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709826817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c43e74d5778ef58ea36618362eff9473a6d8ae3ef599b5757bc7ea50e09db90`
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
# Tue, 30 Jun 2026 23:35:40 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:40 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea1fe1bd88f8173cf0d3949222d0f7c679a5be9683a51f7479d808fd66f94b`  
		Last Modified: Tue, 30 Jun 2026 23:39:51 GMT  
		Size: 254.3 MB (254283364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcb51ab0bed742664e171ac1eb007d60c22f7680463936cf887631f5fbec176`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 16.7 MB (16719074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca54857d19d6667b39322de7d23a2c1dd4c96b954d5ed318fb8972a03f8dd5a4`  
		Last Modified: Tue, 30 Jun 2026 23:39:40 GMT  
		Size: 482.6 KB (482633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62bb25b3bd85e3d48f169a51aeb983ed9ea7c5ae1d4dffd5578a67beeaa191d`  
		Last Modified: Tue, 30 Jun 2026 23:39:54 GMT  
		Size: 409.5 MB (409462597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a91c7f73f4223da04faf1cb5dc453a8e5846b8e7195dd49c15677d1e25a96f`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295f5ce41173e1bd741ab6a482769be3c3ddf63dfa9a0b5dd9ba909418aadf6f`  
		Last Modified: Tue, 30 Jun 2026 23:39:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be852638c47fe9ef554d4378365d5bcf2ad951d3cd4f1801d63bbd35e0f77457`  
		Last Modified: Tue, 30 Jun 2026 23:39:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc76b2cfb77989903b21847d66fc0da1e60d294484072cbb516202f55141a3`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:28c65114f25829a6ef7eb7cb96a8f027a2ac51818c0a4bda80b5bb2551aad29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8505daadf1b00d2c693274f541a4d71a59966f871597a7f4c86cb74dbd2da53e`

```dockerfile
```

-	Layers:
	-	`sha256:318ff156f6674c7db0041d3540ec385d15539720ce18ed46c4dcd59fb65db7ad`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 70.8 MB (70838272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f54b8083e5f920cb9ae6c6bcd6720e0f0a0493f53e2b6995f9ef148b8f1014`  
		Last Modified: Tue, 30 Jun 2026 23:39:39 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:5d24e4b5500f7a02070615cce7de584a8de233c81b6f08af685c730b909a6f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.4 MB (730372124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9f34e342b123d7e214252b368f8cceaaeb3022e0b7097366d0ea5e424571a6`
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
# Tue, 30 Jun 2026 23:32:42 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:32:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:32:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jun 2026 23:32:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:33:01 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:35:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:35:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:35:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:35:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:35:10 GMT
USER odoo
# Tue, 30 Jun 2026 23:35:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:35:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e83db4c0f91c3a2b071bba1ef13204b2a8125ff767668895631b827c30d5e`  
		Last Modified: Tue, 30 Jun 2026 23:39:35 GMT  
		Size: 267.9 MB (267946018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b578ec0bb2e72240c01425d3256e7be25da85c765a9d9d1fa382334dd97e8de`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 17.5 MB (17456519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b81fe9abe408f00b0d14e8786a827cbacf8b5da70d10d5f56708741d46b96b`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 482.7 KB (482666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981971459b68ee73f757375aa1c7cb74f65e859a7f802fe1050c9d3f889c9467`  
		Last Modified: Tue, 30 Jun 2026 23:41:03 GMT  
		Size: 410.2 MB (410170078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a4df37dcd7b26022e1f079a1f62333e1ef752ab6106392ed9a31cf2a1e8a75`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62356f1b949eb954f3c789c01f17258441d2f3e733020442047984c5b1d618`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85470c3a621918e3ee834b3668c0cf220efb787cbbab55a1a716ad084e3a3`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfcae7480e319e6b4d1e448397f372f1f9f63633eec8ebf8792511cd3c045d0`  
		Last Modified: Tue, 30 Jun 2026 23:40:55 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:d10033558a5b0150f11139da0261b3cafef2d9702bf1ef06eb9ec35ed8850d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70866537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683d07cd19bc87e344b7bdc4862b2ce1aea0548d9395b8724df309a3e4e58487`

```dockerfile
```

-	Layers:
	-	`sha256:f00a056413f747ed5d21b80fb23de7249c4c9e5489d1eee4fd169c1c507aa3d2`  
		Last Modified: Tue, 30 Jun 2026 23:40:57 GMT  
		Size: 70.8 MB (70839370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0282cb0c9bc349f17408188d1ad7d2b716bd86f04ed1b63ac3ea72cecc00c6`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:957d6b8a68a035154c682732780272e89b13dc3604d855bcaa2653bdea2d372b
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
$ docker pull odoo@sha256:d45f808cf08accbac383c14fea99da4f72e651aa99d3ae6dc4d1022570870b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.7 MB (713689871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d3a5cf9a7642951b89e457f68039001329c4cd53d44964e650cc0f5f06d5fc`
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
# Tue, 30 Jun 2026 23:37:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:53 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:38:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:39:01 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:39:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:39:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:39:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
USER odoo
# Tue, 30 Jun 2026 23:39:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:39:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e3d3d553f901dedafccf7adf8259846d966d7cf3dab2575984a4126f016cdb`  
		Last Modified: Tue, 30 Jun 2026 23:41:16 GMT  
		Size: 257.1 MB (257063783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa4341931c2942d6d02c72750d021c156cb981fa3ee4d76ed01f2e81765ae55`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 16.8 MB (16779757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7c7fb49ce8a177639e1d8d46569e710f12b57120316785b7ded934e00a27f4`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 482.6 KB (482639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac8325105ae39155ea58732e60421fee9155267e024938b2c8c3cb6efc5cf03`  
		Last Modified: Tue, 30 Jun 2026 23:41:19 GMT  
		Size: 409.6 MB (409628139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a5485e5ef960ca082d5bb15a34c1d5085f1a5da5eab361f7c56f2e96c2d2da`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c94c77677dfa1825591a63f73ca6f5cefbf6e3dfac7606b79da0ba225170a`  
		Last Modified: Tue, 30 Jun 2026 23:41:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b58bc9a47643fa96017ab5cd8f1e1bb3d58b930b5dcf41a8178b0824b70b2`  
		Last Modified: Tue, 30 Jun 2026 23:41:07 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c1bbeadfea29b830d1613d8cdce740f3b45b3a548a9c0564b8d97d9ca014b6`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:6873644659807dfdb10eb545113d249d93b98d3e17d0dd388a9f4b699dc16a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70858086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d068fad4331999ff59a2f5900530a1390f4e31d6f4b8620d261b967cba047`

```dockerfile
```

-	Layers:
	-	`sha256:4dee7414d35a03008ddcc38ac88eae33d9ad9ba83aec60eb988e9118304ca1d3`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 70.8 MB (70830981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6d1ec07ffa7d8ab12f9167672067792c310c42159fcf72a278b15e41e0b7b8`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ca88b278631c86851d073878de9f827d38a92905ac1b5ee1e99fa41ec5d6dbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709826817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c43e74d5778ef58ea36618362eff9473a6d8ae3ef599b5757bc7ea50e09db90`
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
# Tue, 30 Jun 2026 23:35:40 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:40 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea1fe1bd88f8173cf0d3949222d0f7c679a5be9683a51f7479d808fd66f94b`  
		Last Modified: Tue, 30 Jun 2026 23:39:51 GMT  
		Size: 254.3 MB (254283364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcb51ab0bed742664e171ac1eb007d60c22f7680463936cf887631f5fbec176`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 16.7 MB (16719074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca54857d19d6667b39322de7d23a2c1dd4c96b954d5ed318fb8972a03f8dd5a4`  
		Last Modified: Tue, 30 Jun 2026 23:39:40 GMT  
		Size: 482.6 KB (482633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62bb25b3bd85e3d48f169a51aeb983ed9ea7c5ae1d4dffd5578a67beeaa191d`  
		Last Modified: Tue, 30 Jun 2026 23:39:54 GMT  
		Size: 409.5 MB (409462597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a91c7f73f4223da04faf1cb5dc453a8e5846b8e7195dd49c15677d1e25a96f`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295f5ce41173e1bd741ab6a482769be3c3ddf63dfa9a0b5dd9ba909418aadf6f`  
		Last Modified: Tue, 30 Jun 2026 23:39:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be852638c47fe9ef554d4378365d5bcf2ad951d3cd4f1801d63bbd35e0f77457`  
		Last Modified: Tue, 30 Jun 2026 23:39:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc76b2cfb77989903b21847d66fc0da1e60d294484072cbb516202f55141a3`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:28c65114f25829a6ef7eb7cb96a8f027a2ac51818c0a4bda80b5bb2551aad29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8505daadf1b00d2c693274f541a4d71a59966f871597a7f4c86cb74dbd2da53e`

```dockerfile
```

-	Layers:
	-	`sha256:318ff156f6674c7db0041d3540ec385d15539720ce18ed46c4dcd59fb65db7ad`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 70.8 MB (70838272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f54b8083e5f920cb9ae6c6bcd6720e0f0a0493f53e2b6995f9ef148b8f1014`  
		Last Modified: Tue, 30 Jun 2026 23:39:39 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5d24e4b5500f7a02070615cce7de584a8de233c81b6f08af685c730b909a6f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.4 MB (730372124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9f34e342b123d7e214252b368f8cceaaeb3022e0b7097366d0ea5e424571a6`
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
# Tue, 30 Jun 2026 23:32:42 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:32:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:32:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jun 2026 23:32:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:33:01 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:35:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:35:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:35:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:35:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:35:10 GMT
USER odoo
# Tue, 30 Jun 2026 23:35:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:35:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e83db4c0f91c3a2b071bba1ef13204b2a8125ff767668895631b827c30d5e`  
		Last Modified: Tue, 30 Jun 2026 23:39:35 GMT  
		Size: 267.9 MB (267946018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b578ec0bb2e72240c01425d3256e7be25da85c765a9d9d1fa382334dd97e8de`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 17.5 MB (17456519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b81fe9abe408f00b0d14e8786a827cbacf8b5da70d10d5f56708741d46b96b`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 482.7 KB (482666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981971459b68ee73f757375aa1c7cb74f65e859a7f802fe1050c9d3f889c9467`  
		Last Modified: Tue, 30 Jun 2026 23:41:03 GMT  
		Size: 410.2 MB (410170078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a4df37dcd7b26022e1f079a1f62333e1ef752ab6106392ed9a31cf2a1e8a75`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62356f1b949eb954f3c789c01f17258441d2f3e733020442047984c5b1d618`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85470c3a621918e3ee834b3668c0cf220efb787cbbab55a1a716ad084e3a3`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfcae7480e319e6b4d1e448397f372f1f9f63633eec8ebf8792511cd3c045d0`  
		Last Modified: Tue, 30 Jun 2026 23:40:55 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:d10033558a5b0150f11139da0261b3cafef2d9702bf1ef06eb9ec35ed8850d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70866537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683d07cd19bc87e344b7bdc4862b2ce1aea0548d9395b8724df309a3e4e58487`

```dockerfile
```

-	Layers:
	-	`sha256:f00a056413f747ed5d21b80fb23de7249c4c9e5489d1eee4fd169c1c507aa3d2`  
		Last Modified: Tue, 30 Jun 2026 23:40:57 GMT  
		Size: 70.8 MB (70839370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0282cb0c9bc349f17408188d1ad7d2b716bd86f04ed1b63ac3ea72cecc00c6`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20260630`

```console
$ docker pull odoo@sha256:957d6b8a68a035154c682732780272e89b13dc3604d855bcaa2653bdea2d372b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20260630` - linux; amd64

```console
$ docker pull odoo@sha256:d45f808cf08accbac383c14fea99da4f72e651aa99d3ae6dc4d1022570870b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.7 MB (713689871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d3a5cf9a7642951b89e457f68039001329c4cd53d44964e650cc0f5f06d5fc`
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
# Tue, 30 Jun 2026 23:37:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:53 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:38:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:39:01 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:39:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:39:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:39:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
USER odoo
# Tue, 30 Jun 2026 23:39:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:39:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e3d3d553f901dedafccf7adf8259846d966d7cf3dab2575984a4126f016cdb`  
		Last Modified: Tue, 30 Jun 2026 23:41:16 GMT  
		Size: 257.1 MB (257063783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa4341931c2942d6d02c72750d021c156cb981fa3ee4d76ed01f2e81765ae55`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 16.8 MB (16779757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7c7fb49ce8a177639e1d8d46569e710f12b57120316785b7ded934e00a27f4`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 482.6 KB (482639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac8325105ae39155ea58732e60421fee9155267e024938b2c8c3cb6efc5cf03`  
		Last Modified: Tue, 30 Jun 2026 23:41:19 GMT  
		Size: 409.6 MB (409628139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a5485e5ef960ca082d5bb15a34c1d5085f1a5da5eab361f7c56f2e96c2d2da`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c94c77677dfa1825591a63f73ca6f5cefbf6e3dfac7606b79da0ba225170a`  
		Last Modified: Tue, 30 Jun 2026 23:41:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b58bc9a47643fa96017ab5cd8f1e1bb3d58b930b5dcf41a8178b0824b70b2`  
		Last Modified: Tue, 30 Jun 2026 23:41:07 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c1bbeadfea29b830d1613d8cdce740f3b45b3a548a9c0564b8d97d9ca014b6`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:6873644659807dfdb10eb545113d249d93b98d3e17d0dd388a9f4b699dc16a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70858086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d068fad4331999ff59a2f5900530a1390f4e31d6f4b8620d261b967cba047`

```dockerfile
```

-	Layers:
	-	`sha256:4dee7414d35a03008ddcc38ac88eae33d9ad9ba83aec60eb988e9118304ca1d3`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 70.8 MB (70830981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6d1ec07ffa7d8ab12f9167672067792c310c42159fcf72a278b15e41e0b7b8`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260630` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ca88b278631c86851d073878de9f827d38a92905ac1b5ee1e99fa41ec5d6dbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709826817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c43e74d5778ef58ea36618362eff9473a6d8ae3ef599b5757bc7ea50e09db90`
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
# Tue, 30 Jun 2026 23:35:40 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:40 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea1fe1bd88f8173cf0d3949222d0f7c679a5be9683a51f7479d808fd66f94b`  
		Last Modified: Tue, 30 Jun 2026 23:39:51 GMT  
		Size: 254.3 MB (254283364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcb51ab0bed742664e171ac1eb007d60c22f7680463936cf887631f5fbec176`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 16.7 MB (16719074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca54857d19d6667b39322de7d23a2c1dd4c96b954d5ed318fb8972a03f8dd5a4`  
		Last Modified: Tue, 30 Jun 2026 23:39:40 GMT  
		Size: 482.6 KB (482633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62bb25b3bd85e3d48f169a51aeb983ed9ea7c5ae1d4dffd5578a67beeaa191d`  
		Last Modified: Tue, 30 Jun 2026 23:39:54 GMT  
		Size: 409.5 MB (409462597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a91c7f73f4223da04faf1cb5dc453a8e5846b8e7195dd49c15677d1e25a96f`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295f5ce41173e1bd741ab6a482769be3c3ddf63dfa9a0b5dd9ba909418aadf6f`  
		Last Modified: Tue, 30 Jun 2026 23:39:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be852638c47fe9ef554d4378365d5bcf2ad951d3cd4f1801d63bbd35e0f77457`  
		Last Modified: Tue, 30 Jun 2026 23:39:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc76b2cfb77989903b21847d66fc0da1e60d294484072cbb516202f55141a3`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:28c65114f25829a6ef7eb7cb96a8f027a2ac51818c0a4bda80b5bb2551aad29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8505daadf1b00d2c693274f541a4d71a59966f871597a7f4c86cb74dbd2da53e`

```dockerfile
```

-	Layers:
	-	`sha256:318ff156f6674c7db0041d3540ec385d15539720ce18ed46c4dcd59fb65db7ad`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 70.8 MB (70838272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f54b8083e5f920cb9ae6c6bcd6720e0f0a0493f53e2b6995f9ef148b8f1014`  
		Last Modified: Tue, 30 Jun 2026 23:39:39 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20260630` - linux; ppc64le

```console
$ docker pull odoo@sha256:5d24e4b5500f7a02070615cce7de584a8de233c81b6f08af685c730b909a6f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.4 MB (730372124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9f34e342b123d7e214252b368f8cceaaeb3022e0b7097366d0ea5e424571a6`
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
# Tue, 30 Jun 2026 23:32:42 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:32:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:32:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jun 2026 23:32:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:33:01 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:35:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:35:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:35:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:35:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:35:10 GMT
USER odoo
# Tue, 30 Jun 2026 23:35:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:35:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e83db4c0f91c3a2b071bba1ef13204b2a8125ff767668895631b827c30d5e`  
		Last Modified: Tue, 30 Jun 2026 23:39:35 GMT  
		Size: 267.9 MB (267946018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b578ec0bb2e72240c01425d3256e7be25da85c765a9d9d1fa382334dd97e8de`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 17.5 MB (17456519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b81fe9abe408f00b0d14e8786a827cbacf8b5da70d10d5f56708741d46b96b`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 482.7 KB (482666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981971459b68ee73f757375aa1c7cb74f65e859a7f802fe1050c9d3f889c9467`  
		Last Modified: Tue, 30 Jun 2026 23:41:03 GMT  
		Size: 410.2 MB (410170078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a4df37dcd7b26022e1f079a1f62333e1ef752ab6106392ed9a31cf2a1e8a75`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62356f1b949eb954f3c789c01f17258441d2f3e733020442047984c5b1d618`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85470c3a621918e3ee834b3668c0cf220efb787cbbab55a1a716ad084e3a3`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfcae7480e319e6b4d1e448397f372f1f9f63633eec8ebf8792511cd3c045d0`  
		Last Modified: Tue, 30 Jun 2026 23:40:55 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20260630` - unknown; unknown

```console
$ docker pull odoo@sha256:d10033558a5b0150f11139da0261b3cafef2d9702bf1ef06eb9ec35ed8850d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70866537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683d07cd19bc87e344b7bdc4862b2ce1aea0548d9395b8724df309a3e4e58487`

```dockerfile
```

-	Layers:
	-	`sha256:f00a056413f747ed5d21b80fb23de7249c4c9e5489d1eee4fd169c1c507aa3d2`  
		Last Modified: Tue, 30 Jun 2026 23:40:57 GMT  
		Size: 70.8 MB (70839370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0282cb0c9bc349f17408188d1ad7d2b716bd86f04ed1b63ac3ea72cecc00c6`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:957d6b8a68a035154c682732780272e89b13dc3604d855bcaa2653bdea2d372b
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
$ docker pull odoo@sha256:d45f808cf08accbac383c14fea99da4f72e651aa99d3ae6dc4d1022570870b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **713.7 MB (713689871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d3a5cf9a7642951b89e457f68039001329c4cd53d44964e650cc0f5f06d5fc`
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
# Tue, 30 Jun 2026 23:37:53 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:37:53 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:37:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:37:53 GMT
ARG TARGETARCH=amd64
# Tue, 30 Jun 2026 23:37:53 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:38:01 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:38:02 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:38:02 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:39:01 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:39:02 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:39:02 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:39:02 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:39:02 GMT
USER odoo
# Tue, 30 Jun 2026 23:39:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:39:02 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e3d3d553f901dedafccf7adf8259846d966d7cf3dab2575984a4126f016cdb`  
		Last Modified: Tue, 30 Jun 2026 23:41:16 GMT  
		Size: 257.1 MB (257063783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa4341931c2942d6d02c72750d021c156cb981fa3ee4d76ed01f2e81765ae55`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 16.8 MB (16779757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7c7fb49ce8a177639e1d8d46569e710f12b57120316785b7ded934e00a27f4`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 482.6 KB (482639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac8325105ae39155ea58732e60421fee9155267e024938b2c8c3cb6efc5cf03`  
		Last Modified: Tue, 30 Jun 2026 23:41:19 GMT  
		Size: 409.6 MB (409628139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a5485e5ef960ca082d5bb15a34c1d5085f1a5da5eab361f7c56f2e96c2d2da`  
		Last Modified: Tue, 30 Jun 2026 23:41:05 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48c94c77677dfa1825591a63f73ca6f5cefbf6e3dfac7606b79da0ba225170a`  
		Last Modified: Tue, 30 Jun 2026 23:41:06 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05b58bc9a47643fa96017ab5cd8f1e1bb3d58b930b5dcf41a8178b0824b70b2`  
		Last Modified: Tue, 30 Jun 2026 23:41:07 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c1bbeadfea29b830d1613d8cdce740f3b45b3a548a9c0564b8d97d9ca014b6`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:6873644659807dfdb10eb545113d249d93b98d3e17d0dd388a9f4b699dc16a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70858086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d068fad4331999ff59a2f5900530a1390f4e31d6f4b8620d261b967cba047`

```dockerfile
```

-	Layers:
	-	`sha256:4dee7414d35a03008ddcc38ac88eae33d9ad9ba83aec60eb988e9118304ca1d3`  
		Last Modified: Tue, 30 Jun 2026 23:41:08 GMT  
		Size: 70.8 MB (70830981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6d1ec07ffa7d8ab12f9167672067792c310c42159fcf72a278b15e41e0b7b8`  
		Last Modified: Tue, 30 Jun 2026 23:41:04 GMT  
		Size: 27.1 KB (27105 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:ca88b278631c86851d073878de9f827d38a92905ac1b5ee1e99fa41ec5d6dbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 MB (709826817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c43e74d5778ef58ea36618362eff9473a6d8ae3ef599b5757bc7ea50e09db90`
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
# Tue, 30 Jun 2026 23:35:40 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:35:40 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:35:40 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:35:40 GMT
ARG TARGETARCH=arm64
# Tue, 30 Jun 2026 23:35:40 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:35:48 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:35:49 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:35:49 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:36:58 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:36:58 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:36:58 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:36:58 GMT
USER odoo
# Tue, 30 Jun 2026 23:36:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:36:58 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ea1fe1bd88f8173cf0d3949222d0f7c679a5be9683a51f7479d808fd66f94b`  
		Last Modified: Tue, 30 Jun 2026 23:39:51 GMT  
		Size: 254.3 MB (254283364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcb51ab0bed742664e171ac1eb007d60c22f7680463936cf887631f5fbec176`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 16.7 MB (16719074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca54857d19d6667b39322de7d23a2c1dd4c96b954d5ed318fb8972a03f8dd5a4`  
		Last Modified: Tue, 30 Jun 2026 23:39:40 GMT  
		Size: 482.6 KB (482633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62bb25b3bd85e3d48f169a51aeb983ed9ea7c5ae1d4dffd5578a67beeaa191d`  
		Last Modified: Tue, 30 Jun 2026 23:39:54 GMT  
		Size: 409.5 MB (409462597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a91c7f73f4223da04faf1cb5dc453a8e5846b8e7195dd49c15677d1e25a96f`  
		Last Modified: Tue, 30 Jun 2026 23:39:41 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295f5ce41173e1bd741ab6a482769be3c3ddf63dfa9a0b5dd9ba909418aadf6f`  
		Last Modified: Tue, 30 Jun 2026 23:39:42 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be852638c47fe9ef554d4378365d5bcf2ad951d3cd4f1801d63bbd35e0f77457`  
		Last Modified: Tue, 30 Jun 2026 23:39:43 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc76b2cfb77989903b21847d66fc0da1e60d294484072cbb516202f55141a3`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 878.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:28c65114f25829a6ef7eb7cb96a8f027a2ac51818c0a4bda80b5bb2551aad29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8505daadf1b00d2c693274f541a4d71a59966f871597a7f4c86cb74dbd2da53e`

```dockerfile
```

-	Layers:
	-	`sha256:318ff156f6674c7db0041d3540ec385d15539720ce18ed46c4dcd59fb65db7ad`  
		Last Modified: Tue, 30 Jun 2026 23:39:44 GMT  
		Size: 70.8 MB (70838272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f54b8083e5f920cb9ae6c6bcd6720e0f0a0493f53e2b6995f9ef148b8f1014`  
		Last Modified: Tue, 30 Jun 2026 23:39:39 GMT  
		Size: 27.3 KB (27269 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:5d24e4b5500f7a02070615cce7de584a8de233c81b6f08af685c730b909a6f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.4 MB (730372124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9f34e342b123d7e214252b368f8cceaaeb3022e0b7097366d0ea5e424571a6`
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
# Tue, 30 Jun 2026 23:32:42 GMT
LABEL maintainer=Odoo S.A. <info@odoo.com>
# Tue, 30 Jun 2026 23:32:42 GMT
SHELL [/bin/bash -xo pipefail -c]
# Tue, 30 Jun 2026 23:32:42 GMT
ENV LANG=en_US.UTF-8
# Tue, 30 Jun 2026 23:32:42 GMT
ARG TARGETARCH=ppc64le
# Tue, 30 Jun 2026 23:32:42 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Tue, 30 Jun 2026 23:33:01 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Tue, 30 Jun 2026 23:33:03 GMT
ENV ODOO_VERSION=19.0
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_RELEASE=20260630
# Tue, 30 Jun 2026 23:33:03 GMT
ARG ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
# Tue, 30 Jun 2026 23:35:07 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20260630 ODOO_SHA=061db8d7bf1a8e42d6a684b1484cb6d6435dcbac
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Tue, 30 Jun 2026 23:35:09 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Tue, 30 Jun 2026 23:35:09 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Tue, 30 Jun 2026 23:35:09 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Tue, 30 Jun 2026 23:35:10 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Tue, 30 Jun 2026 23:35:10 GMT
USER odoo
# Tue, 30 Jun 2026 23:35:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 30 Jun 2026 23:35:10 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e83db4c0f91c3a2b071bba1ef13204b2a8125ff767668895631b827c30d5e`  
		Last Modified: Tue, 30 Jun 2026 23:39:35 GMT  
		Size: 267.9 MB (267946018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b578ec0bb2e72240c01425d3256e7be25da85c765a9d9d1fa382334dd97e8de`  
		Last Modified: Tue, 30 Jun 2026 23:39:25 GMT  
		Size: 17.5 MB (17456519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b81fe9abe408f00b0d14e8786a827cbacf8b5da70d10d5f56708741d46b96b`  
		Last Modified: Tue, 30 Jun 2026 23:39:23 GMT  
		Size: 482.7 KB (482666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981971459b68ee73f757375aa1c7cb74f65e859a7f802fe1050c9d3f889c9467`  
		Last Modified: Tue, 30 Jun 2026 23:41:03 GMT  
		Size: 410.2 MB (410170078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a4df37dcd7b26022e1f079a1f62333e1ef752ab6106392ed9a31cf2a1e8a75`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 718.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab62356f1b949eb954f3c789c01f17258441d2f3e733020442047984c5b1d618`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 553.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85470c3a621918e3ee834b3668c0cf220efb787cbbab55a1a716ad084e3a3`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 593.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfcae7480e319e6b4d1e448397f372f1f9f63633eec8ebf8792511cd3c045d0`  
		Last Modified: Tue, 30 Jun 2026 23:40:55 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:d10033558a5b0150f11139da0261b3cafef2d9702bf1ef06eb9ec35ed8850d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70866537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683d07cd19bc87e344b7bdc4862b2ce1aea0548d9395b8724df309a3e4e58487`

```dockerfile
```

-	Layers:
	-	`sha256:f00a056413f747ed5d21b80fb23de7249c4c9e5489d1eee4fd169c1c507aa3d2`  
		Last Modified: Tue, 30 Jun 2026 23:40:57 GMT  
		Size: 70.8 MB (70839370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a0282cb0c9bc349f17408188d1ad7d2b716bd86f04ed1b63ac3ea72cecc00c6`  
		Last Modified: Tue, 30 Jun 2026 23:40:53 GMT  
		Size: 27.2 KB (27167 bytes)  
		MIME: application/vnd.in-toto+json
