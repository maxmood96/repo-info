## `amazoncorretto:8u452-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:43b4d437b8ef61d6f319baafeb7ebf02fe3d1f3edd46c1e5649e35891f2fc34f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u452-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3ad9a16fc555a1eee76ac3664736f6a287dcdd54ff77a87e89789e547bb3e6c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171869488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ae714b8208800390228f484d0b40453a56adae49f983b1a8f63ad259de2fff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Apr 2025 22:04:13 GMT
COPY /rootfs/ / # buildkit
# Wed, 30 Apr 2025 22:04:13 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 21:09:32 GMT
ARG version=1.8.0_452.b09-2
# Fri, 02 May 2025 21:09:32 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 02 May 2025 21:09:32 GMT
ENV LANG=C.UTF-8
# Fri, 02 May 2025 21:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:d95443c3dbb00d5bc2eae8f837647b2757c14518822de8c1758b9842856c04b8`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 62.8 MB (62759330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46293d789d9a0946dff6765d6671b3e0596b0a913ea2930800b9f2962f64d9c8`  
		Last Modified: Mon, 05 May 2025 17:34:23 GMT  
		Size: 109.1 MB (109110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f2de102bd3256ebbbe7c9100ac99f645e292d43cc77c1ede778f8bf590422542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4341d86c82e61fb61023d5a35bc5a0cf9c80d999ec8e8ee990f2e1cd219f9f`

```dockerfile
```

-	Layers:
	-	`sha256:17267306c5fa33cb4d8ce8cdea0bed1548db67ca9beab5febb1a2a1997ffe7d5`  
		Last Modified: Mon, 05 May 2025 17:34:21 GMT  
		Size: 7.5 MB (7486555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0399f81ed43f3138f90b6b32790355204a4f166ad544f5d8683c11ad772617a4`  
		Last Modified: Mon, 05 May 2025 17:34:21 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u452-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cbdb51511a861cf85fdaaa971447117c673cfd36f06ba41e852230357302dd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117536733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b53a2494020251fe9451112223fa84fa1455412ce293c3e17d1495f7b2680`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 30 Apr 2025 22:04:17 GMT
COPY /rootfs/ / # buildkit
# Wed, 30 Apr 2025 22:04:17 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 21:09:32 GMT
ARG version=1.8.0_452.b09-2
# Fri, 02 May 2025 21:09:32 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 02 May 2025 21:09:32 GMT
ENV LANG=C.UTF-8
# Fri, 02 May 2025 21:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:08a465b69ed13c6a3d1f2674c3766151b11bcb021ca0e952f6a01f81b18fb3e8`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 64.6 MB (64594727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2308f76682375e2039ecced084085fbf797194c7d5b6ca9fd1e8b53e95762cde`  
		Last Modified: Mon, 05 May 2025 20:41:23 GMT  
		Size: 52.9 MB (52942006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:257a4cc2cf083cd1f93c7c8e399e1c332e9c175729b38b8fc3cdc67f8b41ef5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5615559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a742c587a5a5b647622cbcc2327e85e09731bdf64a5c0211042bd9d780f76446`

```dockerfile
```

-	Layers:
	-	`sha256:9bf6aa2df4ea591806b6204dccb44dd991405c6eb341ba90c3b64073f7d81a40`  
		Last Modified: Mon, 05 May 2025 20:41:22 GMT  
		Size: 5.6 MB (5605932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8fc22ef52352f9bf1ddbb0fd7b32e10fcf05f766b7094aad6fdb3b29416c240`  
		Last Modified: Mon, 05 May 2025 20:41:21 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
