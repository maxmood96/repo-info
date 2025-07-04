## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:eb056791b59808dd9400fb16d328a7a8b011eaf843c1f5f804b6baf26dd416d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e38aecc2502db2c54e18fefad88c228a15459807b0196bb2f834173103cf390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225208971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215a74616648cc77d5680e8a6d586deae483d6eb8c3aba13f6d471035964436d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95737e2f6fb9ac2199b5b883eb5e6ba7a28649082169f50a117acfd5391fa1b4`  
		Last Modified: Fri, 04 Jul 2025 03:21:30 GMT  
		Size: 162.2 MB (162246117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e92cee2c9aaaa56dd59a91a75779b58fe0993e4484ee9d4ebb4d0255664e372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024366852ba628207deb4b279e1e204c2662ebe30b0a23d40a994fba47a034b5`

```dockerfile
```

-	Layers:
	-	`sha256:befa0fa46e4c28cd6dc8efb4a9ac2f0045ed8128765f9d4ee46da2fec8720c44`  
		Last Modified: Fri, 04 Jul 2025 00:47:29 GMT  
		Size: 6.0 MB (5995078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c226db60751ffeb7eadb296713a5ccfa0e8ec1f9e333f5fd45daee5ec86ef4e`  
		Last Modified: Fri, 04 Jul 2025 00:47:29 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3d70b8bc5501184915fe8bcebcdbb019a3f4cc66b030160f0b475a68db60206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217143994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb8581cf88c6773192b1fff5c96654c7a7558da4a4d184223a921f17c2ea17e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570dcc04c162533fd71f00dea139dc5f5c14da59b928540e9f28ec745b1efa4e`  
		Last Modified: Sun, 15 Jun 2025 04:02:36 GMT  
		Size: 152.4 MB (152353248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e81829230190e4a14652dd1c2b81fba36fc6dd96d4f835dc6f8862a221200d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fc6f6037bc76ab4aa71371e11739352dbff229a0bf5b4a66d243fa339d27ef`

```dockerfile
```

-	Layers:
	-	`sha256:eab635a3f72827db3ec0201791da4a3b3be86ab008e8e66f8e708946dfaf6bce`  
		Last Modified: Fri, 13 Jun 2025 21:47:38 GMT  
		Size: 5.8 MB (5787792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3741a6861840bc3992cd58323c0a573b4629c2866c4228042db79bafc9357755`  
		Last Modified: Fri, 13 Jun 2025 21:47:38 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
