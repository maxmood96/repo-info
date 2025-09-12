## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:d15a94dd1d7efae33f181b2026f973549df506a359fdd7166766bc3d67745fa7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:07e88b4bc2e8d2118657b05950292efbae4d426d71a6c5acbe0d023fab0dbf97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156312876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb644c03d03eec689df83c28f3e5e3839f54b705299951b81de1bc2e72c3511f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e12b0751ac24c38f5ccfcd237f4df8132fea81a8b69f767e65bdf4c51d37f5`  
		Last Modified: Fri, 12 Sep 2025 04:09:14 GMT  
		Size: 102.4 MB (102437170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9d1d81561331717e5d3318efd1607f2281cdc63def6336be5f183ccf0095760c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d6fd89a983d566e571cf55c1673b10cb567514e0a8d4439519f09b83430e4f`

```dockerfile
```

-	Layers:
	-	`sha256:b5cc3c0efd3b395698e38b4e45614ee7ec0884fe1408a2f25b8e1d08adf6ae90`  
		Last Modified: Fri, 12 Sep 2025 03:51:05 GMT  
		Size: 5.2 MB (5194701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e30ba367ef5e0564250038dc622a73154f214a6bf78abf29d976fb886b0c4533`  
		Last Modified: Fri, 12 Sep 2025 03:51:06 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:809f8a5b791ffa0311f3a3542993a4d5deb3473a21be4743fb78698bc6713cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154227746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f647a122341e8ef46efc1759992d444738a8851f56bd5d3c0c693c90cc1e73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ce55a7fe93fd119e2925095c51501d3efef800bb7157ddde9fcdda13eaf281`  
		Last Modified: Fri, 12 Sep 2025 05:40:34 GMT  
		Size: 101.5 MB (101452635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a6e69a45ea909fe4d8914c5da95eefe3b190cf5061787beae573953f9e9ab562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c2355a9aaa0f5a774880915adb26143aee053e506fd5826a50ca6b59fa243f`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a43a7100da615139784416bac6d2178d928762dcee9b2c9bedd9f20d12c36`  
		Last Modified: Fri, 12 Sep 2025 03:51:10 GMT  
		Size: 5.2 MB (5193512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5934cb24be835f04220ea51f5a7ed7519087dde4c2d3b8fc8a26bf944522a5d4`  
		Last Modified: Fri, 12 Sep 2025 03:51:11 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
