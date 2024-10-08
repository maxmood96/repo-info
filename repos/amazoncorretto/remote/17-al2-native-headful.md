## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:3a24d11766421d0ae739b924fdc02b5577f5ce06c7a072c2ed05198a3e98c1fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:939419dc98d0af1265cf562908f8880aea1c0812723f7f4fdc1e8b919b8cb554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154110039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f081f2bd2baf56fc112bd1f60bb78fdba7a9fa2d6f610f360a1c56191ec1742b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23d32fb2cd03da7e66758560ce5befd775a62981ade212285ac6e03e9ae22f8`  
		Last Modified: Tue, 08 Oct 2024 00:00:18 GMT  
		Size: 91.4 MB (91431883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fe9c2c4cc3c2e6954ccf7d85586f3e0891d84d91f33f44b5323bc733c2faaa92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5979ac9c8d10789be71662ecb4ceee65797e78e65d14811cfc8e27fd040485`

```dockerfile
```

-	Layers:
	-	`sha256:1f804a6225303164c512484d54cb1daf5174367d186f770683d82bcf567e7b5a`  
		Last Modified: Tue, 08 Oct 2024 00:00:12 GMT  
		Size: 5.9 MB (5860088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f0f05fb85f0a9e95786b64f887d6c93e5531bdb45ca5e5a6912c8b0f4d26d8`  
		Last Modified: Tue, 08 Oct 2024 00:00:12 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4dea889701c3d2219baa6251daed9b4f2dd53d35a4ce6c829ecfd45692301e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146778753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560fd89378cc5a8d41bb44310d1179559da87330ebebc3169136008bac4b9d9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbaf728ad418333b47d1abccc8e51ff10a5136d6f9a63532f87594a411d7cea`  
		Last Modified: Tue, 24 Sep 2024 02:40:38 GMT  
		Size: 82.2 MB (82192206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7a35b150bccbc0523aa3f26e2b9c0dacd6ca1712d8a238fd0d16fe7da4e35c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fba60f79dee0a47385e58882daf2d1e78315e97e5c16d31328231a32ee0dff`

```dockerfile
```

-	Layers:
	-	`sha256:93898e0da5c8b2dc141dc5ba75cd53dc5b6e0bc811d41e8397e12b051910f0b9`  
		Last Modified: Tue, 24 Sep 2024 02:40:36 GMT  
		Size: 5.7 MB (5651477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99da78e3270ad40ad103d9dddbf7edd1dc8e312b38b9bb2a851c5cf999b4cd2f`  
		Last Modified: Tue, 24 Sep 2024 02:40:35 GMT  
		Size: 9.8 KB (9798 bytes)  
		MIME: application/vnd.in-toto+json
