## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:1fffce0555a68cc56437d8014d02587c08d8e8ea79f470d9ce13d4bddb88a014
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4b924133e63b92ccea06f0f15d8905722921c8f64508aa3a4125a47e0be13f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217548208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f483ceaef1acc41bd4d89efe4ee925850bbf1f651a87add6bf3abba465bb0056`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989637037a05e28458bcf670d11bd08dc8e9dfa7d8a6b16b877d4cea67e806ee`  
		Last Modified: Thu, 25 Jul 2024 21:02:30 GMT  
		Size: 154.9 MB (154869042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b52bc7e61515e160ea7e8ab8e8cdebfa2a9c0214a50df785da51d2432dddf191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5688039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f93016151a9759bd60107c589439772e0888ed7a3b9e4ec4c2566f1b8617c2`

```dockerfile
```

-	Layers:
	-	`sha256:aa6b93ec08615f1bdb5627c748afcd1a75660f5a182af0f4a592f1327cda0e98`  
		Last Modified: Thu, 25 Jul 2024 21:02:29 GMT  
		Size: 5.7 MB (5678742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a624243b5fb7875f5d404481f550327bf751947a6859f14cbd8ad9eea3c028b9`  
		Last Modified: Thu, 25 Jul 2024 21:02:29 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9c8a1a21051dac9309d3b533dc971b3c96bf6c9d02c40d98a94b1713ff9530be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211777411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837ffa3877e443ef2f002d4360bff5542c0bc6254ae4185a1671ce21153d8eda`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b055cae54f7977beec9ea8f01a151ff830dc0e09342cffb329ac4fd9781cdc93`  
		Last Modified: Fri, 23 Aug 2024 02:23:18 GMT  
		Size: 147.2 MB (147190276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ab74c46f54db88e54928711306b9c2263867b2a891f078056456540ab8eb04d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5506587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a09176ca80e821a8c09cbadba0bb1a3ed0894cec89827dcde126d3fa56a52a1`

```dockerfile
```

-	Layers:
	-	`sha256:27eb0ba6549edb101fe01a70a774cdca1b455cdde829704dfe92042515de9c0a`  
		Last Modified: Fri, 23 Aug 2024 02:23:14 GMT  
		Size: 5.5 MB (5496929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fd9c61c50f640e6a5786ed03b2b744f6cb9c9bc43d36dd95fe00519219e34b5`  
		Last Modified: Fri, 23 Aug 2024 02:23:14 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.in-toto+json
