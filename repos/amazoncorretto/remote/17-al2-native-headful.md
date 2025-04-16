## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:1a305ca18c19eac24b78ef8d106d6d94665e8f63b8020b1e8e0de62be65c798f
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
$ docker pull amazoncorretto@sha256:ef06e53bb8b3ce67d07a6e99995ad3ad3bb7f0f599f96d96badb63e46185d747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146442452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ac95ba54ed9ab36051dde668214c5008d999803a7886bd314b218fdaa51565`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
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
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af22006daf85108dec3a22b0675372242eb49e6ef21b63b1f61aebe287d1287`  
		Last Modified: Wed, 16 Apr 2025 00:12:02 GMT  
		Size: 81.9 MB (81876630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:65fe98b1f02e16fb9f37cc3d092ef6adb5aa3601572625a5c5295125988dc90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fa054b7bb36c941744b8d285f3a7bb51f050648b3cad4cdfcad5f2984d8c84`

```dockerfile
```

-	Layers:
	-	`sha256:cc1c487538ee7fa3e28cac407edb494231f1eaa13d23b90f3632c1ef30b66ab6`  
		Last Modified: Wed, 16 Apr 2025 00:12:00 GMT  
		Size: 5.6 MB (5641325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2cebc93a9d7f4eae18e729f080c6922f3a2ee2752f3708ab61df6f37292145`  
		Last Modified: Wed, 16 Apr 2025 00:12:00 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json
