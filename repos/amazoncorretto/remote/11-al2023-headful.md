## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c6838e6ac3c7c2dafa4f0d17d0eb2e719b62bfb9445adfbda095ba43e2b43578
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d9388799eb9010e78661df8c9d1692da5667e2124354770d579bc2c0daa68996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130663923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395a92ac7285f853c5db594618934bbd2728f1a41435c45c1bc89ddc59353f00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:59 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:15:59 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:15:59 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0777a40c5b6d65449ea01e3fc5a1bfab3c95fc950cae3ad237358be9af2446`  
		Last Modified: Fri, 14 Nov 2025 02:16:31 GMT  
		Size: 76.7 MB (76687208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75b3533c29eac190cbd247842108583999746d19ec0933d3102a4eb022761fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a61d9a78b9a5010862cbc1c8a9e0969c34f41767ce886f35ac98bac58ad34`

```dockerfile
```

-	Layers:
	-	`sha256:edde5a432cd9c9603b492e5b76bf2d6dbf741549daafe20914b026aa3ca99d73`  
		Last Modified: Fri, 14 Nov 2025 04:47:52 GMT  
		Size: 5.2 MB (5222244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8afe580b974ba68fcc69773d891f4e66b334127fe7fafbe05511989c9e647dd7`  
		Last Modified: Fri, 14 Nov 2025 04:47:53 GMT  
		Size: 8.7 KB (8745 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5e8f88c277ebfe4e937d47c645b16612df68bbaa705245092a80be1cd88713d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128801426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b939b1f259c416dc89f9fb887504bada0bad417030db2bfc1a598e715bfd287c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:25 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:25 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:16:25 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63604ccdab651a3fa59279685253d6b5b2949073fbf0f2d52a03c07a8ba282f5`  
		Last Modified: Fri, 14 Nov 2025 02:17:07 GMT  
		Size: 75.9 MB (75924770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:12a2138bb0da120fa8992ee1de2a67b4d047fe57dd44c435d1cb7a085db07211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b082f815c7edcdeda481a9f26fff62b2e806a8d2b3ee621c7c15893bc1df046`

```dockerfile
```

-	Layers:
	-	`sha256:1489df03cdef6b5550ef2966acbf51a535ca5852020f889f074c2f19e1d7f456`  
		Last Modified: Fri, 14 Nov 2025 04:48:01 GMT  
		Size: 5.2 MB (5221865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43b4ff382adf1f9365fdde7e5bc51f6282b104fdcef44f4b8ae5d88a02de2850`  
		Last Modified: Fri, 14 Nov 2025 04:48:02 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json
