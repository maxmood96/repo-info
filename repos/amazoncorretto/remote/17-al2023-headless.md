## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:7d332677c5289c4fab315f9fd8c8611d48ac91240cb3cfd20e31660e6bc75ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:76263588a3f9960dd053b7d553ee893ba6a71cc850b8dbb75d651ce34379b701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134737120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e0e645af6a35bf03d00ce7dfacd146f7133b03effd1d2f9ab0cf71c1a7ebcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Jul 2024 00:19:47 GMT
COPY dir:1c9e0f4db95e1ae683b8f16b1ecfc5d8693ad4e5e379a2386e2870f38383c7d8 in / 
# Thu, 04 Jul 2024 00:19:47 GMT
CMD ["/bin/bash"]
# Thu, 04 Jul 2024 00:38:36 GMT
ARG version=17.0.11.9-1
# Thu, 04 Jul 2024 00:38:36 GMT
ARG package_version=1
# Thu, 04 Jul 2024 00:39:21 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 Jul 2024 00:39:22 GMT
ENV LANG=C.UTF-8
# Thu, 04 Jul 2024 00:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:860904071dc658e37de73aa1556e7badfb13bef4747965ea3bd1049e8ff87dcd`  
		Last Modified: Thu, 04 Jul 2024 00:20:13 GMT  
		Size: 52.3 MB (52319623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c01db6397b704e0f96733f7afa198e6c4b3351a1c0b5e4607a651edc849b21`  
		Last Modified: Thu, 04 Jul 2024 00:46:35 GMT  
		Size: 82.4 MB (82417497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dc2392fff85af9bd2481a4e54c2cc05482f26c0b03a93f4ab0f31554b680abcd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133146901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca698f45cff36aa363d50dd98ad44a5b5c629a6156ca3b2e5a1a929acc1cf165`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Jul 2024 00:39:25 GMT
COPY dir:a2f5453af1f2210c7b49fadc5acdaaa335139ac35c64847d2f5879056f91a03d in / 
# Thu, 04 Jul 2024 00:39:27 GMT
CMD ["/bin/bash"]
# Thu, 04 Jul 2024 00:57:08 GMT
ARG version=17.0.11.9-1
# Thu, 04 Jul 2024 00:57:08 GMT
ARG package_version=1
# Thu, 04 Jul 2024 00:57:46 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 Jul 2024 00:57:47 GMT
ENV LANG=C.UTF-8
# Thu, 04 Jul 2024 00:57:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f95af119e05065dbdff89fbd219657362e32f7ec50d632e28754e75b5a13806e`  
		Last Modified: Thu, 04 Jul 2024 00:39:44 GMT  
		Size: 51.4 MB (51407040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634ca13d3c2bbbd25902f82af6dc059042c5ce9642c8bb4d4575afe443657f06`  
		Last Modified: Thu, 04 Jul 2024 01:04:08 GMT  
		Size: 81.7 MB (81739861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
