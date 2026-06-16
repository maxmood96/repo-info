## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:a1f7602a861dda287eaec0b0a050c0b301e7234f58cc4ffdb51aed94a0589f4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bbea4243038fa1713c24244ac7b8de543bb257cf6d655480de2e274e49f74501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217336295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae4f0954fb5bce5f174366237583a52ec506c1a2e37f083acc3e35d322be940`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:14:56 GMT
ARG version=11.0.31.11-1
# Tue, 16 Jun 2026 01:14:56 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:14:56 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:14:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f949e1efdd1ad948b0713f5c6a06d38709547b51260b0cf3e1b3f624cc489106`  
		Last Modified: Tue, 16 Jun 2026 01:15:18 GMT  
		Size: 154.4 MB (154394345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cec050b2218faf6202c5b06a7e1e75fb9599adaaf35be799c3a6b688ceead16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4755837f49c3389236a49c7e856738c7dae14fa069d0cbbfab90e8df4a2c77c`

```dockerfile
```

-	Layers:
	-	`sha256:16d2c6eae8a04f8ff9de05ec74181525d9aed7e299f83d814e6723e8389ccfdc`  
		Last Modified: Tue, 16 Jun 2026 01:15:14 GMT  
		Size: 5.7 MB (5683406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53384b4eb40ab0ae57b7e25d4a1bbf6fe482a3ed0cf000b0ed6f7055b040cd98`  
		Last Modified: Tue, 16 Jun 2026 01:15:14 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:37acf5021c919357a6f8cccf61b857934cf042ed40c9353e65bb6faf9c4a156c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211414567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8589061c2bcaa2325f2f1b18ac813084b6d08a618268a5ebd670c1190cb1e85f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:13 GMT
ARG version=11.0.31.11-1
# Tue, 16 Jun 2026 01:16:13 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:16:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5901e2f9012c1262482f44daeb79ffba52638d38a564d2b2fbe41790a33bf8d`  
		Last Modified: Tue, 16 Jun 2026 01:16:33 GMT  
		Size: 146.6 MB (146623858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c6f013dc49f52e668bebc7e39090c72cd52d0a2b99b827b0076c3243b60a2384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c6d15fd6a430303c5d38a63eba62d70110bdd8a65c84fb41fddc33d1acd97`

```dockerfile
```

-	Layers:
	-	`sha256:5a7bf147260764a472074857d022ebd09d332ca539257289db8f66fa60088534`  
		Last Modified: Tue, 16 Jun 2026 01:16:30 GMT  
		Size: 5.5 MB (5501874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:638a93b95db589e7741e596b198207c922b21546118a5f7cdeb14f7101b68b06`  
		Last Modified: Tue, 16 Jun 2026 01:16:29 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.in-toto+json
