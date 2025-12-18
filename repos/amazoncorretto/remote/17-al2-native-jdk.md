## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:76e834dad4111bce121ef3042d89c97a3314e566ad699f610479d5715cfc3ec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:31869d2a9105a02612283cac6231baa2e4be4a7d29c2de08895adcb7c5a7eafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228692097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b54bae99427c5fe1177b472305560ad8429955171a3bcaab92422655ebb0bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:39 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:18:39 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:18:39 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a2d877e41dc1e606f13ce427cf6366e8b76e87ac35e1701c9422f3e70e34a`  
		Last Modified: Thu, 18 Dec 2025 04:49:48 GMT  
		Size: 165.8 MB (165751122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1eb7c51fd019919f44c38c5b3141d8faec1cd8ec588a5d4cb32cf36b4f526b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7db8e25c24440c239c47d34a778bff3e6f5f68f908425e981414cab95bdf20d`

```dockerfile
```

-	Layers:
	-	`sha256:34d60e2822e70ddd95e211adb1d6afb4b7a9dc812df98c4b1f02d8548fcc6040`  
		Last Modified: Thu, 18 Dec 2025 04:49:00 GMT  
		Size: 6.0 MB (5971824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c42411863cf4c6f0ac427a72154076fd39b3d4adda761a13a4fc0f143d65c5`  
		Last Modified: Thu, 18 Dec 2025 04:49:00 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ce1699f407dc97bbb9dd39ce269430eed49fa656bbf05082b42f09eb20e1a59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221067045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9018f690fe66a1fba378b2ee6c0a0211896bc667a60843a051c928d4ebab950e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:51 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:51 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:26:51 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96447ba0d7eee609f86bf5c300897cb871a4d81563246a67123e7e2ee40ef22d`  
		Last Modified: Thu, 18 Dec 2025 01:27:30 GMT  
		Size: 156.3 MB (156271290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d13139c164ff4a3bcb4cba784f438646937083264ebc85ce51d53ad72fa6cf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b2ff7caa7ae3b944a4967fcbd7f452c229037431d448d26a64210e826720f8`

```dockerfile
```

-	Layers:
	-	`sha256:3855a27604a72dc19ef969c728a47481cd82ba22d82ad948e2373293bc16e16d`  
		Last Modified: Thu, 18 Dec 2025 04:49:06 GMT  
		Size: 5.8 MB (5763694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a5be5e67828a321086737e51a5d8b0e1849542a75257a697ed9cce00954cc1`  
		Last Modified: Thu, 18 Dec 2025 04:49:11 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.in-toto+json
