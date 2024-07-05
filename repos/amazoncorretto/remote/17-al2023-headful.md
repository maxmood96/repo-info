## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:0712e9d67e6867e40ad9501ceeb86ebf5e8875da2848e1c4d9d0b60c0bf76ec6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:84ee8c4a46d0c2a984cb508c2b858a117dedee4ca14d950039d9528e5dcecd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135425500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32c358cbf039d04932dfcd2ae6944eabb517d0c4e8c5e93ceddd4512b49ccc5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:1c9e0f4db95e1ae683b8f16b1ecfc5d8693ad4e5e379a2386e2870f38383c7d8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
ARG package_version=1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:860904071dc658e37de73aa1556e7badfb13bef4747965ea3bd1049e8ff87dcd`  
		Last Modified: Thu, 04 Jul 2024 00:20:13 GMT  
		Size: 52.3 MB (52319623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b31626f145916bcc001c6bb8eac8874ff08f2fc236d80624e0d155783bbb2eb`  
		Last Modified: Fri, 05 Jul 2024 19:56:39 GMT  
		Size: 83.1 MB (83105877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:adb5478d1fb827fd41e01c7b2e6c47522cee10635507b916d5c4ef92ee750873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b034641d67e26a9acc3997c31d9386d7e7dd41a8a66874ecf77cbd7cc958f`

```dockerfile
```

-	Layers:
	-	`sha256:50fd9c7dd1de8c6b4b3e2ed72ad278a13951f9c08dc575300f2c29f87b475538`  
		Last Modified: Fri, 05 Jul 2024 19:56:37 GMT  
		Size: 5.2 MB (5180695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b81ad379465d50128323afdf1e635dd28fb0a069380224e22fa1a3f44998ef`  
		Last Modified: Fri, 05 Jul 2024 19:56:37 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5b23442afcf2cfdc68969c0648fb4198ea19156d1d4e88c3522a1c3478ab7af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133843669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12291fe7c9e86f298c344789745eb06659357a7a46c6d15e9d6ca2db1e801a05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:a2f5453af1f2210c7b49fadc5acdaaa335139ac35c64847d2f5879056f91a03d in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
ARG package_version=1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f95af119e05065dbdff89fbd219657362e32f7ec50d632e28754e75b5a13806e`  
		Last Modified: Thu, 04 Jul 2024 00:39:44 GMT  
		Size: 51.4 MB (51407040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dd5af57407a3cc4059f35d7c54b95717ae54fa85bff05878fb083205fc396f`  
		Last Modified: Fri, 05 Jul 2024 20:14:05 GMT  
		Size: 82.4 MB (82436629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7bac93b0f1b282a9368f4e7339aa4b4651513704728fed3b08db35632132fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4478f5d3dc2faac03f72ad304290860a8368cd504ca1c8baf4168b4840f47b99`

```dockerfile
```

-	Layers:
	-	`sha256:b4700f060a2330a2fa4c3a6c728aec42ad2a9a0276bae922e40c81c67753088e`  
		Last Modified: Fri, 05 Jul 2024 20:14:01 GMT  
		Size: 5.2 MB (5179482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e00935eb5c59069ff9b415c8f6f564f22c1731630d5ff92e246b1219b3691e0`  
		Last Modified: Fri, 05 Jul 2024 20:14:00 GMT  
		Size: 9.0 KB (8985 bytes)  
		MIME: application/vnd.in-toto+json
