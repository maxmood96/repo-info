## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:7090a5bd05d930bea8b18c6388bf235c32fd30554694137ce77e8f8a50025fe9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:329db0228c864171322c3c61da9c8e5e71654b04d1282b8762a64f82df246d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171758339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fc86a61bb594382929e2d0704feaa3b41521a68fab817a73ebb487b5bf9835`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=1.8.0_412.b08-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc530eb0886604e2fa2cdd9f8da012f3a886b4a44612d7c1ea4d88962ce4088`  
		Last Modified: Fri, 05 Jul 2024 19:56:32 GMT  
		Size: 109.1 MB (109111701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e9bf886dba348de34e5f33d468a4aa73d271685b06014eee13ab8f6d9b7a9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7469422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c2a5024219795c9b5be80835840ca2511e95be1c5a447ea76094c18a64ef22`

```dockerfile
```

-	Layers:
	-	`sha256:698ab16110eba25166b9f7f48f68f30c536a863f97a89a79e83cb217c513bf35`  
		Last Modified: Fri, 05 Jul 2024 19:56:30 GMT  
		Size: 7.5 MB (7460113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c349c6cc4039dd0587d52c1f3d430b2b62dbcb6d90a2088a7157a20ebc9ada`  
		Last Modified: Fri, 05 Jul 2024 19:56:30 GMT  
		Size: 9.3 KB (9309 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:be8014d1899478ad02611559bf4999085cb9a14e755112dfc6c22e898fef1cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117489865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0240d9b3d89a571cd5b8bab684fe9af2539de1f58b1ba840f19789f835b925fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=1.8.0_412.b08-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ef8981990c5816d1542d77dd0a64c4f20e550f6413b1ac34458e57cead7b9e`  
		Last Modified: Fri, 05 Jul 2024 19:57:56 GMT  
		Size: 52.9 MB (52921100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3dba4b2f58d35d922533d0d6e6edf4b24e871fb4d4833d9f7bf66853acb21a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5596747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d83767fb4664e25d718f0abba7d1a5d343f75916ccc7b61d9f345a0cdf04d2`

```dockerfile
```

-	Layers:
	-	`sha256:dd49acc5526c44773205ef2876a1edbac94fe7da2bd3ec6bae77b09267ed037c`  
		Last Modified: Fri, 05 Jul 2024 19:57:54 GMT  
		Size: 5.6 MB (5587162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca93c5508f65d436bbde7298abcf078a3659c2a48086090d018799c21a6c6ae`  
		Last Modified: Fri, 05 Jul 2024 19:57:53 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json
