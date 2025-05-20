## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:59dd415dbd2c9054162d7e606000ffd8f42ff5d709d18f7440ec2049d4a926fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7612ea9c814ad6c25b2852da63a8eb1d71ac8f6e94c732a947eabcd722c7bb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150273137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba4c28c5bc168fa30399ebe3bbb1936058a97964edc7b68e87c12691dc7167`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Wed, 14 May 2025 22:47:15 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f548d2b0c29cf128e6300fd54778f91a7e6ba6be8b6a0589ed476dd37bd810b`  
		Last Modified: Mon, 19 May 2025 23:37:14 GMT  
		Size: 87.5 MB (87513152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5bdb7acb77122813ad55c52e82572db5c29dd9f68e50e286fbeb765c8acc50ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27823bfa90c0a0376778f1ef3c5621cdb93a21fb650da2a53b15f0bdca3786a3`

```dockerfile
```

-	Layers:
	-	`sha256:7342653b6dc44dd75156c531d1ab3ec3981d6abfcfdf81a8c596b637be1b3be2`  
		Last Modified: Mon, 19 May 2025 23:37:12 GMT  
		Size: 5.6 MB (5627321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c944cea83ab0727dda537dba0436b8097357379ab5c36b6274accef5a99ee6a`  
		Last Modified: Mon, 19 May 2025 23:37:12 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dd89247bb1b8c935a8bb9ba11e24f6ac1a9d2f2956db3f5d7519f407733ad903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144366102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55009cd77da35a72c3662a23ae77bf30a84b008fefd01418ddcbfb0660d0bda7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Wed, 14 May 2025 22:47:33 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92cb0561185bfe576435469c422eb40344d31785d27a11f62fe2292bcd2921e`  
		Last Modified: Mon, 19 May 2025 23:57:53 GMT  
		Size: 79.8 MB (79758621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3f3352170338fb1cc9284b77c99fbd4b146d10153b181121be831b50cf8b760e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20733ca3d8d4a741514ef42f000131ae160f145eb028e1229320a45157452251`

```dockerfile
```

-	Layers:
	-	`sha256:c75988cd7bfc1637ccda30b0ee43a25dc13acf5eea80937cf248410da9d4e1cc`  
		Last Modified: Mon, 19 May 2025 23:57:51 GMT  
		Size: 5.4 MB (5443597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50546d1894cc4793f9bd49f99efa7b515abb1e442c6d44a86f20ccfc6ccf73c3`  
		Last Modified: Mon, 19 May 2025 23:57:50 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json
