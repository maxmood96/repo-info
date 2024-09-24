## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:0eb08180d6d64ebbd72062701b3800d79f78ee1f0c6d0ef6d96be978c08c4bde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f84d497df94ee796cb613d35d470bcf015d66c5f933846297e16567726875428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141367182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4215738d655aab2aeaa0f6a1629554c71f61e0e1fb32c969a8053fbad6fbac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:50 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4230cc35587acc24f2f6b4dff6641d22b18301b729f74798c9e5e524a174e7`  
		Last Modified: Tue, 24 Sep 2024 01:57:47 GMT  
		Size: 89.0 MB (89042224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8e0ced5670bc873846a50beeb60e6c0cc754f8999f7931f17ec1a4477f38b0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (8996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111003d48920218776245cdf8cc1125dd22344835f79e6ffbed75a12d6d7f710`

```dockerfile
```

-	Layers:
	-	`sha256:01e7e6d1759ee3769e0f47dfafa3e3a58ab71bc41a2de1f98252174e5ea50ad5`  
		Last Modified: Tue, 24 Sep 2024 01:57:45 GMT  
		Size: 9.0 KB (8996 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:db9b66990374e48ae21b0a3a70a7c7f5b8c13d5401b16fbd0c90943c297d1734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139434374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd581bb9d25336d644bed6b4f408c34bb2a4b7223de3dadf6ca8df5175831e45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697d04f623c6880c377f4e1515950278fa3e3e29e0e6f3639ec94a607a52eee1`  
		Last Modified: Tue, 24 Sep 2024 02:48:08 GMT  
		Size: 88.0 MB (88008382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c4b52dce7bb80d5074c095dc93c1df28b99f4f93cab7cbcac3d36cc4afc7eb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2459603f8ba3db97001cc673bc13c32bf5c228232b6122ebf83b1b1f11d72da0`

```dockerfile
```

-	Layers:
	-	`sha256:892e092b9caad208ddb870507e590d6d8301d4bcb073bbb285b09b5ef66ef792`  
		Last Modified: Tue, 24 Sep 2024 02:48:06 GMT  
		Size: 5.2 MB (5210415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b003718227aaeb8180289066920d75333bfcebed1d04d21db395c5c8f84c812`  
		Last Modified: Tue, 24 Sep 2024 02:48:05 GMT  
		Size: 9.6 KB (9588 bytes)  
		MIME: application/vnd.in-toto+json
