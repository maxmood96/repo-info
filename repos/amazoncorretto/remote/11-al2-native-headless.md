## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:9b764c91f5f54a80475c8dcf7ffd3ab22b5ea681c9b100a2ddc36e69e355616a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:894b9209e6996fcbd1b7698b4abc4b0279e444424b2b30807d77174611ac67b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217472860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71be857292c25fc2c94370ec6b9bee210b76c1ccb343bb117d96c336e06414cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:23:24 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Jul 2024 21:23:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37503b569a1d6b837f0a3c5bdea379d84f7dfdec0be5caeb368ba9b4c5edcc7c`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 154.8 MB (154823454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e81ff21761419a64d9f74ed44b04574bedcd4074272b11d1dc886cb2d2b3b066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5688039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb42249017546b7f0a4b2f9f61533d0becb1ce579a1d4e2746a4f6368a979230`

```dockerfile
```

-	Layers:
	-	`sha256:236eca82f5d6ae3d9a722dfe12346313eda9831b89256789dcf981c860c00045`  
		Last Modified: Tue, 23 Jul 2024 00:07:55 GMT  
		Size: 5.7 MB (5678742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ea8bea5971dc42790d4862ec67dfa776a285dcf19ecf5a4a30b109430485635`  
		Last Modified: Tue, 23 Jul 2024 00:07:55 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9f68e8c8ebc35c2f41a331b3752e97161c5af29f65192a5a6e20ffca9c04cb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211773975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2463c6d56531e46eb8552db9a8eac46f6f91ec111d99201c826a7f34b864fadd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc7c70cc1c6aefcc09eee14f05c61d51efd453fcfc19b4aa928a750fea04fbd`  
		Last Modified: Thu, 18 Jul 2024 22:53:18 GMT  
		Size: 147.2 MB (147198664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aaf34279255dfadafa3dbef10bd94dd8db4b6b8ac5768dcb5f787ea8b5893b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5506283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c75204e9627b2207273d37e732719ea8ac1b7b9d566cc22a02789c6ee649f67`

```dockerfile
```

-	Layers:
	-	`sha256:3066fa2a151e30999a0336453cea2362ba544393ec77612c80259536438d64c3`  
		Last Modified: Thu, 18 Jul 2024 22:53:15 GMT  
		Size: 5.5 MB (5496913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6af15c7cc66d277ae43f1dea774c004cc3f2174535ad2820ca8a02c8bf4db8`  
		Last Modified: Thu, 18 Jul 2024 22:53:14 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.in-toto+json
