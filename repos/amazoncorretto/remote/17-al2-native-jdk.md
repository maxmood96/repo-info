## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:54f2dc257c9e21d6aa38a4acf7d38fb87163577750d25540811bcd1cd7b3b214
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1284393dc60bebd90f20a912b5eccd2049207217e250d1322885777d6cf168c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228028707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b23b25f8254d4edfd667a7d3c5b5b2b31442bde3636d9f86c917f62a7ac1e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:43fdf45428917f1f386fbfe0eba1ccfdadae7696a4cce30a96cca587ab25ab90`  
		Last Modified: Wed, 05 Feb 2025 10:24:14 GMT  
		Size: 62.7 MB (62665244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ab226b5350b696f8a342f1d05f2696569fdc97b5a05ffb693e584bf50dcb4`  
		Last Modified: Mon, 10 Feb 2025 20:09:00 GMT  
		Size: 165.4 MB (165363463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8318717ce7fd92937dc86ef07e6fffef6129358dd77a4327a4e410ee044d2ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aea97612d7d06552779d74031ff75f9139314b11fc9eacdc0f15137b7bef6db`

```dockerfile
```

-	Layers:
	-	`sha256:7ad2629b6cd2bdf2ae1778823f3dee3f50cd26810662df804f8d7e6ddb2d2445`  
		Last Modified: Mon, 10 Feb 2025 20:08:58 GMT  
		Size: 6.0 MB (5955194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d706175f82acd83883c8da158e43a9fabe04429206f1880ec0cdaa19d97edd09`  
		Last Modified: Mon, 10 Feb 2025 20:08:58 GMT  
		Size: 10.0 KB (9957 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a56360183613a31b00b9f2609bb39453499d0ae4daa08c73fa815c16c45466cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220565926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7480e5270a91f777cc5021b98bda4f13f408657de0f7e26b21209ff38c434f74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216737aa16b7234d4cb52dfeccf70c0c606ffc1cd7334ce33185c4369adb116c`  
		Last Modified: Mon, 10 Feb 2025 20:25:22 GMT  
		Size: 156.0 MB (155987704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27e502d7786dfb05f56301a4e72180c5f03ed15bf83a9925aa51a211e32a1299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fd35bf955ddf9e11d8377a601c60fea32dbf04a5654a9fc1c7bcd3d409f619`

```dockerfile
```

-	Layers:
	-	`sha256:3de52ca7f87c9d2d89972edd78a103ff4aaa3d6893ac138c6759246835aa26e4`  
		Last Modified: Mon, 10 Feb 2025 20:25:17 GMT  
		Size: 5.7 MB (5747064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b654abe09c23dc201729228b3079b014a86bb7483b1fab79620aea7200913c`  
		Last Modified: Mon, 10 Feb 2025 20:25:16 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json
