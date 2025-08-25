## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:705c4fc284b8c50583fe77bc4684cec1d3f6eeedf6efd9f2c4f1e752b60cd841
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b11e91792e5ef1d7461f289e232b88d4baec003d2f4ba260c6795b0f49f4db8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225293478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f6b4e37dfd1f69ff43db66d2049850dc3bb019944f28156fa2cedc22d72090`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5035d261ad511f861630de1a4fa0a482fc57b212e5e44a7219c478fb3e5c94fa`  
		Last Modified: Mon, 25 Aug 2025 20:18:16 GMT  
		Size: 162.3 MB (162315353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d5ecc483fe7665208c47a4b4b3f28643b5f2b7643ef4461d2f17dac6d43ba9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0417d7c8137e789843fc33e65ebbd34016c81816c22cbed9628af0be14cf9e78`

```dockerfile
```

-	Layers:
	-	`sha256:188471adaf741e7f8f00fd27b8e4533f2b49967c665c857bc6212802f096597f`  
		Last Modified: Mon, 25 Aug 2025 21:47:29 GMT  
		Size: 6.0 MB (5995078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1875532999d3e1973fc30ef41020d3308c87f69cab4d66598b740a74ce1ad2cd`  
		Last Modified: Mon, 25 Aug 2025 21:47:30 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ef65111cfb56c592544f67ab5f403b9fd63b1d030d53cee2cb95b374771affdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217201591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36a06834b3179f475bd9d2d700224fc9a58f4da9f83bb93728afa37bbf47e03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999ea5424650f9e0ec12b2dabcef7693f8c95ebd871a97c07464575e1434b28e`  
		Last Modified: Sat, 16 Aug 2025 05:59:46 GMT  
		Size: 152.4 MB (152407227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7bd52306b1ac327afc9ae2c15284711db475c7992d4d52fa0280c379f38f6bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fd3148247cf74728b7e9fcdce12ecd6199d454b2d659c51814926f65ad4101`

```dockerfile
```

-	Layers:
	-	`sha256:5be16dbd1fb1f37433141f3bba01eb153df0d1b239a84c43163b98a36bfe0ded`  
		Last Modified: Thu, 14 Aug 2025 09:47:30 GMT  
		Size: 5.8 MB (5787792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a26d3728c6d8ab80e8ea9a0518424a8fac3a4fa54be932382e8c66aec05cbf`  
		Last Modified: Thu, 14 Aug 2025 09:47:31 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
