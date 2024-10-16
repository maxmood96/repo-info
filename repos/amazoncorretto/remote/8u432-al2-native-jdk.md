## `amazoncorretto:8u432-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:b3a974b929d9921dcedf5490c6fe2a995061b09a7123de87c832e35e4b237a26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:01273a311ae1647cba599b8e653dbad4b0668d80c0b3b0ee14b72a39a234c67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187918471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8bfdf735b86282ae651ac3d30efdec67e52402ddfe17a5b66ceaf72f73bb4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:55 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d52c9e09e06f955a2712873a0f220356a05e70edf7395840c68b262f18b6723`  
		Last Modified: Wed, 16 Oct 2024 17:56:43 GMT  
		Size: 125.2 MB (125240315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40dce1579617bd21484ccc4259fe57738774cc8a55ed3a9f945b947ea9e726d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82c2fd999af85b7c7f7bffb3c93e54f787c943a190e57c536edfe66287787e5`

```dockerfile
```

-	Layers:
	-	`sha256:410ca970b7c6624b235a980e427a3fb4a3c4a6d6853a6e297eaed47bc4bd9832`  
		Last Modified: Wed, 16 Oct 2024 17:56:41 GMT  
		Size: 8.0 MB (7971265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:340dc74edb38da281eb078454524e15fe7fd0685adf7b4675108a82ca9e67656`  
		Last Modified: Wed, 16 Oct 2024 17:56:41 GMT  
		Size: 9.6 KB (9597 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1e843c220628e93b4c858742dd60da0aa7efc77e5ef5d1301e84ee043faf06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132140082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d959341084f24ae9bbbc4d6aa302e69fac71a657ef79d18f1b4091a6435aac7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:59 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4962211d84e5440e61c021e368a311db2e2e6d349a2274eef901af37133d263`  
		Last Modified: Wed, 16 Oct 2024 18:06:47 GMT  
		Size: 67.5 MB (67547423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:76730becd845a870aa05300963c456f52eb669bb298b0b5a5a6c890e001661dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ba4430f5f67dd89dc35d71cd9d7b8e8977354ff39a6d7b20040a9e5fa7c4a9`

```dockerfile
```

-	Layers:
	-	`sha256:8084f6613f0ab6eec54a81eb834446a88f1127fdeff162fd6e83a63b1d3998b0`  
		Last Modified: Wed, 16 Oct 2024 18:06:46 GMT  
		Size: 6.1 MB (6077770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017f6e69b8eb0935337347c8892d5e50a64af86dcf03ba3457005f1059599bbe`  
		Last Modified: Wed, 16 Oct 2024 18:06:45 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.in-toto+json
