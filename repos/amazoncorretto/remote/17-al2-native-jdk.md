## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:06c137dfa57632e85f04cab753ba729a8c80393929b4627719f5a23b701f27e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5231c7a92f4446d1745b7bb59e8558d9a53134d9781c42ef2e050ef41043a00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228663415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb300982577d19c51403026b01714416351cdaa2b08e77bf1ca306dfd98d4d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:20 GMT
ARG version=17.0.17.10-1
# Wed, 03 Dec 2025 20:24:20 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:24:20 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2cc40ee11b2207643b6ca75000314d41bc9d1f56806de21f7a7406ec3d0d96`  
		Last Modified: Wed, 03 Dec 2025 22:50:22 GMT  
		Size: 165.7 MB (165732843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c64297032a0e5ac31f3d12872c35f20cf123d034b8f5484f095e989793b16ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f97701ede9b91a09de1269a58590ee1020ef1f29eabb9deebb924a53bb24a8d`

```dockerfile
```

-	Layers:
	-	`sha256:8da50d4df4c4baf645fde4a22f2818b32226ad88e8eee72fd5c2d8c86543cb50`  
		Last Modified: Wed, 03 Dec 2025 22:48:57 GMT  
		Size: 6.0 MB (5971824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238bbe31dd30a2b296b0d55feb5b8d8b25de5be780611a13d226bfd8cebb77b3`  
		Last Modified: Wed, 03 Dec 2025 22:48:58 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:419a3926a4296b9657bbe05f4fecf9d6ee26623aefe6ca6325b8cfb3c22a6ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221063557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a366556c5d294789b5eb8beb7eaed9079a24aa16952e42e4acd4cd57645e3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:38 GMT
ARG version=17.0.17.10-1
# Wed, 03 Dec 2025 20:27:38 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 03 Dec 2025 20:27:38 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b96d63ebea720bf2d17bdabc0d63d6ed5202348df59f51d57c76188b2a9866`  
		Last Modified: Thu, 04 Dec 2025 00:03:31 GMT  
		Size: 156.3 MB (156270756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aec686a9a0d8b38d084369fe011529df6e10b041ddbe5f08ef4a2ef51343c9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581643d282acfed753e00a441bf665934aa02dbf4290dcc083af9073707d0901`

```dockerfile
```

-	Layers:
	-	`sha256:80d3c0d901bde219132ba2f2dd98c14f0316cc1650eabe77db07a8db1adca167`  
		Last Modified: Wed, 03 Dec 2025 22:49:03 GMT  
		Size: 5.8 MB (5763694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:888c9c5b9ff3bda2a6b4f434891807f80d65f576f68fc04da7c7a4c307059140`  
		Last Modified: Wed, 03 Dec 2025 22:49:04 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.in-toto+json
