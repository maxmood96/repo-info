## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:3652076f67949580decfcd69640a94394c242526d8fadb5bc91f098c8fe79a6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e5853364b37eea6c3e3908e790b64227899c41312214bc178ea89a5f7ba86afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224623319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a31bcae17cb7b183eeb04a564fe777657ba89892032e962ae6156358e39b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:43 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:43 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:11:43 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae9a00a963e8080e1368e94ecd66a44b832fa17ab871ac864c6ec3c23f8a475`  
		Last Modified: Fri, 22 May 2026 21:12:05 GMT  
		Size: 161.7 MB (161671344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b222a01d2cd392cead9d6c1b55704a0ca47cc80362cf31d1dbf30591c83ec8b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f533e5202233a799d30250d5760ba46ee2622ed289557976f3ae1aac9ca1aa`

```dockerfile
```

-	Layers:
	-	`sha256:af4cbe4472bf9347f83004c6bb926f7510779d57e795709593f8bf4bd3c46cc3`  
		Last Modified: Fri, 22 May 2026 21:12:02 GMT  
		Size: 6.0 MB (5995185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf95e39254023b70c9729c1881239421d2ca1a2cf384ded5b6482528fdbb6a06`  
		Last Modified: Fri, 22 May 2026 21:12:01 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:30ede686c06e92315de6e3b71410292f68753152d4cecb5e8ce1e158385691b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216511989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1112ea8df690d01c50e41dc2180c22ca55646b908bcbfa8443e629b5ff3a7b5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:14 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:14 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 22 May 2026 21:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f76e0dcc516d181e29b6f705d4089fdbea33f02c5a81c782cb0db23bd0d454`  
		Last Modified: Fri, 22 May 2026 21:11:35 GMT  
		Size: 151.7 MB (151721972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:000a8d0910d493fde9e9b78f07e0c9540d69e38733de1e6cc9abf4e74e782360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c726348c7f517a22b58de57ce08e479126bf826e94968b5e11784d789c151cf6`

```dockerfile
```

-	Layers:
	-	`sha256:e48489332bc408b522eb675b3c6a7da69350d8ab35d6adc40ad39247f156b721`  
		Last Modified: Fri, 22 May 2026 21:11:32 GMT  
		Size: 5.8 MB (5787899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4734e72a5376eb0610188bbd55e223b39c64f5abe87682dbe9dec69447ab2b`  
		Last Modified: Fri, 22 May 2026 21:11:32 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.in-toto+json
