## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b7dc1bbb58bb18c5c77f121bde22e1e07920b9eca06efe2de7b5ed81552f60d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:95b9b8929e2c84b176990dfd4af1b54dd9f039b39ad437b01cd51e39734566a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135263884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329c8b19aa74fe257cd0646ca375c8dbf9dc12567a6c103dddde8942a1a75232`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0191a6a346e02d9d0f4f978361997c87e160ff59c6c5a4ab9d9debf39aa546`  
		Last Modified: Mon, 10 Feb 2025 20:08:34 GMT  
		Size: 82.1 MB (82113301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3d1d2ad567b529cf5b94b74dbf367fd0e5b46aee7fbabaaabad18d31508d5afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e25bdd92637833dc1f2e3547a9f7a8b1a05ab8c46e64ed6d9d516cab1598b0`

```dockerfile
```

-	Layers:
	-	`sha256:4125d1768e6f7b637bf65d919a5fdbdaa7a7710df32a04122035cc7de6e4a195`  
		Last Modified: Mon, 10 Feb 2025 20:08:33 GMT  
		Size: 5.2 MB (5159712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0920855818716abb0055f603bd72c50a910abd23476320590266e37132d4aba`  
		Last Modified: Mon, 10 Feb 2025 20:08:33 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d4ddac51f13af63c7696ee108c47e1feb735f0efb4870b17be3fe28409e978f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133822547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02da25d749151c3f12aa192b5c8e15bc8cfc8299e19e089761432a0a9ad759c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9401aa851ae176cb396b61d9ba3db43844a1ce1ea62cedfd683a8fec299fb0c4`  
		Last Modified: Mon, 10 Feb 2025 20:21:52 GMT  
		Size: 81.6 MB (81551596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6239096e5ff86879b48ee57a7c4104a483ac6e84fb2300f1bd8bd76e4b533a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f08d4472d7990127358831c055cf49519b9eb1b00db609f183c9a7af0888af3`

```dockerfile
```

-	Layers:
	-	`sha256:58a0c892c98ea9dc53d87607772cbbaa304a63404cb07a0859539cef2d19c665`  
		Last Modified: Mon, 10 Feb 2025 20:21:50 GMT  
		Size: 5.2 MB (5158500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f106ecb24a9f0116cb9fe85c9a3ae0896e76f428b3287eba8fd78f71a8eba6a8`  
		Last Modified: Mon, 10 Feb 2025 20:21:49 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
