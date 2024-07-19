## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:a63766ca304149c53a75d82237b48c2e7620cc86dcbc36af5fdaa3889432da96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6e41009e5331a06e7af4908e169ecd4ef450b102ec760c0e60242f065b32c2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217471422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd167e14ee5fec3fdd1dbc64e8da1ee42f50ebe6fdd8203ba0a2ba658fe7533`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
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
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f8571015ec67df8a24ec201ce8f27adb1d3aaa47e6e42fe898c8635559e5e`  
		Last Modified: Thu, 18 Jul 2024 21:49:29 GMT  
		Size: 154.8 MB (154823496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4787a848370d0fdd714d637631bdce6e28b4aea9d82c084b8fbf106a53b509b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5687834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29f6c8aedb810ec3a71bcaea109c63c0bd41ac512563d26ecb7125a8419587c`

```dockerfile
```

-	Layers:
	-	`sha256:1d6fbccead90d26f6d6bfaca3806c44577aa595c4f6565797c0a4bf004b948ab`  
		Last Modified: Thu, 18 Jul 2024 21:49:27 GMT  
		Size: 5.7 MB (5678742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b108442ca9e560e76562e3fb2e7752c0cbd0248d59781f9f820ad23497822a17`  
		Last Modified: Thu, 18 Jul 2024 21:49:27 GMT  
		Size: 9.1 KB (9092 bytes)  
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
