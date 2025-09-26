## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:c37d0d90a5498cb802ca9fe57b684d1bbd54a4ee6ecf259f6b62d11221338a1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:588aefdf6a738eeb6c7093c0f5d2d075a587b4bc4d170053328493743537b360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225206024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e44ada2d82135570cdd7f54d2bb962359a19dd140d4b943950e1c32dd01fadd`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
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
	-	`sha256:d969ed37d467e4ec5f04702c13a046dfea6f5fa3f5cfa6b183e922a4ae147c3a`  
		Last Modified: Thu, 25 Sep 2025 06:40:01 GMT  
		Size: 162.3 MB (162272183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2cc56a7da315aacfe001ae6d4f9dd08dda7e75da77ff0a4cca8c292f08447801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5f9bf1e620bd22ca1ba768e0b205ff6ed48a268d57e1a35afee50681c421f0`

```dockerfile
```

-	Layers:
	-	`sha256:d0af10e4210241bb6779712a984ea513ad5c02d9ec9f70b9d74018e9fcd7ca6e`  
		Last Modified: Thu, 25 Sep 2025 03:47:43 GMT  
		Size: 6.0 MB (5995078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34576b3fb2c877a9d03b2887c425d93ac479a44f039071daa60395e171028d7e`  
		Last Modified: Thu, 25 Sep 2025 03:47:44 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8c354c9db18f098c125608c00e0e1a7bc4e91cabad63a0c8126c6453f353c74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217193556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d564a8d8a1394ddddc9c897ccb062d87c806b8af64ec261972ed386f33862629`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
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
	-	`sha256:eef8116eece789181df9c4ee70d00ba252da60982f31add6be9b46a39b46cb3f`  
		Last Modified: Fri, 26 Sep 2025 03:26:56 GMT  
		Size: 152.4 MB (152400409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:00ce6d55f39719fe4716ef57c2acd55d3aa98f8ea4461946364bf513dda34fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74860770dba3293042520d011f458a99ea4f5abb63a6cc4e2846d9adf6540f0b`

```dockerfile
```

-	Layers:
	-	`sha256:e1b4bfcae3a9f15508024f44624d1be7f323ad4ff087b6390bc55cf08f31f315`  
		Last Modified: Thu, 25 Sep 2025 03:47:49 GMT  
		Size: 5.8 MB (5787792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb30d4b48c102967e603910711cace5979db873988d12ad8be4c81824a6d891`  
		Last Modified: Thu, 25 Sep 2025 03:47:50 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
