## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:f505ebcc4c344cc4a42597c58a2e4ea60f8369292116a7f760df0650ddebab1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f092b5a0a310927bb75c23c1db44200d3b56f87166b1726849465534519ed391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188281320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b91ced7bcdace8fa66ff0341666df085c048124e0c20820f22877aa1092020`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8af0c705451736d3bb2342429418cec6340ba37eb9dc3fbbd5bf2dd4b69e7e0`  
		Last Modified: Fri, 12 Sep 2025 01:10:22 GMT  
		Size: 125.3 MB (125298032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8a7a6f0af34c3cbac20d03c7e87118c2a549e654fe34979bddebfdbad0e3e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff43e0af38e5b6002fbd649a0da190a88bf88b7e8a5ed349026373f379c77dde`

```dockerfile
```

-	Layers:
	-	`sha256:8b5cc9ae075d432d68fdfba8abcdc2b37b6be5b93409711ddfdcfbca377a0e36`  
		Last Modified: Fri, 12 Sep 2025 03:51:52 GMT  
		Size: 8.0 MB (7977414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf9fc409a046d04ab77a03b2cbc6811c834c7ee41f44cd9a15784f39a510be2`  
		Last Modified: Fri, 12 Sep 2025 03:51:53 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d9561ecf7e98cbb0725fd8af956a87b7e57ce886700c661577f65ceb55c0b8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132338757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e39dc001aaa3f5574ee288c174b43b433b98cfb51f50bd4956b6418725c5fa0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3385cdba6a22d023a9179a85b08c139fbb404f122c66d9683844dfa971158a5`  
		Last Modified: Fri, 12 Sep 2025 01:11:43 GMT  
		Size: 67.5 MB (67547034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b908112c27ba52d1320ae801ee6f3fa7a960dfecaacc476321146a25e6ad7678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b759d103a6af755d444050766b7b3f692de3ab01d586575a86d8dc49630a63`

```dockerfile
```

-	Layers:
	-	`sha256:b1dbeaeb62377a822cb94bf2918f7cb49462923e96326064facfda7fad56ab7c`  
		Last Modified: Fri, 12 Sep 2025 03:51:59 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc5de6d5ac650709ffe1d1cb71ab0e82dec30bfb2154cdc3131b4aeeab0d46aa`  
		Last Modified: Fri, 12 Sep 2025 03:51:59 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
