## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:500226e78f30fa9d204bb0e381fcd6ea4acb4f0203ba18165eef470bd8ec18bd
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
$ docker pull amazoncorretto@sha256:03dbeeaf3d877e3bc1bceed36154f5cb2fae26856e58ba86d65395a5c5ca2050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216952034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9a250f54a12b9ad8a2626f5ea5560f644760c1aa589412ca5b793a2bf1a476`
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
	-	`sha256:928bddcbf112315a029f894cf829df2ae1b28c89ecaa6c142e3d47e62c803337`  
		Last Modified: Mon, 21 Apr 2025 21:48:49 GMT  
		Size: 64.6 MB (64582610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02022c51525511543090ddab802f3772b68c7479f11ed4af0973825b34cac9`  
		Last Modified: Thu, 24 Apr 2025 21:15:03 GMT  
		Size: 152.4 MB (152369424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df698344951cd4c358ba16583f0e2f3b6bcb1e1428f637749f365b8b410f5793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5782966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6cd6bcd9bf9871828ace7f28a3062184497b023d695c8d373601397c49cdff`

```dockerfile
```

-	Layers:
	-	`sha256:6fc7f6b75ef8939fcd20b7045eeae0dd9130353d4f706885e5d316f0d111556e`  
		Last Modified: Thu, 24 Apr 2025 21:14:59 GMT  
		Size: 5.8 MB (5773446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d8d229aba21e10e1b828155a8399f0b1ef189a0959474aed35216d6a06f06e`  
		Last Modified: Thu, 24 Apr 2025 21:14:58 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
