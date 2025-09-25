## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:a591bb9dc29caef0c2e2e038e16212c69e29bf5a289728e80baf78e1bfc8ba50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d0307111be9dc985c6188532bbf4b1d8d76103478641d15dbfe6034cef427992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217931366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc01ba4450bd08a7e29046a95f22087a7c4c938209903f66ceaee9f9e08cb5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fcc68e74b985a5b6eee4c73b52bbf6b5465b7b43a029c51e8950289a9262b97b`  
		Last Modified: Fri, 19 Sep 2025 15:29:12 GMT  
		Size: 62.9 MB (62933841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41bf1fbc95ea006578adec079572b87f9770562a8bc585b49bfa5e14b8965909`  
		Last Modified: Thu, 25 Sep 2025 06:40:18 GMT  
		Size: 155.0 MB (154997525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5d5cbc4d66660790e9fa1c91ce18532de299b80d183d77a124e38ac5b255a286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8234f407149957e4feab30fd3a07028ae23f97a176b51133060baf7ad210fda7`

```dockerfile
```

-	Layers:
	-	`sha256:9c1622b4c9aea20027e18e882792711880619e9c480668284ec4db636ad7c75b`  
		Last Modified: Thu, 25 Sep 2025 03:47:34 GMT  
		Size: 5.7 MB (5683301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce366507169585f0526b96c78b85f44e509aedaa7d809a7ed31f8cda95380e93`  
		Last Modified: Thu, 25 Sep 2025 03:47:35 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b5c71d6010854b5b127177cc47d2491c0028a582d87fefc6afea0ad7605d7d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212127610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657ad8ba2d0d9d06951ae9651919f3b7367d6cae587c1523b4f2cd421be65472`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:43d39e1e5d32e8ac06f789363477524a09029961f1236d4dc3927f200c572bee`  
		Last Modified: Fri, 19 Sep 2025 23:24:58 GMT  
		Size: 64.8 MB (64793147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb8beb95d912eb7264a83c21d722245c3f8bf1142170a0edd32fa57079f77ba`  
		Last Modified: Wed, 24 Sep 2025 21:12:36 GMT  
		Size: 147.3 MB (147334463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dfe1423bcc321754b93c9a600b2996f5e4a70324271378c54332f73d3f20db6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d237ff8fa9c97235c2e04045b884363cba678571ab5240b595b88709e9cfc9`

```dockerfile
```

-	Layers:
	-	`sha256:26f74bcf576549ae897996a7551a7b140c054d572f998adaf4eca8c384cb95bf`  
		Last Modified: Thu, 25 Sep 2025 03:47:40 GMT  
		Size: 5.5 MB (5501769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7994478b25ad78429a4dd8d9ef7ba81ca6b3f9839fdc75dc1f301a50ffdc9e2c`  
		Last Modified: Thu, 25 Sep 2025 03:47:40 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
