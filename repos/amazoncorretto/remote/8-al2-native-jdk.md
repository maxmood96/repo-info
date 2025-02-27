## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:ab377e2c8609c40820ac587dbf055eef97666ded70264ef6b5c4ba8644cd3722
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a14238bc83a4e566e480b05fcf44042ce3dc3b49bc0e7c7bdc9cb4006bcd82ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188044579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efffd6451985c71ace898c8909c3fe9eeedf99a66144d03aec0409dd85eeb58b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f70087326caa943bd232e49e0d0aecae86acb440a4a1bb57308ec63acc7749e`  
		Last Modified: Thu, 27 Feb 2025 21:08:47 GMT  
		Size: 125.2 MB (125242537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cbc3b42317817ebf8fe9a8feab511b40714baa9676105c8c268333cfbba99a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98e7f47200d352e31e0973eb3232ddd33a8a9176e197925557597e73cd5e8b8`

```dockerfile
```

-	Layers:
	-	`sha256:458864bf7fe230547eb4ddfe3f5467a1053af84b47ce353e51bfa8ff4d19ae3e`  
		Last Modified: Thu, 27 Feb 2025 21:08:46 GMT  
		Size: 8.0 MB (7956594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8f1172fe3a3f36c60184dc1b2cbb09eb90cbe77b10e7b0ef562a0f4e45e917`  
		Last Modified: Thu, 27 Feb 2025 21:08:45 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0ba76d8404612bfdd1129bae3b6159c63076aad61093ea3115b34b1921f29dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132137430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e18f9d17d6aa5c2bb48320dadbfa6f25fa116078ae0a64c9fc54a725e29618`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012725a66347fe7f72960e09c2e1dfd8eac6b11176c8f40f5a0733a9d187e63`  
		Last Modified: Mon, 10 Feb 2025 20:14:20 GMT  
		Size: 67.6 MB (67559208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7e9a1a7ffc49ff969f4036a6fd42038beacc8cfa7c49ff3dcbb818a1d6013964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c70e1748285a9c095863cf422b18de4a63e7bb8db8fe82ee2828a297ce1155`

```dockerfile
```

-	Layers:
	-	`sha256:e178bdedfd7503e2adc6966e14d8077c4dd3745da0b30cd30f7adfa4e673e5fa`  
		Last Modified: Mon, 10 Feb 2025 20:14:18 GMT  
		Size: 6.1 MB (6066679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fc03530fde3cd79d25d31916955527fd58bfa9efd10c1af05c6be4d84c0a8f`  
		Last Modified: Mon, 10 Feb 2025 20:14:18 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
