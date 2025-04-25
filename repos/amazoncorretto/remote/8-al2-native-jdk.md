## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:03990bf1fb22c5e736f87d9bfc3c0d491092e2eaad6070cdc8f50f32912a6d83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:15e7350528927dfd135a4d538109f22516d9b046a4fa95817b5166bdcbe0e342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188038691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff291040d5ab55073e30282b6a1dd5ed4c51636d2bade0cd6e408d2d51f9115e`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39f9e5a8ac36b4e057403e06888c86f333f85003290f4e48f2a97d3b448cfa`  
		Last Modified: Thu, 24 Apr 2025 20:08:24 GMT  
		Size: 125.3 MB (125276969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:458ecee31f46a39d2a077d8a5f91270e954c2b0be1062d786eba0e80e4619281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7968043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97d7ddf2ec4729ad46ed4a9fe74c37e50fd40fdbd6f6f5d4b1ad0a678883d0a`

```dockerfile
```

-	Layers:
	-	`sha256:7f6212bab1f6e7b4c155848552e7932d8c4c4e8af880bc3bc5d26d53d70dfd83`  
		Last Modified: Thu, 24 Apr 2025 20:08:22 GMT  
		Size: 8.0 MB (7958450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63b361464af3e71dbea16ec3c95eeaf2f41978566c47a84c72d5a1c8dc3ec3b8`  
		Last Modified: Thu, 24 Apr 2025 20:08:22 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c47353f4837593cd440bae98af71bcd88fa447e960dc38c0804d9733f1f7659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132130273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efc9b65feca8fbee8a2589e14494e412026b42e1704c69f2eba29e1e9094c0`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:928bddcbf112315a029f894cf829df2ae1b28c89ecaa6c142e3d47e62c803337`  
		Last Modified: Mon, 21 Apr 2025 21:48:49 GMT  
		Size: 64.6 MB (64582610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8774aa4422010474a93d8ac7accbdea164f6fadd87fbde82e7ca0e9df25c1b7`  
		Last Modified: Thu, 24 Apr 2025 21:10:07 GMT  
		Size: 67.5 MB (67547663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d6306d0c9657170e3bc6054ea5d5b981eaa034461703aff452b87ebfe7ab88d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbe39b37dd2cf1727e1f33e31a3dc01608b399e9a8b4cd676dc7f8e9b57e1b1`

```dockerfile
```

-	Layers:
	-	`sha256:3c64f6aba12fa98ef67db171e57205280f81954b6cf225a38554db58baeb58b9`  
		Last Modified: Thu, 24 Apr 2025 21:10:05 GMT  
		Size: 6.1 MB (6068591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2896d2a3f3544938f1b1b153c31c5cf564db85d9082ad2027943d8ead77c6d9`  
		Last Modified: Thu, 24 Apr 2025 21:10:05 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
