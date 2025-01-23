## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:4151f0e9ccdc8f046fc0ca7e77dd583e6dab0b272a2b9261993e435c0cca46b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e1718cfdd731a6c29c69b9142f8cd779fe500f571c024e6ba847bfee8db3de8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153708241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad0296fac2877e8825ada1ae9d08620bb59aa2e519d38a0ab254c1d3728cb3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536c041293ab7a9d1639f9e5b49ec37254adf85ccab4cf617cf814e7080db459`  
		Last Modified: Sat, 11 Jan 2025 02:29:43 GMT  
		Size: 91.1 MB (91072411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:57d3206e9fc32d3e3541584889e3ff4b6bc6c8616157227dc12a0c5e6e1190d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041d3b3aae95592374862d34f4436b02a70bd536933f8bb816e1824b84b487a8`

```dockerfile
```

-	Layers:
	-	`sha256:8c809f833eef03bd554f91458574b5b78c080413c1bfc423a11b03d5c15d34bf`  
		Last Modified: Sat, 11 Jan 2025 02:29:41 GMT  
		Size: 5.8 MB (5849558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:526da524b13188c0e415872f5393c8e640d3a7f324b9c54baf6a04c7f7f5220e`  
		Last Modified: Sat, 11 Jan 2025 02:29:41 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27e0238f2f87ee987fe4de175213786f3339e92a0180c5fd01adc2bb062b5b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146453111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a8d1163f7bc718e54db5524596a383ca694d6cc40c40a6357c5390c34c0a27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cebedb43e3bd303d5279a5896a5ba04cf6f470e7d5e389de2f482a7e5f8b3b`  
		Last Modified: Thu, 23 Jan 2025 18:46:04 GMT  
		Size: 81.9 MB (81862806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c2242ae6f5d229c4e2bebf6b4c56669660cbb9f5c7d1cda543ff2f18408b6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b949831631c26a688556ca3ba42a8f4dddfdcbe4b2802e2abe3ea9112c9138ef`

```dockerfile
```

-	Layers:
	-	`sha256:91c4508e8cb60ef8686989c5e2e6e96737666d202108a6f66684f841c02cc7ff`  
		Last Modified: Thu, 23 Jan 2025 18:46:03 GMT  
		Size: 5.6 MB (5641295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d95949b7099421173fe250cf19dd6134f63d94da64b4ab2956256f591757586`  
		Last Modified: Thu, 23 Jan 2025 18:46:01 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json
