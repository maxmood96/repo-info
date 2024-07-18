## `amazoncorretto:8u422-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:1c16972a8ecb6a1182d917c18bc9729df6ac12ad863f3e20ab4b4668a7dcb53d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4be9cdd3a79102e941671c33fbe2c03576944566daa939008818faa82302ea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187895412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945ad06ec167f552dc0c5cae8a23af89ca00ee15512f22df96a8da812431e92d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d655755d4a6f4cc25f35ab72d8b2da7f456ec5e70ae3a024685dff5d981834f4`  
		Last Modified: Thu, 18 Jul 2024 00:56:21 GMT  
		Size: 125.2 MB (125248774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:86d51ac5e141c42c8076ae05ec3098668c8f320f96bce4ee6def5636b2626ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0e304b9146f7f70dd1d0a0485ebf1c3f52bb42de981306afc5b7586262dcbe`

```dockerfile
```

-	Layers:
	-	`sha256:82b1c7e2948f9caf1ab401ab7e07036e085d2cf4ef10bf75ce7f5fd6988c5a07`  
		Last Modified: Thu, 18 Jul 2024 00:56:19 GMT  
		Size: 8.0 MB (7971152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6447b8b4ab731fac6029118022e3f535615540da614978f8a29dd71a2aa6fa16`  
		Last Modified: Thu, 18 Jul 2024 00:56:18 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8b7c50dded30e8129e9baa31159f4563e1c8843ce1a6dcaf79aca5a4707e33dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132108021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2c3f912425190e6e87774057ee54a88640e76be771ca973b22162b025f26b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeecd19b69172b855b808361322fa1cd35d9044de8780f2a6ba94eed0f4507a0`  
		Last Modified: Thu, 18 Jul 2024 00:58:08 GMT  
		Size: 67.5 MB (67539256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cb77619b48675df95afbbcb3eaeb3f7c70f679ed5b9abf83967b88f6fd41c039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5eb12117f2c94d03e9a4ce3c060ea54c07399f2c03ed76a88ccbce696e1c20d`

```dockerfile
```

-	Layers:
	-	`sha256:27ec9c4de8e2b96db9849915c38447da0ba0240540e081dcb5e41ddf70d1ed93`  
		Last Modified: Thu, 18 Jul 2024 00:58:07 GMT  
		Size: 6.1 MB (6077693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4e586aac50264b434197ec49308665ab134118e601b74c322a5d2782fb72de`  
		Last Modified: Thu, 18 Jul 2024 00:58:06 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.in-toto+json
