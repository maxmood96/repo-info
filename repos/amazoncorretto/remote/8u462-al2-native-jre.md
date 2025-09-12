## `amazoncorretto:8u462-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:50a40e66ffe5f8b24f07bfa209cf435acd3b9e6db56b5212d3b6f4caf65f964b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1b45f6c5caf7ad65970ee07cc1f21b1e2a07d863e438aa3c2cbc3558f347f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172140988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2941a1a88d2bd5c92d5e1c4646e952ea48a706df049d7ab680815082c10a50d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9b98901778f6f6d907ac560d9bc7d374485924ec26ab0959b05263fc3fcf4a`  
		Last Modified: Fri, 12 Sep 2025 01:11:07 GMT  
		Size: 109.2 MB (109157700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7031a888cd91bc41a795b7f7d575323fd3a0d929f6b38c606c99e5d185c8f158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c965239db491c18c574fc63fa870ff52c8f0645f619c7be397dea4fae67830`

```dockerfile
```

-	Layers:
	-	`sha256:8e4ee6625785021524fc23bf58f7631231b668a7a63e3b18bb96f0a2d3cd2897`  
		Last Modified: Fri, 12 Sep 2025 03:51:57 GMT  
		Size: 7.5 MB (7504128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e5881c47fcd908f7965d2c15b306b000745797ea52196292ecea762896ff1db`  
		Last Modified: Fri, 12 Sep 2025 03:51:57 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b7cab06c89a8dc53d775b2a6b4ee5a34000aca01c983825cb68df4db108549ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117722678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb95cff954a65b2ccbea32874b5a70356ed6510e5ddf4d4f2b7d04a2e56c316`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb1c6c9957899bdd2bc34230fba42d7c4fc82aee3a67b64eeeeae116c01ed6b`  
		Last Modified: Fri, 12 Sep 2025 01:10:48 GMT  
		Size: 52.9 MB (52930955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e7010ac512db5c6b051e99147529f47d4b82c9aa751243a84ba34480d2998d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5105cc8d902ffb329812376633f3d7a6dfa4e85a7fa9a84b9756f57e382331ec`

```dockerfile
```

-	Layers:
	-	`sha256:c4207af220e2cc9ee2e2797159f817158a893fd1361af97bbcdcc6973e399d06`  
		Last Modified: Fri, 12 Sep 2025 03:52:03 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6861ada37befb92b7c2cba88bfb60f86f0a90cac93d1de8fc9c2408664cf9ea`  
		Last Modified: Fri, 12 Sep 2025 03:52:04 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
