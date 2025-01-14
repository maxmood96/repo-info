## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:da7882591c3d30820a2b7f0ea417ad86ad28398890d1736cba4b1c148b7aed70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3dcbb9d1b3a12a91bf0cc562fa56ee2c55eba7cc29640c5f4ad9c389b4fcdd69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (227984352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593a853a22f90441d81f4dfa821f09ad0a2a6f10f8d7e01ec5d6ea76d02fd936`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdba3b383d7b7b4199e680692018f8ba2d085e30896eead77b876e152e9879d`  
		Last Modified: Tue, 14 Jan 2025 21:28:48 GMT  
		Size: 165.3 MB (165348522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79b1645cca303495c8dbececd2a9f0a3814edffe655bc80d7680bf0f829ce408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd260f4d8fd8d4fac443a7fdfee38ba8edf066719dcd5d7281ae3e8dffd5a03`

```dockerfile
```

-	Layers:
	-	`sha256:53ce35a65c4b2b6db79b3c0c551082b7f5710bd1317c6d7c61a61529ef0bf6dc`  
		Last Modified: Sat, 11 Jan 2025 02:29:43 GMT  
		Size: 6.0 MB (5955200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d73e27d925d928ee70b81f1a5e7da5e9b7085413234397925299b9745afa07e`  
		Last Modified: Sat, 11 Jan 2025 02:29:43 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:da19a8cb650683d7cfc5a910c2b093115dd27a5e3a365fef4bbb616bf8d5eaee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220506133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0c84cee8bf43fb2f674b83d839f796060189b215519b2d300d6c8a480765ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Tue, 14 Jan 2025 20:35:27 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97c2348d725dd63a4d833dff8d6a2a7db01f705eec4f4aea091acac4d5f5dc9`  
		Last Modified: Sat, 11 Jan 2025 03:08:39 GMT  
		Size: 155.9 MB (155915828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:03a5f444d96ef243d586faf8446092848ac42aa8b5e70d6f0556a73a7c73c932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05c021dc459dcf640948e29e0f3ad93a535b2ea491ee7f4f4fc79e64b218953`

```dockerfile
```

-	Layers:
	-	`sha256:e930f102a75af53b0f52e5e157bd3214843552e009df26e014d43f9cff7c3cb2`  
		Last Modified: Sat, 11 Jan 2025 03:08:36 GMT  
		Size: 5.7 MB (5747070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a848fe610432725a65df2496bfb8e3423b8c4a8fc127f6fe8bb63cb3f3ab6dd`  
		Last Modified: Sat, 11 Jan 2025 03:08:35 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.in-toto+json
