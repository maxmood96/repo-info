## `odoo:latest`

```console
$ docker pull odoo@sha256:d2fe034098978bba6d603b3a994a7e6d2ffe62219cd1c92bc974110d07d4b1d5
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
$ docker pull odoo@sha256:e34f2b32ae3ec542cea75f2b6823c3ef2811d6ea97cb26f3ca922f418ef1c408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.1 MB (597067381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9785ec55b41b38fec60054d5fbd60868ca62b382a1e440744f4e92b3f0dd89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=amd64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb00a467be04581de6d0ae3e8490555ceac416a6127b3dd10bd3aa03798eeb2d`  
		Last Modified: Tue, 17 Sep 2024 01:02:18 GMT  
		Size: 233.7 MB (233745038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23de8307da804acac83f2511537bfb9247028ca64da151a7ec00c6c1a50b70ee`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 2.3 MB (2315512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3cd6168060e79236d0001c446bc2c3de655e8887bd93cef47d38ac48d5b28c`  
		Last Modified: Tue, 17 Sep 2024 01:02:13 GMT  
		Size: 472.7 KB (472687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213683c8a6bf0d18279e9d444300475266d1914ca10d4a095da64fa2871dde0`  
		Last Modified: Tue, 17 Sep 2024 01:02:20 GMT  
		Size: 331.0 MB (330996016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e760b719ca046e84ade9e4e77fc86eb5bac1204fd5cc5c675e906c06e4b7005`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d599f08f252a61d26e597082e6ea5102fa0f4535b521c4500ffc9a9d358b171`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139cd9ab1fe0b54ce18cac3bb4e32751a4cf4470d05cbcbdcf2d20f1604459d2`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fa0ac3c34a78f6ba7217e1a3aba2a7b02a7c36357b89829614c7db8cf9fc9c`  
		Last Modified: Tue, 17 Sep 2024 01:02:15 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:fc6230d1ac6eb769cf751382bb23f9566a3e541981aa6ca18230392e66e3e084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39221438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e16388a4909b364fff0f7d96144f6d3f99588e164f387db9ec6bef408f42f78`

```dockerfile
```

-	Layers:
	-	`sha256:c99444a83c2a122c2ff0d1810f6453cd2947bec02cb7ad44a77c6925a0aed57c`  
		Last Modified: Tue, 17 Sep 2024 01:02:14 GMT  
		Size: 39.2 MB (39194563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b072659bf65ec344e306b9bfcb37cc97af525a79ec1f73c9c65c5767b36f6afb`  
		Last Modified: Tue, 17 Sep 2024 01:02:12 GMT  
		Size: 26.9 KB (26875 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:6611f5cd4c4ae8419cdeaf4ec46b8f23c6d326678fd468c6226c0f2ffb475736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 MB (591868851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce022a8be4133de08eafd2688f199b3ac09b10d085140009766a1f31170ed82a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=arm64
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6fadc8f1cdeb7018f3cc730bf5ca5cbd765df35c38756be1faa743e1786be9`  
		Last Modified: Tue, 17 Sep 2024 02:44:10 GMT  
		Size: 231.1 MB (231120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a152b990945175781adb341944cf665969d147ca436c8a7b53374779e6f6941`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 2.3 MB (2307685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb15fba7b3792bd150e5f11e817299c61abde876d36eedbebdebfe879e3a79`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 472.7 KB (472677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3dc0efa25020a1df1f02165d1ae8e54504881e43af46b33f1672199397667f`  
		Last Modified: Tue, 17 Sep 2024 02:44:11 GMT  
		Size: 330.6 MB (330607248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea0c48ec3b5d0f3ed92cee4e1a2efd7d4d49febec8a285fafb4b92979544dd0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f863e745cdbee42411248cd07033079da01761ae92a1e759d5391796f92c6`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5e0c8f3a6fedcfba8dfe25297e2dde28433c647113b14ec50fcbd7f85a5c15`  
		Last Modified: Tue, 17 Sep 2024 02:44:06 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a138850a8bb293831a1edd82ff2eb6c592b601ac7d1e519a934e96926a30768b`  
		Last Modified: Tue, 17 Sep 2024 02:44:07 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:7615a5b62b439b9ec7ca9e2e5ff48ebed15028069877699355956ec4cfffe372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39228264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4cf9f1b29ba9250c8bbebe0dfc04ee73b5c53371f60ad97fa92d00b2bdf348`

```dockerfile
```

-	Layers:
	-	`sha256:09ba83716c6a0b901ce631a4b8758c4339f5d1052c5a908f1979b3c7b9fdd7c0`  
		Last Modified: Tue, 17 Sep 2024 02:44:05 GMT  
		Size: 39.2 MB (39201088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7972446f364fc62b55b326ba9c2d373cb39a93fb680e442bf576262bc1e2297e`  
		Last Modified: Tue, 17 Sep 2024 02:44:04 GMT  
		Size: 27.2 KB (27176 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:787a8f72b46c6ab612133cd9b25832228997e307e0f7bcae00219b0563745402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.5 MB (613535529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1547286e09cca0c7ea3a41737f0be3f4fb8234f00926f442292b7a5294108707`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 09:27:03 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Thu, 12 Sep 2024 09:27:03 GMT
SHELL [/bin/bash -xo pipefail -c]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Sep 2024 09:27:03 GMT
ARG TARGETARCH=ppc64le
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_VERSION=17.0
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_RELEASE=20240912
# Thu, 12 Sep 2024 09:27:03 GMT
ARG ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./entrypoint.sh / # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20240912 ODOO_SHA=4456afb92e3235660c711160b1f457d31902c391
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Thu, 12 Sep 2024 09:27:03 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Thu, 12 Sep 2024 09:27:03 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Thu, 12 Sep 2024 09:27:03 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Thu, 12 Sep 2024 09:27:03 GMT
USER odoo
# Thu, 12 Sep 2024 09:27:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Sep 2024 09:27:03 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714c02d58ebd6534d5afb5a8012d7003f978314b782a10cd19fbc0e6d5d58df3`  
		Last Modified: Tue, 17 Sep 2024 01:53:43 GMT  
		Size: 243.3 MB (243275613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67640bc9b4d0c0923eccbc39ae739c9f734354b3f58be66b9058c61be83d80`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 2.6 MB (2592233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fdfb807d76c75fa16e7bed3d97c1200cb7778b2234fd4ebd57a60a93314315`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 472.7 KB (472652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c78e067de9022a0bd3d724ab7c3a3841af530da68cc046aa7dbc8b32781ada`  
		Last Modified: Tue, 17 Sep 2024 01:53:48 GMT  
		Size: 332.7 MB (332744345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc2e863f289fa232c95ab4f1890b04ad695b45f7456d5b4caa5498f249936cc`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab68b8d104879dbc336262260ea6eac356cd4ce0bc2b45a64939c8fdabfd437`  
		Last Modified: Tue, 17 Sep 2024 01:53:32 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd70b5e06a052e749e914910688b2b6d55d0005dd98dd55dde9073d11e1032b4`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5474009adf7ff1d592384e6e28fdffb03005ee888de7cd8ad193c3cfb7d0220f`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:78eab57ab6e792662a1f31603420132c8cc0adeb52776ff624ac7e9708d4fa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39229807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b1efa18db0e2ba31828df77f5c6e1ac990131e251a409b8c385c241cbf5f5f`

```dockerfile
```

-	Layers:
	-	`sha256:4586ae5019aa9a909fc1bcadc06216ce30cb52e67a9f717a6ae9f5a3158edad0`  
		Last Modified: Tue, 17 Sep 2024 01:53:33 GMT  
		Size: 39.2 MB (39202876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2f144d57bfe690352aba9618874ebbbd3d303c702426731c39660532912e88`  
		Last Modified: Tue, 17 Sep 2024 01:53:31 GMT  
		Size: 26.9 KB (26931 bytes)  
		MIME: application/vnd.in-toto+json
