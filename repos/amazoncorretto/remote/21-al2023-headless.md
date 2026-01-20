## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:3c0c2220681f01fca5d85a8310ce64d302d2b7478ccb72e83b22b400d68a5e17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9220e85337f357c2dac473230c706b531f22539413da824e816d058a25da7a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143268778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6825084486956e6965eca8847d478b3cad72f06c9c6a341d530f2844a14b78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:07 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:10:07 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:07 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:07 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f672f300d1e07283ca8ab853be50a4edbe5ce7484bc3c4d5eebb9e947f8b421f`  
		Last Modified: Thu, 15 Jan 2026 22:10:51 GMT  
		Size: 89.2 MB (89247574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:76279fb9b69d3e1253a9d0eb61442a4aaec8ccdfb2dd6a6858fb297a3019ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1a65f27d1cc11d497d08094bec6a58ee3666a954eeabb68f8dfa7c660cdce6`

```dockerfile
```

-	Layers:
	-	`sha256:f04fcfbcbeba308fbce199de0945fb77c6773c6e5c3b5be07e40aa5b635d5fd5`  
		Last Modified: Thu, 15 Jan 2026 22:51:03 GMT  
		Size: 5.2 MB (5184518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbf212f8c34e2e14c4867a7178074d4bc7132987ed66bfcc782ac56845422165`  
		Last Modified: Thu, 15 Jan 2026 22:51:06 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:551fbb3ac1a0a359422e01b4994c03a6d3965dd743493cb926aacad62973d833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141277265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4d5f2e9b134b09551d19ddf77248dd176c4ab2a63321dbe18fa26e6f2d9f09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:14 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:10:14 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:14 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:14 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee5b491064b280dcf7a6e2fdc42dc449d98cfaaf153c19edf9a34e59bcc32ef`  
		Last Modified: Thu, 15 Jan 2026 22:10:48 GMT  
		Size: 88.4 MB (88362908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a47a3c13b3add71629df42acdae2698d31d340b9d529b710118fdb17f744eca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89d8c828df07a15737d4a2fd989f921d14fd7233fcea6581207bcdcb307de85`

```dockerfile
```

-	Layers:
	-	`sha256:92f27ee5bbd13cd4b2df570291856933482957f7000b4ec974ff5fb10224fe45`  
		Last Modified: Thu, 15 Jan 2026 22:10:32 GMT  
		Size: 5.2 MB (5183308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36de99d11b6f13f5fb7e4b28c3da9e0d381adb8b295fa3b0e91484af9f957147`  
		Last Modified: Thu, 15 Jan 2026 22:51:21 GMT  
		Size: 8.8 KB (8785 bytes)  
		MIME: application/vnd.in-toto+json
