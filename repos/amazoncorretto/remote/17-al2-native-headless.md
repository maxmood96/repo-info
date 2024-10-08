## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:f4bc0e9f0e566668203fdf32ff9980a0257956c1b625c63c6db8accf3135cba2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3f2763beb9e3c1d21f63a112853fcb380e1dcbdf3ad2848123022ee4deb4313b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150466164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931b435a4cf0b98a72c52d2a2ee3123e563f83171a977da4c4d97a8d3ce8ae8c`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
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
	-	`sha256:ec22928a5e71f121b84156f696adfbc74b0c5364a55f935882a57811d20584c7`  
		Last Modified: Tue, 08 Oct 2024 00:00:15 GMT  
		Size: 87.8 MB (87788008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a180e0fa408f4fa584ebf3847fdc1e86ad2280cfbee0a274cb216c626a6bb009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5635398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9194e239215456b8b37e9dc53e0f233d5fd5c7d1a8c22052a2b49b24098d2ab4`

```dockerfile
```

-	Layers:
	-	`sha256:d3d8ad53bc096acd647bc4c50854e9e273f4d8b376dd9e58785e11408f094e64`  
		Last Modified: Tue, 08 Oct 2024 00:00:13 GMT  
		Size: 5.6 MB (5626091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a86d3e515e4822629ccd291142270f9d36e782fdd84a5530b32f4065ca7a621`  
		Last Modified: Tue, 08 Oct 2024 00:00:12 GMT  
		Size: 9.3 KB (9307 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a5cc9bd397135619dfbcfaf0adcf8a621b28b4431b2f07e4eb6e15ea4973c878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144677167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcaaf9c16ea8d72a8e47ee6065425818388d97a691665ddef7ea9900fa2b87df`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b333205913e3817984abae4e579ce0b3af6eb31e1046861c78c06a27758917`  
		Last Modified: Tue, 08 Oct 2024 02:07:32 GMT  
		Size: 80.1 MB (80084508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:06d46dac65f426cbbcf7f313a0963d4655bd37611bb57a5427ae309f38882966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23726399630cfb42586a2fd1811778e31368c4ddbf211e56bcd1c5f96b3cf186`

```dockerfile
```

-	Layers:
	-	`sha256:8563ccc6e608c3aa5652071c061a1afa65c29f8368cab8c464d8f28dd001f9b9`  
		Last Modified: Tue, 08 Oct 2024 02:07:30 GMT  
		Size: 5.4 MB (5442066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac25dcd0112d9346ef2c6a66cb4286997d8ae75f3af8de575a96ed9f177caed`  
		Last Modified: Tue, 08 Oct 2024 02:07:29 GMT  
		Size: 9.4 KB (9386 bytes)  
		MIME: application/vnd.in-toto+json
