## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:6bcdfb8b4844eb0fabbc9c5fbefbb08baaaa4f35379bd8da1123f180cd66bb9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8688af1471db77718215728a639814537213da0c3911c09459b35d357a3de152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228715600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20167545d11543908b2777e6ea8ed84ca112b9cc1c485768fa5887063856773f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:50 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:50 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:14:50 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c1f2e52367f3bdc679c7fe1d8e01f5f5e1f2396b9e8ab7d767dfbb482affa3`  
		Last Modified: Fri, 03 Apr 2026 22:15:11 GMT  
		Size: 165.8 MB (165760299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:93fd687028774656e804f57bb84d3abd431b3c532b25ac5bbe3cbe4bc19b02df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00c69c867fa059d407784417d5faad2e5dda666f5a2d80ac880d05e8f3d5660`

```dockerfile
```

-	Layers:
	-	`sha256:7a918ba387b0e7f5d45f3b357625c381d9d00e53604441ec19153d04f7ba59d0`  
		Last Modified: Fri, 03 Apr 2026 22:15:08 GMT  
		Size: 6.0 MB (5971911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d615bcc0d25df0e43ebb90bd4d80a86df4adee7044a7d61a5a0598591963be6b`  
		Last Modified: Fri, 03 Apr 2026 22:15:07 GMT  
		Size: 10.1 KB (10055 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:753ea404e7ba41f569f655eab525ff44de4bf31952717b231746182f7438d73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221073472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e64aa59a9bd4239dca46cadfe330c107a60a48fcd299f9388af27828ed2ab4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:07 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:07 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:14:07 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a33fb304f92f9497faff3fe31eeb25594220eb6f571a55e0fa048cb97225e69`  
		Last Modified: Fri, 03 Apr 2026 22:14:29 GMT  
		Size: 156.3 MB (156270633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ed70898f2a7112f5a7fe5ef56b40f55d6ba3dca9f626dee696a4429e90f632fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56681a870e7d3fce9bc0b2b61ad3e71e37b5ac45f5ee3bcdb9fe45873578624`

```dockerfile
```

-	Layers:
	-	`sha256:2a1607273c3ebbd545511e6fb4c22364a58b247076bc57d94ba2a76ccb706acc`  
		Last Modified: Fri, 03 Apr 2026 22:14:25 GMT  
		Size: 5.8 MB (5763781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa59fe4bbacbc342c63c0ff72f4bef8c06b11ad6b350f29f37803e82319c9c80`  
		Last Modified: Fri, 03 Apr 2026 22:14:25 GMT  
		Size: 10.1 KB (10135 bytes)  
		MIME: application/vnd.in-toto+json
