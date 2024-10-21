## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:1451be3517bac294a263614df7fc1849e2925295a1f29b231630eac2aace2a1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9aa2b009d9f846da6c88f730526175dc74e0fccdd3741aa03d32570ff8c69efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228022792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de33eaae5c49f92c85eeb671d7e6398195b3b008e39242b0b465d71fe32c74c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaeec2590364e6e172aa09ae5fa8afb97d4abbdabbfcfb3fec35fec1dfac3f0`  
		Last Modified: Mon, 21 Oct 2024 18:57:32 GMT  
		Size: 165.3 MB (165343253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cb57ef9c517c025581686b0e6e9c271e747251f4a7aa12ff7e7672e98be4d94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94c5d2ee7357ffb12d7142f278ecafea2381e67909112e7e1abaa8432651c3d`

```dockerfile
```

-	Layers:
	-	`sha256:0c74167c6aecc27ca5a376cd195d4d7692ecbecf6e4e4aa900a08cb193eef19f`  
		Last Modified: Mon, 21 Oct 2024 18:57:29 GMT  
		Size: 6.0 MB (5966942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da63c21287fba25c600debab5d60cf2850ec0344c6db13e923c0ceb341928c87`  
		Last Modified: Mon, 21 Oct 2024 18:57:28 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:858e1452d6dec074e4732403232b551d5b94863a4837a0d11aa229ea5899e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220480270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2a442225024c56425de241dfa576ded90544e071ee6b6f3936a737b572e651`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf70b67a3fd1dcf27dff4fe9f9532e9783ad04b527782572ed0903ce6dc568`  
		Last Modified: Mon, 21 Oct 2024 19:23:26 GMT  
		Size: 155.9 MB (155893181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a758f072b15fa076ace1e43dd5c76bca587e2f923930e03f660d6c2d9c108405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e245f72a54298fc12ddc1cb1c924bcd5b12464bb381e849a6dda19c809007a`

```dockerfile
```

-	Layers:
	-	`sha256:632726f86aa686575bfc86ffc4cc28def3eb9a8890f3a28d33b628257aa35243`  
		Last Modified: Mon, 21 Oct 2024 19:23:23 GMT  
		Size: 5.8 MB (5758472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b5db7978fe1e82ed0bbef8d7c412d49eb2b979a3c4ac09520dab557057e814`  
		Last Modified: Mon, 21 Oct 2024 19:23:22 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.in-toto+json
