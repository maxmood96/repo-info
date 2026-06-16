## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:c62cdd12789cb5328cdc962f8b05fbf18e8f4d732002270ecc626ae45fda762a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8be9f20e7f97d334803b1f3499675fa076e3eaa571f2870d93fd48f5736906e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154343780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2769e36f7f900ee1bf97f417792e424e5ee0d474296e4140b3179539a581e2f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:42 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:15:42 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:15:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85245287b1cc78c8360289f07a950c952de878ed9ebb24985d6f7ac328d66d`  
		Last Modified: Tue, 16 Jun 2026 01:16:01 GMT  
		Size: 91.4 MB (91401830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75c2d699f10346e03670d6086fbc590a9ed1abf1028d52c22081027fd1b4e403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5876330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034bb5ccd61360a853771bbd37e2ab24605b2ffd31ef1a45259d9bf7ec2c22cb`

```dockerfile
```

-	Layers:
	-	`sha256:b30611aed30aef6a1f7617b35eb1cabdbf164846d2f6cf6894cbe1edd7568140`  
		Last Modified: Tue, 16 Jun 2026 01:15:59 GMT  
		Size: 5.9 MB (5866740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0aa7a3a5dd31651c8288d0bac63f7c044ab9eca4a4a78e8709970d51940c0e`  
		Last Modified: Tue, 16 Jun 2026 01:15:59 GMT  
		Size: 9.6 KB (9590 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:af02976aea16834dc827567756887709be2ea8be5c812a42650d6e13be89b0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146884968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8269966e9acf87be289f92ab2bd3057354686575046d33e65593b2f5c827e039`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:43 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:16:43 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:16:43 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb887b732ef3050d1abfe30d7d77f7f5b918087148d204fbff49da87866579`  
		Last Modified: Tue, 16 Jun 2026 01:17:03 GMT  
		Size: 82.1 MB (82094259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6c4499a0c48124efaf2db30a45f5f732766834adcaa8b06187a90f162b379fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2bf4bc8db3dfff848ba9c91ccb74c899e1ea2fa0f9734b7e64640c98dd8f29`

```dockerfile
```

-	Layers:
	-	`sha256:e9d135ff77f6329463cd7953abf64d68abb631ff012aac9c6ffde245b38c4976`  
		Last Modified: Tue, 16 Jun 2026 01:16:59 GMT  
		Size: 5.7 MB (5658484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c110d1a64a1d1353444bc48a765b8cf1622fdc32a9067e11f296ffd18937c96`  
		Last Modified: Tue, 16 Jun 2026 01:16:59 GMT  
		Size: 9.7 KB (9669 bytes)  
		MIME: application/vnd.in-toto+json
