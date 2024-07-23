## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:e8598b774c0d5e76dbabf4cdb363e80413bbd3e3e5da3cf0b46d19bea616895e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5dd607ba8c55ecfe6a5f0ee52d4412ce12d0b7c023bd0a8cb87f902e5a929c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128477653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c395f4829bdab93ef8a933bf13817b01f4e2724dbb0dc79b70c4b6df815d31f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Jul 2024 20:01:54 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Jul 2024 20:01:54 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f03636e672ba797137f2f72e64c7fdf7947397c0880ca5f9e9962a85462a7875`  
		Last Modified: Thu, 11 Jul 2024 02:05:27 GMT  
		Size: 52.3 MB (52313836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5111b4514baec0829763206383f9612ea002b9baf327d89fd6c7b89e09a00719`  
		Last Modified: Tue, 23 Jul 2024 00:07:24 GMT  
		Size: 76.2 MB (76163817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be2a9932aa51cc91ea33fcd8489210443b71a7e835e4d760368e542088413e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aad84d5e083fedc5b7dd8095927ff3ce594d7839e47a7cf242ae2b7304cddbf`

```dockerfile
```

-	Layers:
	-	`sha256:a4207f2a7154dc4d2b9e0538fc9e0eda4cc4761b45f284abdf29c42226181ecb`  
		Last Modified: Tue, 23 Jul 2024 00:07:23 GMT  
		Size: 5.2 MB (5197285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83970f82dab90722797fa32895d92ed71489207edd2ae9ff434e9fc0d0419f39`  
		Last Modified: Tue, 23 Jul 2024 00:07:23 GMT  
		Size: 8.6 KB (8618 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:56a73520f01bd4eea5cc8f617ea9ad2b2d9233a26e3a2ce078192f3c3a12ca85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126702483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a1fd82aec94cda1de36129bb9ca34775d64d886562a0d0de8f3de057b9092b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4a34b48212c40bcca1258b64322226894987ca2ef7b5b56a35e31fd0f2e8db`  
		Last Modified: Thu, 18 Jul 2024 01:04:27 GMT  
		Size: 75.3 MB (75301345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:edf9f79f31c9afb6e63e69c815ae596a973c50187f1ac5fa0a1d2b3fa3bf3d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3e9104852e7576bd6527f534b8913e5b4dce30e705a295b5ce87811d069c05`

```dockerfile
```

-	Layers:
	-	`sha256:fbcb3992d67f16c13ea4d9d4b15a191a280abd3f5fe7c0bc4d8230f44e6c1bd4`  
		Last Modified: Thu, 18 Jul 2024 01:04:25 GMT  
		Size: 5.2 MB (5196902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198623a7b00abd224a3d7b7a67a6889e3b0cea180ef1dc05b941b30a536768a1`  
		Last Modified: Thu, 18 Jul 2024 01:04:24 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json
