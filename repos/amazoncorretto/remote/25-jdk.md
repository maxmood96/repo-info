## `amazoncorretto:25-jdk`

```console
$ docker pull amazoncorretto@sha256:9fcfe855a80c72f08ad8eb56a8090605d75584fd0f357246b6de6c0fc2cda92c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e1d9bdb4b9eb570943a1ff20805dd07d28b76dc44ca83668442814eb940c26b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243139645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bee880d4a3559d49e4b41911f26784507a8969dcc11f5f2559fdfd98b7adea6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075fb8961d282a9f92fb75aaa159d8011cb3dba1aa6fea626361cc411336906`  
		Last Modified: Thu, 25 Sep 2025 03:19:01 GMT  
		Size: 189.1 MB (189134365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9a39076fd5ca65a6cc775fbb5ed5329176d254536dcf11ba58fa50cdd8f02e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1a36a1504a3a4d1cf9d4dbda12accf236115ccd800c17f0d95701f576fcbf7`

```dockerfile
```

-	Layers:
	-	`sha256:8d558af21f1d6e824a37e98e4a0946d6936e65e580fdfa9896ddc51d19e019d4`  
		Last Modified: Thu, 25 Sep 2025 03:51:48 GMT  
		Size: 5.3 MB (5329178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3903a911206e684a9a6e9c69182f57b4ff2663c76d82212cf649d994b519b5fa`  
		Last Modified: Thu, 25 Sep 2025 03:51:49 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:374de4391b5ed0563cc2a5697c9f1772743a83ab0704528ff2bc5043fafcaca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239919229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab657948b7083148e0891961d7612445ee91de95ee9bfc64564cc7a796208b49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bb6a5c4e092b471dfbda1890bda78055f9989087ac015177c092ddf1ad3cf`  
		Last Modified: Wed, 24 Sep 2025 22:15:39 GMT  
		Size: 187.0 MB (187019791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d1f9377ec4c28bad9492e5f7e0667757ef94bb7a0e35e79d79a15abd001f762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385041f9f53b25d1299fb5267d0c1bc0bc9a6d7d25af14511dec9b4848a1b052`

```dockerfile
```

-	Layers:
	-	`sha256:d0b7544aab8b28b06077607539133f6e56699c0339bdd828f98a86d9b49c8f53`  
		Last Modified: Thu, 25 Sep 2025 02:28:42 GMT  
		Size: 5.3 MB (5328146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7845e59eb5725fd178bf6e4684c3a16d8aa407e5cee382c5bacee07c4a5ac68`  
		Last Modified: Thu, 25 Sep 2025 02:28:43 GMT  
		Size: 10.4 KB (10355 bytes)  
		MIME: application/vnd.in-toto+json
