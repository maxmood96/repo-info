<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `odoo`

-	[`odoo:17`](#odoo17)
-	[`odoo:17.0`](#odoo170)
-	[`odoo:17.0-20250930`](#odoo170-20250930)
-	[`odoo:18`](#odoo18)
-	[`odoo:18.0`](#odoo180)
-	[`odoo:18.0-20250930`](#odoo180-20250930)
-	[`odoo:19`](#odoo19)
-	[`odoo:19.0`](#odoo190)
-	[`odoo:19.0-20250930`](#odoo190-20250930)
-	[`odoo:latest`](#odoolatest)

## `odoo:17`

```console
$ docker pull odoo@sha256:861f3c301ccb9c8de070d595d023e3b7039d4f36fa436056caaf2637f38727fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17` - linux; amd64

```console
$ docker pull odoo@sha256:33508fe5b5790ebad1ff9f13e44d925562252fff496cccdfd5483c5ecc4cbb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605315986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbd556354d4a4aca336137a13f88fd9482591d8ca5de7626b3e60e98abddd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0143d45a9742e06d1ddfdfacbc76d73bad50cbf0a88693f5736ef27a8822146f`  
		Last Modified: Wed, 01 Oct 2025 13:24:07 GMT  
		Size: 233.8 MB (233818566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee454d2e10150da2ed1a9672ae93bffed0d9420f8f0a329532014e1da7ea9a6c`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 2.6 MB (2595034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aba55e5494b271093840c256abe2f85ce6c71a6f6166ca75ad7c2fb37c0dde`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 480.2 KB (480223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcedcb43660704fbbdac273689679f3060f95da95681225987b1d8965761612`  
		Last Modified: Wed, 01 Oct 2025 13:24:09 GMT  
		Size: 338.9 MB (338882791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8dc6a1065b1c7dec32da7e44d168b96eea544d214f4f02df17cdfb194b162`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0b3768235d630dd2b0cccaa211b4ace3629fe9e61c9ce644276df8db8b410f`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31114a2b3fbce134fe11c7e64206fd2b41113fcc0d7123fadf08c042c405e30`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd0cf0ff7b57b1fcca8333395a75c1c44bb2585cc0b80d412730a22b5e0cef`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:a120fb50d3db2c0689ef51b42e3dc9cdbf1005bcdcd2c1872efda07b318f600a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985c21374756f15c70efde989cb845baa73740d5f15b7b782626b213ac41953`

```dockerfile
```

-	Layers:
	-	`sha256:048b1713d485428416888cccfdc7014105402864dee4593c2bef5066cc02ba3a`  
		Last Modified: Wed, 01 Oct 2025 16:12:24 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3125e0679c12cf13a6f9fe6714daa453cb6f034c9daf88473a2ff0f055e2a88`  
		Last Modified: Wed, 01 Oct 2025 16:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f288c57d6685c8853570dfce97019c08b34d63d3422a52f9b7b27d4f6e5b02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.3 MB (602255227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da45bd0e813f3b7366f88b8d2a8d3100639c1238e528eafb3b5e2bab0f04301f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6b8705fb479d9b4bb20e0b5750a5dfe2635197f882eac87208348f446516d`  
		Last Modified: Wed, 01 Oct 2025 22:13:48 GMT  
		Size: 233.3 MB (233327670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460ff3b662e8beb67eb0068531a0dc1c72919e92a4eefd1604d76b4212ccf0d2`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 2.6 MB (2590639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14174baa48ba9645d815e6774c602261c2c58b838e824ad5c046fe291479914b`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 480.3 KB (480258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4611388deeb8bb23367948ee58d8c846f17c105fd84db08f20d0c319dc0e1286`  
		Last Modified: Wed, 01 Oct 2025 22:13:42 GMT  
		Size: 338.5 MB (338492756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3905006313b38f8abc47f2c48226d59ee6637e9bd0835eb6063536d0d4c46831`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7205f5948021e75bc78a88e9a3587fd2868e73918519f2d1cad1111d4cb14f`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e852ffd3e52b5835b93470f12e071876713dde90150191bb0827bb314b0579`  
		Last Modified: Tue, 30 Sep 2025 16:48:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363ebbad233c629c84e55a7052a9f3c440af24bd9a1d42a2a82eb6f2acfc756`  
		Last Modified: Tue, 30 Sep 2025 16:48:12 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17` - unknown; unknown

```console
$ docker pull odoo@sha256:b76a0eafe1cf74d3257e16ce2d290c000d909e574c618db3e5baf5adb32c6765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29735bd5c9e1d63403feb7a9f9c4999db6a8ee69748c41e45f404e65c58268d`

```dockerfile
```

-	Layers:
	-	`sha256:17fa2aab13adf2f20926edf4500b453f035789a2e13eb6db0a17679a6b7ae018`  
		Last Modified: Wed, 01 Oct 2025 22:13:04 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61f4fea0e362cbd26d52e426b3a1f2ec779f865a85d360f7dbfd3a70d206d1b`  
		Last Modified: Wed, 01 Oct 2025 22:13:05 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0`

```console
$ docker pull odoo@sha256:861f3c301ccb9c8de070d595d023e3b7039d4f36fa436056caaf2637f38727fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0` - linux; amd64

```console
$ docker pull odoo@sha256:33508fe5b5790ebad1ff9f13e44d925562252fff496cccdfd5483c5ecc4cbb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605315986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbd556354d4a4aca336137a13f88fd9482591d8ca5de7626b3e60e98abddd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0143d45a9742e06d1ddfdfacbc76d73bad50cbf0a88693f5736ef27a8822146f`  
		Last Modified: Wed, 01 Oct 2025 13:24:07 GMT  
		Size: 233.8 MB (233818566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee454d2e10150da2ed1a9672ae93bffed0d9420f8f0a329532014e1da7ea9a6c`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 2.6 MB (2595034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aba55e5494b271093840c256abe2f85ce6c71a6f6166ca75ad7c2fb37c0dde`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 480.2 KB (480223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcedcb43660704fbbdac273689679f3060f95da95681225987b1d8965761612`  
		Last Modified: Wed, 01 Oct 2025 13:24:09 GMT  
		Size: 338.9 MB (338882791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8dc6a1065b1c7dec32da7e44d168b96eea544d214f4f02df17cdfb194b162`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0b3768235d630dd2b0cccaa211b4ace3629fe9e61c9ce644276df8db8b410f`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31114a2b3fbce134fe11c7e64206fd2b41113fcc0d7123fadf08c042c405e30`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd0cf0ff7b57b1fcca8333395a75c1c44bb2585cc0b80d412730a22b5e0cef`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:a120fb50d3db2c0689ef51b42e3dc9cdbf1005bcdcd2c1872efda07b318f600a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985c21374756f15c70efde989cb845baa73740d5f15b7b782626b213ac41953`

```dockerfile
```

-	Layers:
	-	`sha256:048b1713d485428416888cccfdc7014105402864dee4593c2bef5066cc02ba3a`  
		Last Modified: Wed, 01 Oct 2025 16:12:24 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3125e0679c12cf13a6f9fe6714daa453cb6f034c9daf88473a2ff0f055e2a88`  
		Last Modified: Wed, 01 Oct 2025 16:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f288c57d6685c8853570dfce97019c08b34d63d3422a52f9b7b27d4f6e5b02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.3 MB (602255227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da45bd0e813f3b7366f88b8d2a8d3100639c1238e528eafb3b5e2bab0f04301f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6b8705fb479d9b4bb20e0b5750a5dfe2635197f882eac87208348f446516d`  
		Last Modified: Wed, 01 Oct 2025 22:13:48 GMT  
		Size: 233.3 MB (233327670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460ff3b662e8beb67eb0068531a0dc1c72919e92a4eefd1604d76b4212ccf0d2`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 2.6 MB (2590639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14174baa48ba9645d815e6774c602261c2c58b838e824ad5c046fe291479914b`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 480.3 KB (480258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4611388deeb8bb23367948ee58d8c846f17c105fd84db08f20d0c319dc0e1286`  
		Last Modified: Wed, 01 Oct 2025 22:13:42 GMT  
		Size: 338.5 MB (338492756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3905006313b38f8abc47f2c48226d59ee6637e9bd0835eb6063536d0d4c46831`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7205f5948021e75bc78a88e9a3587fd2868e73918519f2d1cad1111d4cb14f`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e852ffd3e52b5835b93470f12e071876713dde90150191bb0827bb314b0579`  
		Last Modified: Tue, 30 Sep 2025 16:48:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363ebbad233c629c84e55a7052a9f3c440af24bd9a1d42a2a82eb6f2acfc756`  
		Last Modified: Tue, 30 Sep 2025 16:48:12 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0` - unknown; unknown

```console
$ docker pull odoo@sha256:b76a0eafe1cf74d3257e16ce2d290c000d909e574c618db3e5baf5adb32c6765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29735bd5c9e1d63403feb7a9f9c4999db6a8ee69748c41e45f404e65c58268d`

```dockerfile
```

-	Layers:
	-	`sha256:17fa2aab13adf2f20926edf4500b453f035789a2e13eb6db0a17679a6b7ae018`  
		Last Modified: Wed, 01 Oct 2025 22:13:04 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61f4fea0e362cbd26d52e426b3a1f2ec779f865a85d360f7dbfd3a70d206d1b`  
		Last Modified: Wed, 01 Oct 2025 22:13:05 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:17.0-20250930`

```console
$ docker pull odoo@sha256:861f3c301ccb9c8de070d595d023e3b7039d4f36fa436056caaf2637f38727fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `odoo:17.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:33508fe5b5790ebad1ff9f13e44d925562252fff496cccdfd5483c5ecc4cbb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.3 MB (605315986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cbd556354d4a4aca336137a13f88fd9482591d8ca5de7626b3e60e98abddd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0143d45a9742e06d1ddfdfacbc76d73bad50cbf0a88693f5736ef27a8822146f`  
		Last Modified: Wed, 01 Oct 2025 13:24:07 GMT  
		Size: 233.8 MB (233818566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee454d2e10150da2ed1a9672ae93bffed0d9420f8f0a329532014e1da7ea9a6c`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 2.6 MB (2595034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2aba55e5494b271093840c256abe2f85ce6c71a6f6166ca75ad7c2fb37c0dde`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 480.2 KB (480223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcedcb43660704fbbdac273689679f3060f95da95681225987b1d8965761612`  
		Last Modified: Wed, 01 Oct 2025 13:24:09 GMT  
		Size: 338.9 MB (338882791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f8dc6a1065b1c7dec32da7e44d168b96eea544d214f4f02df17cdfb194b162`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0b3768235d630dd2b0cccaa211b4ace3629fe9e61c9ce644276df8db8b410f`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31114a2b3fbce134fe11c7e64206fd2b41113fcc0d7123fadf08c042c405e30`  
		Last Modified: Tue, 30 Sep 2025 18:00:03 GMT  
		Size: 594.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd0cf0ff7b57b1fcca8333395a75c1c44bb2585cc0b80d412730a22b5e0cef`  
		Last Modified: Tue, 30 Sep 2025 18:00:04 GMT  
		Size: 582.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:a120fb50d3db2c0689ef51b42e3dc9cdbf1005bcdcd2c1872efda07b318f600a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41507727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8985c21374756f15c70efde989cb845baa73740d5f15b7b782626b213ac41953`

```dockerfile
```

-	Layers:
	-	`sha256:048b1713d485428416888cccfdc7014105402864dee4593c2bef5066cc02ba3a`  
		Last Modified: Wed, 01 Oct 2025 16:12:24 GMT  
		Size: 41.5 MB (41480892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3125e0679c12cf13a6f9fe6714daa453cb6f034c9daf88473a2ff0f055e2a88`  
		Last Modified: Wed, 01 Oct 2025 16:12:26 GMT  
		Size: 26.8 KB (26835 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:17.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7f288c57d6685c8853570dfce97019c08b34d63d3422a52f9b7b27d4f6e5b02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.3 MB (602255227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da45bd0e813f3b7366f88b8d2a8d3100639c1238e528eafb3b5e2bab0f04301f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
RUN echo 'deb http://apt.postgresql.org/pub/repos/apt/ jammy-pgdg main' > /etc/apt/sources.list.d/pgdg.list     && GNUPGHOME="$(mktemp -d)"     && export GNUPGHOME     && repokey='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${repokey}"     && gpg --batch --armor --export "${repokey}" > /etc/apt/trusted.gpg.d/pgdg.gpg.asc     && gpgconf --kill all     && rm -rf "$GNUPGHOME"     && apt-get update      && apt-get install --no-install-recommends -y postgresql-client     && rm -f /etc/apt/sources.list.d/pgdg.list     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64
RUN npm install -g rtlcss # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
ENV ODOO_VERSION=17.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=96bb5a5134ac430686599588bef22b2b28a625f3
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f6b8705fb479d9b4bb20e0b5750a5dfe2635197f882eac87208348f446516d`  
		Last Modified: Wed, 01 Oct 2025 22:13:48 GMT  
		Size: 233.3 MB (233327670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460ff3b662e8beb67eb0068531a0dc1c72919e92a4eefd1604d76b4212ccf0d2`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 2.6 MB (2590639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14174baa48ba9645d815e6774c602261c2c58b838e824ad5c046fe291479914b`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 480.3 KB (480258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4611388deeb8bb23367948ee58d8c846f17c105fd84db08f20d0c319dc0e1286`  
		Last Modified: Wed, 01 Oct 2025 22:13:42 GMT  
		Size: 338.5 MB (338492756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3905006313b38f8abc47f2c48226d59ee6637e9bd0835eb6063536d0d4c46831`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7205f5948021e75bc78a88e9a3587fd2868e73918519f2d1cad1111d4cb14f`  
		Last Modified: Tue, 30 Sep 2025 16:48:11 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e852ffd3e52b5835b93470f12e071876713dde90150191bb0827bb314b0579`  
		Last Modified: Tue, 30 Sep 2025 16:48:12 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f363ebbad233c629c84e55a7052a9f3c440af24bd9a1d42a2a82eb6f2acfc756`  
		Last Modified: Tue, 30 Sep 2025 16:48:12 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:17.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:b76a0eafe1cf74d3257e16ce2d290c000d909e574c618db3e5baf5adb32c6765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29735bd5c9e1d63403feb7a9f9c4999db6a8ee69748c41e45f404e65c58268d`

```dockerfile
```

-	Layers:
	-	`sha256:17fa2aab13adf2f20926edf4500b453f035789a2e13eb6db0a17679a6b7ae018`  
		Last Modified: Wed, 01 Oct 2025 22:13:04 GMT  
		Size: 41.5 MB (41487399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61f4fea0e362cbd26d52e426b3a1f2ec779f865a85d360f7dbfd3a70d206d1b`  
		Last Modified: Wed, 01 Oct 2025 22:13:05 GMT  
		Size: 27.0 KB (26987 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18`

```console
$ docker pull odoo@sha256:7c9649e8776823da2dabd163cfd95b35572b5b64e8940385ec9630aa5e483964
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
$ docker pull odoo@sha256:ae693d1d13f22f784d2a60698980fd6d89bcbee9c620b43d8de3c5d2d02f3e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676985310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0743d582402fa9a2adafc0019181e1703bde6203b08ef8ae66a3162c9f90f9`
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:18c780b4ec78ec55b2bc8d6396642109b472b845987c507c55fd6681c261b3f6`  
		Last Modified: Wed, 01 Oct 2025 16:13:06 GMT  
		Size: 254.6 MB (254558403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dc840923a8b46aeeb85f244632220891a12af3d147c1ca2b561a2272190312`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 14.3 MB (14339224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a307b3c18d23bb86824b608d0a0f118c5c6512684bb9aa12ba58e44a185ffa1`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 480.0 KB (480048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b088ff29347cbb747d087736e7a1a1fec1375f54a1752febd10c89d5820fcc`  
		Last Modified: Wed, 01 Oct 2025 16:13:11 GMT  
		Size: 377.9 MB (377881749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f7344c5291479931b480ae3093b47cde4aa8351e2a5002f78533619813db0`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05840729df4e10d79d6dac6ce9688776e0f9b1ec9e1d6a6bee6ebe7f7be458`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c187a6867248eb35520fe145120dc69c4b09e2993f97b5546cf06b0dc89040e`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d44d8995ecf99415603813ee414df719f1a6e3a71da704dacee6758ecf5cae`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:71e55157cc87d0c04e38118fcb7fd530429bef3867a8946772c5eb0d5ebab3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279eaccd1cde500c026ff832785f2d1d6f5c8897f28372b06cd05ca65ab54d7`

```dockerfile
```

-	Layers:
	-	`sha256:9ca83d072da7043ce952f9f7d2602341cf00856482b446d986be54ee3dc448ab`  
		Last Modified: Wed, 01 Oct 2025 16:12:33 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbd949cae4c497b0ec4b8fd1573fa9064f704ea57ad33a08aa1ceda604300de`  
		Last Modified: Wed, 01 Oct 2025 16:12:34 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:aa15f36c0d3f8b8b80ae5bec31112872f9b3fbb98e024755c5145a79a1792bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675600763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91b19f197f7102b1df180db23577ecba9839910c54fb1a681f75c5d876ffc1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e51716fa8fe1fa9612d92ab57e9cd41c5a2ed89621f4708c583c2b5f47bf49`  
		Last Modified: Wed, 01 Oct 2025 22:13:52 GMT  
		Size: 254.2 MB (254200509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a191865c2e0db182273e330c998da787882d97052d5e1f0d40c3d70a57b60b7`  
		Last Modified: Tue, 30 Sep 2025 16:49:31 GMT  
		Size: 14.3 MB (14320133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34c0476e5eb4011292490ace37deab256dfbf6580e713f20852d78e5d437cb0`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 480.0 KB (480000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cde203287de0376fa7a1440c71288f605147f3417f77956bad8ba8d3c4a458`  
		Last Modified: Wed, 01 Oct 2025 22:13:29 GMT  
		Size: 377.7 MB (377736366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e515548ad7c36fe28851025cc8821bb66dc2146d8841c4534a39a47071b18f9`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346cadf5d5ae5af574be16db7907b0e209bb6b1a20af7aa4905bdfabfd083fa1`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a1956fb13cb6117034ad61376609dc6790a3b3d02a83e2b93b32296d7f53ec`  
		Last Modified: Tue, 30 Sep 2025 16:49:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30430cd84066de85460871dce90f51a0e2146317ce0cfbdee7d49ce8142787`  
		Last Modified: Tue, 30 Sep 2025 16:49:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:c16f3005fde7d10d9f4aa68a41cf1f09c951e4dd3c04586cf63ed6ffac46d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f610b693dc24bf4a79ef02231066d533589f3f78b3c32c32b8776030ff8e1cf`

```dockerfile
```

-	Layers:
	-	`sha256:ad200698890c258fab146c43539e331a79f2ee3b33882e9e1fa497675b28d763`  
		Last Modified: Wed, 01 Oct 2025 22:14:20 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee995fc5cb029cb060f7bd5e55d492abe1f7fb22454308e8c53fb86e146b049`  
		Last Modified: Wed, 01 Oct 2025 22:14:22 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18` - linux; ppc64le

```console
$ docker pull odoo@sha256:5d94ec1f554b13e43b417939e8a7e74787a8dcb0ea1255f999fc8a12e464e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695794473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4230edd05a99c8f8119cd81108a2f5ec65cd04a8bce777821a480f6e2abf17d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c3d56ef8312271aac7fa9961c7d447618b08b510ef9b5d3b60df55646d9e4`  
		Last Modified: Wed, 01 Oct 2025 19:59:33 GMT  
		Size: 267.7 MB (267726716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3820839802ff5606e3173e40ee27a10fb45e0a3c685308a25e94296b12467`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 14.9 MB (14867960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b560cc55c418f1481a33eb9a23a7c1ef497d836a7d94bb7269e6b2b0b785b`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 480.1 KB (480090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e6b49f8d4048022fd2d89c1cdafa40f0d674fe1e01cf718e5d9c6ddf20f060`  
		Last Modified: Wed, 01 Oct 2025 19:59:13 GMT  
		Size: 378.4 MB (378414138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab429104ffdebda9f1d212c0d0525449a5ad628c12fac90fb911a0816c074fd`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb41e7046a3c1ca475f570ffc5d3ae20fbfde9f9b8b9d4c6ccc8e5d61b3301d`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fda95f563177b8a7e3ce53331475e4926bde4662b60788c88ad094b2c31b9`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca6ae99d714064e466704cc76b5db5900b6c12c0e78955abd46d02abc6669a7`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18` - unknown; unknown

```console
$ docker pull odoo@sha256:09724fc5343e5b97e1f759f4eed47f91ca6195e7ad640801a8538bfdeebc101f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3147db43287ca4886e746994198d211be49bf0e84fa82e253d0007f54693ed0`

```dockerfile
```

-	Layers:
	-	`sha256:966244fff2dd5e719b79a426901327ea2a742fd9420f55e4139cb4ec90e7bd05`  
		Last Modified: Wed, 01 Oct 2025 22:16:07 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101924b83fa2372ffd6081faf92734f894b81f7dfd56f47e39adcd5a12cc055a`  
		Last Modified: Wed, 01 Oct 2025 22:16:09 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0`

```console
$ docker pull odoo@sha256:7c9649e8776823da2dabd163cfd95b35572b5b64e8940385ec9630aa5e483964
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
$ docker pull odoo@sha256:ae693d1d13f22f784d2a60698980fd6d89bcbee9c620b43d8de3c5d2d02f3e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676985310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0743d582402fa9a2adafc0019181e1703bde6203b08ef8ae66a3162c9f90f9`
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:18c780b4ec78ec55b2bc8d6396642109b472b845987c507c55fd6681c261b3f6`  
		Last Modified: Wed, 01 Oct 2025 16:13:06 GMT  
		Size: 254.6 MB (254558403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dc840923a8b46aeeb85f244632220891a12af3d147c1ca2b561a2272190312`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 14.3 MB (14339224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a307b3c18d23bb86824b608d0a0f118c5c6512684bb9aa12ba58e44a185ffa1`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 480.0 KB (480048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b088ff29347cbb747d087736e7a1a1fec1375f54a1752febd10c89d5820fcc`  
		Last Modified: Wed, 01 Oct 2025 16:13:11 GMT  
		Size: 377.9 MB (377881749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f7344c5291479931b480ae3093b47cde4aa8351e2a5002f78533619813db0`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05840729df4e10d79d6dac6ce9688776e0f9b1ec9e1d6a6bee6ebe7f7be458`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c187a6867248eb35520fe145120dc69c4b09e2993f97b5546cf06b0dc89040e`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d44d8995ecf99415603813ee414df719f1a6e3a71da704dacee6758ecf5cae`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:71e55157cc87d0c04e38118fcb7fd530429bef3867a8946772c5eb0d5ebab3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279eaccd1cde500c026ff832785f2d1d6f5c8897f28372b06cd05ca65ab54d7`

```dockerfile
```

-	Layers:
	-	`sha256:9ca83d072da7043ce952f9f7d2602341cf00856482b446d986be54ee3dc448ab`  
		Last Modified: Wed, 01 Oct 2025 16:12:33 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbd949cae4c497b0ec4b8fd1573fa9064f704ea57ad33a08aa1ceda604300de`  
		Last Modified: Wed, 01 Oct 2025 16:12:34 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:aa15f36c0d3f8b8b80ae5bec31112872f9b3fbb98e024755c5145a79a1792bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675600763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91b19f197f7102b1df180db23577ecba9839910c54fb1a681f75c5d876ffc1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e51716fa8fe1fa9612d92ab57e9cd41c5a2ed89621f4708c583c2b5f47bf49`  
		Last Modified: Wed, 01 Oct 2025 22:13:52 GMT  
		Size: 254.2 MB (254200509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a191865c2e0db182273e330c998da787882d97052d5e1f0d40c3d70a57b60b7`  
		Last Modified: Tue, 30 Sep 2025 16:49:31 GMT  
		Size: 14.3 MB (14320133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34c0476e5eb4011292490ace37deab256dfbf6580e713f20852d78e5d437cb0`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 480.0 KB (480000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cde203287de0376fa7a1440c71288f605147f3417f77956bad8ba8d3c4a458`  
		Last Modified: Wed, 01 Oct 2025 22:13:29 GMT  
		Size: 377.7 MB (377736366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e515548ad7c36fe28851025cc8821bb66dc2146d8841c4534a39a47071b18f9`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346cadf5d5ae5af574be16db7907b0e209bb6b1a20af7aa4905bdfabfd083fa1`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a1956fb13cb6117034ad61376609dc6790a3b3d02a83e2b93b32296d7f53ec`  
		Last Modified: Tue, 30 Sep 2025 16:49:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30430cd84066de85460871dce90f51a0e2146317ce0cfbdee7d49ce8142787`  
		Last Modified: Tue, 30 Sep 2025 16:49:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:c16f3005fde7d10d9f4aa68a41cf1f09c951e4dd3c04586cf63ed6ffac46d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f610b693dc24bf4a79ef02231066d533589f3f78b3c32c32b8776030ff8e1cf`

```dockerfile
```

-	Layers:
	-	`sha256:ad200698890c258fab146c43539e331a79f2ee3b33882e9e1fa497675b28d763`  
		Last Modified: Wed, 01 Oct 2025 22:14:20 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee995fc5cb029cb060f7bd5e55d492abe1f7fb22454308e8c53fb86e146b049`  
		Last Modified: Wed, 01 Oct 2025 22:14:22 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:5d94ec1f554b13e43b417939e8a7e74787a8dcb0ea1255f999fc8a12e464e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695794473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4230edd05a99c8f8119cd81108a2f5ec65cd04a8bce777821a480f6e2abf17d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c3d56ef8312271aac7fa9961c7d447618b08b510ef9b5d3b60df55646d9e4`  
		Last Modified: Wed, 01 Oct 2025 19:59:33 GMT  
		Size: 267.7 MB (267726716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3820839802ff5606e3173e40ee27a10fb45e0a3c685308a25e94296b12467`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 14.9 MB (14867960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b560cc55c418f1481a33eb9a23a7c1ef497d836a7d94bb7269e6b2b0b785b`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 480.1 KB (480090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e6b49f8d4048022fd2d89c1cdafa40f0d674fe1e01cf718e5d9c6ddf20f060`  
		Last Modified: Wed, 01 Oct 2025 19:59:13 GMT  
		Size: 378.4 MB (378414138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab429104ffdebda9f1d212c0d0525449a5ad628c12fac90fb911a0816c074fd`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb41e7046a3c1ca475f570ffc5d3ae20fbfde9f9b8b9d4c6ccc8e5d61b3301d`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fda95f563177b8a7e3ce53331475e4926bde4662b60788c88ad094b2c31b9`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca6ae99d714064e466704cc76b5db5900b6c12c0e78955abd46d02abc6669a7`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0` - unknown; unknown

```console
$ docker pull odoo@sha256:09724fc5343e5b97e1f759f4eed47f91ca6195e7ad640801a8538bfdeebc101f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3147db43287ca4886e746994198d211be49bf0e84fa82e253d0007f54693ed0`

```dockerfile
```

-	Layers:
	-	`sha256:966244fff2dd5e719b79a426901327ea2a742fd9420f55e4139cb4ec90e7bd05`  
		Last Modified: Wed, 01 Oct 2025 22:16:07 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101924b83fa2372ffd6081faf92734f894b81f7dfd56f47e39adcd5a12cc055a`  
		Last Modified: Wed, 01 Oct 2025 22:16:09 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:18.0-20250930`

```console
$ docker pull odoo@sha256:7c9649e8776823da2dabd163cfd95b35572b5b64e8940385ec9630aa5e483964
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:18.0-20250930` - linux; amd64

```console
$ docker pull odoo@sha256:ae693d1d13f22f784d2a60698980fd6d89bcbee9c620b43d8de3c5d2d02f3e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676985310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0743d582402fa9a2adafc0019181e1703bde6203b08ef8ae66a3162c9f90f9`
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=amd64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:18c780b4ec78ec55b2bc8d6396642109b472b845987c507c55fd6681c261b3f6`  
		Last Modified: Wed, 01 Oct 2025 16:13:06 GMT  
		Size: 254.6 MB (254558403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dc840923a8b46aeeb85f244632220891a12af3d147c1ca2b561a2272190312`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 14.3 MB (14339224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a307b3c18d23bb86824b608d0a0f118c5c6512684bb9aa12ba58e44a185ffa1`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 480.0 KB (480048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b088ff29347cbb747d087736e7a1a1fec1375f54a1752febd10c89d5820fcc`  
		Last Modified: Wed, 01 Oct 2025 16:13:11 GMT  
		Size: 377.9 MB (377881749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f7344c5291479931b480ae3093b47cde4aa8351e2a5002f78533619813db0`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 705.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05840729df4e10d79d6dac6ce9688776e0f9b1ec9e1d6a6bee6ebe7f7be458`  
		Last Modified: Tue, 30 Sep 2025 17:03:29 GMT  
		Size: 555.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c187a6867248eb35520fe145120dc69c4b09e2993f97b5546cf06b0dc89040e`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d44d8995ecf99415603813ee414df719f1a6e3a71da704dacee6758ecf5cae`  
		Last Modified: Tue, 30 Sep 2025 17:03:30 GMT  
		Size: 578.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:71e55157cc87d0c04e38118fcb7fd530429bef3867a8946772c5eb0d5ebab3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61088147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4279eaccd1cde500c026ff832785f2d1d6f5c8897f28372b06cd05ca65ab54d7`

```dockerfile
```

-	Layers:
	-	`sha256:9ca83d072da7043ce952f9f7d2602341cf00856482b446d986be54ee3dc448ab`  
		Last Modified: Wed, 01 Oct 2025 16:12:33 GMT  
		Size: 61.1 MB (61061305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbd949cae4c497b0ec4b8fd1573fa9064f704ea57ad33a08aa1ceda604300de`  
		Last Modified: Wed, 01 Oct 2025 16:12:34 GMT  
		Size: 26.8 KB (26842 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:aa15f36c0d3f8b8b80ae5bec31112872f9b3fbb98e024755c5145a79a1792bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **675.6 MB (675600763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91b19f197f7102b1df180db23577ecba9839910c54fb1a681f75c5d876ffc1e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=arm64 ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e51716fa8fe1fa9612d92ab57e9cd41c5a2ed89621f4708c583c2b5f47bf49`  
		Last Modified: Wed, 01 Oct 2025 22:13:52 GMT  
		Size: 254.2 MB (254200509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a191865c2e0db182273e330c998da787882d97052d5e1f0d40c3d70a57b60b7`  
		Last Modified: Tue, 30 Sep 2025 16:49:31 GMT  
		Size: 14.3 MB (14320133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34c0476e5eb4011292490ace37deab256dfbf6580e713f20852d78e5d437cb0`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 480.0 KB (480000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cde203287de0376fa7a1440c71288f605147f3417f77956bad8ba8d3c4a458`  
		Last Modified: Wed, 01 Oct 2025 22:13:29 GMT  
		Size: 377.7 MB (377736366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e515548ad7c36fe28851025cc8821bb66dc2146d8841c4534a39a47071b18f9`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346cadf5d5ae5af574be16db7907b0e209bb6b1a20af7aa4905bdfabfd083fa1`  
		Last Modified: Tue, 30 Sep 2025 16:49:29 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a1956fb13cb6117034ad61376609dc6790a3b3d02a83e2b93b32296d7f53ec`  
		Last Modified: Tue, 30 Sep 2025 16:49:30 GMT  
		Size: 595.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30430cd84066de85460871dce90f51a0e2146317ce0cfbdee7d49ce8142787`  
		Last Modified: Tue, 30 Sep 2025 16:49:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:c16f3005fde7d10d9f4aa68a41cf1f09c951e4dd3c04586cf63ed6ffac46d0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61095574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f610b693dc24bf4a79ef02231066d533589f3f78b3c32c32b8776030ff8e1cf`

```dockerfile
```

-	Layers:
	-	`sha256:ad200698890c258fab146c43539e331a79f2ee3b33882e9e1fa497675b28d763`  
		Last Modified: Wed, 01 Oct 2025 22:14:20 GMT  
		Size: 61.1 MB (61068580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aee995fc5cb029cb060f7bd5e55d492abe1f7fb22454308e8c53fb86e146b049`  
		Last Modified: Wed, 01 Oct 2025 22:14:22 GMT  
		Size: 27.0 KB (26994 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:18.0-20250930` - linux; ppc64le

```console
$ docker pull odoo@sha256:5d94ec1f554b13e43b417939e8a7e74787a8dcb0ea1255f999fc8a12e464e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.8 MB (695794473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4230edd05a99c8f8119cd81108a2f5ec65cd04a8bce777821a480f6e2abf17d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
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
ENV ODOO_VERSION=18.0
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_RELEASE=20250930
# Tue, 30 Sep 2025 08:05:28 GMT
ARG ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
RUN curl -o odoo.deb -sSL http://nightly.odoo.com/${ODOO_VERSION}/nightly/deb/odoo_${ODOO_VERSION}.${ODOO_RELEASE}_all.deb     && echo "${ODOO_SHA} odoo.deb" | sha1sum -c -     && apt-get update     && apt-get -y install --no-install-recommends ./odoo.deb     && rm -rf /var/lib/apt/lists/* odoo.deb # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./entrypoint.sh / # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
COPY ./odoo.conf /etc/odoo/ # buildkit
# Tue, 30 Sep 2025 08:05:28 GMT
# ARGS: TARGETARCH=ppc64le ODOO_RELEASE=20250930 ODOO_SHA=e1d45235189baf437efe38e8fa3a32b19e93efb2
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c3d56ef8312271aac7fa9961c7d447618b08b510ef9b5d3b60df55646d9e4`  
		Last Modified: Wed, 01 Oct 2025 19:59:33 GMT  
		Size: 267.7 MB (267726716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3820839802ff5606e3173e40ee27a10fb45e0a3c685308a25e94296b12467`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 14.9 MB (14867960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b560cc55c418f1481a33eb9a23a7c1ef497d836a7d94bb7269e6b2b0b785b`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 480.1 KB (480090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e6b49f8d4048022fd2d89c1cdafa40f0d674fe1e01cf718e5d9c6ddf20f060`  
		Last Modified: Wed, 01 Oct 2025 19:59:13 GMT  
		Size: 378.4 MB (378414138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab429104ffdebda9f1d212c0d0525449a5ad628c12fac90fb911a0816c074fd`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb41e7046a3c1ca475f570ffc5d3ae20fbfde9f9b8b9d4c6ccc8e5d61b3301d`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fda95f563177b8a7e3ce53331475e4926bde4662b60788c88ad094b2c31b9`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 600.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca6ae99d714064e466704cc76b5db5900b6c12c0e78955abd46d02abc6669a7`  
		Last Modified: Tue, 30 Sep 2025 22:10:13 GMT  
		Size: 580.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:18.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:09724fc5343e5b97e1f759f4eed47f91ca6195e7ad640801a8538bfdeebc101f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 MB (61096586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3147db43287ca4886e746994198d211be49bf0e84fa82e253d0007f54693ed0`

```dockerfile
```

-	Layers:
	-	`sha256:966244fff2dd5e719b79a426901327ea2a742fd9420f55e4139cb4ec90e7bd05`  
		Last Modified: Wed, 01 Oct 2025 22:16:07 GMT  
		Size: 61.1 MB (61069688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101924b83fa2372ffd6081faf92734f894b81f7dfd56f47e39adcd5a12cc055a`  
		Last Modified: Wed, 01 Oct 2025 22:16:09 GMT  
		Size: 26.9 KB (26898 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19`

```console
$ docker pull odoo@sha256:9a5b69c96b6ec2c7efdaa008e2e7457bd541c3e1fc63bcddabf1935858447e15
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

### `odoo:19` - unknown; unknown

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

### `odoo:19` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c368ca78cc03b3ccda1205667d4caaf2395f6657142ecaf5862cd21608240a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad669cb53e72884d8dbd528e623da628da382daaf3b8607e136ac036cd1a510f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2d170bf6dcaf876ee182d00be0570068282c884b272249b5598c3ad08081fd`  
		Last Modified: Wed, 01 Oct 2025 19:50:17 GMT  
		Size: 254.2 MB (254200442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d49b17f834d23759d57e0b2d04f71ea8c08f39a7f5ad06be1827400cc10083`  
		Last Modified: Wed, 01 Oct 2025 05:36:47 GMT  
		Size: 14.3 MB (14319938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c2516829e08fa721f466c1c6ea0d56db591381581ddbd429a0c8b59138b584`  
		Last Modified: Wed, 01 Oct 2025 06:31:36 GMT  
		Size: 480.1 KB (480057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22446d6b773a9a453f275e3b472105de77aad55560b15678d8cfe77a86eef92`  
		Last Modified: Wed, 01 Oct 2025 19:51:03 GMT  
		Size: 379.1 MB (379078880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea62bd14d298aa7bdce8aee7cf804ca7afbff855aec550796667d1d7ad81d3`  
		Last Modified: Wed, 01 Oct 2025 06:37:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc14b90602d67188b9aaf1a7455fca7a064d06891ef398bd2b0a411699f1919`  
		Last Modified: Wed, 01 Oct 2025 06:47:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869a3d92b0c97956ea06858b6547bc2b98019ea6595b2593d2364a19237516e`  
		Last Modified: Wed, 01 Oct 2025 06:37:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfed8c303926de7bc8f07ec4727c71ea89ceaca3aafd573dc0b004bfd7a8f0b1`  
		Last Modified: Wed, 01 Oct 2025 06:47:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:fc5df018e15a8c3a3ddcfbb41f8c77dfa57f59e699796b3900cf7f24cbe389d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bb5906e2c6f006fa982e633c7ff35d7b8f359350bfbccc2edf0468f5f7fa3`

```dockerfile
```

-	Layers:
	-	`sha256:e972af85da7aecdcc7950e00eee42d7626376af6cd95fd2b1888144de2aac454`  
		Last Modified: Wed, 01 Oct 2025 22:14:52 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6d42597a4825aea2f15ac2881d4ac075cc3aa711f36895837e34c7c90d8285`  
		Last Modified: Wed, 01 Oct 2025 22:14:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19` - linux; ppc64le

```console
$ docker pull odoo@sha256:2850b5ee1606286994fba01870950a12a16e3d4c52bcf689b09c9bbe11bce6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697156886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24772baa0567ad2a4aad9dd67b683b7bbd1e26828bfc47b68da091917d3850d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c3d56ef8312271aac7fa9961c7d447618b08b510ef9b5d3b60df55646d9e4`  
		Last Modified: Wed, 01 Oct 2025 19:59:33 GMT  
		Size: 267.7 MB (267726716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3820839802ff5606e3173e40ee27a10fb45e0a3c685308a25e94296b12467`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 14.9 MB (14867960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b560cc55c418f1481a33eb9a23a7c1ef497d836a7d94bb7269e6b2b0b785b`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 480.1 KB (480090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa45e9ac6f7e262c32b001da94c6f606c7644dc3ca3697b3810eb6364099d83a`  
		Last Modified: Tue, 30 Sep 2025 22:03:51 GMT  
		Size: 379.8 MB (379776552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300b9a550d53c89d37bb1ba1f735bfaefb0f6b1e71bd2e08870d31f721444b83`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dea4c04271cb743df4e9fa35f0c86940d57a79338e23b5304e8c0dc8c8bcda`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54692b6b1f7237c5002ea281e43d7b60e8eae7c2c455c463a5ec288afcc33dd0`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc271f9337e6b4f846efe8a3d7abb6d37d7437768366d314b9e59fac4c41303`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19` - unknown; unknown

```console
$ docker pull odoo@sha256:38c1df898be58dd69f605803272254d03fe571bb825d08005fa3bc97c96b2332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dd2528716efe250b884c0bc0c59bcc9398fd8f87f2c1e6ddc318d3d2e93ab9`

```dockerfile
```

-	Layers:
	-	`sha256:f664f4bd95ecc9d2d2283282240e961d07f2befd8646f6b7578ec7050a742b3e`  
		Last Modified: Wed, 01 Oct 2025 22:16:47 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74d03d5a5868bb42367b42f08894c1009b75a10bcc0e38d6236359ed0f01689`  
		Last Modified: Wed, 01 Oct 2025 22:16:48 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0`

```console
$ docker pull odoo@sha256:9a5b69c96b6ec2c7efdaa008e2e7457bd541c3e1fc63bcddabf1935858447e15
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

### `odoo:19.0` - unknown; unknown

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

### `odoo:19.0` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c368ca78cc03b3ccda1205667d4caaf2395f6657142ecaf5862cd21608240a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad669cb53e72884d8dbd528e623da628da382daaf3b8607e136ac036cd1a510f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2d170bf6dcaf876ee182d00be0570068282c884b272249b5598c3ad08081fd`  
		Last Modified: Wed, 01 Oct 2025 19:50:17 GMT  
		Size: 254.2 MB (254200442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d49b17f834d23759d57e0b2d04f71ea8c08f39a7f5ad06be1827400cc10083`  
		Last Modified: Wed, 01 Oct 2025 05:36:47 GMT  
		Size: 14.3 MB (14319938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c2516829e08fa721f466c1c6ea0d56db591381581ddbd429a0c8b59138b584`  
		Last Modified: Wed, 01 Oct 2025 06:31:36 GMT  
		Size: 480.1 KB (480057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22446d6b773a9a453f275e3b472105de77aad55560b15678d8cfe77a86eef92`  
		Last Modified: Wed, 01 Oct 2025 19:51:03 GMT  
		Size: 379.1 MB (379078880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea62bd14d298aa7bdce8aee7cf804ca7afbff855aec550796667d1d7ad81d3`  
		Last Modified: Wed, 01 Oct 2025 06:37:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc14b90602d67188b9aaf1a7455fca7a064d06891ef398bd2b0a411699f1919`  
		Last Modified: Wed, 01 Oct 2025 06:47:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869a3d92b0c97956ea06858b6547bc2b98019ea6595b2593d2364a19237516e`  
		Last Modified: Wed, 01 Oct 2025 06:37:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfed8c303926de7bc8f07ec4727c71ea89ceaca3aafd573dc0b004bfd7a8f0b1`  
		Last Modified: Wed, 01 Oct 2025 06:47:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:fc5df018e15a8c3a3ddcfbb41f8c77dfa57f59e699796b3900cf7f24cbe389d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bb5906e2c6f006fa982e633c7ff35d7b8f359350bfbccc2edf0468f5f7fa3`

```dockerfile
```

-	Layers:
	-	`sha256:e972af85da7aecdcc7950e00eee42d7626376af6cd95fd2b1888144de2aac454`  
		Last Modified: Wed, 01 Oct 2025 22:14:52 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6d42597a4825aea2f15ac2881d4ac075cc3aa711f36895837e34c7c90d8285`  
		Last Modified: Wed, 01 Oct 2025 22:14:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0` - linux; ppc64le

```console
$ docker pull odoo@sha256:2850b5ee1606286994fba01870950a12a16e3d4c52bcf689b09c9bbe11bce6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697156886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24772baa0567ad2a4aad9dd67b683b7bbd1e26828bfc47b68da091917d3850d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c3d56ef8312271aac7fa9961c7d447618b08b510ef9b5d3b60df55646d9e4`  
		Last Modified: Wed, 01 Oct 2025 19:59:33 GMT  
		Size: 267.7 MB (267726716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3820839802ff5606e3173e40ee27a10fb45e0a3c685308a25e94296b12467`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 14.9 MB (14867960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b560cc55c418f1481a33eb9a23a7c1ef497d836a7d94bb7269e6b2b0b785b`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 480.1 KB (480090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa45e9ac6f7e262c32b001da94c6f606c7644dc3ca3697b3810eb6364099d83a`  
		Last Modified: Tue, 30 Sep 2025 22:03:51 GMT  
		Size: 379.8 MB (379776552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300b9a550d53c89d37bb1ba1f735bfaefb0f6b1e71bd2e08870d31f721444b83`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dea4c04271cb743df4e9fa35f0c86940d57a79338e23b5304e8c0dc8c8bcda`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54692b6b1f7237c5002ea281e43d7b60e8eae7c2c455c463a5ec288afcc33dd0`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc271f9337e6b4f846efe8a3d7abb6d37d7437768366d314b9e59fac4c41303`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0` - unknown; unknown

```console
$ docker pull odoo@sha256:38c1df898be58dd69f605803272254d03fe571bb825d08005fa3bc97c96b2332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dd2528716efe250b884c0bc0c59bcc9398fd8f87f2c1e6ddc318d3d2e93ab9`

```dockerfile
```

-	Layers:
	-	`sha256:f664f4bd95ecc9d2d2283282240e961d07f2befd8646f6b7578ec7050a742b3e`  
		Last Modified: Wed, 01 Oct 2025 22:16:47 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74d03d5a5868bb42367b42f08894c1009b75a10bcc0e38d6236359ed0f01689`  
		Last Modified: Wed, 01 Oct 2025 22:16:48 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:19.0-20250930`

```console
$ docker pull odoo@sha256:9a5b69c96b6ec2c7efdaa008e2e7457bd541c3e1fc63bcddabf1935858447e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `odoo:19.0-20250930` - linux; amd64

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

### `odoo:19.0-20250930` - unknown; unknown

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

### `odoo:19.0-20250930` - linux; arm64 variant v8

```console
$ docker pull odoo@sha256:7c368ca78cc03b3ccda1205667d4caaf2395f6657142ecaf5862cd21608240a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad669cb53e72884d8dbd528e623da628da382daaf3b8607e136ac036cd1a510f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2d170bf6dcaf876ee182d00be0570068282c884b272249b5598c3ad08081fd`  
		Last Modified: Wed, 01 Oct 2025 19:50:17 GMT  
		Size: 254.2 MB (254200442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d49b17f834d23759d57e0b2d04f71ea8c08f39a7f5ad06be1827400cc10083`  
		Last Modified: Wed, 01 Oct 2025 05:36:47 GMT  
		Size: 14.3 MB (14319938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c2516829e08fa721f466c1c6ea0d56db591381581ddbd429a0c8b59138b584`  
		Last Modified: Wed, 01 Oct 2025 06:31:36 GMT  
		Size: 480.1 KB (480057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22446d6b773a9a453f275e3b472105de77aad55560b15678d8cfe77a86eef92`  
		Last Modified: Wed, 01 Oct 2025 19:51:03 GMT  
		Size: 379.1 MB (379078880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea62bd14d298aa7bdce8aee7cf804ca7afbff855aec550796667d1d7ad81d3`  
		Last Modified: Wed, 01 Oct 2025 06:37:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc14b90602d67188b9aaf1a7455fca7a064d06891ef398bd2b0a411699f1919`  
		Last Modified: Wed, 01 Oct 2025 06:47:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869a3d92b0c97956ea06858b6547bc2b98019ea6595b2593d2364a19237516e`  
		Last Modified: Wed, 01 Oct 2025 06:37:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfed8c303926de7bc8f07ec4727c71ea89ceaca3aafd573dc0b004bfd7a8f0b1`  
		Last Modified: Wed, 01 Oct 2025 06:47:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:fc5df018e15a8c3a3ddcfbb41f8c77dfa57f59e699796b3900cf7f24cbe389d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bb5906e2c6f006fa982e633c7ff35d7b8f359350bfbccc2edf0468f5f7fa3`

```dockerfile
```

-	Layers:
	-	`sha256:e972af85da7aecdcc7950e00eee42d7626376af6cd95fd2b1888144de2aac454`  
		Last Modified: Wed, 01 Oct 2025 22:14:52 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6d42597a4825aea2f15ac2881d4ac075cc3aa711f36895837e34c7c90d8285`  
		Last Modified: Wed, 01 Oct 2025 22:14:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:19.0-20250930` - linux; ppc64le

```console
$ docker pull odoo@sha256:2850b5ee1606286994fba01870950a12a16e3d4c52bcf689b09c9bbe11bce6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697156886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24772baa0567ad2a4aad9dd67b683b7bbd1e26828bfc47b68da091917d3850d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c3d56ef8312271aac7fa9961c7d447618b08b510ef9b5d3b60df55646d9e4`  
		Last Modified: Wed, 01 Oct 2025 19:59:33 GMT  
		Size: 267.7 MB (267726716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3820839802ff5606e3173e40ee27a10fb45e0a3c685308a25e94296b12467`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 14.9 MB (14867960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b560cc55c418f1481a33eb9a23a7c1ef497d836a7d94bb7269e6b2b0b785b`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 480.1 KB (480090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa45e9ac6f7e262c32b001da94c6f606c7644dc3ca3697b3810eb6364099d83a`  
		Last Modified: Tue, 30 Sep 2025 22:03:51 GMT  
		Size: 379.8 MB (379776552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300b9a550d53c89d37bb1ba1f735bfaefb0f6b1e71bd2e08870d31f721444b83`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dea4c04271cb743df4e9fa35f0c86940d57a79338e23b5304e8c0dc8c8bcda`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54692b6b1f7237c5002ea281e43d7b60e8eae7c2c455c463a5ec288afcc33dd0`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc271f9337e6b4f846efe8a3d7abb6d37d7437768366d314b9e59fac4c41303`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:19.0-20250930` - unknown; unknown

```console
$ docker pull odoo@sha256:38c1df898be58dd69f605803272254d03fe571bb825d08005fa3bc97c96b2332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dd2528716efe250b884c0bc0c59bcc9398fd8f87f2c1e6ddc318d3d2e93ab9`

```dockerfile
```

-	Layers:
	-	`sha256:f664f4bd95ecc9d2d2283282240e961d07f2befd8646f6b7578ec7050a742b3e`  
		Last Modified: Wed, 01 Oct 2025 22:16:47 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74d03d5a5868bb42367b42f08894c1009b75a10bcc0e38d6236359ed0f01689`  
		Last Modified: Wed, 01 Oct 2025 22:16:48 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json

## `odoo:latest`

```console
$ docker pull odoo@sha256:9a5b69c96b6ec2c7efdaa008e2e7457bd541c3e1fc63bcddabf1935858447e15
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
$ docker pull odoo@sha256:7c368ca78cc03b3ccda1205667d4caaf2395f6657142ecaf5862cd21608240a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.9 MB (676943075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad669cb53e72884d8dbd528e623da628da382daaf3b8607e136ac036cd1a510f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2d170bf6dcaf876ee182d00be0570068282c884b272249b5598c3ad08081fd`  
		Last Modified: Wed, 01 Oct 2025 19:50:17 GMT  
		Size: 254.2 MB (254200442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d49b17f834d23759d57e0b2d04f71ea8c08f39a7f5ad06be1827400cc10083`  
		Last Modified: Wed, 01 Oct 2025 05:36:47 GMT  
		Size: 14.3 MB (14319938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c2516829e08fa721f466c1c6ea0d56db591381581ddbd429a0c8b59138b584`  
		Last Modified: Wed, 01 Oct 2025 06:31:36 GMT  
		Size: 480.1 KB (480057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22446d6b773a9a453f275e3b472105de77aad55560b15678d8cfe77a86eef92`  
		Last Modified: Wed, 01 Oct 2025 19:51:03 GMT  
		Size: 379.1 MB (379078880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea62bd14d298aa7bdce8aee7cf804ca7afbff855aec550796667d1d7ad81d3`  
		Last Modified: Wed, 01 Oct 2025 06:37:03 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc14b90602d67188b9aaf1a7455fca7a064d06891ef398bd2b0a411699f1919`  
		Last Modified: Wed, 01 Oct 2025 06:47:59 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f869a3d92b0c97956ea06858b6547bc2b98019ea6595b2593d2364a19237516e`  
		Last Modified: Wed, 01 Oct 2025 06:37:10 GMT  
		Size: 598.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfed8c303926de7bc8f07ec4727c71ea89ceaca3aafd573dc0b004bfd7a8f0b1`  
		Last Modified: Wed, 01 Oct 2025 06:47:18 GMT  
		Size: 581.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:fc5df018e15a8c3a3ddcfbb41f8c77dfa57f59e699796b3900cf7f24cbe389d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67740998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bb5906e2c6f006fa982e633c7ff35d7b8f359350bfbccc2edf0468f5f7fa3`

```dockerfile
```

-	Layers:
	-	`sha256:e972af85da7aecdcc7950e00eee42d7626376af6cd95fd2b1888144de2aac454`  
		Last Modified: Wed, 01 Oct 2025 22:14:52 GMT  
		Size: 67.7 MB (67713698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c6d42597a4825aea2f15ac2881d4ac075cc3aa711f36895837e34c7c90d8285`  
		Last Modified: Wed, 01 Oct 2025 22:14:54 GMT  
		Size: 27.3 KB (27300 bytes)  
		MIME: application/vnd.in-toto+json

### `odoo:latest` - linux; ppc64le

```console
$ docker pull odoo@sha256:2850b5ee1606286994fba01870950a12a16e3d4c52bcf689b09c9bbe11bce6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **697.2 MB (697156886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24772baa0567ad2a4aad9dd67b683b7bbd1e26828bfc47b68da091917d3850d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["odoo"]`
-	`SHELL`: `["\/bin\/bash","-xo","pipefail","-c"]`

```dockerfile
# Wed, 10 Sep 2025 05:44:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:44:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:44:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:44:36 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 10 Sep 2025 05:44:36 GMT
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
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c3d56ef8312271aac7fa9961c7d447618b08b510ef9b5d3b60df55646d9e4`  
		Last Modified: Wed, 01 Oct 2025 19:59:33 GMT  
		Size: 267.7 MB (267726716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e3820839802ff5606e3173e40ee27a10fb45e0a3c685308a25e94296b12467`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 14.9 MB (14867960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2b560cc55c418f1481a33eb9a23a7c1ef497d836a7d94bb7269e6b2b0b785b`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 480.1 KB (480090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa45e9ac6f7e262c32b001da94c6f606c7644dc3ca3697b3810eb6364099d83a`  
		Last Modified: Tue, 30 Sep 2025 22:03:51 GMT  
		Size: 379.8 MB (379776552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300b9a550d53c89d37bb1ba1f735bfaefb0f6b1e71bd2e08870d31f721444b83`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dea4c04271cb743df4e9fa35f0c86940d57a79338e23b5304e8c0dc8c8bcda`  
		Last Modified: Tue, 30 Sep 2025 22:04:15 GMT  
		Size: 556.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54692b6b1f7237c5002ea281e43d7b60e8eae7c2c455c463a5ec288afcc33dd0`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 596.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc271f9337e6b4f846efe8a3d7abb6d37d7437768366d314b9e59fac4c41303`  
		Last Modified: Tue, 30 Sep 2025 22:04:16 GMT  
		Size: 583.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `odoo:latest` - unknown; unknown

```console
$ docker pull odoo@sha256:38c1df898be58dd69f605803272254d03fe571bb825d08005fa3bc97c96b2332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67741998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dd2528716efe250b884c0bc0c59bcc9398fd8f87f2c1e6ddc318d3d2e93ab9`

```dockerfile
```

-	Layers:
	-	`sha256:f664f4bd95ecc9d2d2283282240e961d07f2befd8646f6b7578ec7050a742b3e`  
		Last Modified: Wed, 01 Oct 2025 22:16:47 GMT  
		Size: 67.7 MB (67714800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74d03d5a5868bb42367b42f08894c1009b75a10bcc0e38d6236359ed0f01689`  
		Last Modified: Wed, 01 Oct 2025 22:16:48 GMT  
		Size: 27.2 KB (27198 bytes)  
		MIME: application/vnd.in-toto+json
