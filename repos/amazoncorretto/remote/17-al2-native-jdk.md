## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:b9ec86e5207a55d405de75ed81a3f27170728462b4c4f3ea63c00376525d4622
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bda756b07445c78ff6802f8e4386ecc6177f8582b8c8a4fb2b23e9f0a5f037ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228274948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b57fa7e8676384f429b484fa1a5c4d8107bcb445cfc61d34d236ff107167d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Wed, 14 May 2025 22:47:15 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa747e16ae731586c826798095fa7e61954d22b815a82ac631b5eb466c84a274`  
		Last Modified: Mon, 19 May 2025 23:37:33 GMT  
		Size: 165.5 MB (165514963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a1d92ef8974d83dd9f66bd652d34df3e8f4c10626cab8d936a4a18d833cd4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5977333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b702a19cc96b2fc1a6b02840633c134cb78a920796b1341738bb2e76134fbd`

```dockerfile
```

-	Layers:
	-	`sha256:c26a745fc62964172e15a71fe167b2b9ea4962a2457c67ebc3f400d4a65483a4`  
		Last Modified: Mon, 19 May 2025 23:37:30 GMT  
		Size: 6.0 MB (5967376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd5251a56d963408b7db6cc21686edb8e4b8cb7958cec0f75740a3c0f884ecd`  
		Last Modified: Mon, 19 May 2025 23:37:29 GMT  
		Size: 10.0 KB (9957 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2445fcce9fc36a117d8c5da38617e77270b7e2dd230f8f76839fdcf823a0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220672804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8876d7911c6ec195d969f0a4e2b4e647ad59d87ec7bdbd90a65b6b91c7caa74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Wed, 14 May 2025 22:47:33 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bf996562dab5133933df2ce4baba45a62ffd1e78e68fd9ad027ed15c58f50b`  
		Last Modified: Mon, 19 May 2025 23:59:41 GMT  
		Size: 156.1 MB (156065323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9f750c21c30f8e2e4890ca0e69b2f12073eca5b69f38f6f45af24129f61e70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e87a3b6a4125f9f795da71aeb9bd6152d183f7bfe6a506d62085ca1db47c740`

```dockerfile
```

-	Layers:
	-	`sha256:7193fe358fc8ee23b76160ed625190509b0ec315c14b7014a7d55e5b8273af6c`  
		Last Modified: Mon, 19 May 2025 23:59:38 GMT  
		Size: 5.8 MB (5759246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:885003f3a329d837b9fd59c35a732ef1ceb7eb140293ac1de1fcd2b6463e1203`  
		Last Modified: Mon, 19 May 2025 23:59:37 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json
