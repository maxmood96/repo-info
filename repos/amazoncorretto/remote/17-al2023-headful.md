## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:668f36f37bdd1d007511b730642e5a2dcdce6fcb124e07069e76bcb24cafd8dd
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
$ docker pull amazoncorretto@sha256:5db3a3c93d36e66ecf48eb3a5247b1cfd39e8cc555c24a6eb305e67f618a0359
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133615754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c677f1ab817a0d8dd0fb3cb92ff5286d1b3002f0b404b526f77f069bced7d83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 20:02:38 GMT
COPY dir:c3490ddfaf576048c53c1266c10c570c0c31d1ef25f639153f91097415fe319b in / 
# Thu, 04 May 2023 20:02:39 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 21:18:06 GMT
ARG version=17.0.7.7-1
# Thu, 04 May 2023 21:18:06 GMT
ARG package_version=1
# Thu, 04 May 2023 21:18:53 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 May 2023 21:18:54 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 21:18:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2356aaf73de639cb8d40c53e05e60b5aa503113b2f9cf79ee0c5fdf574f1a50f`  
		Last Modified: Thu, 04 May 2023 03:06:59 GMT  
		Size: 51.3 MB (51303115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db462165a08170c52261ccd5d8058c61e21cd3fc295c73dd2a60a4fade89529b`  
		Last Modified: Thu, 04 May 2023 21:23:33 GMT  
		Size: 82.3 MB (82312639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
