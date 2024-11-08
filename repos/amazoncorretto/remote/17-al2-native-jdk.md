## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:01d3a11d6028d851404f8459451d53d48fd802ddf3bc1f6edbc7e5193f7a0e85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e593a2e609ac9a08046cdbd13106b82a803206f694d8e5edcc16b254e477ca29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228024523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100fca75ff274529325c33234ecb61a3880dad999d30042c7c89b20864c35602`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
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
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4956e8e5352443d5e23830dd78e166cb1c7bc25ba8d0387e6aec770222563`  
		Last Modified: Thu, 07 Nov 2024 21:48:28 GMT  
		Size: 165.3 MB (165343481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c94ebed60262521ac5a3b50510085cbf50956f57829669588de7fbc8330d605a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de0ec805e4f179a7108ef7953bf8ef64db096a00309caf6357c85ee355f1fa2`

```dockerfile
```

-	Layers:
	-	`sha256:ff22a25f57ab9077dc1fd032953997bbdd9abf7f31bd1bdc7904735f2c65f132`  
		Last Modified: Thu, 07 Nov 2024 21:48:24 GMT  
		Size: 6.0 MB (5966942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3552032d776d79a9fb5dd5a3ebdf0fc327c007b1e8d6348943337185c83b9cd3`  
		Last Modified: Thu, 07 Nov 2024 21:48:23 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:49f4da834858012dc3a16fb5d98ed7fde06980c8362af594c353698e6ef003a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220497148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e2c96691d9cfafb0340f2a1c3550cf82a5aad2fc6901b0e259059b37ead64e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
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
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00449e8cb1de9a0fcf08b4ab10292a5c6983c6c53662682a0ebadaae9977bc53`  
		Last Modified: Thu, 07 Nov 2024 22:02:22 GMT  
		Size: 155.9 MB (155908577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aebd6c562f926754b03417dca58182ec0c4d21e7543eeffd989c3bb0a7858fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58e115913e64e6c64678e32832075d5768c5d9b106e11110a2bd33d04417389`

```dockerfile
```

-	Layers:
	-	`sha256:35e9c2a21fd24af41248f60de1c1a9776cc0ddf13f3d97ed8935fd62a0a119cb`  
		Last Modified: Thu, 07 Nov 2024 22:02:19 GMT  
		Size: 5.8 MB (5758472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d347a5fe11b7021f3887bf7d44c6e995bf3e449721061d89267f6259599366`  
		Last Modified: Thu, 07 Nov 2024 22:02:18 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.in-toto+json
