## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:557590fc33a87777589f53afab2e7b80d0c984d0b45b094113144ca3e9a83cdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a61a9b2c80f46d37c5a8356d24047dad30afc12eedf7b415ca994a558c501887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228734563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ce58e4134e0ae459d9308e8aca886c9c88030240cf8af9a6f22c5e9c8d4a07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab4403109afcb971348d6b67cdf6842e2df90378b885abaeb680ce29f9c2692`  
		Last Modified: Sat, 07 Sep 2024 01:06:09 GMT  
		Size: 166.0 MB (166039016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd9da323b1221a1fa14624dc2f9020b76ea9e21042a7691042dd68bc03ca4062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e40a7e22cf19d0b2f1c297f6be64e9ac4798dc11ad327d1d109b4854cb88f9`

```dockerfile
```

-	Layers:
	-	`sha256:41c72be8648babf1be1e4a7c426f26bac3706f2b92dd7068be2de2921c8ecb7a`  
		Last Modified: Sat, 07 Sep 2024 01:06:07 GMT  
		Size: 6.0 MB (5966104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9841295cfc42c6abc8f4ff410c506d1f301bc8c15f8d48c920e290ba526671`  
		Last Modified: Sat, 07 Sep 2024 01:06:07 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c42d1826fd7520d0657701b6677cff7781ce8cfefe09b8b10626c1c46a889994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221199281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59bb0fabe12c8e5f84f2d9645eee83f47994da9fe32326a226b78f7e36116c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523a6313d6028769e84a7f290ae636816bacc1a1cc1069a9bb2b4a4a1ee44b7d`  
		Last Modified: Sat, 07 Sep 2024 13:24:16 GMT  
		Size: 156.6 MB (156612938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:468fa947abb060cd28c4ff17b62bca102e9f42c210f29e3329bb270f28158c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5767917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb90b20ffe46ec702c152653c7d62e5d79874513a386eff8fa2a862d80d505f9`

```dockerfile
```

-	Layers:
	-	`sha256:903680a05726145b6276f32c92409dfbcbc4b2f83707f2952b494cd4a0464100`  
		Last Modified: Sat, 07 Sep 2024 13:24:13 GMT  
		Size: 5.8 MB (5757633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f751216e36d5bc5b328f884ed6fe8d058811cd784ddf7415d00a62f4504e8ea6`  
		Last Modified: Sat, 07 Sep 2024 13:24:13 GMT  
		Size: 10.3 KB (10284 bytes)  
		MIME: application/vnd.in-toto+json
