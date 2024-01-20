## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:657f0b3edddbf1455f0b58584d3a634e4be0fe6a44b6d6dd775b81b101e44aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3a8a9203a5e6b798e1d44411e411f99ae5aa4799e8830a37440630afff08b42e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142463036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c34bc5f7ad05761179653bfd26c435499e31e221267cd8b4eaa84760793cc4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:41:37 GMT
COPY dir:8f7245a97c061726fd1f5e8ec557a254660d588f51008b0475bdcdcce3a48bba in / 
# Sat, 20 Jan 2024 03:41:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 03:49:17 GMT
ARG version=21.0.2.13-1
# Sat, 20 Jan 2024 03:49:17 GMT
ARG package_version=1
# Sat, 20 Jan 2024 03:50:23 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 03:50:24 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 03:50:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:cd4602cb0e84e00e8b7d38510ab92c4d091288133108bb74e581c22d31377e8b`  
		Last Modified: Fri, 19 Jan 2024 19:08:42 GMT  
		Size: 52.2 MB (52244936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0445fc0cffab561e76b19fe526463cc534a50d2cabebc3b7ba14ef9bf10e58a6`  
		Last Modified: Sat, 20 Jan 2024 04:00:01 GMT  
		Size: 90.2 MB (90218100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4243caae1961b07e05bd7996734ee9105d84291f067601644e69b10430281c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140611236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8e7c41214dcfd654fdd76bde67ce8d4e988196c840aa748c1e690011eab743`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:48:00 GMT
COPY dir:bf3fca734fa6b784c9516c9f20cd0ad6226e1fba4faa2ef00cc5ba4e2d3631a7 in / 
# Sat, 20 Jan 2024 03:48:02 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 04:30:34 GMT
ARG version=21.0.2.13-1
# Sat, 20 Jan 2024 04:30:34 GMT
ARG package_version=1
# Sat, 20 Jan 2024 04:31:31 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 04:31:32 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 04:31:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2cc150e431896856b2c36c9075baaf386855a496fe588adc23ed44af495843dc`  
		Last Modified: Fri, 19 Jan 2024 19:08:39 GMT  
		Size: 51.3 MB (51309289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ab80a0709dbc546c65516ec084cdcc9052bc76a80ebb0496d45a5c9d74ae60`  
		Last Modified: Sat, 20 Jan 2024 04:36:11 GMT  
		Size: 89.3 MB (89301947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
