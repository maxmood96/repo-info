## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:d8476e8ac2311a434e0fcf5b476304464d678ff08eeb8af2624114a77fd39043
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5eb4cb133228675b3b696aae5d0a03fde18a1c1ca26e7e0fc472519afbe10369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171832688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248664a9a3ca13982eb045f6f1e08bee17147295dae8dffea576a80d97cfcfd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb109085c804a64dde34375a7d0ede0a682c4d2bda567c5dcce27bad2239984e`  
		Last Modified: Sat, 07 Sep 2024 01:05:53 GMT  
		Size: 109.1 MB (109137141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:042d62bbbdb7e5c663d630fce6faccd9cb96779037533e7885beefcd93c49090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d333132a1380a147d356ca19686603dfb5610aa8219ebdf44090ef6c7f4af58`

```dockerfile
```

-	Layers:
	-	`sha256:aa6359ca629d9b35f8d60ee48d2ccc337473653bc1ea717929008b3a555136c1`  
		Last Modified: Sat, 07 Sep 2024 01:05:51 GMT  
		Size: 7.5 MB (7497704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a86192c149480ada3451378badde0e563cf0c5b66a9fbe841d093a5ffc8c99c8`  
		Last Modified: Sat, 07 Sep 2024 01:05:51 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f1c288f45e6e1c73469c789564789cb6346a6ba0a0b6576b076ae3e698f38c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117523252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb5ab7db205182174b0806f20933bee32948092019d9cbe8ee5afc79e4f39be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a76f5c44506982b7eb54b2f9622707d5bf9bf66d769b1f089a41e685b27d2`  
		Last Modified: Fri, 23 Aug 2024 02:17:51 GMT  
		Size: 52.9 MB (52936117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:53e9dfaa7513cd48a46e461f15a0106cbcb1a5025bfebd7c3cdd30b249891f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74d1f6775571932830d97b4ef32b85b106f679808ac7b70da2cfdb1b54b0db`

```dockerfile
```

-	Layers:
	-	`sha256:38997ee312f54e8c3bedf1a7d33e29d31112a7a9b15b21d9a22064402a530278`  
		Last Modified: Fri, 23 Aug 2024 02:17:49 GMT  
		Size: 5.6 MB (5613432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc80b6e0bef6cb99cbc515c871fc5c4ee6070e4acc10f4305fa7ecf9fa627bc`  
		Last Modified: Fri, 23 Aug 2024 02:17:49 GMT  
		Size: 9.9 KB (9874 bytes)  
		MIME: application/vnd.in-toto+json
