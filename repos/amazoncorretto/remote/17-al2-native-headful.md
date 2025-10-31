## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:e594aa490e9633b1041721e31b65b29dfd7f6dd06019279ce82455a10ea04058
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1cbfca3a0c6a1e5b344b73b82a250d42099ee5f55e7db2ca40e2cc3334a98f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154200433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ae5a91a858179828c2512c7f4757bd01927e8df72f0fe94ea71f82a73f5ab2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:26 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:26 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:12:26 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc54994913ac8e299f4924c0b789d89ca1e2532a1595e9d938e2aff82b7b41e9`  
		Last Modified: Fri, 31 Oct 2025 00:12:55 GMT  
		Size: 91.3 MB (91266365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27e9d59e128b173f7d24bd9ff2fa3f1864ba96a87b9e2c0c2c85b8d24a4bd8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82ce6bb0dfb69a4ad9d794b473882be62014b06e184f8164474d099a4ece1ff`

```dockerfile
```

-	Layers:
	-	`sha256:ca39354592109004178c0bab9fef7282d63f1e5020c7650d08b4d4b969b73a64`  
		Last Modified: Fri, 31 Oct 2025 03:48:53 GMT  
		Size: 5.9 MB (5865820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99c452948d4a48455e0682b502d2c9acf8e75e0fa85f67cf6ce1767bad53679`  
		Last Modified: Fri, 31 Oct 2025 03:48:53 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3afda461274cbce6bd8f5c6e11de297c7d54e95c1ce23ffaa338c37d3eeb816a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146786952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1fa03a57f330c76f9f08c265b8751986633fa4cda80132d1f80a63b3b495`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:35 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:35 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:12:35 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f05e6a68a9609358497f14c50aba4aaa942bc27f7252f3a7956247fe90a5c11`  
		Last Modified: Fri, 31 Oct 2025 00:13:06 GMT  
		Size: 82.0 MB (81993494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0fe59eb3402646fcdd3c72796655b9f4af4e00405ac9e0aa75b2d44a25d6d963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02332049fb69c5b0d2fe3a340c90431b98f46501ac18d2df459947aef6a7c1a8`

```dockerfile
```

-	Layers:
	-	`sha256:e4cee2409e51af464d8109cf38feac0d9fa55d29f6e752aa905f7c52be35109c`  
		Last Modified: Fri, 31 Oct 2025 03:48:59 GMT  
		Size: 5.7 MB (5657563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b452b7f71e18e4d1f43d0793d73b9506f883b9e9357e53e46a4fef324766d4b3`  
		Last Modified: Fri, 31 Oct 2025 03:49:00 GMT  
		Size: 9.5 KB (9509 bytes)  
		MIME: application/vnd.in-toto+json
