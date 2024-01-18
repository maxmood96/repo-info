## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f488827d68aa3384d919ba9f616d359c1983c2ae39a72beb6d023971a7fc80a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b71f2ef405bd00a1b9ea2791aa842a8740d8fbb087992a7b395a42e0693d8814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134567163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722b4fd9237fa5f28252beaf266963b232d6ea916c6b81d24c73552f3e406e32`
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
# Wed, 17 Jan 2024 23:48:04 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Jan 2024 23:48:04 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:48:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:592fcbe9ebcec6e31ad10b3d219e4f61ce8e39180e215fab37ae75bc7ac4c0b7`  
		Last Modified: Tue, 09 Jan 2024 00:19:51 GMT  
		Size: 52.2 MB (52238109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3fd0a5c16983e16828824a6f21b54b821ddba40a14a68be074b6fca09ae906`  
		Last Modified: Thu, 18 Jan 2024 00:05:09 GMT  
		Size: 82.3 MB (82329054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:23625697facb9765924b3b0d61699ade0665395fe8d74d9c934d098be82416b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132966369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce780e0b428d1589f9672fc4a5092772be61581507ae803dcfd94c55345782d`
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
# Wed, 17 Jan 2024 23:43:01 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Jan 2024 23:43:02 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:43:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6126164e178e3570337610ef0b171038c4426a730623557513d2ce511166a065`  
		Last Modified: Tue, 09 Jan 2024 02:25:54 GMT  
		Size: 51.3 MB (51303151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de19393a3f2290643230153fd80963c8be8abcab3988aa91c222d91ddffbcbb`  
		Last Modified: Wed, 17 Jan 2024 23:57:34 GMT  
		Size: 81.7 MB (81663218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
