## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:6e1d17cd73474b5508a61d8c757a30a17e1f9c1fdc389b286d291d53bc388aa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f74e0268a0c2eecbbc7bddadbd8c8d8db7461d0143dbd47e962b559aec81e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154246689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89207a7ac085e2c49050c5826272dcd65c5ac3f4205170564c435b82c4de2ac9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:08:55 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:08:55 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:08:55 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:08:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aebbf3ea37cb38ce84c6877225452947ff5b96e6fca3c03888017d1db2b9e41`  
		Last Modified: Fri, 03 Apr 2026 17:09:12 GMT  
		Size: 91.3 MB (91290179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9e54dcb5489feb31490a95ed371f672acf3f9a7c31596c0f1d69518c2bb423ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d863e691741bc47f33d11193c35bdf0af1c0c95c38259815d2cf3270e2753f38`

```dockerfile
```

-	Layers:
	-	`sha256:4aea017126160551904eeb340a27c494c62380fda4bb50e493bad029de8305df`  
		Last Modified: Fri, 03 Apr 2026 17:09:10 GMT  
		Size: 5.9 MB (5865818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c3eeeeab0cf66513dc94e39758487630d0f1cf819521e23e0d006e7c5f8980`  
		Last Modified: Fri, 03 Apr 2026 17:09:09 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8dd0e667282c3da96c0e5d7719fa75a2ef04bcd81e2936ecb08800a2116206bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146791124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbd82fc16c391e6db8929e280c37090a9c31a88c51a4032f46a4465c4704c42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:16:35 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:16:35 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:16:35 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:16:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173790de5aa6e1a16337b02c3ed858162f207b1bef57a6a441caca2755c40b0d`  
		Last Modified: Fri, 03 Apr 2026 17:16:52 GMT  
		Size: 82.0 MB (81987975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e534e5dffff5859934cf86f81d49de9d57ccd022ad2824121975b9b4867f1804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96afd2b851609b37f4b7f331b113479ebd32c2af4f3cdedf38caf6595cd8238`

```dockerfile
```

-	Layers:
	-	`sha256:46bacd89014de0b1713551411f3f7700b0ffdf77f7430665a1added15467b03a`  
		Last Modified: Fri, 03 Apr 2026 17:16:50 GMT  
		Size: 5.7 MB (5657561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad893ede0ed8c9e4ffd5542672869a8a588ff37d2b2675d9e7659e0fe0ff17b8`  
		Last Modified: Fri, 03 Apr 2026 17:16:50 GMT  
		Size: 9.7 KB (9665 bytes)  
		MIME: application/vnd.in-toto+json
