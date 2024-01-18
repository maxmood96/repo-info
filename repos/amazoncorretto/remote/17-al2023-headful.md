## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ba3a1bf4bd5188da54b7799ddca73477d5b000d620aa7dedcb01bbd2d6baaab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5b8250bcbd62e314c07971b2b76a281df0a8e4e17250e14ba75537fd71ca788f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135247952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba68ef0a6279c138b5cd41ca015bc1397c97e9b0aba4689d3dbbcc428b074a55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:33 GMT
COPY dir:3d1c4d9e1017e7de559aec6b3779bdf6668d0e4f73f6af00952a84abd805da43 in / 
# Fri, 12 Jan 2024 21:45:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 23:47:18 GMT
ARG version=17.0.10.7-1
# Wed, 17 Jan 2024 23:47:18 GMT
ARG package_version=1
# Wed, 17 Jan 2024 23:48:24 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Jan 2024 23:48:25 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:48:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:592fcbe9ebcec6e31ad10b3d219e4f61ce8e39180e215fab37ae75bc7ac4c0b7`  
		Last Modified: Tue, 09 Jan 2024 00:19:51 GMT  
		Size: 52.2 MB (52238109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1feb109da08f00f63ada847471dd9a73f059efa9894f3ba7a034567dabd4843`  
		Last Modified: Thu, 18 Jan 2024 00:05:27 GMT  
		Size: 83.0 MB (83009843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e6bad1a75074c3c9f9e715e83034fdd4f087b4a192b98a4ab2f6b5e5a294a722
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133662596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79fc1150f4ad44926a83c8597cb4911f8d086493e8f32ec25239e9c0925863a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:07 GMT
COPY dir:80de4926459dcf07edafbe2044439672e4fed6bf5796881b9953e9ffab3571d8 in / 
# Fri, 12 Jan 2024 21:49:08 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 23:42:25 GMT
ARG version=17.0.10.7-1
# Wed, 17 Jan 2024 23:42:25 GMT
ARG package_version=1
# Wed, 17 Jan 2024 23:43:18 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Jan 2024 23:43:19 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:43:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6126164e178e3570337610ef0b171038c4426a730623557513d2ce511166a065`  
		Last Modified: Tue, 09 Jan 2024 02:25:54 GMT  
		Size: 51.3 MB (51303151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fb3a21240d04649166f52ddde5934414bc2ef7945655b1d042e4dfd77d2a7f`  
		Last Modified: Wed, 17 Jan 2024 23:57:51 GMT  
		Size: 82.4 MB (82359445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
