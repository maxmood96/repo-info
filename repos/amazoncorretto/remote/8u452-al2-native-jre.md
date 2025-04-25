## `amazoncorretto:8u452-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:a76411271b77cf53691743cf784c090fb7ee52f76a2f1a92a429de26103a5408
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u452-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:453b88a26597eda6b44cc448f9881c41f026ebde1eea2e99be8312b36ebd7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171877893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13151d8bfdaa10eeba83d018ce67cfce2b35f89063070d08a03e5ae6e38652bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8431a700718d39b9a71d46bc346a608e1d04fabed545f3f72950eb19345c4cb6`  
		Last Modified: Thu, 24 Apr 2025 20:08:15 GMT  
		Size: 109.1 MB (109116171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3026531a54b6fc5bf3ab0fa4f547e2664258fef0b972403ff262b4701de458ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbbd8fa300e920d341c6c253b90756d1cd92bee8698a4fd9916c5c20aca37f7`

```dockerfile
```

-	Layers:
	-	`sha256:2d7a48122f71b9336850e0ebde4b1b9e812519d44e7e3bba3b11edd948acbf28`  
		Last Modified: Thu, 24 Apr 2025 20:08:13 GMT  
		Size: 7.5 MB (7485341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a602bd37b018f2e6e7b1df88c9bce8c84d71f6bb6f7f3f5cb817862823f5d453`  
		Last Modified: Thu, 24 Apr 2025 20:08:13 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u452-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:437584a93e385d6a97bf9940b0237bba6134b1865ce101f399d133ab41d80777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117520627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ce38bc11b9fcbf086cbb7b3fd47d55a54243079da8194e08637136f84f2a98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:928bddcbf112315a029f894cf829df2ae1b28c89ecaa6c142e3d47e62c803337`  
		Last Modified: Mon, 21 Apr 2025 21:48:49 GMT  
		Size: 64.6 MB (64582610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d16a4bfed11eceff698d4341254a84d9db05ad5bd8732da7f3016c018ef4dd`  
		Last Modified: Thu, 24 Apr 2025 21:09:21 GMT  
		Size: 52.9 MB (52938017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5338d6b0cc0f611b55dfdf430940851352cce3a5940ddce20c982c2ce012965d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58820f230c53546c909df867eefd7d7cf248e24175560b068dc4d60a0868375f`

```dockerfile
```

-	Layers:
	-	`sha256:7a1457f6de85642e2f796e9fa3d1110a68080353c24c7588ad54a0bb73c17390`  
		Last Modified: Thu, 24 Apr 2025 21:09:20 GMT  
		Size: 5.6 MB (5604718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6adcb55253c2223b5ed666e87de4e29cf7937b7d3a13f977e1f9536f9d9988c3`  
		Last Modified: Thu, 24 Apr 2025 21:09:19 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
