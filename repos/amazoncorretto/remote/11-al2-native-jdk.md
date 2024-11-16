## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:f8d806b9e46a77e6752624914cd32cbc5525310a14701f611f7f763bb569f6ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9d3753d396963fb25a2f2ccce1eabb192ed7f1b4b15b005f449ff68d677073e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224837355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6eb9a0681179787ef5b36b11640b0721b4992abf43b12118b8aff7abbbfadd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b25fe65bbf39e68a13c8a30b7c8e833475eb3bf9ecba67346b82a7b859ce09`  
		Last Modified: Sat, 16 Nov 2024 00:48:21 GMT  
		Size: 162.2 MB (162159916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:abafe2f8a10f9408c609e86ef82ebd4533ac5e5b300d454987aa8779420ef23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62823d3442a81c1d17e8fe8cc98a610f75f48f2c5bfc8b2fe562ba14f622f856`

```dockerfile
```

-	Layers:
	-	`sha256:9cd510bdb27abbceffb48744caab02e5908539747a037150881158a637be441e`  
		Last Modified: Sat, 16 Nov 2024 00:48:22 GMT  
		Size: 6.0 MB (5990325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:071c208c306aed5da45847ea15d773bfb0c312ad2527ff89a43a29879a3a9c6e`  
		Last Modified: Sat, 16 Nov 2024 00:48:19 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e81c88273a7adb6ffa496da4e60ba67715b9acd6a57173cc432fedb309dff91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216893283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9ee74fc1c69a2ef43039e03809befc9d4890cc7c699a4d91dbfa00e7d9e792`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd27f3e76b59887c758dc42fd5a28f08b1b4d5e53efd9de1ce559213461b0b4`  
		Last Modified: Sat, 16 Nov 2024 00:57:23 GMT  
		Size: 152.3 MB (152311396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:473ac345bbb7176abda5482d1bdcd45d8c64326bb97b4ae484601978b66181fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a6642c131612a595b906a51b9a829c73044e033fce56413557dbb2384e3418`

```dockerfile
```

-	Layers:
	-	`sha256:0b89ad74438ef76418a3de34cad30f67818773dea2014221068173df7c4038a1`  
		Last Modified: Sat, 16 Nov 2024 00:57:19 GMT  
		Size: 5.8 MB (5782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:987333a3f37a799604c4c63bf5bf93d148b69744e9edf2e7f0980d405c38b162`  
		Last Modified: Sat, 16 Nov 2024 00:57:19 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
