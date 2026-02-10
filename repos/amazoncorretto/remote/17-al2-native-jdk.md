## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:70da85758fd430fcfb12d0c661072e07ea78783d6ead16bcfba32f90e02fc404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7c6736ec32e3b0077decbb5801e6bd28e681c9918c25cc9e59eff5d2fa9e3fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228711972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de84ae89651f81bca0493d5923abb1dbb62bab7866cd72d8722147612ddd16b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:03 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:32:03 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:32:03 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c858e997e57b66e7feee9cebc6c0f1829f3f4f8716d2276ded115d5dca020`  
		Last Modified: Tue, 10 Feb 2026 18:32:30 GMT  
		Size: 165.8 MB (165753015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:080be227a395facab5094415a7373e81d2f9a64db865f9195548fc62f7ea47f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bcf8649c4cc93fe56b0201e3fc5a85758154b5169dadb4834dd7191568a70f`

```dockerfile
```

-	Layers:
	-	`sha256:765afc875d56b49bcfa54a5179b0a48f963a314bb3c1ffc2796b743f5cdc59e6`  
		Last Modified: Tue, 10 Feb 2026 18:32:21 GMT  
		Size: 6.0 MB (5971814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d6a08ada776bf07d0d4b87d3e08144fca629874fd2462ed57e0eb16da18367`  
		Last Modified: Tue, 10 Feb 2026 18:32:21 GMT  
		Size: 9.9 KB (9914 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:04f79a4ff841829bb638efd76c06fd3e1d1fa37b2612e285815ef87c548369b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221079354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b949db363cfb824914485722bbbf7e3fc5216755020d2b63021e68c3734a5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:44 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:31:44 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:44 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b888fd90266210c87ce4c967753628b20c5cf6951ddf7883417c164c9d37ec`  
		Last Modified: Tue, 10 Feb 2026 18:32:06 GMT  
		Size: 156.3 MB (156279878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48398704bbd35f6fd9225c437e920420dc1513c366fe281473424bf39158055b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b1bba46dc929e49717ed9ea7329ab9a904d655bced309acea6bee89413f8ee`

```dockerfile
```

-	Layers:
	-	`sha256:5afae25b6bd17c380a43b502e7e69ce4864615fc184d94d7e1c23d5bce2b7ddd`  
		Last Modified: Tue, 10 Feb 2026 18:32:03 GMT  
		Size: 5.8 MB (5763684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d63c131355189cc5d614b1c59abcb20efab5936328a72e70ee1c6abdefca0c4`  
		Last Modified: Tue, 10 Feb 2026 18:32:03 GMT  
		Size: 10.0 KB (9994 bytes)  
		MIME: application/vnd.in-toto+json
