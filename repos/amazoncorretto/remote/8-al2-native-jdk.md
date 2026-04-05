## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:5be52c7f7cf578d2647e46b603304b699c9a35c212d528fb45c5a52e69d7f606
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2d1e06e075d2203f40491e6afe8fdd1bf89d777bd1482a7f2525ea6dfd314502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188265969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de0d1c130ac3de58468753d46fc8f7c892b8e46a8fbabd5ae02c1e9347efd2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:01 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:14:01 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:14:01 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973ca353f6833a9f3425881e10e592c61bd15a9af95c7ec0de9908ba6816732d`  
		Last Modified: Fri, 03 Apr 2026 22:14:27 GMT  
		Size: 125.3 MB (125310668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7499eba9eb19aa1a4d8fa9e87494883774288e25a47c835c0154c04beb5a25bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e6976d411a1f24a584d31a13dba3352c52437b74e8be600c2011012a5054fe`

```dockerfile
```

-	Layers:
	-	`sha256:9ceaba4d73688308475f1d5e1ac40148766faad20b78d026afc745d2d9fe99a2`  
		Last Modified: Fri, 03 Apr 2026 22:14:23 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc57682b9323c632842e453301b8b490795a7d9b02b29a0383e9e6a28342d896`  
		Last Modified: Fri, 03 Apr 2026 22:14:23 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6d9419d14559bfeca6a6a4e71d066c13501480575f5a788570cb40ce48b513cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1a04b336d5fe730c11d08911c9f06711d6dd6c811d2f5085f8ea5f247f577e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:12:01 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:12:01 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:12:01 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:12:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b1cc47a8a7baf134a1b76c45547c5faf44262df9946035eb3a3072669daef`  
		Last Modified: Fri, 03 Apr 2026 22:12:17 GMT  
		Size: 67.6 MB (67596926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4ac5b48061f5d498073b9430b23635a6bf2f9a30a051260a295d97d3b6734366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa88937d45640053dd27d46ed6eece566bd1d4875c49065a2e374dac627d070`

```dockerfile
```

-	Layers:
	-	`sha256:27b93da92cde70e4774dc60ce16b4672888a4c5622d617ad72567ef53da84736`  
		Last Modified: Fri, 03 Apr 2026 22:12:15 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e10dbd84d05428f1a01def2b560df8be38a9dfb6341d2f4f0d5eefb0135bc95`  
		Last Modified: Fri, 03 Apr 2026 22:12:15 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
