## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:f18bef23fd4113fce0e2570516bf80fa38cc083935385995d8e67df15c6de958
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0d7cf384405215a9fbc51f4aec7539edaa1ea3fe323243b01840f1e133bc04e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188007928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2fa1f72583bee292360e59e1e199c6d9dbbed9d311239db790e85f9595955a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e77e238c4b99a2c23b22f26dd2bf0c7794ffff245b94322c8167aae533e32d`  
		Last Modified: Tue, 20 May 2025 08:07:27 GMT  
		Size: 125.2 MB (125247943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2abb04011baf67b8ff9d5f1ac809de9c3117b52ba3de00eb07e21d780efb6ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7982556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1de38362912c34ce8e542f790742044d1458cf14f0ddd55620075e77100169`

```dockerfile
```

-	Layers:
	-	`sha256:5d5f7beeb89f68bbf03cb543c4c8d2c009273e231d379c496b010833e4b16a1e`  
		Last Modified: Tue, 20 May 2025 00:50:41 GMT  
		Size: 8.0 MB (7972964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72df53e1518c25316356bf7d89b03bec312e21db27127d958c19a1300a86e4f7`  
		Last Modified: Tue, 20 May 2025 00:50:42 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d2e8e9cdb5687039c9a8cdbddbab19f0ad9571b617c357a65a8d51e7ac5692ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132155645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c11b417b20697b0ec6a7200ea78e5636f8324756782390fb55c50bddf8d3c3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=1.8.0_452.b09-2
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc906cb9de59241cab72f3e75c841c9d754cb570c35df8bbfc352036be69151`  
		Last Modified: Mon, 19 May 2025 23:50:01 GMT  
		Size: 67.5 MB (67548164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0b3c151e77f9fd17c2a8e248c49e2bec06411735865a91e228feca17c6800a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6088175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a30c0ef8bb585449c960a646100a773d1b2a5f765d35442cf4c8c4e483921c`

```dockerfile
```

-	Layers:
	-	`sha256:87cce5a4eab37c156f34027fa34012303530b294e1f6c3b8b4021fd7b67ac1f8`  
		Last Modified: Tue, 20 May 2025 00:50:47 GMT  
		Size: 6.1 MB (6078503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6705c4dabe699d953127d277a2898e0c75959a5f96c9eab03f6f25bd8300344`  
		Last Modified: Tue, 20 May 2025 00:50:47 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
