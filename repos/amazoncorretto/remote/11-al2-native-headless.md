## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:4125b548130ba9a2dcd7c0ba74b6abe2a70a85cac57f2ce054f86e7539c86816
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e890cc975163f1cf7b3a75501e448e26e3218f9b22162caf29d92d2c3ecd03de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218025137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ab8e679e4e44fd0e6b86ab3b3751da5123dba36c17f7db8d3caf0ab08e5fc8`
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
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ec4ac01df0260d20f94f370e3d27eb138456ba2efe3a3eb4fc28971812aba`  
		Last Modified: Fri, 12 Sep 2025 01:10:21 GMT  
		Size: 155.0 MB (155041849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44f4e873b9c52dca8949e9beb4f4a1609fd407691132ab30c2bfb1d55422a209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d776b3067951c2673c3470334a29205cb5b5052601b312b7375a7793281a1d81`

```dockerfile
```

-	Layers:
	-	`sha256:b6a2104c8be425f2d934947ef83d14caf30d6fb7b3f83687fe8719eb1dde1021`  
		Last Modified: Fri, 12 Sep 2025 03:47:33 GMT  
		Size: 5.7 MB (5683301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be1427adab9032367ff831238dc448b6c706dc0bab2ecef1215069d71592abdc`  
		Last Modified: Fri, 12 Sep 2025 03:47:34 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4f7c459a2c17369c18ec2235a2b849a08ef07333d2c9ab3ef530753af1a5c58b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212125556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46890e02810f15af4572b77d943591b1535cd840097ee31920b1ee3154cb136f`
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
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe8daba7461ad27381f982303abe253db2bb996734c301f32c1d273344fadd2`  
		Last Modified: Fri, 12 Sep 2025 02:10:42 GMT  
		Size: 147.3 MB (147333833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b0a691627d9cbc254ea3386ee176a965c57ad2ed25c69e91a51a65c5a8251bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba95320ffea127a0999b71fb01336c005ee6d594d85ca03a0d8e4df87181a797`

```dockerfile
```

-	Layers:
	-	`sha256:0f96645c5e17440cf8178a27db5182d5b1033ecda784d91eab2bef019f74cf1f`  
		Last Modified: Fri, 12 Sep 2025 03:47:39 GMT  
		Size: 5.5 MB (5501769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b28d651207fd51ac1dedf68229acd412c822609e962a39ab882f02daca067c0`  
		Last Modified: Fri, 12 Sep 2025 03:47:39 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json
