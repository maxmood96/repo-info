## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:df6b4886a40287a594594a7864f6f94fddf8a60a4648c54e12d697e0b524304c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3eef89f9167b2d34e8ff3a710c3852a3ed9bfe9f870e7c0dbc481cecef051d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153950340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feed5f22f064ba7392c0890392b6673b603d864be99deb015d5a77f5ba5aee7b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24b8132eaea284321f9c9e5a919cbed970e2f9535ebb5e564418b031dcb51b4`  
		Last Modified: Thu, 24 Apr 2025 20:08:22 GMT  
		Size: 91.2 MB (91188618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d010433741496181d5e6e3aafb7bf065dbc59dba1b73a87c1eba175582080bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5860939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91b41ad63d8ce41f116f6ab4fdda913446b0f4163b8f2f9c07b9378c01d4dac`

```dockerfile
```

-	Layers:
	-	`sha256:8aa12014551a50c339cea4c08701e1e69088f2c794e269e90331371c4502355b`  
		Last Modified: Thu, 24 Apr 2025 20:08:20 GMT  
		Size: 5.9 MB (5851468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73696033d10e00823d87992b1e1cbcc17c2b542b6f53abd83c749f50c2441d87`  
		Last Modified: Thu, 24 Apr 2025 20:08:20 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ea79c5110aacc5b85181a679474d350c6222ba8f41b307b8a0c102db7572c450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146480913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e920df2627729c2b352027a9785724a04d8dbed06c53423894e20e5360d216b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:928bddcbf112315a029f894cf829df2ae1b28c89ecaa6c142e3d47e62c803337`  
		Last Modified: Mon, 21 Apr 2025 21:48:49 GMT  
		Size: 64.6 MB (64582610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4d65d938b6555da9c7553733a8cdf8a8cec85795b46cf8221706e5ba4e14d7`  
		Last Modified: Thu, 24 Apr 2025 21:19:42 GMT  
		Size: 81.9 MB (81898303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:085fdb5357fdd25659a7c7aba20650b742f6006e8963864fd3a9ae6a6531489e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d440b02466bfe363cd2fb105a8957803d80016280829dfd87d4df9e4f6dfb86`

```dockerfile
```

-	Layers:
	-	`sha256:ce788d8f20a13fd929e4b0f7b68e043a5dbafcb6298cd30fda0bfe2f7e1f71b4`  
		Last Modified: Thu, 24 Apr 2025 21:19:37 GMT  
		Size: 5.6 MB (5643211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e785e347c96242553f3985ec33d66a838156661eb9dff7230d356e5b973faebe`  
		Last Modified: Thu, 24 Apr 2025 21:19:36 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json
