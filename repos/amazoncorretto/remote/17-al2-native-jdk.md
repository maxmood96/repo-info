## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:1ea2515955036fdb430c2b0b3764c3028972f0eedea5ee1c694cf0493b81d2df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ab3fdc6d6f951fa26540177a4b6bc6ddaf0fc688f48a9a88ab4ef2ae835fb296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228663192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34574fafdeae825bdee41a1efcbfa6b040f8e0cfe90fa67406e80d8c9595150f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:05 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:17:05 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:17:05 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5391a5d09d76a9d4addbb76ab7137bd44e2181b27f59d4ab0b80b933aa585f07`  
		Last Modified: Fri, 14 Nov 2025 04:52:59 GMT  
		Size: 165.7 MB (165732620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20dd1f2b57c7d3915309b91e7c6baa40fb768fc3b2c65044baf0adf05849a812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d0a1ddb1f7b2b596bb13c6facc8a8a34c9670e09e512d0be7d35eb371d8ebb`

```dockerfile
```

-	Layers:
	-	`sha256:70e2c859fb792c64e942e4eb2c9fdf2c972a618262996ad376848a983b25ffe0`  
		Last Modified: Fri, 14 Nov 2025 04:48:58 GMT  
		Size: 6.0 MB (5971824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a89ae5d8172f87cfdf8e625c8bd2acab332591695f2a19cd8cbd2adbf6cb2db6`  
		Last Modified: Fri, 14 Nov 2025 04:48:59 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2e99f6d9728a7655eb33d29691fc1d854df414261cdd087d5c98e20d99f94200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221063627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf2b38f9cc636a13be47a818409388f33377fe326c0aac96b153f8bef8abac2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:19:37 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:19:37 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 14 Nov 2025 02:19:37 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:19:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0090cad553bdaff3a93c4116c8dabc4db09e0db6b6a48644071bece6f74fd26`  
		Last Modified: Fri, 14 Nov 2025 04:57:45 GMT  
		Size: 156.3 MB (156270826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:676526ad441ca0a21a022a3b8e5bad2185cf2350f5bc35cc13ae178a928505f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff65d7124862e86b1959ef0b3920c378f733b148c27daf81e88541e58c1e0407`

```dockerfile
```

-	Layers:
	-	`sha256:8865eaa9830c16feaf64b2ddc021f446f66429e5b5f165b6179b43b49be7c128`  
		Last Modified: Fri, 14 Nov 2025 04:49:04 GMT  
		Size: 5.8 MB (5763694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74e84771daa8e5f91978bf9b3f8a4bd145691b00338287db60c191e8c180dc7`  
		Last Modified: Fri, 14 Nov 2025 04:49:05 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.in-toto+json
