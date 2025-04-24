## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:c67666fc2241cd9fe85f89dc956cc1cfae845c1cb0b197237b948419c9a38d0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c38d30c4115b17f2bc09d96ad60e7d20c8b018ec8d812fd9befe25e0371dfec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225011256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8fb4f060b48a73c3c22cb031b3e35934fc6460ba14dc2bd7c5cfd5313cd941`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613c87a6c29779bd7bb11a74a287f4f70b58bb0da9e84cf2e99900c39d946de0`  
		Last Modified: Thu, 24 Apr 2025 20:08:28 GMT  
		Size: 162.2 MB (162249534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:877111a98c8cf7322c8c02a1310597de695f3bdd6fa26ff0b10ef3589d274320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5990172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73885575b326069acf3dd3b91185161c395449ede80ca31df88a25fcc3d327c3`

```dockerfile
```

-	Layers:
	-	`sha256:12a5c93128dcf154b952892161cc043573c97b9e4591a0431791f2ccc975df41`  
		Last Modified: Thu, 24 Apr 2025 20:08:25 GMT  
		Size: 6.0 MB (5980732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a10a576548f7488e2c39d110a803d6ff8462bc828e277e13de44d3affa8a5b73`  
		Last Modified: Thu, 24 Apr 2025 20:08:25 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8ac6769592098a2a4786bb4cdeb0491e91610cbb5c09de91088797c263f61843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216889936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4553fe39a6ef59617f89aa448a057531faf4ec21a47c92bdc03f5504b3debb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab0349f22158a97a34a6f68fe3cd87eab40b77552eaea1103d4dd124c6e4300`  
		Last Modified: Wed, 16 Apr 2025 00:05:27 GMT  
		Size: 152.3 MB (152324114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:03284915b358842243c98257b09e2bea8b13f19ba4481d2d7849f23e32077975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9e3b45019779edb4e3d3d3c65f1c22c94bacd4dffef2b3380858c2e8edab6b`

```dockerfile
```

-	Layers:
	-	`sha256:65a1d80acd86802de7c656693f526702419673d74e1eaa40c2dcd90c70ea7ad5`  
		Last Modified: Wed, 16 Apr 2025 00:05:22 GMT  
		Size: 5.8 MB (5771560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305c2a5bbd1b5e2626fbb77ef925c2fe9b85f4897b9b56202bf636c9fbe8d9fd`  
		Last Modified: Wed, 16 Apr 2025 00:05:21 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
