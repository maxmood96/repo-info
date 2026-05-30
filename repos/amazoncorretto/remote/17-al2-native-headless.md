## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:c49527278bb4ee6a837cc6c946d062e9d5ac7ecc8e7ec265ed20a204b505cba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5e0ac167d0da2ecf6a5b9c15e0698fcec0c1ab5e8df0885cfe547734345cc851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150645355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938a9d4c0fde99fb238afc846f9d65f044ab9f56fe5f97a2089da7eaaeeba687`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:03 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:12:03 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:12:03 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505d16aa944a2d05b4d128b9d86344a14e25ea2de24b69ab0b5c4f392caadb46`  
		Last Modified: Sat, 30 May 2026 01:12:21 GMT  
		Size: 87.7 MB (87703405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:56c6df77206b5b1aa891a754125fc14fabecee91747f0c621f83f69ff0df4dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5642142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e0989f974b028c4517f5078352c801ab0e3bb1b2e24965e1f274dd37a7cbd1`

```dockerfile
```

-	Layers:
	-	`sha256:65d84cdc0a4991e9b730acca44b108643d5bc7df883ea0a2cfeb1d49183b5753`  
		Last Modified: Sat, 30 May 2026 01:12:19 GMT  
		Size: 5.6 MB (5632679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ebf88559abd7ba45777d2a4f8ed47c242a3c74b08595a733213c95e9838dea`  
		Last Modified: Sat, 30 May 2026 01:12:18 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:14a87a16907ea047c2618338d27ba140d1a73f1b1ad485fa443c034cef43bcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144741961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea265fea69b1a240209be25187ba9966232c9d2fadc9d4ec69e5e917d0726b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:47 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:47 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:11:47 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8bbe0f32f8573f8dba8e79b9f43deba9e43cfea318b737ca8fad1a09e2bad1`  
		Last Modified: Sat, 30 May 2026 01:12:04 GMT  
		Size: 80.0 MB (79951252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cc6e8546731d176d7446bbb3e4e370597bee48befaf3d5ef522fabd587bb84e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d2f0881806e60d0e59ec11aa31566c882191ae9cde2545709277f117e8227`

```dockerfile
```

-	Layers:
	-	`sha256:c524369a53a1cf43cbbced29ff53c6c68c4849ea239a98453cfb561dcccaf77a`  
		Last Modified: Sat, 30 May 2026 01:12:02 GMT  
		Size: 5.4 MB (5448956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a0907dffa01b49ef2f842cd63dbbeb9ea66f0921f7f62ac886ff75c79acc649`  
		Last Modified: Sat, 30 May 2026 01:12:02 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.in-toto+json
