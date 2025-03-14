## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:bb75988485444de656f977f852d51d2f91b5fe70c04b6cbfc16da6faac0c5fd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6a75a3830feb9859768309b282b1831e93892cb7b45d80f3c6bc50b9f29d3316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217714806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0995c932a8e04cc25f8012cde3a744facafa2188c6b28837264184af216291a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6922de3dab6e60bd9230fbf6ee33f20a87d33903d8a76bc02754248b7b1fc4`  
		Last Modified: Thu, 13 Mar 2025 22:53:23 GMT  
		Size: 154.9 MB (154941968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9b43f94b1fd806ad50317000a83f4e71f6e44b8e65c1441524b923cf26179102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5677084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6205e35e5c8e6d3522fb411f53cc4084dc57da3c3842fa83344247fd7ed7c107`

```dockerfile
```

-	Layers:
	-	`sha256:a19e264b65fd9e5890e3edefa6a3e7243637b008a570e86155320d62099960b3`  
		Last Modified: Thu, 13 Mar 2025 22:53:20 GMT  
		Size: 5.7 MB (5667753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d9000e0106a0ab731cd3584c4b5e0f8f6b93ed81bb62da7dea226283c24376`  
		Last Modified: Thu, 13 Mar 2025 22:53:19 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5b4666e8b253b95e1c360cb3601df1cb58acb47c76a22b251149446c5ba9139f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.7 MB (211686875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f16705bd148114aeb53baf66fe84ab438db864e948d4fc254b2823f3fe1a96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413898f3a90d0d75722a5159318cc9271c57eda8ae67513db57d539972711f77`  
		Last Modified: Thu, 27 Feb 2025 21:13:57 GMT  
		Size: 147.2 MB (147165667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:697bb3e580347d16da328d0786be04a608a90b608450afd46b4c05c3cf11625e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5495632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa3df12e270c9cb22bbca0c65174d7ba69535dba17062bb0acf9d186aeec7e`

```dockerfile
```

-	Layers:
	-	`sha256:0079b9feaa781c7c5db4170e1e276156268b22747f4ddc8609b92ceb9cb779f8`  
		Last Modified: Thu, 27 Feb 2025 21:13:54 GMT  
		Size: 5.5 MB (5486221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48d6b5bae88a956426f824a9a64316517d4dbf8c2bf8f106ebd709b90464ee2`  
		Last Modified: Thu, 27 Feb 2025 21:13:53 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
