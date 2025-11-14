## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:67eef7bb30229edb15f71aa32bfcd7a38e3f1bfccd3f98e9b5ad92a6ca674b75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7cfce86bb9e32739bc7a556c2253f6e96812010871cd3000d0b2256d31ed8ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154200162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c28b5b63db13bdeb43540670d309600fad0ec0a7b199c64a6486dab47a7a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:51 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:16:51 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:16:51 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f68117b6ffedfb68e2dca35a0301b7becf63e02f2495dcff877b3a47dc2c27`  
		Last Modified: Fri, 14 Nov 2025 02:17:25 GMT  
		Size: 91.3 MB (91269590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1d4ddbb27bb2f2a54e7ee8512b3cad2ebc7b66eb34f74b921ff53542e0f0d58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db130742aab7729b5fa4f9bdf83b79cf9d98ca354ac465c47583ebaed548745c`

```dockerfile
```

-	Layers:
	-	`sha256:569ae9fc1d7b1b331b85ddc453e3b2e0ff3860792f8be1509ab1d77a2af12904`  
		Last Modified: Fri, 14 Nov 2025 04:48:45 GMT  
		Size: 5.9 MB (5865824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b41cf7f83728421b67d47da19378eea2dadc2e5d0657236804c29a09750f51e`  
		Last Modified: Fri, 14 Nov 2025 04:48:45 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:685fd8badb7bd96fcd4eb3a6fb225a1439fcc40c62b93269e2e26e20f0700ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146786485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39977cb885a7bf0e5a0c551f0992b24924bca493c9ffe36ec483fe81510cbb53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:18:48 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:18:48 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:18:48 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:18:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71431a0eaffc621c55cdd5f53253357caaadbd56799e8e987ae0fb2fe64718f`  
		Last Modified: Fri, 14 Nov 2025 02:19:25 GMT  
		Size: 82.0 MB (81993684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:718185698e78bb63c47f180075c1e37daa88b83b6415467dfb791dcad896080d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e5489d7ae006df3ef87b155a4323b31256943fc4e5c2ddfb0ae841b3b485bc`

```dockerfile
```

-	Layers:
	-	`sha256:13be3ecd236fbf8876df08ccb24b53412ebcd5115b78cf3672ce3a085432cae5`  
		Last Modified: Fri, 14 Nov 2025 04:49:35 GMT  
		Size: 5.7 MB (5657567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f430bb4cecac728ec88d3b45c4d222a963f520c12bc2e4ee0d78930a0bc659`  
		Last Modified: Fri, 14 Nov 2025 04:49:36 GMT  
		Size: 9.5 KB (9508 bytes)  
		MIME: application/vnd.in-toto+json
