## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:8fb2c9675911fca659c06d693b6a7d430bd2aad15c73b91fe75878b5e2f3b678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3cc97b7b7bfa8c969c41643eeedf33cfd16a0aa022758aac165d6e5fa950ce55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135260059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596262d80b123d91abf649c64680f03491af52a5e3fc6a6e6bdfe5ec4a55bd04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:41:37 GMT
COPY dir:8f7245a97c061726fd1f5e8ec557a254660d588f51008b0475bdcdcce3a48bba in / 
# Sat, 20 Jan 2024 03:41:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 03:47:47 GMT
ARG version=17.0.10.7-1
# Sat, 20 Jan 2024 03:47:47 GMT
ARG package_version=1
# Sat, 20 Jan 2024 03:48:52 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 03:48:53 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 03:48:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:cd4602cb0e84e00e8b7d38510ab92c4d091288133108bb74e581c22d31377e8b`  
		Last Modified: Fri, 19 Jan 2024 19:08:42 GMT  
		Size: 52.2 MB (52244936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc222dcaabe39c6f1dc6463ef11fdb7b09f45ba66afc27c5f4613e9bd3416f44`  
		Last Modified: Sat, 20 Jan 2024 03:58:49 GMT  
		Size: 83.0 MB (83015123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c07a38fc4f81f9315a0dee7535e0b6229c3e09c0ce5104f723c58edd9d2dd463
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133672328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97cd937c7e97fc246b706c9a1d98f6a3e4ba15bdd60c9c4cefd3d7b812dc79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:48:00 GMT
COPY dir:bf3fca734fa6b784c9516c9f20cd0ad6226e1fba4faa2ef00cc5ba4e2d3631a7 in / 
# Sat, 20 Jan 2024 03:48:02 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 04:29:23 GMT
ARG version=17.0.10.7-1
# Sat, 20 Jan 2024 04:29:23 GMT
ARG package_version=1
# Sat, 20 Jan 2024 04:30:17 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 04:30:18 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 04:30:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2cc150e431896856b2c36c9075baaf386855a496fe588adc23ed44af495843dc`  
		Last Modified: Fri, 19 Jan 2024 19:08:39 GMT  
		Size: 51.3 MB (51309289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ef9fbfa2c0531be8b6aa6598b768be889c4207c2e97b7b8051dd6eced1a98b`  
		Last Modified: Sat, 20 Jan 2024 04:35:05 GMT  
		Size: 82.4 MB (82363039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
