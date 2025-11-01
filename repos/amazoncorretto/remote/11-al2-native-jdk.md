## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:adb4ab3b22e9a5a06077ee9005a9d44e4fadbced52f5d9697c734a26c096472d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3e88c364ddfb9f29201d825abc4a49bafca7d20a2437ddd70d69a80ae2dd2caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224516277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ea13f756c8206f1d2dea0fb528a4be253409523220df4df81b6b55d4c86110`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:58 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:58 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:11:58 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1000fd89801fa9a5ec1dcb5ac05fb62c6ede03eb5d4078ef53eed51af55ab2`  
		Last Modified: Fri, 31 Oct 2025 04:00:43 GMT  
		Size: 161.6 MB (161582209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:11a79e78fff321c7c6f72d13407a7622584615434bdfef71bcb05c629c890d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87af0deb5bda89fcbee86d72ef5e246d344b98eb7995a5eb281d207889b01df7`

```dockerfile
```

-	Layers:
	-	`sha256:37e3e59ee08f57bbe6ac8c81db5b29c75e31f11fe0d37601d71be8d39ca06adf`  
		Last Modified: Fri, 31 Oct 2025 03:47:39 GMT  
		Size: 6.0 MB (5995078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c8908440b92d63c600b7b23e9b0bc030de591fe607a17bb2a864a5c687bd0c`  
		Last Modified: Fri, 31 Oct 2025 03:47:40 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ce538d52bd0df000bb1e3cfd977897675ca61b9ed2d29fe885af5097bcd3cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216446040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c010b2a0794fbea0aa8ff2d314ec438b7d167f1510432bfae66aacc0f73cb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:17 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:12:17 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:12:17 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07facbef2f00cc79eb71d219748d2ed727e269278e639ede4538caddb39b021b`  
		Last Modified: Fri, 31 Oct 2025 20:29:56 GMT  
		Size: 151.7 MB (151652582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d8b90c69451fda5c6151f6552d933159d4b88c2170e31f6fe9e20ec8fc0bd2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c9ef8d6d1632f99b76e8c3afc793fbdd4506b1cad5cc5f61d5bcd0a91e68c1`

```dockerfile
```

-	Layers:
	-	`sha256:a522031d7467e400ca61c4d3763f0205eb8f52f92ac7bf40f32c657b3b42ccd1`  
		Last Modified: Fri, 31 Oct 2025 03:47:45 GMT  
		Size: 5.8 MB (5787792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a77a7f1621d057cad3c2f07b9ad1d204520e6f3b2218900fdc7d2afb9412c0b`  
		Last Modified: Fri, 31 Oct 2025 03:47:47 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
