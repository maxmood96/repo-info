## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:7b23ef2ad26d72135f12c5f59d6d5807051db695b081e363373e9ad87e431620
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:45b0a31853ebf7e44d2c8a5cfff41cd929832a86d9e566a648bdee5581cefd4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150089055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e161ec9bdcf59afd2d2c2cc143786b52bd21dc4d2d98a170248a6bd1b611d4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da68c59d88d75d55b09ba1ec7b0b36905c9daf018329c4caa29c2fd0e5d59958`  
		Last Modified: Thu, 07 Nov 2024 21:48:14 GMT  
		Size: 87.4 MB (87408013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9026c7e658f358eac9e8b8392b141ddfdb519f9db42575dfdec692794cb4dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f96f457d7c36f8181c0c23d504eaf7dca81ddfc02d98c83d79e631885feaa7e`

```dockerfile
```

-	Layers:
	-	`sha256:3f875bc70347cf42c290e1a6a6efdc67089a354d226d1e29f0f5eefc7f2e73e2`  
		Last Modified: Thu, 07 Nov 2024 21:48:12 GMT  
		Size: 5.6 MB (5626910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074089eab8900214deb9de9ebb0205cc15f9c8a9a2707e5d3af34bc1892de39d`  
		Last Modified: Thu, 07 Nov 2024 21:48:12 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1ac81b3faf00519f168a77e25e04e6fbfc3dbca87474972537ccb8e91c973e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144272794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fae7ed94d9c0739fc05e5ceabe70cf4fa885ab36c8127e9fa39e86d9d5b639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84571f19959cb9157ee8179b58529035fbdd1fe58552f3cc34a0d353ac6a866b`  
		Last Modified: Thu, 07 Nov 2024 22:00:15 GMT  
		Size: 79.7 MB (79684223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b70b4e508afeef7a3c834e3b41e520e885d4c3e8f33d09c7cbfb5aac5a2ac90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d528619148cee7bbf6554abd996b4612583683e61f296c8a83ac6f2aa011f430`

```dockerfile
```

-	Layers:
	-	`sha256:bc965236ece95512b061d2b3808353f16584c83b95f41ae37ff547f6b794edef`  
		Last Modified: Thu, 07 Nov 2024 22:00:12 GMT  
		Size: 5.4 MB (5442886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e43443271dd725b79ac05f35f2607c83dd2b7a879919690571d3cb1e2539494f`  
		Last Modified: Thu, 07 Nov 2024 22:00:12 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json
