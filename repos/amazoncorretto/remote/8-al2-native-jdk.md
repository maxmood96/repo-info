## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:2a00867b9e304b1eb2e2b9a43ff29a8d7375246b42c587a540d8eda9ea8a3bb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f566794d08551d05d196f43d60b13038aabf77d62b32162ad323a664f8a520a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188007108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c6c666bbd0a5f84a7b299e1c8f64fe79afd0cfffb42a1d94b5de340a8f43d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52629a0bd12b244f783a973327bf5ea8768a948cebcc57e204fa09bebf64c8c`  
		Last Modified: Tue, 15 Apr 2025 23:56:09 GMT  
		Size: 125.3 MB (125254219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4ef6f362251f8b6515960835183268b9e801e0787411d08515a160c387dc8fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d207c528736ba231950bfcb22991c9f7a2847fc6488b398b64918807b39b1710`

```dockerfile
```

-	Layers:
	-	`sha256:6e0aceae70a96c20421c851961c2a77991344c66cb50766c91a6716b26166de8`  
		Last Modified: Tue, 15 Apr 2025 23:56:06 GMT  
		Size: 8.0 MB (7956564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c620311a7afd315cc3b841111f53a46cd78fc4e6184927b84b24521dd9f5c60`  
		Last Modified: Tue, 15 Apr 2025 23:56:06 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2fd1bd4d5d0f7431f3e9acd9f1a0246589ff91a242c0742f1caa8bc35584e1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132099485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9015d641639729fb8a77748b1d34224d099ae8633b0687034d8c23693fb2be4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b96b88041eb89075d678455b4bd20a3850bce942bec1d72ef5e15efe82abdbd`  
		Last Modified: Tue, 15 Apr 2025 23:57:30 GMT  
		Size: 67.5 MB (67533663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6fc1740e85befc6ae065227d57f56f969bdaf53c4def9a80365af43dfc434c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2156c99650deb8c96cbc90c0174111599f5915ce2708bd29c56916529337dc77`

```dockerfile
```

-	Layers:
	-	`sha256:99a351902dc32d08fcc707f23eecfa8b90bdb17b009bcba0fd9d92ba2c65905c`  
		Last Modified: Tue, 15 Apr 2025 23:57:28 GMT  
		Size: 6.1 MB (6066705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcda195d6c23aa179d397dcf03512d41b4731ca4cd0ce21d36e58da75c6a8b57`  
		Last Modified: Tue, 15 Apr 2025 23:57:28 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
