## `amazoncorretto:8u422-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:cc5aa0b9671bb9ba0301fc3e3953817fbc588aaa122819d74d4a1ad6f14906b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e63bd9e4c18c3994cf0526f7ae03d9957d117cf474c88ba58ba48a6569c083b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187907616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d000ab49f2200c99f550325b5e3e140cf50dcde1d9e8f02ccfbec357a44f93da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7884b6ca98a10d204db5722aa11ddbf0429d4374fc42af22e74dcca80e1264c2`  
		Last Modified: Tue, 08 Oct 2024 00:00:16 GMT  
		Size: 125.2 MB (125229460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a9117b7e3c21fbfa0cfb07a8a432fb13bfe97aae1e57e0b1827e61059939f5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aca48ce78a2c4e243777c0688d1311653c67041bf13e0403bf81a351f7dbc3`

```dockerfile
```

-	Layers:
	-	`sha256:dda3b871caf3deea09aa169b67a5a6c51136770e9cd742903f1645f5d5a23572`  
		Last Modified: Tue, 08 Oct 2024 00:00:14 GMT  
		Size: 8.0 MB (7971265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ee14d6771c693ed1f83b7e6411244414561a2cbc83d577975546a1f9f12bfd3`  
		Last Modified: Tue, 08 Oct 2024 00:00:14 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5e186671560949ba5fad3f0246eee3ba141160d26ea47147d3259c57e5967daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132141618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97c888a5ee9d565dcfc20b6ee4c43a55ad3d322106a302f0aa60e15b99b2ba1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22517130cc3ee2483417bfba24397db051ba582a16df9ed5276bfea158ffa760`  
		Last Modified: Tue, 08 Oct 2024 01:56:24 GMT  
		Size: 67.5 MB (67548959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6720268ab1154a7a0d96c7a240e8fb9d80055246185989c39f6af1e2b31289a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c79aa4c866c3f16c25474ec992b893cf2237aa70bf7e74797b7563aac57324`

```dockerfile
```

-	Layers:
	-	`sha256:303d4baeca115581ed9da06e962ffa17b94d8e76505b3ea75d591eb89c71df22`  
		Last Modified: Tue, 08 Oct 2024 01:56:21 GMT  
		Size: 6.1 MB (6077770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:682631994bf67e816a4f004505a18f39b04d720fe4e23cea48d647a8aa23d8e7`  
		Last Modified: Tue, 08 Oct 2024 01:56:21 GMT  
		Size: 9.6 KB (9643 bytes)  
		MIME: application/vnd.in-toto+json
