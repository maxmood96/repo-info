## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:d8cf46c60e8521f539a33b38c00f342e5592fa999f7b73bccfa29d02d769dd6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:17398f96e75b9fa536892223fa622e55eb556f1636ca8d8bdbba462cc1c5a4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172053216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fa270237b9967c2f8a491f73a196dfa2514039e4bf7139b65880762c240be6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:14 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:15:14 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:15:14 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571eeaa98d5496af2ec59564a39355f1fcec9329cede87492cfdb9554131bc5a`  
		Last Modified: Fri, 14 Nov 2025 02:16:02 GMT  
		Size: 109.1 MB (109122644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9353d63dc56562e233c6356326592d4a93969503fa69b6399a4f3cfefc5a864f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd71defa9e5dca043821969337c0a9603f9e9c453bf7cc4129aa36144aa6a4a`

```dockerfile
```

-	Layers:
	-	`sha256:6cdd80ac74d03a4bd3c9723b7582f69e4ab8ac30197e1531c52eeb7ab5ef1a59`  
		Last Modified: Fri, 14 Nov 2025 04:51:49 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb982d9b0f3dd29982a76ba6ebdb968b62d70c6b1ccad3d49fadf9d56ac9aa6`  
		Last Modified: Fri, 14 Nov 2025 04:51:50 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:92491df25d39c1962d29740db50b3b319246db47ac536e69dcd98a42afa67135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117732753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d75cf0fb35f522a6f656f68afa986c1e8bbf9bd0b0612d2cf2625c1da8e415`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:25 GMT
ARG version=1.8.0_472.b08-1
# Fri, 14 Nov 2025 02:14:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:14:25 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205d9f4cf6163c83fb299b73286a379b86ed2e8d2f82b96ddebff407348e7b01`  
		Last Modified: Fri, 14 Nov 2025 02:15:16 GMT  
		Size: 52.9 MB (52939952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3d2c967ccc97ae53474c5c574701b061abaaa08bcd926cea4e8175833b2d6cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e11d6728ad32670da9f5ad994dd93a676bfe815170ee7f16fa4ea32907cb497`

```dockerfile
```

-	Layers:
	-	`sha256:f8134a1c320b7c267cdb5fd9f34915de7d1e40e7434a753d636477c2263a81a4`  
		Last Modified: Fri, 14 Nov 2025 04:52:20 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0475439bfbfe66efd12c78a6d0ef6f6964e3c4e071dff4389df3240052a7eb75`  
		Last Modified: Fri, 14 Nov 2025 04:52:21 GMT  
		Size: 9.6 KB (9582 bytes)  
		MIME: application/vnd.in-toto+json
