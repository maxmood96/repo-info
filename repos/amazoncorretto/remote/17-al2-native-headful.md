## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:07b86d19f9758867d23dddcff36ae1e50764e996994baf60a5e4543b66acd5b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5fbe67d9f5ea8079be7a0b511ed7eacaac91a6c65ed0dfca8ef50e8cf46ff6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154247282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76333d86436522adce67db646ae70ddd45414bd46bb8a236b713e0385f12df9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:25:42 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:25:42 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:25:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:25:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d43ecc8d72b2084d886c58e7130d3e2e797f7d30b1509f5ca2da4822cb060`  
		Last Modified: Wed, 15 Apr 2026 21:26:00 GMT  
		Size: 91.3 MB (91292016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6983edae541a59b3b679036e4ec2d1be7f3929f7b1e1f73d7223db2eeacbdda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7048bada75f24e4d676ccb0d2986339ad9133f6f26107d79b89b8e4dbc94b8b0`

```dockerfile
```

-	Layers:
	-	`sha256:f0f9493fe3b5b2596018f90213305bb7427b9eb821f094309a36dd2c0fc1e901`  
		Last Modified: Wed, 15 Apr 2026 21:25:57 GMT  
		Size: 5.9 MB (5865915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65ea3b10ec3ebfcd082adf403e5e0ac4c681dfcc19f17e76aea0e3e234ccba1`  
		Last Modified: Wed, 15 Apr 2026 21:25:57 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0dcf3d236b5b90ec2fc52d37ee20e24a66af6129c5c624fb0ba54c343aa62bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146777846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a8034096a2aeaff7b0d5c9996a029742ab1f6a0d9a3a7d2253a051c13584dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:16 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:39:16 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:39:16 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95818160894e29d5c208af5c2aa327eb84df6fce3a0fbf7e613f62509afee177`  
		Last Modified: Wed, 15 Apr 2026 21:39:35 GMT  
		Size: 82.0 MB (81974871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2f1438034f5108c1c6b0d09540a8216f5f4ae53086b9bc9ebe911d772d18052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb04a08a03620d7a5d145e63aacbe791475b115dbdd5caaa37fc17fdee6ebc`

```dockerfile
```

-	Layers:
	-	`sha256:56ed5c5985daa658e96cb2dc953ed3faadb03aab3d9bf1266ecab8e2ae90a939`  
		Last Modified: Wed, 15 Apr 2026 21:39:33 GMT  
		Size: 5.7 MB (5657658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72ba89999c7f42fa71a53f6943183ae6db2e3f04b2ca24c513dcb0bf1fecbf91`  
		Last Modified: Wed, 15 Apr 2026 21:39:32 GMT  
		Size: 9.7 KB (9665 bytes)  
		MIME: application/vnd.in-toto+json
