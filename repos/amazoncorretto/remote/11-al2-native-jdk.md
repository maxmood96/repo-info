## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:f46ab0ad9ffa5c706c33519c8c58891b4d1817acf84f58180dca03fcd8e19ef5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:01bf89bbe2b4c49f5d5aaf86601a75ee048ab8e0b875492483fd021b64ce964f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224609030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef07f7eb9a15689a85e453ed3a809e993dbebb1627d53813f9efd2ec884921e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:47 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:47 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:33:47 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b2a8ef82c071abc36c53a68b940ddf1c729297017728cbeb68a3459f2528d8`  
		Last Modified: Wed, 22 Apr 2026 21:34:10 GMT  
		Size: 161.7 MB (161653764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b36a73a2af39094b0fde1d8740f7e230ec2b87d93dfd972eaae1be58bbcee32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86589f187aa71cb8b38f4235347acf63470c778ac49189bd40104f18f9e1d0a`

```dockerfile
```

-	Layers:
	-	`sha256:25080746982e6642d083789e93fa9accdf5043b1314c03ad6894f203975c724f`  
		Last Modified: Wed, 22 Apr 2026 21:34:06 GMT  
		Size: 6.0 MB (5995185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636a13ad884b73808d9bc3e94c437ce6f99d714c3bfba2f330151b025976c818`  
		Last Modified: Wed, 22 Apr 2026 21:34:06 GMT  
		Size: 9.6 KB (9558 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:536e8b952c6b8b771602a9355b9092042a6f5cce706e6d2ccbeaeb107acd292e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216539201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55228599f39fda435410f9a502da876653502349596007c6a39b0eb4c01311b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:33 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:33 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:33:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bde8049704b54595f9583614c448df14e4b2a450c0d5aa3d1905a498bf60a67`  
		Last Modified: Wed, 22 Apr 2026 21:33:56 GMT  
		Size: 151.7 MB (151736226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c30564dc6359ebd5bdb81e6c45bdbd2bb0bb7b3c0fa9c0b56a6e97b381148589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def480ec2d018cc1a0d49e7209a12591a9b49cb434b3af834732b08643701ea4`

```dockerfile
```

-	Layers:
	-	`sha256:138c8ac89d470cb1f8e67add8acc3ddf95662af31eacfc34b59272dd61143a2c`  
		Last Modified: Wed, 22 Apr 2026 21:33:52 GMT  
		Size: 5.8 MB (5787899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc05952eee9ddae9ae2017fa7e76cdad01c6f2d00f50232225e027139c1694c`  
		Last Modified: Wed, 22 Apr 2026 21:33:51 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.in-toto+json
