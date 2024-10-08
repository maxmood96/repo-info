## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:43ab15448a80c34d7c3f0e581e4cd05d16fd5d310c613e577ed0c71f24414267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:939419dc98d0af1265cf562908f8880aea1c0812723f7f4fdc1e8b919b8cb554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154110039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f081f2bd2baf56fc112bd1f60bb78fdba7a9fa2d6f610f360a1c56191ec1742b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23d32fb2cd03da7e66758560ce5befd775a62981ade212285ac6e03e9ae22f8`  
		Last Modified: Tue, 08 Oct 2024 00:00:18 GMT  
		Size: 91.4 MB (91431883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fe9c2c4cc3c2e6954ccf7d85586f3e0891d84d91f33f44b5323bc733c2faaa92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5979ac9c8d10789be71662ecb4ceee65797e78e65d14811cfc8e27fd040485`

```dockerfile
```

-	Layers:
	-	`sha256:1f804a6225303164c512484d54cb1daf5174367d186f770683d82bcf567e7b5a`  
		Last Modified: Tue, 08 Oct 2024 00:00:12 GMT  
		Size: 5.9 MB (5860088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f0f05fb85f0a9e95786b64f887d6c93e5531bdb45ca5e5a6912c8b0f4d26d8`  
		Last Modified: Tue, 08 Oct 2024 00:00:12 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1c2e650c39255f2540d5570b32d4cbcd0af8f7ff1943f7daf7dbbcc6b24b2a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146793037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c0122d26e5400f4ae525d2348be28aff398e79f29cfde553dacdec71560b27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d0127da3c432875fb6ad73ec64f4cc24f1e7e698a28cfb7ea2bc506ebb7534`  
		Last Modified: Tue, 08 Oct 2024 02:08:39 GMT  
		Size: 82.2 MB (82200378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3debae84a3b6347a68c7cd6872efc592539147ac78c5ce5e771d323f81281452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f2c57cd2f082b5d323cd969c25602593918fad51f9b7d40ecc1733bed4c42`

```dockerfile
```

-	Layers:
	-	`sha256:a9c4f0bc2f0cab3526c34e4cc6b0b73461a3b4a30e5070e30b258de3b2e728c7`  
		Last Modified: Tue, 08 Oct 2024 02:08:37 GMT  
		Size: 5.7 MB (5651490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0180d34cb8768f37a210a87f96db36628dfdba41a07334ec0d914c509532fe92`  
		Last Modified: Tue, 08 Oct 2024 02:08:37 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.in-toto+json
