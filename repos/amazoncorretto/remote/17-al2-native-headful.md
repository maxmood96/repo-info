## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:dcd865c94b6b9dc9ce48eaafc3c1548cc983c0a9a51cde3a62955a3a50a42fb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:714f08e8578449a0f0b90d9df487762e0342e31d5eaf8be2450359dd62dc01b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154355150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422d600b995e55548434f0451e863ff7d6b6ae6ec27f9482e841faa7aa7ccd92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:24 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:24 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:34:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3464b70f25db7baf2d02996fbbbd6edaae14ec273b773237822b0ca8dd768019`  
		Last Modified: Wed, 22 Apr 2026 21:34:44 GMT  
		Size: 91.4 MB (91399884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d6bf76d096ac754d2a0d6cc544834935fa29ec34a6b83a86c3faa767ed30d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5876329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2eecbf993226ad582f9a8eb8c5d0f490c3932b30cf230ce4a49013ef3273eed`

```dockerfile
```

-	Layers:
	-	`sha256:f10a0a571d0b42fbb43472f71b35cf4ec25cd6edc7ff049e2c28b3166263cf95`  
		Last Modified: Wed, 22 Apr 2026 21:34:42 GMT  
		Size: 5.9 MB (5866740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c525ca61d52983202f79187cfe7c4b3ac30eab6d1e7f8ccb0155a34603086d6f`  
		Last Modified: Wed, 22 Apr 2026 21:34:41 GMT  
		Size: 9.6 KB (9589 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1e4a94562fefd4cb5ca3c9836067310a6035d63ea9da689ed649a2ad747fc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146901985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad44822d728a6a605a3dc5f8a3ec6b242c5797b2d865cc431d508638f4be4e0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:15 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:15 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:34:15 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9ba37299584e31b3225bf60c76c29949d2abf0726cdb053b447085e7c4cbfb`  
		Last Modified: Wed, 22 Apr 2026 21:34:33 GMT  
		Size: 82.1 MB (82099010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0f0b269b2d574a1268d923d8d5097cda95b0e7b57d263abad0e6fdc267b154a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23a4ada49b23bc77949844f51c11aa4b8160997e07df50031df19f7b28b2968`

```dockerfile
```

-	Layers:
	-	`sha256:c83ede01e004e0452548613dd5726b01f959a6a25bf000cfe541b68069c6e942`  
		Last Modified: Wed, 22 Apr 2026 21:34:31 GMT  
		Size: 5.7 MB (5658484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca61a3199aa74e7b89eb746b324543db3facaa6a5eb58e9d3013fc1cb4ada0e6`  
		Last Modified: Wed, 22 Apr 2026 21:34:30 GMT  
		Size: 9.7 KB (9669 bytes)  
		MIME: application/vnd.in-toto+json
