## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:70f62376d1c134c61cdf8b59ea3b06e87c2aac376f6547d5e5d7a3133b79fe02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f5fc9fd0ea83c412521c38203b3d528639b678265da0a691521c024b265d28be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172053446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b199206486e57c8dedda7c16e44d79fab3e275554aa4e3d18214ae044382f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:15 GMT
ARG version=1.8.0_472.b08-1
# Wed, 03 Dec 2025 20:23:15 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:23:15 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d41d5f6ce8992269075ea3d61f40163d98e766aebb5245fe397c7dde9249785`  
		Last Modified: Wed, 03 Dec 2025 20:23:53 GMT  
		Size: 109.1 MB (109122874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ee41e76ff37bebed18b931c6842c1715bbac212b3e494aabbf1400ffe0fd05f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc672161099353ec786154198d3497f5838afe2dec9564f54c9d02fb8c77585`

```dockerfile
```

-	Layers:
	-	`sha256:ca8c156d27c57ce82e69c7e6df4f207022bada89352219a38120ed9662ceff92`  
		Last Modified: Wed, 03 Dec 2025 22:51:47 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0737ecdce8678e2a15fe2f9e91df85821d0bedcd74b7dbe37dd8b01f738d0e94`  
		Last Modified: Wed, 03 Dec 2025 22:51:48 GMT  
		Size: 9.5 KB (9505 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9eb1de6710d4d342634b3972e6543dcc968c16669d17d1279201d271fdaa2c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117732678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b1adc6e9ba16471a676c8438f6d1d5da7575012d42d806ef5e6e851c004ec6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:26:10 GMT
ARG version=1.8.0_472.b08-1
# Wed, 03 Dec 2025 20:26:10 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:26:10 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:26:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b016973c8491d940a3162e386d7a7d71a8ad9f7877351329c2afb965e2690a3`  
		Last Modified: Wed, 03 Dec 2025 20:26:36 GMT  
		Size: 52.9 MB (52939877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8952e7948e454335227812c8de696ff7ebdd9ab4284b3a265622f6b7bada4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69c9a5b7c91d8a666304f62a7dfc8f08ea587d4f5f8afb76e09ae96e231f84d`

```dockerfile
```

-	Layers:
	-	`sha256:c9c711d88080463d5629052cd2721ecedb434713eee1f38e689f3e9541bc7016`  
		Last Modified: Wed, 03 Dec 2025 22:51:55 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e20e8b6e5ee0509a90f94e663d4b311abf48a5721dae7da58c90bc66e5bb6be`  
		Last Modified: Wed, 03 Dec 2025 22:51:56 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
