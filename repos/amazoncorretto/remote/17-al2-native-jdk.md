## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:a3f646e5bb093d81c95b12cdc88970f650d4a58010fe6cb49833bc3bd97e0b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:96a71f307b6d05015fa3cfdb99e5c4f5f09ca8d307e13e1dd310c119aab27ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228660746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362ae7d2d6df5bf117e50dbd2ba384355f707f5409eeab209d27ef2ece5541c8`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
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
	-	`sha256:dc1bb57f64d7d64dce253e79a9b316b4a5a409c414f32a3e91752789bdcd089d`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 166.0 MB (166000802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:26632ae486fb76d1e574dfbf39cb2af616a58a2b56a6ec13fa47ccaf575a47e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555edb9b9f229fc6516b6361d302c12562377fda2f30b05f8aeb46c38dd89888`

```dockerfile
```

-	Layers:
	-	`sha256:c9514084a9e324cc6be7d846c29e063455a0a94afeaac5fd72dba60d49287330`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.0 MB (5966104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e41d17f2b1f6131be529a1d9fd7dc6a22705dfd75336f519959678d2aae8ba`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:459cddc56bcbb240223de7cc6ec52b305faeaa70a1b8ac63f009d4def6560993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221200169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4ba2e301159161bafa2c8e68cc3bc3e1a64f4a7123d7886dc2cd0db913222c`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
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
	-	`sha256:9b56602e274d813f6fefeb67077b6e108af58ac9c0c2fec81da69d33c642247f`  
		Last Modified: Fri, 23 Aug 2024 02:31:58 GMT  
		Size: 156.6 MB (156613034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e6189a2c072769a7afac6881520eed126a6d458725eec5a8617938f36b9bed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5767917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c09ee4bcf4c25c55db9093de8369bc6f4bdb76894f53bd641bd7869f106b19b`

```dockerfile
```

-	Layers:
	-	`sha256:9fc963707e1b3b5cdf45d41094932def5affb1f90ccee79adaefa4a499df8b8b`  
		Last Modified: Fri, 23 Aug 2024 02:31:55 GMT  
		Size: 5.8 MB (5757633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14beb792fedcdc51da8e069ccdc27acc7927f90472ec642b979cdcd086764525`  
		Last Modified: Fri, 23 Aug 2024 02:31:54 GMT  
		Size: 10.3 KB (10284 bytes)  
		MIME: application/vnd.in-toto+json
