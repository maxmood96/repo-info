## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5bbfd9e9193cd7ea70ad90aa8afade78c143c8900df2a9f9541963d6362dafd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2c567bd2cecd53dab386ae5db0153d96903db68251824d88c3557aad5bac02fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134757612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f039681888859c74401649484ad5db26ece40deed244de9d201060c95f409c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba431a148b7ccfc98a2f72303719716b2561e93432655c27207b70b561242f9`  
		Last Modified: Tue, 08 Oct 2024 00:00:02 GMT  
		Size: 82.4 MB (82432307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8c6d3cb6e02224e0a18c32a8240837f2894ea7170f67d3e2cf6eb0b2a9a046ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaea5ba7d76587de19138c0a6dfcb2197ca9b3bb6c747ecce9027bd7a890e19e`

```dockerfile
```

-	Layers:
	-	`sha256:25e08725ce3c133994f0dd80c8d7a3668ed28ae4a20a2f0dd65c45c2a0fafe73`  
		Last Modified: Tue, 08 Oct 2024 00:00:01 GMT  
		Size: 5.2 MB (5183740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f81790e9af554c25154723c32f69b5237b9128017c58e45c62ba180a2dc1d18`  
		Last Modified: Tue, 08 Oct 2024 00:00:01 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8a3b05299396bd1a91bb417760185ab282ceb48f08cfc2db06d66331cc9b83c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133176106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b31779a59fd45072bab88896cab385b19881213ce816bc4a3ffa6e757dee20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cd59f7db0c8de954444ea8dad313695dd88c8f1164ba3089f07cb878760dc5`  
		Last Modified: Tue, 24 Sep 2024 02:37:53 GMT  
		Size: 81.8 MB (81750114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0b0e6dff16b5f0f902755d06470264ab79c3254e3d40327c73ddb88e3ab8c34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8470d2022df6fc9468d46101700115559bace2f72be28f05b21cc5e4da9d77`

```dockerfile
```

-	Layers:
	-	`sha256:267b9ebaa6bbb45ea3f5cd171df6f32facb3a3f9659fd57d41ee9ea436246d34`  
		Last Modified: Tue, 24 Sep 2024 02:37:51 GMT  
		Size: 5.2 MB (5182512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a04c7ef6775bfae00b1e9db2cda25e48c0dfe2318b69dbcce9d4a416e0e84c8`  
		Last Modified: Tue, 24 Sep 2024 02:37:51 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.in-toto+json
