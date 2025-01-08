## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:b229a1144e5525b623d61f5427f3607cf622b7d14604a3658e8a5dc8df02c4f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8161e1915cd76555f375bb71f040f779f2ac509e47fbd2b874db1fcf8c5dfcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225793701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decee2c93189cd95d7c0c183496c01140ad4f85c8acdf7babe114e75d52e5774`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e81558d0b1735db8ecc647d70df5f825b25d21cde446fd4f962509b49b26ca8`  
		Last Modified: Fri, 20 Dec 2024 22:32:33 GMT  
		Size: 163.1 MB (163116262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:325d9768d66128b6700cb6211ab833810e8c655efc56d5c56360e4e913daa374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5677080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b83d3d959752c770d7758ecdffde93f8ad67a0d4a11998379ff77964637eafa`

```dockerfile
```

-	Layers:
	-	`sha256:02e76443ae63ea2c61cd66c6e190fc7401990b354858b3d123710b612bd1f4c5`  
		Last Modified: Fri, 20 Dec 2024 22:32:31 GMT  
		Size: 5.7 MB (5667749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0e8aaf0c31b465a6241c8e68c4e75ae57fa55042f974e97e43322ce14a9c5d0`  
		Last Modified: Fri, 20 Dec 2024 22:32:31 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:880025f4e8cda81ee1b4b383593d6af8170ae2842a57a67b470235233b778a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211807913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a147e6ac803406e2ce643c51daa20ada5f4d82ff2f3808d1613eadad19a94b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729635bb0cc7dab0bfe175795c62b1fe801c1716498723108126f225a55ba43e`  
		Last Modified: Sat, 21 Dec 2024 01:41:31 GMT  
		Size: 147.2 MB (147226026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc1f1eb70c7c8c83ecbee87bf2d78c9a1d115b0b712384c41e34545c428b0b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5495628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f04f338f8aa612c719d905978921eca6e72187f3131889b934fc5f22b14d72a`

```dockerfile
```

-	Layers:
	-	`sha256:fae1b4d58ba76be9c857edb9648e01f7c72c197e017e829efd7419c1118a9333`  
		Last Modified: Sat, 21 Dec 2024 01:41:23 GMT  
		Size: 5.5 MB (5486217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf46e4324b4658569089d1a60a57d5d6a0a3fdd482ba064d8f962ca67a61a28`  
		Last Modified: Sat, 21 Dec 2024 01:41:23 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
