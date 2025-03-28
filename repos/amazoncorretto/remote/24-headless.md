## `amazoncorretto:24-headless`

```console
$ docker pull amazoncorretto@sha256:140cfed00078217f01b68105d8a8c6a90c373eb4ff5f8cf099f54722f2c89d9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:00be59c41245fcab1b8fa350d0167f9946635eb4454c0d76fe042f4b2041a4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155390206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e66ddcc8d93a8096b99d3edb19c85a7ce27add13357756cf8f0e5c961de4d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c637df27d7b7848f13f201f44964d1dff6943dc050fb44817ce646a0978bde`  
		Last Modified: Thu, 27 Mar 2025 23:58:50 GMT  
		Size: 102.3 MB (102266917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:370ba8bc15e1c6c51a2b1f17c6695912e1bec8c1503bc2e4d83bc94096ddf1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5180663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d5ecb9ea7d7119a8ff2032b7c728e3458f8b306efbe569a07815ec3698209f`

```dockerfile
```

-	Layers:
	-	`sha256:5c041df130931b5a2455a9ffa79ad22892aeeaa6c9b252e3de5494e4de7ea3ba`  
		Last Modified: Thu, 27 Mar 2025 23:58:49 GMT  
		Size: 5.2 MB (5171589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b45a7c5c70b3425bf70e66632ad4d2f561bece5a629af1df497acee5a94f3b`  
		Last Modified: Thu, 27 Mar 2025 23:58:48 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c1447c313e7c67148783b472903e383ed22d4f8fd6e0ac5cc05b4bec99f4c469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153511949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f91888b085f15b1df9686d1b4b83f492fc3e8212c0c4b325aa3039ddbc2e99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Mar 2025 18:35:42 GMT
COPY /rootfs/ / # buildkit
# Fri, 07 Mar 2025 18:35:42 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8491ca965b68d39b6dc49f0a0e34bfc83346de889ce4d67a9d6f1621f0a2fa`  
		Last Modified: Mon, 24 Mar 2025 17:34:26 GMT  
		Size: 101.3 MB (101265971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:096e39619bbd1c65f5733c5a83e697f763a568c97223edd804d2ed9e877b3b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de27bd4122fb020cf49b4abb0890fa7a6fed4e816a443ba98b16abda0471e0a`

```dockerfile
```

-	Layers:
	-	`sha256:0246f345e35878d48111d0479af570b9213b6afd619fbdc1cf28d9647c43237b`  
		Last Modified: Mon, 24 Mar 2025 17:34:23 GMT  
		Size: 5.2 MB (5170400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c82b1ab828b03f681b30ce3ec66c55f65e757287509d0d6be373ff3af51f415`  
		Last Modified: Mon, 24 Mar 2025 17:34:22 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
