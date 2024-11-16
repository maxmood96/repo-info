## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ef53bd593d7cb0e1f6d21b6d918e28603a64da38d8d531628e3f4da61f18923d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9028b9aa2427f67edec88f6e93873194873c6745e03e7062d5a5a3613d475c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134460613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291760193513cdd5706566fefd289e0b7ffa6844a9a9596a0944595bc73c4f81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:46453255c2f610c1cb9c8197635e6d542bbd326425a9898df0de76e5bb566461`  
		Last Modified: Thu, 14 Nov 2024 23:11:22 GMT  
		Size: 52.4 MB (52379519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a973bbfdd6c19671d433f547a3beafb6dda339c40d6925ea5afb57c13fe7ec4d`  
		Last Modified: Sat, 16 Nov 2024 00:48:04 GMT  
		Size: 82.1 MB (82081094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9284bc198f4389464bd56cb6d482e610bed06e38a1f33cdf743a7b8c6eec3206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c89dcfaac31d02adf56bf29fc7b3a1fe32991735372ea9fc6c14123d2ad0839`

```dockerfile
```

-	Layers:
	-	`sha256:2616517e0787c3cf790cc9d35915ae10764f2b2c996cf06e88ec05c34a14490e`  
		Last Modified: Sat, 16 Nov 2024 00:48:03 GMT  
		Size: 5.2 MB (5184529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8021852e2ed1170d5668781222e7d3f9006ca2c8b4e3e21ee8c8756539cb88f9`  
		Last Modified: Sat, 16 Nov 2024 00:48:02 GMT  
		Size: 8.8 KB (8756 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:74c38e524208f928d00195618c8820fe49535c9692316d6f02880e2f81285bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132929047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fae58e415b0c6a083a69a7dd236384fff017e25e405f8dcd590b1d341057a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:aa4cd91a180503f7c5ac34b85fdd22c27356599a1d700f978c6d2fa5858867fd`  
		Last Modified: Fri, 15 Nov 2024 02:20:08 GMT  
		Size: 51.5 MB (51456561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5934d87b93f6eaa8a3393d80d71dffdb6a6645788c20e13ae85cec457ed6c0`  
		Last Modified: Sat, 16 Nov 2024 01:00:16 GMT  
		Size: 81.5 MB (81472486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b426262e24cd7866e6955fd8c1589d1a0c455fc08b47e946464d9a291b863d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b7706c16d2ac4ebad0d55d3968ab143c606726495c6d8fed369002d072f4d1`

```dockerfile
```

-	Layers:
	-	`sha256:c779f5cb6150f536638db49472753d84cb652ce31a130775f655c81e9f0b0ea6`  
		Last Modified: Sat, 16 Nov 2024 01:00:14 GMT  
		Size: 5.2 MB (5183315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a209eb78c472320ab2aa2c82a166c8232dc9e0593f6f8fb7c7b90e81160539a`  
		Last Modified: Sat, 16 Nov 2024 01:00:13 GMT  
		Size: 8.8 KB (8836 bytes)  
		MIME: application/vnd.in-toto+json
