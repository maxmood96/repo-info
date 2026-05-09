## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:47b0a402e54292be04219a9acd7eda41ee13bc643a3176e2074ecf65dc840d7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:900a291421ee16bdcb5d005cf03ade97232f083a1ea8c904ec9f9bc429fb3c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217203284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f487fb6b3313cfe185d8032bc96d5e29e9486ea1488200566e98eb24687adffe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:05 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:18:05 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 09 May 2026 00:18:05 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b32f53ab90530438e60b6845f0ccded19d7e8da9142bf078eef2f3d7bbc55b`  
		Last Modified: Sat, 09 May 2026 00:18:27 GMT  
		Size: 154.3 MB (154343546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bdf431cb3dae77952761bd250107c139ad1b52b0f7c03ab66f6f213795cfd14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f2e8791d83fecd393418a0e1bb34883f3886aee15f9a34ceaf06d401c4af57`

```dockerfile
```

-	Layers:
	-	`sha256:deb31fe78b00194eed8d4adbc4fadc6d15ac11d37ed2e6ecc225136fa68926ad`  
		Last Modified: Sat, 09 May 2026 00:18:24 GMT  
		Size: 5.7 MB (5683406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27455e9f2dd32f8e38161f83bfc5c484ded43af09cd4b8267f0916ae7dd69e0b`  
		Last Modified: Sat, 09 May 2026 00:18:23 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:24dd7dd9507689a376077a8c3cbebaca5869225333ce3250a51d090d67dd823a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211439882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018e9591552da69de4af8f0da0a83890b9069be0108e3eb353c33205469a116d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:52 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:15:52 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 09 May 2026 00:15:52 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad295d6ecafeb8c89c0b0a77e625209fcd6626667c23ef7910fa5b8c482b7b0c`  
		Last Modified: Sat, 09 May 2026 00:16:14 GMT  
		Size: 146.6 MB (146630967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b873965eb22a14679b0bcb3238e8260b04ffd58abe62ae1bc69d6562331d936b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d49c63f0e0c0b733ad2ce18641ff1e5a392c80b4383347f868184ccb53fc79`

```dockerfile
```

-	Layers:
	-	`sha256:a84a36be8309cf948829dfc350f8f5a3f50b5bcfb5cda51d00065794675e6896`  
		Last Modified: Sat, 09 May 2026 00:16:11 GMT  
		Size: 5.5 MB (5501874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776760ea417a96a7dda152bb9ebb1e62dca2c7f86fb759a036488e2121a8ac22`  
		Last Modified: Sat, 09 May 2026 00:16:10 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
