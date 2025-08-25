## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:01bf3326992ad5a136746f72444b871612492d64c4182c1fce922a2d4da6bd2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f4c71d0ad74fed8ec68ee253834b85200961614e79d5c615b1d19234455f33f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156296231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cca33339db97816c12e5bf98366244088e1d0f241cafcd44e08ca1aa16594c`
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
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb06a3d0464fd8eaaf16e694314b4ca4ebc4a2c76b5eb249bda87f0e19e17032`  
		Last Modified: Mon, 25 Aug 2025 20:18:59 GMT  
		Size: 102.4 MB (102427501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2d1bbf0ff33e5b4b006c71c1c8d845eb6aa63678d0529b0353358d5312cf2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c986c4abbdcf619318835259fa8671e07280ff24f8a7690666230cdc94cf32`

```dockerfile
```

-	Layers:
	-	`sha256:f6f851ea0ec16d3dc35bad2537c87437bd075900e9689ac659bf28d91d23a93e`  
		Last Modified: Mon, 25 Aug 2025 21:49:31 GMT  
		Size: 5.2 MB (5194701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e936efb93734908f6d82b0539cf9e1585056e82dfc99e786d4b7ad0c1d9e19d`  
		Last Modified: Mon, 25 Aug 2025 21:49:32 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d2d0156984e17eb80cc8c1da9ddd514facb2353e0526875d560d1c1a1dd2930b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154169447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309097852ed86937f5abe3cb46d62e8f7bab3f33f415976894fb3776d36cff36`
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
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4841fc67883835471701617323ebd995eeaa6e4c9d7cb2fa1b8bf9a2077c49b`  
		Last Modified: Thu, 14 Aug 2025 15:15:50 GMT  
		Size: 101.4 MB (101443053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:734cef3fcccdee16fd84f91ba720b270c19daf8eb7148edbcd578f6d27049801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b7bb5d94d78005c7425cc351ec5b526f26007d82b1ea8ab9e91a7a1c8d7a9c`

```dockerfile
```

-	Layers:
	-	`sha256:7e3740bd3af70345d7edb37b1d364eef31440a5a8143b8737c121db8be7c0563`  
		Last Modified: Thu, 14 Aug 2025 12:48:25 GMT  
		Size: 5.2 MB (5193512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b72b489c309315ea3d2e71c5bef872b318d1e620c58325beaa645ec75d3e7d4f`  
		Last Modified: Thu, 14 Aug 2025 12:48:26 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
