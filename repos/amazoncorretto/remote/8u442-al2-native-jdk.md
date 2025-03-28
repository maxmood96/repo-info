## `amazoncorretto:8u442-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:7c9dc7394b5ac1bf5be0fcfee8fe21cb99251581fec4e89bbaa88550b7415b9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cd598fc58ad314fa1bb864e04002f903079a60db7b5c7dd50bd7e32d0063c1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187980172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae96230007a1a0b449c2ca51e908aa5f66b157b48da3fc4847e7c821a062ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=1.8.0_442.b06-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc805ee2c52588ca043d2ff7aca4703f12dcd78c733e67f94395135045da4371`  
		Last Modified: Thu, 27 Mar 2025 23:59:01 GMT  
		Size: 125.2 MB (125227283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:deea96c777ec3804c279bc226f40c1e98944c3b1a4d49fe4ed4f4e023eb3b68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc1868b702ecd4cdc8c96399a2b53ce769cb25e8ed1f0365993fc0a36f10c52`

```dockerfile
```

-	Layers:
	-	`sha256:af08766028091cd46e434f47f5b30c1709fc39ffb4f441137bc4d67f4a8ac0e4`  
		Last Modified: Thu, 27 Mar 2025 23:58:58 GMT  
		Size: 8.0 MB (7956516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563712078d3bf20ecf8e9479afa2b92a07dad65696c8e06da50e8bde8fad0e94`  
		Last Modified: Thu, 27 Mar 2025 23:58:57 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:70ae05d49a144382d914d1f4e780d9629aee3326cf74332e3d9ed98773cf69fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132085748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046d7efa43bd597d21d926382a2d569690685db9fbaf0a1b3a8854e4282c1929`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=1.8.0_442.b06-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dec35fa7d230c500250d9644cb587c41b4378e335bce427ec965a5d64798af`  
		Last Modified: Fri, 28 Mar 2025 00:07:05 GMT  
		Size: 67.5 MB (67519926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ccb80a687e4aa9f4d99f29f944f53add11fde8a299af17813062c31d9dff4bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84da3485428ee583666e088a8e348e236a0893ccc7fa17380285208358742e6`

```dockerfile
```

-	Layers:
	-	`sha256:d6fdca40d0ae710fc87c5e15e2f3441f388f1516a3053526d19402234687f6aa`  
		Last Modified: Fri, 28 Mar 2025 00:07:03 GMT  
		Size: 6.1 MB (6066679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36765016ae7937a79f723e28f421e7dd82a5140357240fc111154e0a3a2ba651`  
		Last Modified: Fri, 28 Mar 2025 00:07:03 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.in-toto+json
