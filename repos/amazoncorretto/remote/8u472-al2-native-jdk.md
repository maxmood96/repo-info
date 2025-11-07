## `amazoncorretto:8u472-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:da66d665298739496bc078010761f2239d3996185c81ea43da5ef11146985235
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e4ad080b9275cc7587cedb28d30108b274bf05c0c6d170227a60d2044a450d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188174846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60afda7cd42f73256567beb08a3ba6d69fa1470f71aa1b99f4c66d74a38f3831`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:10:54 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:10:54 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:10:54 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:10:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cf84ccec6d2c8ae58c8817c070e0883d58789046db9c2458aea73e8e29c41`  
		Last Modified: Fri, 07 Nov 2025 08:50:45 GMT  
		Size: 125.2 MB (125240712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4cfaddef9fded0515eb1b9563b45ca7dbdf3da5e29a3467ae5edbcc0c0ee488c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e46861a8cb4c06874b2811ddd68a17f381ba78b277981a1b0de1a494e5c93b0`

```dockerfile
```

-	Layers:
	-	`sha256:6e62a54dc1eb7365c43de8bade6bd8838577739b6127e6a4e538274ade2d13af`  
		Last Modified: Fri, 07 Nov 2025 01:52:07 GMT  
		Size: 8.0 MB (7977414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c45a8f6b121b6b7e834d2691ac0ba957d708975e2ac58800924674b7b4905bd7`  
		Last Modified: Fri, 07 Nov 2025 01:52:08 GMT  
		Size: 9.5 KB (9549 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ba3ac4433ae80ed4c6ab990407c37152e34d6b9b50f2807ddc9a84696b651cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132358036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81f317efd18cc4449ff4e9b5324cee5b40506d8b83be5038a0fcc4774634f53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:13 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:13:13 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:13:13 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f9b7ed4aa7e4fe4260bc92a3a1aa32383c31cf0b0a08301a2c1e40f73841f`  
		Last Modified: Thu, 06 Nov 2025 22:14:04 GMT  
		Size: 67.6 MB (67564740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13c37bd468c99986dd5d0565160db99b4866b1c3a003ad1b0b8b30679bf29a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb09db8a32ef579bcd8e6c98b5246ccba1893e3b5e2c239f2288a2b32ece934c`

```dockerfile
```

-	Layers:
	-	`sha256:7b66f8a4fb883cf7ee89bee2f4465c1d4bbe530c1a75200b46006b45bbbafd29`  
		Last Modified: Fri, 07 Nov 2025 01:52:15 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b87945855069d4a01d38f0107e946a14e7698fb27403c71b39319b2bc865ef9`  
		Last Modified: Fri, 07 Nov 2025 01:52:15 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
