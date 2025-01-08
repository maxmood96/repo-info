## `odoo:latest`

```console
$ docker pull odoo@sha256:543477de90679293a85df149702b36f495669635efe12d1720ae1bc13f686e2c
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
$ docker pull odoo@sha256:a498cae86713a72149e35a1c11d1cf87dbeb62430af14567cf1407d3db8a7784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.4 MB (665427867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b6544e1db91a142d2c520f79b9a47616b5943d650980964dde2089d622105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=amd64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45887c5bf36402135d3e8159888d8ff9b09ab897d3a90f477e330ef32b7ae686`  
		Last Modified: Tue, 07 Jan 2025 02:32:21 GMT  
		Size: 254.5 MB (254516340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59a74fe4514c470984758b86d9f4346217337f639f879106cba18ff0d0434d`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 14.2 MB (14230118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779ba51ba9acb9f403e7edde3fcdba2d6e41c4f57234338771b72c88737fa16`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 484.9 KB (484911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485b916b73cef04bcacbf17ab015401c49254ad71a4c042aed754b899d438337`  
		Last Modified: Tue, 07 Jan 2025 02:32:22 GMT  
		Size: 366.4 MB (366442093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c3af110c11e78703a052f7868f1e44d199a26581b7932b0cade9fad97f3880`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ebf5753311702190b3351f562a8b8dfb1fc0f21c70c26b07cd8085ffec6143`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d84072118698624ab758a78d90820d1a3fd02c4c5ecc77edb3e7610f390e5`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcd84a8f05c331526c12eaf53c1e4af3c2e4ca5807bf362a7392f552177642d`  
		Last Modified: Tue, 07 Jan 2025 02:32:19 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:64d1c65e58cad0864196065e5b240fa319fb5a3679db41b8293fda4d76f18db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58364432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aecabbe8d04e417c58799658bc5a16954242bd67ba3c43941587f276756a38`

```dockerfile
```

-	Layers:
	-	`sha256:eff02ed18115b0801edae6c8f6973fc48e581a85389736e9b75b255684a7e2d0`  
		Last Modified: Tue, 07 Jan 2025 02:32:18 GMT  
		Size: 58.3 MB (58337296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fc62a67d30aa95c392dcc712100c54b7a5f722c7da486ee96e0b89444130346`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 27.1 KB (27136 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:b580ded05326157c2298f89b77037f123d36032f286c660a944e6e3f51f81c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661820054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99376e4e9b2067b5a1db4a820e2bba6526b5e815299c842fff0f9a43373a5f07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=arm64
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d565ed86e62ed5d5676c9727f5b1a3633ee3969c042d236ac1fba49d667c49c`  
		Last Modified: Sat, 21 Dec 2024 00:50:36 GMT  
		Size: 251.9 MB (251942487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cc4a9b6e811923fcc8654b16fbe78b05100b28f0b1f7105f09898bf1bcd42b`  
		Size: 14.2 MB (14204415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b59dc1c63a4356c8a42497e257f940b2c3eab334ecfe5269e8b0d460ca6a1b`  
		Size: 485.0 KB (485011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfdab3d8df1faefb7de77c3510c909b0d99bcc1178d007b57aa9fa14fb7708e`  
		Last Modified: Tue, 07 Jan 2025 03:08:06 GMT  
		Size: 366.3 MB (366293034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2acfe7737e2bc45549f931b08c66b4a369dc9bb65f6cbe0cd87429c3dd953d`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26168a6ee953389d3643543cdcf15bb5a1528243bf1c24211be96e4cabd0b73`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a10bb73bc2141fdbe9fff870d974984a6d7957459ca3c281a740af23d7e61b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c07ee242d4ef58b8ea6cc8982985575954ca6467b7fb00a01b48aae31aeb054`  
		Last Modified: Tue, 07 Jan 2025 03:07:59 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:660d0fa1249a6d89acd57d3a74a4e400a769e52a38da6f93f7782f5d1d518be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58371887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c050e05a959ebbc656f5ec34b21cb22cef19c4570a37f688ebd0062ed178002`

```dockerfile
```

-	Layers:
	-	`sha256:1e581cee7af1c587bef0d3f8380b79a872b62ab3270490c2295cf05758f760e8`  
		Last Modified: Tue, 07 Jan 2025 03:08:00 GMT  
		Size: 58.3 MB (58344587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a028aad2cee0766059b838aa806f374cc72ae58d95ad5bb62c39fc2dc7034b0`  
		Last Modified: Tue, 07 Jan 2025 03:07:58 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:b697b0ddf3ad2d4af5898bdc66da21586229734cb6c13e853887b80fa6f53d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **681.7 MB (681736287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83741869a79d9a0715568c8ae3ccecd75b5acc24b807a1b78a78f07ca2589251`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 06 Jan 2025 14:01:12 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 06 Jan 2025 14:01:12 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jan 2025 14:01:12 GMT
ARG TARGETARCH=ppc64le
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_VERSION=18.0
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_RELEASE=20250106
# Mon, 06 Jan 2025 14:01:12 GMT
ARG ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250106 ODOO_SHA=3517a8f0e635553c98ec8c52787e1fb7c7c1937a
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 06 Jan 2025 14:01:12 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 06 Jan 2025 14:01:12 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 06 Jan 2025 14:01:12 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 06 Jan 2025 14:01:12 GMT
USER odoo
# Mon, 06 Jan 2025 14:01:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jan 2025 14:01:12 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42831175c8b861df666e9a65f1af816a551faf715979d2c3aa91cb8f416f2cc5`  
		Last Modified: Fri, 20 Dec 2024 23:53:48 GMT  
		Size: 265.1 MB (265089390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f73e3480e0f5d139d043e19f354056aac0e3eb3d96dbec9611d9858240b5a8`  
		Last Modified: Fri, 20 Dec 2024 23:53:40 GMT  
		Size: 14.8 MB (14776313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60ffb8de052783553ede75de3dcf047207b1020f389a00dc7c9a47f559006ed`  
		Size: 484.9 KB (484925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396dc4cb926aa2a8ffba5bbc0efd80eb54163b1ab9ce89ceda59c1a92b994590`  
		Size: 367.0 MB (366994400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c2c0160ebfb3debc4fcdd3f9a207bdb108367f7c369b0b38d72de794b773ef`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e4a21b179f843fa4d6aeaf5fdc92317d8184aa3111ee93cd33a675a3dbc9b`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 554.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798846e905b54fa491b50be015bf621884d34e4d62319a80cb5253e583e418ac`  
		Last Modified: Tue, 07 Jan 2025 02:41:05 GMT  
		Size: 597.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6925157dec2af072810af50593a5b824f8865e952c4f77c1a0ee5af7069a8cd`  
		Last Modified: Tue, 07 Jan 2025 02:41:06 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:f68f3f61505e82340d0c463c04d18ba420cbd560551f5a6a504769699cc3d367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58372657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9d42833478f3b62b0785d4227c4d0f177fe9a4b41944a23f9f65ca4adfae0b`

```dockerfile
```

-	Layers:
	-	`sha256:eb4b48bd1b3ac530a7b3347d18c723b6ce76cbf64171c402de6ed292ea031d10`  
		Last Modified: Tue, 07 Jan 2025 02:41:07 GMT  
		Size: 58.3 MB (58345459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb70fd5251e0f584e7d9cd98c270a9e70778d88f3d38285ed979f1f089075a79`  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
