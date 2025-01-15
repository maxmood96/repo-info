## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:29fe3cd1db0bd9fe4cbe98a8840a69705c0bb064a6e56a30fea2e5804e2a70ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f719bce3c1a76557dfe4285ca456c070ff278a22228f8d52cd5997024c8cd79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187884197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e784fde5948fda47509cfd1d09c5e27643c2bb7f1c15a6b35b5c34ac0fd66d0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275c9fdf099ea6949560e3ea8d837d87bab087f4f25917e6a310373973439238`  
		Last Modified: Sat, 11 Jan 2025 02:29:47 GMT  
		Size: 125.2 MB (125248367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ab317246651aede1968f3a050c2a0797f53664de49506867c2afaef1d03b606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27874047337b4da46e9fe1509324d9b2eb3f9cd4b7f2230aadd94593452abd59`

```dockerfile
```

-	Layers:
	-	`sha256:c6f27a844a4101c90f3705f683bcd24511fc85ed2526b4167b2d5dd5b3529224`  
		Last Modified: Sat, 11 Jan 2025 02:29:45 GMT  
		Size: 8.0 MB (7956590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a0982e614b76dfbd7e296cd77014c8556deb1c9129018c1be752e8571ef57e3`  
		Last Modified: Sat, 11 Jan 2025 02:29:44 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bc6f051365286febe3183ce7224505c28b239af5a19837444e3ab159de424c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132161308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19caebeab56ced9d4e26fd597649c9d46caa8a3b62aa633c730f00a33664ce4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c270bc6bf24f7e228c2f07b3e3d9f5a06d132f0cc2a57bad3600e5f9e25e2c09`  
		Last Modified: Sat, 11 Jan 2025 02:57:59 GMT  
		Size: 67.6 MB (67571003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:893e1e344a16f08bc3c17f871bdcbfcf37dd5a134276520763021ebcbea7b4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53427912fc7457a0446207d98a396f64b6840b6dc07314a2960424a64598c303`

```dockerfile
```

-	Layers:
	-	`sha256:6f1661a08789b6f1bd74dfef898d2c6a85865733dc0ec76c055dc6e61401473b`  
		Last Modified: Sat, 11 Jan 2025 02:57:57 GMT  
		Size: 6.1 MB (6066675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81e06c924f815fa297acf000893e2d371e937a75c6c6a01e5314df9b0a85e311`  
		Last Modified: Sat, 11 Jan 2025 02:57:57 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
