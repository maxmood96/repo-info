## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:5340a81c35aca11ccda409f79c469edd2623dbc107a2d8f7a1c82fd3d1cd730a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6bd5edd692e2dd5f3b2b691d5ec34c55d8d08a46a87020d129eff05b7c1afc91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150329247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d8c39a516b9721d3a8b8c8a6c978f9714ed03dc0fcff4e7124bd4e17ab716e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:31 GMT
COPY dir:eb203b2e14f406c161ffae3b2fa7ec59db3f5a04437b6e040395c2bc34835c5f in / 
# Wed, 26 Jul 2023 19:20:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:18:57 GMT
ARG version=17.0.8.7-1
# Wed, 26 Jul 2023 20:20:54 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 26 Jul 2023 20:20:55 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:20:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a8d554425610d474f28e23ecfc3224dd78fca045a5c09515dbf51a8606c33d8f`  
		Last Modified: Tue, 25 Jul 2023 11:25:06 GMT  
		Size: 62.5 MB (62451920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d52bfe5b6a25d45dd46a4daaef4fe7572801239bb8feb704c6176f3de0953c`  
		Last Modified: Wed, 26 Jul 2023 20:31:03 GMT  
		Size: 87.9 MB (87877327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5330c3db2fdd287087e23217266d6ec31cd172f490d9913496e6e783e435c1c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144045666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0a7ecdb30a57edb6a19d8f258c398b7907f3b121201e175438a549cd54e1ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:59 GMT
COPY dir:680654fa7b59b44a83c6e6e3392ca226b5dd93f22761e5f1147351db4c3466cc in / 
# Wed, 26 Jul 2023 19:40:00 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:21:30 GMT
ARG version=17.0.8.7-1
# Wed, 26 Jul 2023 20:23:06 GMT
# ARGS: version=17.0.8.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf
# Wed, 26 Jul 2023 20:23:07 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:23:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:51a637e5b43ccbed5bec2958dc012693f30cc3c6b3a2760e6d675bedbae44e84`  
		Last Modified: Wed, 26 Jul 2023 19:40:35 GMT  
		Size: 64.1 MB (64129279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f47592d04c5c6d7534c1464c95d2596a8fa74004e44093e8d9b8713b141f61`  
		Last Modified: Wed, 26 Jul 2023 20:31:19 GMT  
		Size: 79.9 MB (79916387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
