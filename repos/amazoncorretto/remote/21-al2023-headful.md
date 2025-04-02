## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:4e759f4a9e262f52fc4a54814b668458390eb77316fa389481592bebdff5020a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5787a726d849694f016272a91c2cb986b77a1bfc8f0b47f01226f73b4098f2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145704186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a9473ae033262c48d31cc8f56611c3b4d50d5d0dd86de1c0af7f573d80c592`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3561851cd5fff0d31668d1a31d0bbe27e0111ea2d887ff988564865e23a8a123`  
		Last Modified: Wed, 02 Apr 2025 00:01:47 GMT  
		Size: 89.8 MB (89797133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:331cb1456f15035c9b1c05a272ef44afc235d8b6b0fb869749cdb417de2ca82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711ac74f2162deedfeec7961edbb1ffb3fb4de4f36583907db7fcdde3b784270`

```dockerfile
```

-	Layers:
	-	`sha256:63a99e39ff71cff5876c7af5da02a00db757c46c2ebea82d8ea7903a8241af39`  
		Last Modified: Wed, 02 Apr 2025 00:01:46 GMT  
		Size: 5.5 MB (5452644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d12f5af6e7759502a56d20ef25b55f36e89f8c6c437774d4a434ebde5c8abc9`  
		Last Modified: Wed, 02 Apr 2025 00:01:45 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8f0b243ef80b6df41d5639c3ee6f8044d21f51308592a5609b5af99d9fbaa548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143897405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3552f14f3358987c690cd3204212e424f53a8be356cf25d3008e02b8b70b97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4675159c23acdb63333fb3bbb9eac6cb0a9233e4a51d087b279aea20244d979`  
		Last Modified: Wed, 02 Apr 2025 00:34:41 GMT  
		Size: 88.9 MB (88936396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de3f4b71d8a24e7c3666a544efa73949b95088ec989c4762ce7046fcc2311473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d7779ee258f510b881d0ab5a8e0384a58fe02853a501cf8c4aeef506dbda7`

```dockerfile
```

-	Layers:
	-	`sha256:618e00ab4f5ce3e379da72176893955753381d204b0835b5496e7000d630bc9e`  
		Last Modified: Wed, 02 Apr 2025 00:34:39 GMT  
		Size: 5.5 MB (5451437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044c49a453d8ba89d70d3700c8fa6979fb63f016d99d9a2ec85943abc95a2c47`  
		Last Modified: Wed, 02 Apr 2025 00:34:38 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
