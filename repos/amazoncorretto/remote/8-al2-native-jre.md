## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:32756c300d40544d8c216b24843e1783ea2737156f535609de0481aba47f4821
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ef9d5c5bad19d1f41af13450c3e4ad2d5c767fca3cf85f4e2f99cea0edb7b3f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171775094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5525d28b47a369583dbbda89443a7f8413a9bfa2791d0f7335458ca7f6b9be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:6eeabd86b075e80cf303c4a0348cf048d31ba6ae2d42b051bb230016153f8809`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 62.7 MB (62659944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69d38fb4cd4f09518cf58e6ea193174e354c3374e2f817ee7ab10d7dace1adc`  
		Last Modified: Fri, 23 Aug 2024 01:50:38 GMT  
		Size: 109.1 MB (109115150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6fa6bd31abe80395933aa9498c580cd31ed0498ada7b8435d6236d97233bd8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fe3ea63559afbfea2c2025a6d9d4501d2cba57236dfb684cb3c82f61413174`

```dockerfile
```

-	Layers:
	-	`sha256:b0f4c49af74581d2445383c26509dc1d09346ffdc6941fceafb3dda02795266d`  
		Last Modified: Fri, 23 Aug 2024 01:50:36 GMT  
		Size: 7.5 MB (7497704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2d90061638c8c8ff5c391d331e3b5e4bf20c3f5948bd24960a4d2b47709e90`  
		Last Modified: Fri, 23 Aug 2024 01:50:35 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f1c288f45e6e1c73469c789564789cb6346a6ba0a0b6576b076ae3e698f38c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117523252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb5ab7db205182174b0806f20933bee32948092019d9cbe8ee5afc79e4f39be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a76f5c44506982b7eb54b2f9622707d5bf9bf66d769b1f089a41e685b27d2`  
		Last Modified: Fri, 23 Aug 2024 02:17:51 GMT  
		Size: 52.9 MB (52936117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:53e9dfaa7513cd48a46e461f15a0106cbcb1a5025bfebd7c3cdd30b249891f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74d1f6775571932830d97b4ef32b85b106f679808ac7b70da2cfdb1b54b0db`

```dockerfile
```

-	Layers:
	-	`sha256:38997ee312f54e8c3bedf1a7d33e29d31112a7a9b15b21d9a22064402a530278`  
		Last Modified: Fri, 23 Aug 2024 02:17:49 GMT  
		Size: 5.6 MB (5613432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc80b6e0bef6cb99cbc515c871fc5c4ee6070e4acc10f4305fa7ecf9fa627bc`  
		Last Modified: Fri, 23 Aug 2024 02:17:49 GMT  
		Size: 9.9 KB (9874 bytes)  
		MIME: application/vnd.in-toto+json
