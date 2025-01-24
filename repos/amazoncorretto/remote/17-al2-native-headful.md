## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:4da7519aac6f8c3282f467ef31b32df581603212be4b64f27adf8ce638cee58d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:56e00ba63875ea5e0fff826f43ef591356dd8254d7d8d39c67a1398fa1ba0361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153717311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d84fb9470210fd1a8eab4e45b73cf47944741721899cce8376d9c54233f33c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:24 GMT
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
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20533a75179a9515252eda4630e0222e6ff5ccaee013334eab8e9fe38ba3b017`  
		Last Modified: Thu, 23 Jan 2025 18:27:53 GMT  
		Size: 91.1 MB (91081481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:097c7ed61eb04dac55a575de5e08d2e9c437d4c8ed2a144d7a825c0493fd4eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aa3e15a85db6ad128309090439a8b5e8028fc0f15e9c75b1f028b945c0f0ec`

```dockerfile
```

-	Layers:
	-	`sha256:e6f5ff7c50ff5131c422ee79ad456eb39a788b123a20833d0a01953716f7b2dc`  
		Last Modified: Thu, 23 Jan 2025 18:27:51 GMT  
		Size: 5.8 MB (5849552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2c8b8eb65ebfb593bc2d32163339ec9118cc37261ad671cb304e206676efd2`  
		Last Modified: Thu, 23 Jan 2025 18:27:51 GMT  
		Size: 9.5 KB (9470 bytes)  
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
