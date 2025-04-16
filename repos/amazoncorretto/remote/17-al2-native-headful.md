## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:5660e479b4d057384d8e5f864bc0b1353c14b60148e9cc030a0c24874f0b85d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:af28ad661676a2eecdf7b20b981eb08b7c7e4c6ffd0cee9b2f14ad02e649e9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153932843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69982e38621ab1018514cac55efaf7e1ab6f7ef80d225b3ddd37f8e639d061b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127476ddf910890cb19a0056001179aed7c9370155a670b366b2090528022b4e`  
		Last Modified: Tue, 15 Apr 2025 23:56:01 GMT  
		Size: 91.2 MB (91179954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fd4d02120c56637fa5bb34249bb103accae2988fa5377a71b2c472cacd2ad299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86dd239ffd3721183ed6e3cb80eb2dd0ac8a325c46c5d10cb4a1db17bd68bd1`

```dockerfile
```

-	Layers:
	-	`sha256:427a5cb2a477415ca7e1b2d848a3db9543dc25dadaa317238da0129f070792a0`  
		Last Modified: Tue, 15 Apr 2025 23:55:59 GMT  
		Size: 5.8 MB (5849582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc466d5a98995d4712b36b27e9f66c026d846cbdf80f38988d513f54c8ed3e7c`  
		Last Modified: Tue, 15 Apr 2025 23:55:59 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d3738bcc65af0017d3da766d4137321a2b411e5b50c305524f8315da0126fb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146414335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c851938f07d6dbb15a508a6ff5fed828f03003a0aec6f1dba5b6d20f6585a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fb89602e297b9b05419bc12c0ad00d4286b2d2d8bea2a0879d2cc5c8901452`  
		Last Modified: Fri, 28 Mar 2025 00:17:37 GMT  
		Size: 81.8 MB (81848513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e2c7a8d91515e8676ecfdf98d9e7df068e0d66450825704b0ad6fd7ba728bcee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c051c7a4f31dff11480fd13157e91a964b73f1fe989f0b081487a110c11eaf98`

```dockerfile
```

-	Layers:
	-	`sha256:30fdeaed90eb70c4e82607689ef8938c24f2b7457eabc29721e102d5ae4f2c93`  
		Last Modified: Fri, 28 Mar 2025 00:17:36 GMT  
		Size: 5.6 MB (5641299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb59566817226a8ad3de257c037bf7c3bb27c7a097758c00b380ee23a095ccc`  
		Last Modified: Fri, 28 Mar 2025 00:17:35 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json
