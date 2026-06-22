## `amazoncorretto:8u492-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:9eda05f87d3f9e00464bb078920a3960bed4f682498b5718b1c3170500b22016
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cc96f05fba60554c9b63603067878176a10fc9ecdbcc1b5e9f259a0f0a0de816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172098935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63389cf4b53ee0bdd0d1c59085cf02e0846ae9fea90252e99b6b171ddf1e2e35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:07 GMT
ARG version=1.8.0_492.b09-2
# Mon, 22 Jun 2026 18:14:07 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:14:07 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e3103e18d401a3214d092c5cc79d62a24b21266a8554b9eccb61407af897db`  
		Last Modified: Mon, 22 Jun 2026 18:14:29 GMT  
		Size: 109.2 MB (109156916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8b28d0b966e2fdc682829e692d78b5b42f0092fa3241bc219baa585e85324c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f278270c1c362911475786d38d2c870326e5a290abcd5caa417f0b2d4af8320`

```dockerfile
```

-	Layers:
	-	`sha256:1a5d0b142675f0122ef2ff683623613c791aa53820a26ed03b295938588b1a4f`  
		Last Modified: Mon, 22 Jun 2026 18:14:27 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bed2fceb45286cd1d0aaee25f94d7c55f4d07f75ba5f19943bb20d318e531da8`  
		Last Modified: Mon, 22 Jun 2026 18:14:26 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:696dd99fe6150c09dd1318f687d0fddc03feed3e5dd59762ab06997e1aa78ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117691732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04fbec0c709604b3b1a2370bc7403579943c3cecdbbe26338e7596d5cecef12b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:13:51 GMT
ARG version=1.8.0_492.b09-2
# Mon, 22 Jun 2026 18:13:51 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 22 Jun 2026 18:13:51 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:13:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3a230e2e615fa656af26b66a9218a9d17141098e9b25efb9c2a6a557728b51`  
		Last Modified: Mon, 22 Jun 2026 18:14:07 GMT  
		Size: 52.9 MB (52896996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e3491565edef9bd55bd8f8fd68d37cf25b9495fb30f86d6162e014e598343e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9e4beb9831f902ce68936e0a83da3e0af2213d9040d47a03a566e8271014c7`

```dockerfile
```

-	Layers:
	-	`sha256:a4b67ae3edd63057192483532793c18c71f176f125276e569c9dddd249727e94`  
		Last Modified: Mon, 22 Jun 2026 18:14:05 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05b206da58f3863557162cedc8349b12a0e9eb0d95df26b324d1c421ff195299`  
		Last Modified: Mon, 22 Jun 2026 18:14:04 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
