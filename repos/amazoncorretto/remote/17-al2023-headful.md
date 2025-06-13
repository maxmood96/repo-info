## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:0702119fcdf6b0bc5f5166a3b53a089922a5f0dc1bcf5bde397f971704739c27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b4910bdb0881fc3386fe7c80097a969634e288496c59b038c665e86e0b392324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136468590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df947fc33126c33d4371d547c3105da267d98191ac37f58ec5565078f5e73617`
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
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b8edd8b21439eebdaed3fba89ca1edc7c6163fd46ca0dfd0578504026c25ca`  
		Last Modified: Fri, 13 Jun 2025 17:04:07 GMT  
		Size: 82.9 MB (82898230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a788f3f4c81f6b72c165415bd1afa244e537cbc84883afc9e131f448b9e8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d450bed0208a29613420fd2cf855057a56b570533a65ad10d3979929ef12ea3c`

```dockerfile
```

-	Layers:
	-	`sha256:75c9cdecb83c4fa422756de80cd4a8a6bb5f262bea656afe2eac9e8f80ac29c4`  
		Last Modified: Fri, 13 Jun 2025 18:48:20 GMT  
		Size: 5.2 MB (5208948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667313b737966443d9a45b717692e147a8a3a2da3fabd35eeacbf4e600bb3a57`  
		Last Modified: Fri, 13 Jun 2025 18:48:21 GMT  
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
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78fec3afe334bd2aeb0d30a4cead80423b72b58776a7a0c4a421ff55444c1fa`  
		Last Modified: Mon, 19 May 2025 23:57:43 GMT  
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
		Last Modified: Tue, 20 May 2025 00:48:50 GMT  
		Size: 5.2 MB (5204725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01677917c9c39b8ec90b241b6c52a98b364942b5f3329f36414ed8c47c4c0c57`  
		Last Modified: Tue, 20 May 2025 00:48:50 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
