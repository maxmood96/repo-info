## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:ba9131e76af7d627111ad623f73019a767115f0233a0fa005c56ce06ad73e8b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c3b7b763137da68c77106e99b0df67504f8157e7c3c7c5866e1d05df525011f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154063368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22572e52ff47cffa98e1b8b881dd5a54c029d597724af2d4c936d775b83a0b53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:23:24 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Jul 2024 21:23:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b888bb26c527613e32c5bb59892507bdf5c8eb8deb02148df81d12793acf81`  
		Last Modified: Tue, 23 Jul 2024 00:07:45 GMT  
		Size: 91.4 MB (91413962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a805df9ef9aea62a8deb56b818bb66396b72429af5ff35f27caadd9d812707ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e0970887d7ed57c3bc9a1f1cf1f136aff3cbad67633860272400e5b94973c0`

```dockerfile
```

-	Layers:
	-	`sha256:753841c361d8f71c7a440fb512eab712ab12b9d1b92afbf04ee8143e61dbac66`  
		Last Modified: Tue, 23 Jul 2024 00:07:44 GMT  
		Size: 5.9 MB (5860059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2fa294bafb77d68263bfc1b8ed4204be9cdce9b14b05fba549339cfce533695`  
		Last Modified: Tue, 23 Jul 2024 00:07:44 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a41575aa4ad6b6be3ea92f17501b9bb8c64521e1351c9128cf72f31cf8424293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146779850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bd252c31c577d7eeb5a7fcef406104133b1a3054a504b799dc6cc51c2e9d8b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411920c9cbcaed23d0e1ce2311288c8ba3ba769ab1879a1b3ec6328d2341f85`  
		Last Modified: Thu, 18 Jul 2024 22:57:07 GMT  
		Size: 82.2 MB (82204539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1f738f738d68e61f9e3e31c8e2f60c428c474113dd7d00f0478fa5a273ef25f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5660970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d28f34406eeb0a7d52a3b446eaa2af0aec0b28a92fce4af6b42eae7560ed578`

```dockerfile
```

-	Layers:
	-	`sha256:8784d933e8ad3de669fe566a77db09d14b881734a630459db3e6fbacb51f43ec`  
		Last Modified: Thu, 18 Jul 2024 22:57:06 GMT  
		Size: 5.7 MB (5651461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e63c805f8ac93171cc14c614677137f26897896e7831d1b071900cc482cab85`  
		Last Modified: Thu, 18 Jul 2024 22:57:05 GMT  
		Size: 9.5 KB (9509 bytes)  
		MIME: application/vnd.in-toto+json
