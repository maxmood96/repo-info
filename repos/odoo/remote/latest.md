## `odoo:latest`

```console
$ docker pull odoo@sha256:55be8055bebb50cc6b9565e30ffb9a522b7c9b7c61a0558b005662ba9f0a06dc
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
$ docker pull odoo@sha256:c1937bf49fc09babde747a277b76e1c448b97a71a7bc1908d1dea0afc2f4cc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 MB (661826305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9bc77230906d0a98c0a68d2cbca9c0b53c77a1d545ff21202b0b2bb787bd35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=amd64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d128a82529d7f28af0e23bc19a8d74cad84efc84ba3893b6f88cd9d65c57cb`  
		Last Modified: Mon, 25 Nov 2024 20:27:30 GMT  
		Size: 254.5 MB (254514976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c54e86137ce82f955e630c041345b730dad696ba14e446d4ed651fb924161d2`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 14.2 MB (14230240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470f846b2c4ac19e54ae3282c351d9e7f3bdb70aa031ae20c7ec26565ab4e56d`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 469.7 KB (469717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e520674f58c111e938bc91c1880ec2396fb84b04126ae2925595895185348b1f`  
		Last Modified: Mon, 25 Nov 2024 20:27:32 GMT  
		Size: 362.9 MB (362857155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663db6c71feea36a64b3935fa528dd80a19ad90c027207737d986080836c6080`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 704.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3787ee00e67a74e30b531a36efba223e90527fe2e4008caae792de868527a07`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a6357344d35acba8166cf1be5df64acbd8b4a8a25e41f4112090d0aa41279f`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828f145cef64dc7178611127c3b2adc5a0174f46e26c918770637132ebed09e5`  
		Last Modified: Mon, 25 Nov 2024 20:27:28 GMT  
		Size: 579.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b1e73eb636656d2f0315585c9c9806eb847ca47b7eb26ec6ee791a14fa66ec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57280723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e47fd308d2b42ac39b532c65ff05ae0177acad5467962cf49fb20bc18cc4825`

```dockerfile
```

-	Layers:
	-	`sha256:0e5849635127ef6ee3ecb3c8e4ac8e69438e46d119285c8ba9ad58262414bcb6`  
		Last Modified: Mon, 25 Nov 2024 20:27:27 GMT  
		Size: 57.3 MB (57253588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48b6cda47f47e47a42ef1d8d41c28c0b973e6a9d7368d3ee947d64a3789994b`  
		Last Modified: Mon, 25 Nov 2024 20:27:26 GMT  
		Size: 27.1 KB (27135 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:a1b56d7071b2928346e5b0db697e380e308963787081ee095f8f2435b48c0953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.2 MB (658199642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c5fcdc5afadd8ad803fdbe024500ebf5ff6ee8e6a72097d5281f2cbc333d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=arm64
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3587d98cf945cc8b8cb28976463626a968b75cfb85a7bc134788ca4acf3a2f07`  
		Last Modified: Sat, 16 Nov 2024 03:28:14 GMT  
		Size: 251.9 MB (251945445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bea938de0828dade1c18a83a12fb524e0eee9b0c70216313f5a11e1971311d3`  
		Last Modified: Sat, 16 Nov 2024 03:28:07 GMT  
		Size: 14.2 MB (14202621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236ec3799ba5acb8613b5e789989e4eb51b91db56eac165301dd71ba9e697ac`  
		Last Modified: Sat, 16 Nov 2024 03:28:06 GMT  
		Size: 469.7 KB (469730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14acc5f94928508504ccb131cb0e7cac6fb981267531c47028d0a39cf1ec6bb1`  
		Last Modified: Mon, 25 Nov 2024 20:31:34 GMT  
		Size: 362.7 MB (362686981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7cd84dc5a1410241f06c30b3bff9fef79f097614187bd0d75719672882accc`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 707.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15859d1c6a5683189016bbdb9f58bd08e052c64be5aedc6f782bee6b0eb063`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a31ffc577a6edce14511e0404d73b48461b272bcfb60bab890cc7ccf4e61c0a`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3d6ead5b26e1a32d1d3c1b71d9767aa00743fc64733b871c6bbf2591d81d9d`  
		Last Modified: Mon, 25 Nov 2024 20:31:27 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:75ef835d7b856c1f934a370f28c1336a8bf0c0c0944462062a9317cf254d4ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a332ef769be7ab9d9d100bae943b3e2f1af4fc69a07fd08c591da9bf40f49`

```dockerfile
```

-	Layers:
	-	`sha256:3696bda8b095f58496bd3db9f0795eed260b1c194a955d81ee26ac412e6dbc02`  
		Last Modified: Mon, 25 Nov 2024 20:31:28 GMT  
		Size: 57.3 MB (57260886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a36439b8d122b7727196c04e60688c8493e56dc9dfdec71bab35384df7975b4`  
		Last Modified: Mon, 25 Nov 2024 20:31:26 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:249394c80de1afe549e21df093182a3562ac870e8f33aef14ae7fcc1a33b1b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **678.2 MB (678165891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e527f4a1fdf4de582ad9fc12ca026d3ee07e71c92c30cbd8f52ff97887ff58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Mon, 25 Nov 2024 09:49:34 GMT
MAINTAINER Odoo S.A. <info@odoo.com>
# Mon, 25 Nov 2024 09:49:34 GMT
SHELL [/bin/bash -xo pipefail -c]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV LANG=en_US.UTF-8
# Mon, 25 Nov 2024 09:49:34 GMT
ARG TARGETARCH=ppc64le
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN apt-get update &&     DEBIAN_FRONTEND=noninteractive     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         fonts-noto-cjk         gnupg         libssl-dev         node-less         npm         python3-magic         python3-num2words         python3-odf         python3-pdfminer         python3-pip         python3-phonenumbers         python3-pyldap         python3-qrcode         python3-renderpm         python3-setuptools         python3-slugify         python3-vobject         python3-watchdog         python3-xlrd         python3-xlwt         xz-utils &&     if [ -z "${TARGETARCH}" ]; then         TARGETARCH="$(dpkg --print-architecture)";     fi;     WKHTMLTOPDF_ARCH=${TARGETARCH} &&     case ${TARGETARCH} in     "amd64") WKHTMLTOPDF_ARCH=amd64 && WKHTMLTOPDF_SHA=967390a759707337b46d1c02452e2bb6b2dc6d59  ;;     "arm64")  WKHTMLTOPDF_SHA=90f6e69896d51ef77339d3f3a20f8582bdf496cc  ;;     "ppc64le" | "ppc64el") WKHTMLTOPDF_ARCH=ppc64el && WKHTMLTOPDF_SHA=5312d7d34a25b321282929df82e3574319aed25c  ;;     esac     && curl -o wkhtmltox.deb -sSL https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-3/wkhtmltox_0.12.6.1-3.jammy_${WKHTMLTOPDF_ARCH}.deb     && echo ${WKHTMLTOPDF_SHA} wkhtmltox.deb | sha1sum -c -     && apt-get install -y --no-install-recommends ./wkhtmltox.deb     && rm -rf /var/lib/apt/lists/* wkhtmltox.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ noble-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le
RUN npm install -g rtlcss # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_VERSION=18.0
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_RELEASE=20241125
# Mon, 25 Nov 2024 09:49:34 GMT
ARG ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./entrypoint.sh / # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20241125 ODOO_SHA=855fddc45b4c9bc2e2a832d275f8168918ffe08b
RUN chown odoo /etc/odoo/odoo.conf     && mkdir -p /mnt/extra-addons     && chown -R odoo /mnt/extra-addons # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
VOLUME [/var/lib/odoo /mnt/extra-addons]
# Mon, 25 Nov 2024 09:49:34 GMT
EXPOSE map[8069/tcp:{} 8071/tcp:{} 8072/tcp:{}]
# Mon, 25 Nov 2024 09:49:34 GMT
ENV ODOO_RC=/etc/odoo/odoo.conf
# Mon, 25 Nov 2024 09:49:34 GMT
COPY wait-for-psql.py /usr/local/bin/wait-for-psql.py # buildkit
# Mon, 25 Nov 2024 09:49:34 GMT
USER odoo
# Mon, 25 Nov 2024 09:49:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 25 Nov 2024 09:49:34 GMT
CMD ["odoo"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56ece3150b789ddce6e306870839a2059e2166b1c870f50ce72bb0f64f7afb0`  
		Last Modified: Sat, 16 Nov 2024 03:26:15 GMT  
		Size: 265.1 MB (265135565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9a057cad9c1029c466b8b4485c7e9959db3377ccb15d544d27fa01baa45706`  
		Last Modified: Sat, 16 Nov 2024 03:25:55 GMT  
		Size: 14.8 MB (14775605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1086a5a3d25f4fd37742c7ca85a30675397dbfa6a99c4be7c0ab236712db1ef5`  
		Last Modified: Sat, 16 Nov 2024 03:25:54 GMT  
		Size: 469.7 KB (469725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7171c978e079b5f38d49480060c57fbdc2109fe4dd925b4deec46f41d2a6ff`  
		Last Modified: Mon, 25 Nov 2024 20:33:47 GMT  
		Size: 363.4 MB (363393731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d226da017e27af535cefe9931994faddca35b7d916f648f1dd8368b8dabc5d`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6ec2d2f254202a162279de968878bbd07d01e9a8e2cfe7865f85dd0f473fea`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1584ad5a62aeeac9c71767750791bb6a7678373a2fdafaaeec5ae275695400c1`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77534b5938029530e4096968ea8c54f944e4746e8461b7989b949465b9301fb`  
		Last Modified: Mon, 25 Nov 2024 20:33:23 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:b39d5177f242c90faf213fb94814d3f11ed56d89e4d977e3762a0c93f6d3f53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57288949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac861a439bba788c553fe1545ab03af9f83b0c25f2c10cca6c2e44a0c9f3adc5`

```dockerfile
```

-	Layers:
	-	`sha256:d0b34ce28ec2bd9d116d571ab93d2398bef6baedb218ac7f7ac926fa32be56b5`  
		Last Modified: Mon, 25 Nov 2024 20:33:26 GMT  
		Size: 57.3 MB (57261751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bac00a9d8108fec117b5d00b192de8d2f5cfd669f283d7d0654a1429a8e6c6`  
		Last Modified: Mon, 25 Nov 2024 20:33:22 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
