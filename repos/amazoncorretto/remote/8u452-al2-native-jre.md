## `amazoncorretto:8u452-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:3b9d585c1cc14d88589bee02fff1e52bf032e3af8545166fee074b6f61ad1723
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u452-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:53c7c77b19720d99a7acc7ce3c9e4c8329e15b69f9b99f5fd9e49bf4aa047057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172091580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1159b42dc1051d4458b97461116ec9ac88fefa3f49cebf37156832487dfe156`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb885e293b05c812f41833f76be78553e3c9b923f4a66b019d125da87eadb13`  
		Last Modified: Fri, 13 Jun 2025 20:04:12 GMT  
		Size: 109.1 MB (109128641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d357c966071de52814423fcc2d88893bfb7feed42bace3e31c545e2ba984dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a6ea530445fdaca8db61fb5a092d00902de7d1a5ac2930d364c08dd5e75975`

```dockerfile
```

-	Layers:
	-	`sha256:78ca19f0f6c10526f616f48d9f38401802ef7b8cef16c47b50dd345efbce4f81`  
		Last Modified: Fri, 13 Jun 2025 18:49:54 GMT  
		Size: 7.5 MB (7504112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b2c43eaf08ffddf0275cb627cec9f4c78f49e130d0638f7307632b44ee0a65`  
		Last Modified: Fri, 13 Jun 2025 18:49:55 GMT  
		Size: 9.5 KB (9547 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u452-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d07f6725f538d9012956373344e905993ca51f63e329e70d609fadcb2e6dd53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117717338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4ab154996cd3e93cee1535a3d9d98ee8138e76b4b48540df97607276cc7920`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02f1090f24cb0d8ba48a86c0fa93f97055cd034894ce15a17bd6208e5941a86`  
		Last Modified: Fri, 13 Jun 2025 19:52:12 GMT  
		Size: 52.9 MB (52926592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f36536456d06067c54470045972830dad2c58eac89dbf103cbcb350c6d5d6a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c22a581662368a54f829a485523970c02453d9196fe07c8ad3f24bca9623ba`

```dockerfile
```

-	Layers:
	-	`sha256:a5029cc3a8b48d0c262c24ec9b3959fac52a94122a67e7267679eddee0db804c`  
		Last Modified: Fri, 13 Jun 2025 21:49:52 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fcddf19716e879977c8bedce76f7a216cabc870edf4066c5fe7aacc7766ea3`  
		Last Modified: Fri, 13 Jun 2025 21:49:53 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
