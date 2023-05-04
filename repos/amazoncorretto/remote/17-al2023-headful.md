## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:daa48795565484381eefee201f9b8abd3eb3cb4ab3d8597893956baa66a1d5e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b9603e658fe5b9c003c46ae3fd7c4fa209a036531ce9654c0f9a9241f2448e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135229110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3868d64796d98a9f2f3e925ab40853e27de3969e8016cd5cb782bd9c4be81cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 19:19:50 GMT
COPY dir:54e5777658be1a3cce5e4a60768f16ebadb522eb8101c0ae54ee1f769c3b164e in / 
# Thu, 04 May 2023 19:19:51 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:41:07 GMT
ARG version=17.0.7.7-1
# Thu, 04 May 2023 19:41:07 GMT
ARG package_version=1
# Thu, 04 May 2023 19:42:01 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 May 2023 19:42:01 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:42:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c863b89e86f3f74e3b816088bacc4f7e984643e02457c9de2f2a80f6f92b9c34`  
		Last Modified: Thu, 04 May 2023 03:04:23 GMT  
		Size: 52.3 MB (52264363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee97706a769814ee1beecdc048f48b486f6e0807b6c432bdaec55e046d552428`  
		Last Modified: Thu, 04 May 2023 19:47:35 GMT  
		Size: 83.0 MB (82964747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e6716fac1cbf66ae92180bcc094c16c7f095557515597cf5cf7064c1346779f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133603403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7675c1082a95c29e3aafdb867011d8a9130141f9a0290bf5e7f054f6af191c01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:39:52 GMT
COPY dir:0b162ee66bcb569c55f662aaca3ee7fff9bf5a498748208a280de7797569e5dc in / 
# Tue, 28 Mar 2023 18:39:53 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 17:43:09 GMT
ARG version=17.0.7.7-1
# Thu, 20 Apr 2023 17:43:09 GMT
ARG package_version=1
# Thu, 20 Apr 2023 17:44:01 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Apr 2023 17:44:02 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:44:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3a410071be52fec7335cb666804896319a1ac81ef15af4c0f1302ffe8834b63f`  
		Last Modified: Fri, 24 Mar 2023 03:10:43 GMT  
		Size: 51.3 MB (51297211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92371ff3ab7f2316940e2a3c16644ab2e3640e1389f37419a761bf4fd05e5385`  
		Last Modified: Thu, 20 Apr 2023 17:54:13 GMT  
		Size: 82.3 MB (82306192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
