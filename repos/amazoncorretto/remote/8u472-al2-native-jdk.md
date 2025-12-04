## `amazoncorretto:8u472-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:d7b2df1ad461becdc41ff62f4a28b64daff20af3e24607b4c8e9ead1c21303a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:453d78aaa36bed9f227d4566f47fbf7a93ab5a21377cc04845921ae4d9500a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188177662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c084f0cd0e95401455d6a61167ab2a820c74fce37184fb98f1a6f2a6e19179c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:24 GMT
ARG version=1.8.0_472.b08-1
# Wed, 03 Dec 2025 20:23:24 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:23:24 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7680157bbfd411ccb71a00fd71abec2acbccc5edf69a16fb0aca83e545b5a4d`  
		Last Modified: Wed, 03 Dec 2025 20:24:04 GMT  
		Size: 125.2 MB (125247090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d42c506920f2bbc40eec4c639ea5a5263db0ccd11e309ec50b5dd358867b00c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7779aca012e2d13c0411e5409f01a26f20d6c709683d004c40b285f74dbda96`

```dockerfile
```

-	Layers:
	-	`sha256:d6b93260fc77ebff60f93ea98ccb703dbe9271c71659b4293758f64599f51ff2`  
		Last Modified: Wed, 03 Dec 2025 22:51:40 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a619c4482d4e608c68a38feed7ee783362ff7cdc966ad58942ad96ca3983072f`  
		Last Modified: Wed, 03 Dec 2025 22:51:41 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ca553bb64343957c8fcf939320231e452ec2c7dc39082ad2abeb7b4df730a8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132357574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5d59d5bc749a9e44d5cf9429dd7c388e8c9a2397346ad6fa8a8553d61b8e39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:26:56 GMT
ARG version=1.8.0_472.b08-1
# Wed, 03 Dec 2025 20:26:56 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:26:56 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:26:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e6508e4d0df745565df39fcabcc03864021da968de1771706f2da4a3c05440`  
		Last Modified: Wed, 03 Dec 2025 20:27:24 GMT  
		Size: 67.6 MB (67564773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c77ae7c3068e3f50fdeb39f899d3727d3b424e5e3c47eb504fabe0fa7f21b44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d62e649d935236075c3df51c58c088d717340b7e1b16eac1b1fa9eca8501f68`

```dockerfile
```

-	Layers:
	-	`sha256:d132941a97f04038f793900f0fce54df93a4991e62524e1d8c983fa340c284e0`  
		Last Modified: Wed, 03 Dec 2025 22:51:47 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f37589a0e485af247465003b8a0bc5b34208545fedea2b8ddf160a6d60e7f73`  
		Last Modified: Wed, 03 Dec 2025 22:51:48 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
