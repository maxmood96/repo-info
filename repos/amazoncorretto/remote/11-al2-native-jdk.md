## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:ed68b393c6326d2523e62922768751c7762f9c8f70c8bf087d8cbd3b56d20b73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:00f9ad81ae79bb102abcc5b9dbc0a2627b6d6f1dcfbcf47a9e78b52f45d40df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224807405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d555346759046bfc80b0f3885adac0d6f1e4038cb80746fc829d42ec7d19d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91ee6303e79d654f97fa93efa05757cc6f09798f1ca613c9ef29d8badaa76c5`  
		Last Modified: Tue, 08 Oct 2024 00:00:16 GMT  
		Size: 162.1 MB (162129249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ae421a8e83b1b7a5f24af0cfdc52231f5f559906ad85c845768630ba7fa0e27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aacd93fb7ded0f85e43e6d3adc19abe528f67bc71bc23c1c9e64e93e5f868e2`

```dockerfile
```

-	Layers:
	-	`sha256:820de0fdd557be3fa65c7fc86cffc4427a25c018a70b9448aaaa7f94373a1ba9`  
		Last Modified: Tue, 08 Oct 2024 00:00:14 GMT  
		Size: 6.0 MB (5990338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ac044c0bc1b582cb9f15214e9994652c74c2f51b54608a996d3e39c1d78e571`  
		Last Modified: Tue, 08 Oct 2024 00:00:14 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8dabfaa62cb15da1d47baa5ed253b07a451e48daa49fb0127ee03642483d720d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216885124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3cea449150197bf5e36356aad316bf2f6bcb2c89be4ed1ee67912dbdc422cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47b1a9cf2cd4dfa1a2234e76961af0d6edad52951d94e35f851358806fa4c67`  
		Last Modified: Tue, 08 Oct 2024 02:02:50 GMT  
		Size: 152.3 MB (152292465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d3477790543c4a244edf719c356b0390420d5e335e36b00a369119f7338f639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706096583b920ec861b28336850554768bcdb6b2adcfcae96c14acd48170726c`

```dockerfile
```

-	Layers:
	-	`sha256:5859db2696af20440e3746d6aed6d7cb07b40c786d582660a35687470e6c40d7`  
		Last Modified: Tue, 08 Oct 2024 02:02:46 GMT  
		Size: 5.8 MB (5782713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b171232055e9ab7dcda96f648c57615df5220953fb9d9932a09ce008fc84208d`  
		Last Modified: Tue, 08 Oct 2024 02:02:45 GMT  
		Size: 9.5 KB (9490 bytes)  
		MIME: application/vnd.in-toto+json
