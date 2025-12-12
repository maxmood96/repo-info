## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f98cb84d8250f23640be11538c55baa32ef4ea8043f023ea37f43c9a1c6214ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e47619e5bc5ae35716a91f1011d8b08d9dc2c94d290d7efa6b6ac4ddd2f3bdfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129967768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74382f40d09e236fa6da9d5e6263dfe715a418a88fd289a70a5336a4745a2db0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:43 GMT
ARG version=11.0.29.7-1
# Thu, 11 Dec 2025 22:11:43 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:43 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e83914fae3dc6edb16fcbbdef2219027971b2f1e595673d6df107ce690c940`  
		Last Modified: Thu, 11 Dec 2025 22:12:17 GMT  
		Size: 76.0 MB (75979308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a5adbc9becef1f92cb80cc0a9d9cf9411a51694dcdc05c2821986832b1785936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0d81fd63cdaa3e3c3c072b0cc7bf92f904194daf99da6cb703be67cddf74e3`

```dockerfile
```

-	Layers:
	-	`sha256:347a94c0b800c6bfba1f7c866eae2be0b8c745984c1a15be18eb602ed1f17fd1`  
		Last Modified: Thu, 11 Dec 2025 22:47:58 GMT  
		Size: 5.2 MB (5196819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a4d630d77d1b205c0ab5ebb4644fbb3cf57c800b10f0ed7ccd99e0488cedaf`  
		Last Modified: Thu, 11 Dec 2025 22:47:59 GMT  
		Size: 8.6 KB (8609 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b88fbd538a9776c0d35909cab937e0c7b28b15cb15ddb9e412477f1e9614927c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128080947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffc44fcd7a8d4ba16395035e9d33ebdf3741d10ab028e496bdd2de80c78391a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:52 GMT
ARG version=11.0.29.7-1
# Thu, 11 Dec 2025 22:11:52 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:52 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28a82c4d5fba8a563ba03fe9b01e4bdf7adcde6e062a3cbe7ca62b0f3d2b77e`  
		Last Modified: Thu, 11 Dec 2025 22:12:21 GMT  
		Size: 75.2 MB (75207497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db436d1359ab86edf095e13eac7264db0e8c081b12c9bf7935d2cf29681958c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c742ac1ab6b84aa1c105eb8d3b902b842abe5858adb8bcefd21372142d93e907`

```dockerfile
```

-	Layers:
	-	`sha256:746f5b9c49bb0258445500ff8f66a2e905fba5aee81e16092eabaa1b201a89a7`  
		Last Modified: Thu, 11 Dec 2025 22:48:07 GMT  
		Size: 5.2 MB (5196437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7339c2195c22d1810af3039ac5008d016dfef7209fafd0e1dcd7a10a307d5b32`  
		Last Modified: Thu, 11 Dec 2025 22:48:08 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
