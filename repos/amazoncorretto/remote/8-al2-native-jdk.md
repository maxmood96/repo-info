## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:ab3009cf9fc5710965e5f7ab13ac018c569941b2b2c8a3b37bf67c5879114681
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:90bed3e4c9867a9b92d66442b284d40536c7af4d06c7a5f8586357549bb6efae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188215193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413426d031142be4cf0c78871abbcb484ee51d2398b619815e53accb35bebc33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7734346fe09756c0f4e4d4e77dee99165f05808405e5e0a279e81d15eb68e8`  
		Last Modified: Thu, 03 Jul 2025 23:07:13 GMT  
		Size: 125.3 MB (125252339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1c0b15079a5286b23e1f4edea4cd4cd20b9995c833bf97c850e3c3e979e628fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5ae4067f3a4c5e395a4456de4e6423066b5be875c937fc07fa6f608451eb9d`

```dockerfile
```

-	Layers:
	-	`sha256:82142d67ff8dee8bd83cac3020a877f589b7ab15bd154781bdffd09ea3ebfce1`  
		Last Modified: Fri, 04 Jul 2025 00:49:54 GMT  
		Size: 8.0 MB (7977398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e30cc40eba17c9bc6f6d597aa12af05d4a2326936b74231c692369d6ac594d`  
		Last Modified: Fri, 04 Jul 2025 00:49:55 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4929854a1497bebfb10e624fcfd8546f23bf49657370295bd4b3821ee560f5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132342186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377dbd6358a3890a95070afe5b591281e34825fb1250deace94a06726916dc83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:409bf1beed8b3d18aa6739b3b654d78ea6e9842b177c58b3fde860845eae1b51`  
		Last Modified: Wed, 25 Jun 2025 19:30:21 GMT  
		Size: 64.8 MB (64794781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ca386333edbf14aaa81cd52ab95dfbad69b888bec984d6814a72308be7dd94`  
		Last Modified: Fri, 04 Jul 2025 14:25:04 GMT  
		Size: 67.5 MB (67547405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:507f819dea2e7c1818616cb28bf2107027ae1679b1fac8582c267bf5ba7ce27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470b4827458888e98a1a74c94e12dfa7896702f54e91798e06b24a745bdca166`

```dockerfile
```

-	Layers:
	-	`sha256:b96e0adbe8f11c1714bd47669612664268ce41aadac1442161872c7c4b651071`  
		Last Modified: Fri, 04 Jul 2025 03:49:54 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d94db5120d585f937c56a56a355c32884385f105e8728fb687a5d78b4301d4f7`  
		Last Modified: Fri, 04 Jul 2025 03:49:55 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.in-toto+json
