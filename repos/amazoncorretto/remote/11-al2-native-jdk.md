## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:c077e4b4ba23e36a8d3bf1d28cf3631463ee2174ec11360a488e430015a8cf92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:573421632c844227d37b145d3766c845ac272f75a9b92f2c2cd418e9933985e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224579486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22012b76756feda2817e79ea690623366f4c4a600a80359223415d618606ea7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:57 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:57 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 22:48:57 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 22:48:57 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ffd657d1006a8cd3fcdcb666edbf80da561348a81bf81bd1638c6c3c6821d`  
		Last Modified: Mon, 13 Apr 2026 22:49:18 GMT  
		Size: 161.6 MB (161624220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db6ab76c48d1aa0608252f2c14e45d0663e1864b60974a9a2e64eef9e7e1bc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ef30389b5d78c8a5d511be8d6ec87edea8015b112f06283005571dadb52936`

```dockerfile
```

-	Layers:
	-	`sha256:371e64bf9ea7062daa69f2ba47490f7543d16790276d3c5556ead78da8fb33e6`  
		Last Modified: Mon, 13 Apr 2026 22:49:15 GMT  
		Size: 6.0 MB (5995179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:159e1bd7805968fe97fbc77ba75e33e2c69b2022e7420e315dc42fbb1c223578`  
		Last Modified: Mon, 13 Apr 2026 22:49:14 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:40e3fa107d9ae5f7469c7f0cc6e8e09f2ea157a891b48ba18f4a1bd431ae1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b309f1a10c9a3980a4b9831bbadc08e23ff66d0290e286613a8c7e3abd2ec8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:22:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:22:09 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:11:25 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 23:11:25 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 23:11:25 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f101af3d9395a4b2adaae76d18985a41684d9e16d892ed33d8fdb52f46925b`  
		Last Modified: Mon, 13 Apr 2026 23:11:47 GMT  
		Size: 151.7 MB (151702282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6d7ec77a9b2e362f16b6e324fcb19d6da8c8918a02b94b38fc7827aec3cf790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0276760961bbf6b82ef4c964a9f9abe6d936eef771d5caa029353b82d4d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:3f2f386a6e55602639d525698dda7a92a025037b64f0286a24005e18aaa594ce`  
		Last Modified: Mon, 13 Apr 2026 23:11:43 GMT  
		Size: 5.8 MB (5787893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:641b9747a27fd27cc9f370f7a4dc23eca5cf96211d896ecc9bc625e356e25111`  
		Last Modified: Mon, 13 Apr 2026 23:11:42 GMT  
		Size: 9.6 KB (9634 bytes)  
		MIME: application/vnd.in-toto+json
