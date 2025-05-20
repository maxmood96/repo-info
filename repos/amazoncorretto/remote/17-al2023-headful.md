## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b79637337d9ea996699b099f1d996dbb7db5f076123215ed70747fcd25adc7e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1251c75aca68cc177af2853b6bb4ba40082e5f9bc28e58806f9dfe919553d2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136500980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42daf5e2d32f637e74df32bd80452c206a122d46ea2c0a47c79fc6b7bf8c8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b846294c0090f0c0a55e5d76df5d2b1af7c36ea7ce8e1ac6ebc61c9cf1b7832`  
		Last Modified: Mon, 19 May 2025 23:37:08 GMT  
		Size: 82.9 MB (82886278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c2b724e86856d816fe60ffaa3cf253b0175f7c6f394c05705ad9c074bb65f5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e2ec19e62f16a856317a82acbe12a42db9133373b704eddc6dade2e6b1f9a2`

```dockerfile
```

-	Layers:
	-	`sha256:24f7348e0994ce351c96e780b3f9254aad9161aec6ef9163c639a0f40412aa61`  
		Last Modified: Mon, 19 May 2025 23:37:07 GMT  
		Size: 5.2 MB (5205934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da525c4f5659c265c30265d129fa5950d0749db15939dfc09fd1a1b62853f384`  
		Last Modified: Mon, 19 May 2025 23:37:07 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:11527444a0cf8d17fef29d0c71ed2b7fd3dbbe524724bf83558412e159ba8831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134913131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1ecaeb0983c9bc0cf48fc94d94b1fdc45d880c41ed3a0d274733d1b5321a76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78fec3afe334bd2aeb0d30a4cead80423b72b58776a7a0c4a421ff55444c1fa`  
		Last Modified: Mon, 19 May 2025 23:57:09 GMT  
		Size: 82.3 MB (82347394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8b903f1cc6b9b6b974a60f53e80360c00b3d0c1ae1cccc2a9ea6c0b2e980ea12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d5168abbe6637d74517d2c9d8aef9b76d52c26643fa7e6ba7d8c8c1c1c70b7`

```dockerfile
```

-	Layers:
	-	`sha256:ea4097b78880f4cf63c2a9521af616fc8f686a04612edfb5d8a3e8994fed5793`  
		Last Modified: Mon, 19 May 2025 23:57:07 GMT  
		Size: 5.2 MB (5204725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01677917c9c39b8ec90b241b6c52a98b364942b5f3329f36414ed8c47c4c0c57`  
		Last Modified: Mon, 19 May 2025 23:57:06 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
