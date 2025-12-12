## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:7ae149d50426068c53ead6cc82f831bea2cf5c746e414e1a950ded450f0d1d63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2607feb2cd652601adfbe3d55bb529dadbdee33bd63d6f514ffc9854f8452ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188194699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ff0b43b42d4b355b70ba401e5e72781294c0475a4e43cbb066444d78e7e9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:57 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:57 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:11:57 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9820af0db218c620dbd2062fc12fa5de6202605262d42228f6e8bc45b6c523f4`  
		Last Modified: Thu, 11 Dec 2025 22:12:50 GMT  
		Size: 125.3 MB (125253724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c244e23820a24ef35500c4ca1fb0a9804dbfc910866f97cd7258fa6a418ea053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3157c5f7368a8c565348095e230ee044b12aa50fb4d9a27b0cce673c5f1dd4d7`

```dockerfile
```

-	Layers:
	-	`sha256:4b1f935c4fd766f0f9e6743de72ac118f94931aa6b87024a51aec26a2b292be9`  
		Last Modified: Thu, 11 Dec 2025 22:51:42 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7316e65da1a267d14dd5a615436b31140fb091a3c526fcdaae752ebbc1533f`  
		Last Modified: Thu, 11 Dec 2025 22:51:43 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:09cbdf1f234df62b9f8eaf0a266a1910f30c141266012857312b3c61b2a56aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132360373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f878203af290f1073e654d852c5edf3b2e0192c4f670d5bec8cb67dfad7344a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:29 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:29 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:11:29 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ae5ca10bbf5731af3c5824f3f1eb412221eeb16e6f3e07af1f48249b298a71`  
		Last Modified: Thu, 11 Dec 2025 22:11:59 GMT  
		Size: 67.6 MB (67564618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1aa97a8da64238be60e92ff11acef3ab9c4a4937f69de77ba33b848e17f8a964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e38e26bf3878472ab29f51310bf3ea767901460b45d90f6b3282dc06d320fd`

```dockerfile
```

-	Layers:
	-	`sha256:cd6b41dd53da2d56eded30f86b9c22cfe25ddc329ed6cfc514223806dc655a05`  
		Last Modified: Thu, 11 Dec 2025 22:52:29 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0737954fe59c526bf54e5dc53cab6c800d9c0dc308cded05958276f62ed353e`  
		Last Modified: Thu, 11 Dec 2025 22:52:29 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
