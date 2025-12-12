## `amazoncorretto:8u472-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:f32307aa09eee9777d1df52f01fa4376294a2893d182381ea76faae974da22da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8b7200d59819a7a376bf6a7ff612848cff9cecdd124d1e5f8f3a02d5b5980d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172059346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31a850c957e1cec8387afa5894c4eba1a5426b808e8c229010cb4a2ca7ceb5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:52 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:52 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:11:52 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7357b8d04588c46bc8db8719baa0cd8f3116afb1e777c6148b36397e5420e918`  
		Last Modified: Thu, 11 Dec 2025 22:12:40 GMT  
		Size: 109.1 MB (109118371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dad1c204215613a89b75d1ff700f9af202e4828525b60bbdba986024e689843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fe7232124928dff324def0d309434d9f75fdb1691f8bc62c2828a40453b9dd`

```dockerfile
```

-	Layers:
	-	`sha256:39e50ee59e9d11143401ba07dba12ca4b2747925266386d1dc0c855a50e37fa6`  
		Last Modified: Thu, 11 Dec 2025 22:51:46 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28202fe31819d08600d78f0c17e6fcc2f6c656553174271e9444b2c6aee483e1`  
		Last Modified: Thu, 11 Dec 2025 22:51:47 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3dc1c91a01f551866f21173f8f6f0251e958e71c24cb0771696a03c9d85e90ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117736111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8efea1c998c3eb718131a950fe077d0050cf8f2d55192aebbc8b515edc9d846`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:10:48 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:10:48 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:10:48 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:10:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156478f876aefc8b22302e12ccc08de3f28b1ae0bfe9545d9dbe5251b5fcc440`  
		Last Modified: Thu, 11 Dec 2025 22:11:48 GMT  
		Size: 52.9 MB (52940356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:76f72176c7392df24cc09b14d8d1cd5412b6accba9d8e3a06fa2989c66bcd630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a16ebbe2c14f474f67d290d051bdbfc6b7dad1b0e4095e305e3c6b19bd8096`

```dockerfile
```

-	Layers:
	-	`sha256:9267d10aafa236b5805b1f37166edf28952c2c23c43c5d71d6fb66fb336633e8`  
		Last Modified: Thu, 11 Dec 2025 22:51:54 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3fb638771a6975e94611507594f697aa0aa65b850d717ad3054f07b4614f460`  
		Last Modified: Thu, 11 Dec 2025 22:51:55 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
