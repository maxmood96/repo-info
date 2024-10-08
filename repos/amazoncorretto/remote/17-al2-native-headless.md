## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:48b434aa6052b1f1af383305081954a19e8bc9732a1c98cee14a22160578d315
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
$ docker pull amazoncorretto@sha256:e44961517edb5b1a38d171e02a40033e817b9bfd41cef1ca55dafb394adcebee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144662452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0173294391446f503d6b5810e678493e8adeefad8b6e75065aab3faba8cd192b`
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
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
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
	-	`sha256:57bf50bc2aa5d59e6c68304bfb76801051ba1895ed48faec4dfae117fcae421b`  
		Last Modified: Tue, 24 Sep 2024 02:39:36 GMT  
		Size: 80.1 MB (80075905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8e6ef1118af9401ef37c3a929c1b11c3d5fdacda329694231e52a8058db0bbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab0569cdd5b2a5df184b985ab62a44c699d20b48fd4b08c58b1f1188a3ea7d4`

```dockerfile
```

-	Layers:
	-	`sha256:0903b325fa2e72afb9493e2e556fd05962add6e7bbdcac1230ac80a4baebaf1f`  
		Last Modified: Tue, 24 Sep 2024 02:39:33 GMT  
		Size: 5.4 MB (5442053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0e8c9fdc836fea880d2bb71a01e0c16d84d92c40fcdb6bb9c6093c4f0df2ce`  
		Last Modified: Tue, 24 Sep 2024 02:39:33 GMT  
		Size: 9.7 KB (9662 bytes)  
		MIME: application/vnd.in-toto+json
