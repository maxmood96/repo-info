## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:1872a824922e60cec6ae0aa7a02a26761d171bd617db2ea57d604bfc5ce3b3d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05684902f608aebbb5b5fbff20c5f7755c2ff0e6a49037526264683ea05499c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150428653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0484d911927843df854a546eb5c59b8ace18c2422cc51d88ab9b551ac86b08d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6eeabd86b075e80cf303c4a0348cf048d31ba6ae2d42b051bb230016153f8809`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 62.7 MB (62659944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70ee33b94073fea468d9f23ff8c664fb4afa1d1a9c743cf3cdae189599aec30`  
		Last Modified: Fri, 23 Aug 2024 01:50:40 GMT  
		Size: 87.8 MB (87768709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7a959b2080fa12c2c105c32360a22720b5f902d110ea59adb8ed95553f4ccc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455b58e07151df78859f3370010d3e95761bfbef4462d58eef8e7183981c1206`

```dockerfile
```

-	Layers:
	-	`sha256:6a31ed40fdd8eedf0cf6ab314395be60509640e98d5b83ecb5e8e407ffc5ec17`  
		Last Modified: Fri, 23 Aug 2024 01:50:38 GMT  
		Size: 5.6 MB (5626078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506d4fec759b4fe0ce02418bb248bf62ae430b281bdaa72c03961fc48a7a8a2b`  
		Last Modified: Fri, 23 Aug 2024 01:50:38 GMT  
		Size: 9.3 KB (9302 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b2055d7f41f8d97bd7fead1377f925f78dc6921c43c6e01f40426b3a5aaefdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144663310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cf35fdede625927725db21918b8155e4ee223aa729314c630a2faf6e768232`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a8d68eeecccb38ff978eda023f6f33ca4601db140bb0325b73d68aad6c0514`  
		Last Modified: Fri, 23 Aug 2024 02:29:54 GMT  
		Size: 80.1 MB (80076175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:351d9478f8dea4dd72cac3857f270634fe3054d61fd817dd20c867089240f584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14eb11296d8d72ae3ddb07d12d29d6b4fc827b52b61892ff1873197385ed53fa`

```dockerfile
```

-	Layers:
	-	`sha256:591f46f783dab4f675ece962152b6871cb6d5979605c968784738fcf20ea6ae0`  
		Last Modified: Fri, 23 Aug 2024 02:29:52 GMT  
		Size: 5.4 MB (5442053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55189d9dfc84334411f58ba47006d0dfc0702c472e4e1ed6a10124d1322e029`  
		Last Modified: Fri, 23 Aug 2024 02:29:52 GMT  
		Size: 9.7 KB (9662 bytes)  
		MIME: application/vnd.in-toto+json
