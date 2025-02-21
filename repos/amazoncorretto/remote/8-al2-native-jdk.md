## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:9047c39eaa31d42c7acb5c2adcb4f14c7f7c9753aeef077f3998a186a0960c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cfb4886b7f7fc92da39690797a04edfc577a36ec44ee0208d8d014c02132b65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187903128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500681dcc8e7a1e822d6b016037ac489bb49433107939e002c4bb49d8f4fe9e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:43fdf45428917f1f386fbfe0eba1ccfdadae7696a4cce30a96cca587ab25ab90`  
		Last Modified: Wed, 05 Feb 2025 10:24:14 GMT  
		Size: 62.7 MB (62665244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a09a590e09e36b314feab7a5382f1ec987cde3277468b1f109e770a33007bb4`  
		Last Modified: Mon, 10 Feb 2025 20:09:00 GMT  
		Size: 125.2 MB (125237884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2c15da46a5d1d4516441287dac81700c9af128c38e0811f578ba7d8af99a8c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b54f726ef4e4f026c2df8e287347da58e31d1aec4aa23017bcffafaaf152655`

```dockerfile
```

-	Layers:
	-	`sha256:3ecb289dc866889a071653acde963b1c53a7ef7f0a605ceef7af7d476ad8534c`  
		Last Modified: Mon, 10 Feb 2025 20:08:58 GMT  
		Size: 8.0 MB (7956594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b799cb41b6e57900a27c38279487c4d286b0f2a2650f47a715c06a4864c1d01a`  
		Last Modified: Mon, 10 Feb 2025 20:08:57 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ba76d8404612bfdd1129bae3b6159c63076aad61093ea3115b34b1921f29dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132137430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e18f9d17d6aa5c2bb48320dadbfa6f25fa116078ae0a64c9fc54a725e29618`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012725a66347fe7f72960e09c2e1dfd8eac6b11176c8f40f5a0733a9d187e63`  
		Last Modified: Mon, 10 Feb 2025 20:14:20 GMT  
		Size: 67.6 MB (67559208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7e9a1a7ffc49ff969f4036a6fd42038beacc8cfa7c49ff3dcbb818a1d6013964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c70e1748285a9c095863cf422b18de4a63e7bb8db8fe82ee2828a297ce1155`

```dockerfile
```

-	Layers:
	-	`sha256:e178bdedfd7503e2adc6966e14d8077c4dd3745da0b30cd30f7adfa4e673e5fa`  
		Last Modified: Mon, 10 Feb 2025 20:14:18 GMT  
		Size: 6.1 MB (6066679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fc03530fde3cd79d25d31916955527fd58bfa9efd10c1af05c6be4d84c0a8f`  
		Last Modified: Mon, 10 Feb 2025 20:14:18 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
