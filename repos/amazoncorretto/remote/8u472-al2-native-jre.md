## `amazoncorretto:8u472-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:964267b76082a674318efec283f5aca86ff51451b2b0d899fc28a36bd0c35373
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c0586589bb6649029125381d27a9298a6b4d5dfff308e7c323397d0d9c11e455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (172042515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035060908726bd8e05276f4bb5c6ed95f0d8805116ff9285605ad410010626a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:09:51 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:09:51 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:09:51 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:09:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb7c782c75907a9e339c8827206e8132f92d6864682dc271731ba525f86c6a4`  
		Last Modified: Thu, 06 Nov 2025 22:10:28 GMT  
		Size: 109.1 MB (109108381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0b65f85937129f5111e0a117bc9a076dd9cbee0e0a2ea9f26b4eb29d6ba9b0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5018e31f3ad71a32a36f1c8df11ca870edc688684cc9d253ddc959ca11fc00f4`

```dockerfile
```

-	Layers:
	-	`sha256:13789cdaacd106aa9a35bf40959ed6b3e047f7e6cea941addb9213f002089b59`  
		Last Modified: Fri, 07 Nov 2025 01:52:14 GMT  
		Size: 7.5 MB (7504128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e38912ab13c60a8464a7d8b5a009aa5050dce4259a64963107da0f8023ca23`  
		Last Modified: Fri, 07 Nov 2025 01:52:15 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aa38f6a72f41cb3b2f5fc58922cbab3c14b17f5fa0d8bef998426e21934d4412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117733191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c768d573883787f929873cea783ee7b44e92107fa61eb3adcb9b06c4514bd6a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:12:05 GMT
ARG version=1.8.0_472.b08-1
# Thu, 06 Nov 2025 22:12:05 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 06 Nov 2025 22:12:05 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:12:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b24050be1b3308f1b5e007a5d2e8249f056b58e9adca03bd3f919cc60f9c852`  
		Last Modified: Thu, 06 Nov 2025 22:12:46 GMT  
		Size: 52.9 MB (52939895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b49de0b086b5a641faa95a470eaa034be6e08ee4a26aea32839a0c0fcbe6a36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86805437103dcb435b76f1ab5ccda8f30c823d5ad6d4322924af11bb2ed36592`

```dockerfile
```

-	Layers:
	-	`sha256:e4694bf905f49638aa2a2fcfdc08fe30e919422c160d7c0795b2f094b0f18828`  
		Last Modified: Fri, 07 Nov 2025 01:52:21 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab4f70620e3c861fbdb3d3f1efccb55843428c9f3e146f7f16730b0135cae9b`  
		Last Modified: Fri, 07 Nov 2025 01:52:22 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
