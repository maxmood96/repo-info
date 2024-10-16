## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:44f5fe286ba774e53dc7076d0efb9dd8880827994f806c1ed36a5c79af96f1b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a20c4fb44807fc2b0df068bef1b5fd65451f33a0bd7b1fe2b353f8dff863a9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228016159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae21272e3053facd01f495211f794ce0981feab3fec3b41d0871800aed0eb5f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:55 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c6537a62457ca4b10a722b4ab9c8bdd7ede7d4e16e71c27ccf50018984775`  
		Last Modified: Wed, 16 Oct 2024 17:57:53 GMT  
		Size: 165.3 MB (165338003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3062547caeed2fa5483cc5ff1a959971ff9b0175f7e22c47a823a78f7b4b7d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e87778b4e4a7b71efedd9ea5dea85f5c93667f9bb67ea7601b5001da3c0f4c`

```dockerfile
```

-	Layers:
	-	`sha256:deb660b98942f5a3f5f270be6e28375f8a373970a5259dadcc915c342373ba96`  
		Last Modified: Wed, 16 Oct 2024 17:57:51 GMT  
		Size: 6.0 MB (5966955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f28bcd79c48df91e08122438587f17e4dd160883641fd48b9c1e6713bb14bfa3`  
		Last Modified: Wed, 16 Oct 2024 17:57:51 GMT  
		Size: 10.0 KB (9966 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dbe77f83956154becd3f86b564089a7e1494aca0ccd50ae95600605be6d82613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220495309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c55e451a54d2f8e6773ebb97adeffe7379d0edc3c1a14a9a4f4295cd058ca2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:59 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ba106ad7f15c392ebe256e8888a1c28c51fea2c5215d0c5cccb96722bc9647`  
		Last Modified: Wed, 16 Oct 2024 18:27:46 GMT  
		Size: 155.9 MB (155902650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:791f073fb348912c7b644201a47b72efa07630d9c0ffcbb33b918a220e973d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ca0b55eb3646eb79bacc4e0c3f48526992d3bdcfec617931caef05bf79168d`

```dockerfile
```

-	Layers:
	-	`sha256:19f9cc1a531b5ec76c84ddfe3877b2cb34d7d255b37bcadece5646745a145743`  
		Last Modified: Wed, 16 Oct 2024 18:27:43 GMT  
		Size: 5.8 MB (5758485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86d051cba90496ae5a4bd1e2c5269e9c8a2ed4ecd9c8bc77c5e914eb72ff25b`  
		Last Modified: Wed, 16 Oct 2024 18:27:43 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json
