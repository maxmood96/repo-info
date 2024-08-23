## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:97e27149cd85ad27dcd874cc75af98d7542d3f72dbf8d9d6b1dac12031e322c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5faf46188f32525f33da81ec413a2d6366e7a193d09ec403e1b2366098ab72b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224770101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773f710757cb084f19f966421072ea1d8f41be8465f874d74b6c08fc20674fe3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6eeabd86b075e80cf303c4a0348cf048d31ba6ae2d42b051bb230016153f8809`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 62.7 MB (62659944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24425c58fe0c26bd61582f9009cfc8f9e28927534d8ecb50219f57d639956c3b`  
		Last Modified: Fri, 23 Aug 2024 01:50:49 GMT  
		Size: 162.1 MB (162110157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0b0237e77478b01859d02dbfc78ee6db43f906dfa8b9d8005823e04efcc5e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e35ea7fe1be7b3a1ed53e7a0c7041ec1e8efd1369eff91a541b7db54017e5a6`

```dockerfile
```

-	Layers:
	-	`sha256:e90b25a50bb57260265b51c8a99fc8088496527d52ca3e1e05a16c923e23b93a`  
		Last Modified: Fri, 23 Aug 2024 01:50:45 GMT  
		Size: 6.0 MB (5990325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9644ec073dc851d5c3ca423b5b19be06f8b9cf62d1319cc50951f925c8ed3dd`  
		Last Modified: Fri, 23 Aug 2024 01:50:45 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1027b48f52bf2436d4510cb8e416319f19f9fdd31ad9bc7925726ac6ffdb732a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216870013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6203aa06e8e8d4f7cc421b48634a0fa3f96e2e1846e063f4fcbcad10d7a34a0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3866c6db913d2a3c4b00b80e7cf5572d3f8fff5e96c04c546ea7b0c5e38f84`  
		Last Modified: Fri, 23 Aug 2024 02:24:28 GMT  
		Size: 152.3 MB (152282878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a383275785c4266869e4f71182761f70bfbd36383b7b00a24045381c60349916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ea82dfdbd99fda2ce7f842d10a954b59682614af62fcc1c907d67753b5bd95`

```dockerfile
```

-	Layers:
	-	`sha256:3eb3362e4dde92b2aa33091438fcb17f71dc5d522d883c62a2af2684dd2d02e2`  
		Last Modified: Fri, 23 Aug 2024 02:24:24 GMT  
		Size: 5.8 MB (5782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0080264c6d1b49212677be879459f761f5a837ffcd56c8b83ccf7913c79b5314`  
		Last Modified: Fri, 23 Aug 2024 02:24:23 GMT  
		Size: 9.8 KB (9767 bytes)  
		MIME: application/vnd.in-toto+json
