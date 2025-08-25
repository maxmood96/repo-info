## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:b5361b65da5ff9cda1b90d8bc980d0b1a3bbab5b40c57b27d68c62570f73c4ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e4e6eac4686fe83a131d0575f0da7078f473ab65b5b2d84fae39aa7cb7ce498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218017441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79ee52240f9a044e7175fc5b70a265b7b7517d4558b52966088918f1d16705f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72aeed506f7ad581538b16771f238dadf6a5410c7566b77eec2c5509ad72bd80`  
		Last Modified: Mon, 25 Aug 2025 20:18:22 GMT  
		Size: 155.0 MB (155039316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c1f87d60a2499c52a54dc43d9a90b59f3d5b8729aae3b8076482105d4b8700f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7146d7b4024033580d79cf4f6e6c6d6b4d2da9cba1e754e1f89f640a91ced2`

```dockerfile
```

-	Layers:
	-	`sha256:f9b66929a07161f8596ac7319f668165c3ff78e824db6f6e49c1e8d7c78a43c4`  
		Last Modified: Mon, 25 Aug 2025 21:47:25 GMT  
		Size: 5.7 MB (5683301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:316a32765a4e78e45525cd5a93af0e551b90952746fb2b933df04b25015f2980`  
		Last Modified: Mon, 25 Aug 2025 21:47:26 GMT  
		Size: 9.3 KB (9330 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:89044beef27bf259f98d7abfaf951c62868aa90d3c17b5ccce85b67e1b9b8984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212129512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5743ef10f30fa9ea45bdf3b7a652d9aeea3e1cca0272af9cc382bae179f454`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c49dc17c629648cf0aa9804df7729b43b9edb508c7ed317807628cc8fb7e7fa`  
		Last Modified: Thu, 14 Aug 2025 09:47:30 GMT  
		Size: 147.3 MB (147335148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d08fd21d6279d727d4813f481c264528c1f4dd0ebc8dc47e940ab14ad2255e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e440c191fa12995c89f82ffcd78ff4521f71bebcde52855c735b8064e4711ce1`

```dockerfile
```

-	Layers:
	-	`sha256:223b5eb520577f6434c2ab61a2d9e42d5c9fa80e59e49639655c5ec865016a67`  
		Last Modified: Thu, 14 Aug 2025 09:47:27 GMT  
		Size: 5.5 MB (5501769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:611a4d4b9f0e9139d89a74b75f1ec28be023c51e3d5ad935fbb27b1865ed8fb3`  
		Last Modified: Thu, 14 Aug 2025 09:47:28 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
