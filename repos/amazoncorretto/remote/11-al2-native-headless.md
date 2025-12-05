## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:e9c2c21fefce86be246d768642c88cbafa28d1409720bb1e3b0be4a14774769f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:55cb71894d78e8ccc753560070030a2933f1773b5ba6003fc63a424193c6c786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217239613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8cfec1f093aa556f3b6ac92c80bf6d6ece48d0ed630c525830ac58b7052062`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:14 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:24:14 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:24:14 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916e5e5aca6efd1507d1eaa4f7f1fb013426777b9a2249d8b461d03343a9b7f7`  
		Last Modified: Wed, 03 Dec 2025 23:42:47 GMT  
		Size: 154.3 MB (154309041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ea23bc90fe84fcbfde2e24493c74d2b649e480dc3bb002665ef43e4474e7961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745c12ef9f370983e1a015d5910bcb4202dd3978cfc9bb879495ad8c6ce46d15`

```dockerfile
```

-	Layers:
	-	`sha256:4b4485cbe3ea85ca1a12d4c40739bc804cdbbf5a5c3bae634015aeb43c14eb2c`  
		Last Modified: Wed, 03 Dec 2025 22:47:33 GMT  
		Size: 5.7 MB (5683305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7a2049ab9ed608df70e1cb84c71fcfb87e9d3bf136779c9f822595534da463`  
		Last Modified: Wed, 03 Dec 2025 22:47:33 GMT  
		Size: 9.3 KB (9287 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2705212c114c8cc81902f527a27c7ae1efe6c4ed32b4324407892097c0c2c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211380804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0e108dba02b07e661be766d4c15339b7ddf177baca5ee45761c90659b1238b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:28:19 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:28:19 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:28:19 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:28:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961c91d3acea8d4a3e7dbbf75554f4efce094ee378d0ce35c1eb3675b380c0e3`  
		Last Modified: Fri, 05 Dec 2025 11:22:35 GMT  
		Size: 146.6 MB (146588003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:769a3caf1bdcebab18e46d58f4fc8c35f558f5c02bcd2ffaf1caf70994fb8003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92356811ac0af8d794138a78a666b264398633ec4a1edbd4b964ddbed438ee0e`

```dockerfile
```

-	Layers:
	-	`sha256:791425a17b7fcca94062c9bf428b9f72a5fba2818df6e4735d91bd170c558c15`  
		Last Modified: Wed, 03 Dec 2025 22:47:39 GMT  
		Size: 5.5 MB (5501773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5befc672e5ebe96ddb1441e8ec5ff90983dfaf8d6be24ea217aa29adc7b841fe`  
		Last Modified: Wed, 03 Dec 2025 22:47:40 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json
