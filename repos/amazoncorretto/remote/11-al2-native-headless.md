## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:db7aac2cbf1fd2175270dcdff1bdca873f32441961e36ae23f6ecbc61679d49b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3514bda3bbb8dc07ff89f764a66ac5a6c01517b19a396573493d85cc54714f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217307274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89380daedd81c695c664ca8bb52a9f3d25817be9bb6403606aa54247f180de73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:58:57 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:58:57 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 18:58:57 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c168a3e545483a6c924fb79d8939646db90ce7483daf0e1709a54facdfae74a`  
		Last Modified: Wed, 21 Jan 2026 18:59:18 GMT  
		Size: 154.4 MB (154367118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1dcc78f34af4fcb31e1983cd8bdc95cba38c280a2d028262f8f6037b316808ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d12f27af2f89d659864059c0d779fdaab1bd4a65d032a4963252fdd9ac2fa0`

```dockerfile
```

-	Layers:
	-	`sha256:5a906ca13998dc636444da9d416d8bf8a546f62011477af2020db74c39495558`  
		Last Modified: Wed, 21 Jan 2026 19:47:44 GMT  
		Size: 5.7 MB (5683305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd26564663e8f8a53e593ad20a1c1883f6cbe40c0823b27b2fc1e7795eaf8c76`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:868211446b983a558dc50eb61854b245001d61d1ad9dd6f894fec925167e4572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211413254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d862af85f56f67fcd6519bce0aa8dca9383ae3f311abd7568f8167d5e78d15bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:13 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:13 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 18:59:13 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7c9ebfc8192a36f539adf5629e7eb90c635e968a7b0bb003fa85853b2e6df2`  
		Last Modified: Wed, 21 Jan 2026 18:59:33 GMT  
		Size: 146.6 MB (146642820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cc0975e311719f8425636df852a29a4c85569286ca1288a53c013c01afbc07f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061cf7586abe965a2ed15318807a89e1e14032b7854b91a240591ce76c6501b0`

```dockerfile
```

-	Layers:
	-	`sha256:bdbf154a843f047f6ddf324a217c5ae528127dd1b7b2c473fe7b337c2551faa8`  
		Last Modified: Wed, 21 Jan 2026 19:47:48 GMT  
		Size: 5.5 MB (5501773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf9017245191dc9683fabc48e7444b1ab16d66cb6f60309cc6b646ac5867fe18`  
		Last Modified: Wed, 21 Jan 2026 19:48:27 GMT  
		Size: 9.4 KB (9367 bytes)  
		MIME: application/vnd.in-toto+json
