## `amazoncorretto:8u472-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:9722b982955042bfdcdf7d44cebcc56b16387c70c6f10154c5a522a482585b50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ddddfc22d25ed9e393b3a3a7ca32e64a62b423f8f773866e0d77e01c6a181b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188194787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f9df3786ab4fba9c7bc69d6986fe41e355fb5fc48cefae0b723575fc04a9b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=1.8.0_472.b08-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fa57f679e37685a3c3e8ca879507dabaf664b648302b3d78d4c41f70375ff8`  
		Last Modified: Tue, 21 Oct 2025 23:26:48 GMT  
		Size: 125.3 MB (125254167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc958022ff73cdbeb800757ff32ec7fa4ccdb17786863fa56ae4ef771ac4920d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f265b425351b43cb232c8693fbfc3f248fc2ff0069b8057504d12d2b39afc840`

```dockerfile
```

-	Layers:
	-	`sha256:60f39f2721512aed01a047fa343ec4569be9f99479910d1b6a8c70ee876bfad7`  
		Last Modified: Wed, 22 Oct 2025 00:55:01 GMT  
		Size: 8.0 MB (7977414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6079c54db7dd9db97b55fafb923e3ddaf0358d9c7305aad51d9a7b3f133b099d`  
		Last Modified: Wed, 22 Oct 2025 00:55:02 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:69fffdf1de814410c4e32a848910aec473b5e0a2e820839bd59333f86697813f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132358100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed03c56bdeb32898aab6da6592334168fd1f976202700ee9f2ba9a28e06efe91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=1.8.0_472.b08-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b479b48b34d51ababacf86206350535d2285e5f486e71482434126a8af4e5549`  
		Last Modified: Tue, 21 Oct 2025 21:49:23 GMT  
		Size: 67.6 MB (67564892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2b2a4a42ac3e9ab573a2a39eb14641ec89cc9c71a4ac959970fe95a4c518be49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1134d63c28dbe0f2be4645205d1f8cf46c06a2057c20abf3ae0bffd89ae4d2`

```dockerfile
```

-	Layers:
	-	`sha256:be9093b7fa97a1d17950a609d6e944ca6ffbfa65f7afb69f1a264677f4641e8f`  
		Last Modified: Wed, 22 Oct 2025 00:55:08 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0409e1a31512fb58efa502d5e9e81ebc58c1fc51c5f8190ced65660ff35b9a6`  
		Last Modified: Wed, 22 Oct 2025 00:55:09 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
