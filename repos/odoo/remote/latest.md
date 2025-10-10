## `odoo:latest`

```console
$ docker pull odoo@sha256:8d5ac4da0713865f9222230e0ec5e4b12131d02e3e677fbdd4586cf234c34d01
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
$ docker pull odoo@sha256:0816eccd81dcdfe7405c60ac3a8d7c18c5e362e3c03fe2794a8bc729c3824214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.1 MB (681052716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d5400790ca4dc2768ca19767c1adb74583ce81fc042fbcd66dd138f17cc974`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=amd64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a8ac81d94bde42e34ee4a1130b2d11c24abbfa8b9605d22775918c6a598744`  
		Last Modified: Fri, 10 Oct 2025 01:15:11 GMT  
		Size: 254.6 MB (254557943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1fc2b39f87bfe22f66a47e2328b2e4265ff3e40f696e6ae1424fbebda91b07`  
		Last Modified: Fri, 10 Oct 2025 01:14:06 GMT  
		Size: 14.4 MB (14355897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad9ac3bf579d5c2297c991a1e690f0f0ad1d5f3104a4bf4ee73baa054d1382`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 480.0 KB (479990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a7cd7ddee95c71dcd500777eef020995eb4b373eb7b04f5d4d4bb9e263d426`  
		Last Modified: Fri, 10 Oct 2025 01:15:12 GMT  
		Size: 381.9 MB (381933305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0355a58aeb025d119b15445efab770268251b578622ce9294cddfe950ba41869`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5301470dc69464f9afb9844c2fbb49e4370ae1d66fab0dcf1e63ed263789e392`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7abbfab2606c7af4b42e281ba61f60b62dcd34c3309d588d80cd0d4b3973f7`  
		Last Modified: Thu, 09 Oct 2025 23:02:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad329fad58aa2e2692a11cf1bba26f8ab8f8f05b84167a182e15b6d9d61efd32`  
		Last Modified: Thu, 09 Oct 2025 23:02:27 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:c415a7fecfac8daa80333c16efd1960e6e90906e3c4565e1a5b712764db4ecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67774795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f28280c8c5565a21014036141c8bc29cecf5b45123df9c0cdee6506e0335d1`

```dockerfile
```

-	Layers:
	-	`sha256:72ec2abc6044ddcd5521c8009e9019e2201fa200e4793f7485ba5b3dae97a1c2`  
		Last Modified: Fri, 10 Oct 2025 01:14:01 GMT  
		Size: 67.7 MB (67747659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e73e617b7fc33a594fb000513cc4dcef01e6b76392acd882f5ff7cda491a02d`  
		Last Modified: Fri, 10 Oct 2025 01:14:03 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b4b519f42e4927dda2d754119b4f5bd07cac6638598d3075bf3fd794a79665f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.4 MB (677409644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbfa59155bb08c7537622ba80e57d850d0348f8c323a3ea8fe8c3aef21f76e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=arm64
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82e287495a5e85388b5a079cb0e406289ae6a33708551e3b963ae2eb7ffa9c9`  
		Last Modified: Fri, 10 Oct 2025 01:15:32 GMT  
		Size: 252.0 MB (251958001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258c4350f5ef1026c617ae2e603af78d4e33a59947ea48449143946d8bd2b5e4`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 14.3 MB (14333882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537148a17c731e0dd2d7c24e29bfa1e5df2a03f74f8aac9e885e7fa85c6e7e3c`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 480.0 KB (480008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1da89032b23008d59f199d69cb70314369df7ef88560915eefaad179e3434`  
		Last Modified: Fri, 10 Oct 2025 01:15:22 GMT  
		Size: 381.8 MB (381773599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a000f0e70bced001eff4997d1ab0d2cdc02b98644f59dde2d2d1773e8e25b7`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999afe814c933091c329d7aa0815b31021d2f12b655df05b50ea3705128bcce9`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 557.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ed884d8f9d697cf1444db8850f58087fff1f28c1498c030c9ee0b75d7c6094`  
		Last Modified: Thu, 09 Oct 2025 21:28:01 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55b995bb519239ac851d2654d311c332345bf8f7ffcc217d2484311f153e7b0`  
		Last Modified: Thu, 09 Oct 2025 21:28:02 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:cbee11f44e30d09ad7816c526aa35c149b15a7024f277688387346b324e821d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67782244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4527ede488d6e501fb22bdf921773746c5ba8f4dac372ec46aeb130d2dda1ef`

```dockerfile
```

-	Layers:
	-	`sha256:49e52d9aacbaad5b4cabbf12e099f240e5a83ab730452f9e3e1920a3e2cbd09e`  
		Last Modified: Fri, 10 Oct 2025 01:16:08 GMT  
		Size: 67.8 MB (67754946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab67edb7216439a7a6cf8eb6c95131a89369b51f4d15d744075839c22d2c33f`  
		Last Modified: Fri, 10 Oct 2025 01:16:12 GMT  
		Size: 27.3 KB (27298 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:1c4f621bc44fdbd4f89388fa2f30d7151ca86f5fc7dce249350a94811e8d9ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697223179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b977193a3433b32ba06a0c746da4d9abaf319965f6494cb70bcb56741227b0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Wed, 08 Oct 2025 14:56:20 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Wed, 08 Oct 2025 14:56:20 GMT
SHELL [/bin/bash -xo pipefail -c]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 08 Oct 2025 14:56:20 GMT
ARG TARGETARCH=ppc64le
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_VERSION=19.0
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_RELEASE=20251008
# Wed, 08 Oct 2025 14:56:20 GMT
ARG ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./entrypoint.sh / # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20251008 ODOO_SHA=36dde7d124ca4b0f957949f0b2c88b87d9da07f7
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Wed, 08 Oct 2025 14:56:20 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Wed, 08 Oct 2025 14:56:20 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Wed, 08 Oct 2025 14:56:20 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Wed, 08 Oct 2025 14:56:20 GMT
USER odoo
# Wed, 08 Oct 2025 14:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Oct 2025 14:56:20 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365e10012916edf5827ab48daa2a0e2d76ab0fe26240a6d8585f47267e43c588`  
		Last Modified: Thu, 09 Oct 2025 22:17:22 GMT  
		Size: 265.1 MB (265079703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74db884b565963874180a2af82ba963a1d4611a8402d4708c1797097b804fb90`  
		Last Modified: Thu, 09 Oct 2025 22:07:00 GMT  
		Size: 14.9 MB (14883559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d234cbf81875448957faff2c426ab594a8402e92b0fe58fd91cdc13f3593801`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 480.1 KB (480093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3865409814e38a7bd75e01d1dc1a0179cfaf8c3af6769b43d5f1f67f827088`  
		Last Modified: Thu, 09 Oct 2025 22:15:25 GMT  
		Size: 382.5 MB (382473853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8f196f1ef328e58674d9e2c9278684874b3eafafffd083c2c04330e5ee1d60`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1d709655517db715241f0b007b26c4e62c8e7ec2a719957e658bb0dc7b26d0`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01361e855b34f7e471f7e38049e551d2cfc872314c3ab252bb2e066da53cee18`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 601.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a9c37dd7fc840c7e268533c5f4d7cc708c0067e294a6b1d925cb021f0b841`  
		Last Modified: Thu, 09 Oct 2025 22:06:59 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:2ad0f9da585335b978ddcd7c543d1b841bd576d7ef68bb279d4de438c946fba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67783246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165efa7311b385e3fcfe40acb7870d32cb2b59376dcaef61327aadd915ec0e45`

```dockerfile
```

-	Layers:
	-	`sha256:445ed5d82e3a44a48d7a5f5897d4a518d6e8952553f3f17610bc2d0f61a2f927`  
		Last Modified: Fri, 10 Oct 2025 01:18:16 GMT  
		Size: 67.8 MB (67756048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629eecb262c7a3bd0e31834d20806b749d7bb3e75f74c446fa58d4ee7b307aa0`  
		Last Modified: Fri, 10 Oct 2025 01:18:17 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
