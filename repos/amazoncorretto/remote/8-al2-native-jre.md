## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:6cc354a85344343541c6189840fb3f7b54b1c1810fba62669d0d3a1d42958471
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
$ docker pull amazoncorretto@sha256:0322d596936231ef6cc07f9a08c2c2633ee95da1bdff9184c8944ce5b63d4a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b034c991e5cdfb36d9f3cfe5b130ee6f8898022049eb5105eb8e1325725693d3`
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
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f15eaa2da692577d536cb3198acbb0e2a10da7608e6206f4fa51b6fa8663b6`  
		Last Modified: Sat, 07 Sep 2024 13:09:10 GMT  
		Size: 52.9 MB (52935943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:432b1f7957c76e13f0d5948790a5b6b825248983d89bb71f76903517cfdd4819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4723b68c2d84e2d21a8d9a64d6f3df98fdc049c8425ce35a11050b6644eafca2`

```dockerfile
```

-	Layers:
	-	`sha256:95ce2ccd320d457924eccc7b36c81e286a802cd9321efe3fc260ce8ef1905725`  
		Last Modified: Sat, 07 Sep 2024 13:09:08 GMT  
		Size: 5.6 MB (5613432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0565c3f3ea8b93434d3b3252bb6d0f0b077ca753aafe8800b04bb41355558a`  
		Last Modified: Sat, 07 Sep 2024 13:09:08 GMT  
		Size: 9.9 KB (9874 bytes)  
		MIME: application/vnd.in-toto+json
