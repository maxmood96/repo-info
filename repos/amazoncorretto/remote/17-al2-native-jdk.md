## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:58b7f9cdc2f4af1bfbba7d7914e172d1fdf3e139e820179115e39184da39c092
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d778b9fdd902e4c1efd6c8eb15164a1c64267f2922d66db93fbc26a4f2ae1603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228677451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67addb64dcc2d8bd7b7d79b5042c6afc57f1d435a63c12e5a08975528d32a0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:31 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:31 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:12:31 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc08f9d96521ffe2ea412984a0440ba033448173657d0be6b78f7ab22aa8b4c`  
		Last Modified: Fri, 31 Oct 2025 03:51:18 GMT  
		Size: 165.7 MB (165743383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0381d963e5a6af0b0f11c0d9998798c506e2802e978b4bb7b4c95ab0d6f68b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a657f1c4a1bf5ab3a66c6d04e14e9cfd73c23bfe60b375d30f9de3dc25eb7b24`

```dockerfile
```

-	Layers:
	-	`sha256:f0bcebb29b7c5ca2023e89338f04827a42688b194ad39b83da71e0daa655b002`  
		Last Modified: Fri, 31 Oct 2025 03:49:01 GMT  
		Size: 6.0 MB (5971820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d5abbd77c6cff77f6291579743a836feab878c7c4e87259bfb8df19fceeab0`  
		Last Modified: Fri, 31 Oct 2025 03:49:02 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:40bd9c624fea39c87e90544b24ad0e7ab8f06597a4cb6f3a998de2c3be000791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221064491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969f5cb7ebaf792f73fd00714c4f96a5d3c3de69b0641afc9b46fe06244289d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:55 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:55 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:12:55 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cba21fa853b4d678ced9aa350781debfa6e92870b65387426aa0850a526bf6b`  
		Last Modified: Fri, 31 Oct 2025 00:13:18 GMT  
		Size: 156.3 MB (156271033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4c79618bf43d944d5d0243ac2b4528569664f582a757649e4ada20c78c603d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac883deb6bbcdd896e0265430d5685879e747b3b8b68ed758f2d2437c468677`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4eed42d74e6ab87d03e5c7a73f51285606fc8509f8f9b05cde4963061a5c5`  
		Last Modified: Fri, 31 Oct 2025 03:49:07 GMT  
		Size: 5.8 MB (5763690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eb4d411ea2373c35fd70ecc183caf712546085414c10e18fa8242168f00ff1e`  
		Last Modified: Fri, 31 Oct 2025 03:49:08 GMT  
		Size: 10.0 KB (9997 bytes)  
		MIME: application/vnd.in-toto+json
