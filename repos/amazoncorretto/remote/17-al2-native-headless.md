## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:ed568fc3526be8e35e4c523b0546c3aa9103bc52dfd65bc7ef3e818381dcf8f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a75391dcaca7e9f2e8298f6e5e5cd74bf2c692629583af0ffe5f7993fccb4c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150259551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e43cf9318eb08e6459d48bb4c80de186ccfab3b834ac22ec4109172b7ad27b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07add2c3a4368d38727c4e834a674dcd6b6f4672eb20962c41c625d56fa50443`  
		Last Modified: Thu, 01 May 2025 21:08:25 GMT  
		Size: 87.5 MB (87500221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:589f166a235b0a6aac8bb5f9c71a3eebf6880a62608422bff13d2164f0301240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44343c5e1e2f6024ddb0faf167f68993c123abf7e7e681fca344c1cb0ba7a022`

```dockerfile
```

-	Layers:
	-	`sha256:ac4338660aa2f986c622eb522ef3b50c6b1423d85c0e661ab66b73758bc4027e`  
		Last Modified: Thu, 01 May 2025 21:08:23 GMT  
		Size: 5.6 MB (5618977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d722b8a57dad3a197818da21b07d39eb27abe986acd985e4ab6b883831269ff5`  
		Last Modified: Thu, 01 May 2025 21:08:22 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f4f8bdd1007ffa7c2d1ae3e2443b7e5270a8e7d915fe95677494eeb6c9843adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144364192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d80b13e27b70a5ab44190a609ba6aaa4255210e059a74b32de4d7cc26e46b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df212576414e8710524db14a5e65d47f6356544a963b63d450e2c171411b570b`  
		Last Modified: Thu, 01 May 2025 21:19:13 GMT  
		Size: 79.8 MB (79769465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b849f60e5a5008ddbe5663a180256f2148535f102d0a03b5a788e7ec4fd3c097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090ab6e4886e997c405771eeebff1aa3dd516130e19462d1e58c3591a23f19b3`

```dockerfile
```

-	Layers:
	-	`sha256:637aa444c08e302513985115064e734316e90b74bb2e9ec6b6a585510f91258b`  
		Last Modified: Thu, 01 May 2025 21:19:11 GMT  
		Size: 5.4 MB (5435253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a6ebc81d86f7a0986b7bd87ead9f1632b99d343df2c641738b75cdc5309989`  
		Last Modified: Thu, 01 May 2025 21:19:11 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json
