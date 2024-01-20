## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:973970fd1c55acf3607b723b0a7cfc7e3eb19a9e3d126046b2f87550ae8ee2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cc1637584a511897339eaf56a85c43c0b54d7aa0778891d486a4918c0d6c1727
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128307020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fd0a94f411e3b49b02b9e68666a22fe75df40df4d61895ec263b2cd4fd5957`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:41:37 GMT
COPY dir:8f7245a97c061726fd1f5e8ec557a254660d588f51008b0475bdcdcce3a48bba in / 
# Sat, 20 Jan 2024 03:41:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 03:46:24 GMT
ARG version=11.0.22.7-1
# Sat, 20 Jan 2024 03:47:04 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 03:47:04 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 03:47:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:cd4602cb0e84e00e8b7d38510ab92c4d091288133108bb74e581c22d31377e8b`  
		Last Modified: Fri, 19 Jan 2024 19:08:42 GMT  
		Size: 52.2 MB (52244936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231a9988cc2732c5ad65556723786677bbc55aad0632acca269f3cd326c8bbd0`  
		Last Modified: Sat, 20 Jan 2024 03:57:20 GMT  
		Size: 76.1 MB (76062084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4da9dafa1d194d1c92c46ae5a06fc33ace3953577b4d63cb0951bca8231cabe3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126542373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddd89422b1dd99d6c374bf82855f674665c8c467b51c480531bd83c6d9e550f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:48:00 GMT
COPY dir:bf3fca734fa6b784c9516c9f20cd0ad6226e1fba4faa2ef00cc5ba4e2d3631a7 in / 
# Sat, 20 Jan 2024 03:48:02 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 04:28:16 GMT
ARG version=11.0.22.7-1
# Sat, 20 Jan 2024 04:28:53 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 04:28:54 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 04:28:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2cc150e431896856b2c36c9075baaf386855a496fe588adc23ed44af495843dc`  
		Last Modified: Fri, 19 Jan 2024 19:08:39 GMT  
		Size: 51.3 MB (51309289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78e0edea27f7f91fb1211221a67c2f4f2278858d47078c5c5576c7a995f5d18`  
		Last Modified: Sat, 20 Jan 2024 04:33:47 GMT  
		Size: 75.2 MB (75233084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
