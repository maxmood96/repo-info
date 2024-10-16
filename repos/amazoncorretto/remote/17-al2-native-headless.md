## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:9bce26a380726bbe0e3f86380b78458766e978f1b29342c18031b02bb8e864c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8c552ca57818cae2fe1c4a8be87dd43a6c1f034998e76d4a9ee61d8df5e37f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150079008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa331cad5bdb6ac091a2718ecdc41c88f775ac3f3493c6d604a8cc9bcc6ed83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:55 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ea112d23eb140db9e044cd990cd6196d4299e354e62526d6bf4d13ea09b81c`  
		Last Modified: Wed, 16 Oct 2024 17:57:54 GMT  
		Size: 87.4 MB (87400852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7b2ea0ad12e925e884dce0500dbe586bbb67748298a9f7166137d85c91db5ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5636264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5731f03bd93ba2af984c1ffe423726f8db9e3827cb1aad2c62335ab4f2021b`

```dockerfile
```

-	Layers:
	-	`sha256:3ee7f63c270c3effb4bb44897e11bb903c086aa72f36aee7faedc1ebeb9c532c`  
		Last Modified: Wed, 16 Oct 2024 17:57:52 GMT  
		Size: 5.6 MB (5626923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86f1d82d87d28d3e936d941b549e1673d1f99fab3d8802faf50a48177bff79ff`  
		Last Modified: Wed, 16 Oct 2024 17:57:51 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c2ea45dbb76aaa8c513d6aed2099843635676e191e7749c9a131bc1fbdbc784b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144276663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e431e6895b82b938f6863bec6070f2b76caa21ecdf53a474f568b3a338787`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:59 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08e26217c9dc5413b0295a090055472650a89c86b4634888893e5b234d98531`  
		Last Modified: Wed, 16 Oct 2024 18:24:21 GMT  
		Size: 79.7 MB (79684004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b01f587078b34393c3bb1ff1e0ebf9fb86090a9f13d1d993b08b3e2bbff8355f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0121c1ddfcd30ff45d40da86cbdf39fcfac1c88b205eb332c15451261a84a9b`

```dockerfile
```

-	Layers:
	-	`sha256:f841f35fa26ead78cf9de9673286ce7708ee3ef085a7ee3b23195d0ff60bff80`  
		Last Modified: Wed, 16 Oct 2024 18:24:19 GMT  
		Size: 5.4 MB (5442899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555689cd120f3fafdb33995195877db0f5e84416dd61fb93511416e838070f65`  
		Last Modified: Wed, 16 Oct 2024 18:24:18 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.in-toto+json
