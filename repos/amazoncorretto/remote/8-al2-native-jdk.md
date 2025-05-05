## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:d9601e086fb36edb2cbd87e1a363702db8a1fb86185ae67c2dbe164c6bc55ca4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5dc6d267c972bc0352e119b84e985542e2d97a10c87e19134c055689039c5f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188004271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9d3d03b1a0f6cd028ce894960a88bcb4e0b4464daef3eab177983200d26c6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Apr 2025 22:04:13 GMT
COPY /rootfs/ / # buildkit
# Wed, 30 Apr 2025 22:04:13 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 21:09:32 GMT
ARG version=1.8.0_452.b09-2
# Fri, 02 May 2025 21:09:32 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 02 May 2025 21:09:32 GMT
ENV LANG=C.UTF-8
# Fri, 02 May 2025 21:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 01 May 2025 13:44:39 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5d92f49d03ce36f74c2b7bbd3a907eb916bb14f8f3f6b6dab3d64e8b04dadc`  
		Last Modified: Mon, 05 May 2025 17:34:25 GMT  
		Size: 125.2 MB (125244941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9b5b0781671c7179ac33b6c2d3f7348243003cfa31c4b9464271de443e41817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18ddc2dc61d5d95e4809a25c835119e7d523759fa402bb65a996356321f690c`

```dockerfile
```

-	Layers:
	-	`sha256:7e1ebd2a53217db8a7a767804943ebbd333a467b924316655654ebde2c76292f`  
		Last Modified: Mon, 05 May 2025 17:34:24 GMT  
		Size: 8.0 MB (7959664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e9088e606d8e75832b0845cd19b1f6475e2d0176ea1ea326578d210e87bbd5`  
		Last Modified: Mon, 05 May 2025 17:34:24 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a90a1be04843823f86a32a3a465be59a9f896551dbf6f9e226b4f106210a2386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132148947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a535fb7661cbda59041059b1233f7923d911f796bcf3b930bc3839186a91c52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Apr 2025 22:04:17 GMT
COPY /rootfs/ / # buildkit
# Wed, 30 Apr 2025 22:04:17 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 21:09:32 GMT
ARG version=1.8.0_452.b09-2
# Fri, 02 May 2025 21:09:32 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 02 May 2025 21:09:32 GMT
ENV LANG=C.UTF-8
# Fri, 02 May 2025 21:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 01 May 2025 13:44:52 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe7770e59031bf355d5e7406d2af96cf309fdb7b47604dc014372a64b531ffe`  
		Last Modified: Mon, 05 May 2025 20:42:15 GMT  
		Size: 67.6 MB (67554220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b8a28755eb0e3e65a3f970912b193ef185b0cb8bb7c059a7a23c939286199570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f513e785f73f92fead8be6779c19005e64da65df82278eafe99b3988222aa7`

```dockerfile
```

-	Layers:
	-	`sha256:c296d7494de11b416f577c5e4607f7719b061c4a97be26a402edf309456c55e5`  
		Last Modified: Mon, 05 May 2025 20:42:13 GMT  
		Size: 6.1 MB (6069805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de704c516289752b8af926f46dec457fcec0048dab2906befa8e126ca528b7b5`  
		Last Modified: Mon, 05 May 2025 20:42:12 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
