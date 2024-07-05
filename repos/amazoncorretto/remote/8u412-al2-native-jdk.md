## `amazoncorretto:8u412-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:829def7064e46ddd69d06007f8978bd4291dbf26ec067342ceac118242db8e58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u412-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:37afe09f0ca3c90d22fbc3b7c9f43fc12c72087632d2be170d5eccca82f82a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187910212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274702f18ebf7a6bf615d9a1beef4b3d2b29e57a69dca388c47267c184151a17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=1.8.0_412.b08-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a507a0d0a8397053da7d90996ee7a4a065a9e5af867d8c914ada77b48467777`  
		Last Modified: Fri, 05 Jul 2024 19:58:18 GMT  
		Size: 125.3 MB (125263574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u412-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:718a7aad4680fba87835c44d3e9c61af9830feb8c4752f6fdd0c4902820aad7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7938943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772484e721477ff6a42a1c117ac37cbda8a4155b1d132055d68f7fa18f9e25a0`

```dockerfile
```

-	Layers:
	-	`sha256:0756355edf3645404377fb92be8973dad5f0898f92e586d8f8eb9f1863f4b458`  
		Last Modified: Fri, 05 Jul 2024 19:58:17 GMT  
		Size: 7.9 MB (7929589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158219ff1fda4dc36b94255d316419a15edf570786b0c70aa1c77c8a4d6aa81a`  
		Last Modified: Fri, 05 Jul 2024 19:58:17 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u412-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:60b4ecde39d037f61c1a9532d891d63398a6f48736c5dee298e5fe47b4adc95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132105051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ccb42d41db3b9029d144f089953dd3736d9ccf147e058aca095b6f2cce955f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=1.8.0_412.b08-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51031ede6b82c5f630ea72c3a606951d726af1ea7f3f648cf9dd60bdd8c62a0`  
		Last Modified: Fri, 05 Jul 2024 19:58:47 GMT  
		Size: 67.5 MB (67536286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u412-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:33415d43db200c7dbba5d52d94c5c626846a9e4d776928b9f84aac266313eab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6057495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5bcaea8e3f52cde2b7f74970fe48b8f3b50ed1fca1f31731cc6d0efdde5da2`

```dockerfile
```

-	Layers:
	-	`sha256:ab782a0ec7f22f3d7ebae8d6e6117d6c85ef6b5a39cee51d586c70135e5d2027`  
		Last Modified: Fri, 05 Jul 2024 19:58:44 GMT  
		Size: 6.0 MB (6047864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fcc846c2830e1617031621a561fd99a9d6d3bd16ddfb4ae124fd672a18386c2`  
		Last Modified: Fri, 05 Jul 2024 19:58:44 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.in-toto+json
