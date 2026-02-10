## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:185c2c8b76a84c3a578c9101fab4a1b5c78e37de1d84c6af241e6945b6151c64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0343e72da99f5910a441c6bd6543d26dfe1747f9f420e353b783691c2ca426fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150542245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3dd1093d60ef9773a4c72a0a996de6f88be1ed63c68fe908fee5b0beafca66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:45 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:31:45 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:45 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415e6de4ef482139b980c6c21014ba1c2e821579e3b99056c91e13abd6e584ec`  
		Last Modified: Tue, 10 Feb 2026 18:32:04 GMT  
		Size: 87.6 MB (87583288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:04a9753ec22db3da2ecdd1a5aa008f5f230d9fade187e02fb73895695c2c1eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c42e0ab5ce84335920662f009e968a7158f9f171f9eaecb23811a6a239bb923`

```dockerfile
```

-	Layers:
	-	`sha256:090e83b4c0b59775238f6f0790e5f8cbda28f0b3898db3bfe08b67f4e78664fc`  
		Last Modified: Tue, 10 Feb 2026 18:32:02 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf3bdd05b182d49cd97e0b7f393f0d40ee116f7aeeba8d98c5a44e28ea63d8e`  
		Last Modified: Tue, 10 Feb 2026 18:32:01 GMT  
		Size: 9.3 KB (9293 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0635ee632659e941e5d6abd2dd6101d9ac0893e633511fdb0d90947f09ae94a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144647314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e59c448c34bbcb04e79a518d71c0b53f776f10aa96609b050923e055da37a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:22 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:31:22 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:22 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dee5905d8eeb3aedba7b68f79e846060ddbcc994223f93881bb9acb6aaa1a6f`  
		Last Modified: Tue, 10 Feb 2026 18:31:40 GMT  
		Size: 79.8 MB (79847838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7073273d339261e99d022d2a3dced25566939ff1e0859db89a3fb15bea16e2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3d49ff7279f77c3e168ecc1faf4385ca9c68a2af9914bb15a3ca72db6e1b03`

```dockerfile
```

-	Layers:
	-	`sha256:ab88aac0f43eb4ae266ead17b098b8ebc2ab7175c8511e8babbc1959f394b929`  
		Last Modified: Tue, 10 Feb 2026 18:31:38 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2101ff1aa482f1b30ba6c0924f3ea46bf00292e3e1bc2892bc8e5269594f4610`  
		Last Modified: Tue, 10 Feb 2026 18:31:38 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json
