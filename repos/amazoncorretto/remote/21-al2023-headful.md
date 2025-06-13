## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:a3724797c62357db32463136d18d26c742b9fb0456e44ad9209d0c0c35c29334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:214fcc407142738c633a8978476095446dcba608ae01adbce6f0ee223cbf822c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143312184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74db6602faace5819c7050deb23a6b07d3928aa97c2511bbc15fda25d909819`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc45ad609f2bfb26773fb5626a427b1c9287fb31c33e3c929ec7f18cbd9e6c6d`  
		Last Modified: Fri, 13 Jun 2025 17:04:03 GMT  
		Size: 89.7 MB (89741824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4cc872e353f49cce060e43e57d0aca22896941c66e1f228f98bbb91ec2d53941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f01b6f83bd6de2b1ae51f135e83e0ddbfde38f0b74ff2f07fa69328ff13b6e2`

```dockerfile
```

-	Layers:
	-	`sha256:3e62a7b5fed6ef1479202507dc4ea83462a1a2920e886ad018924cc0a5b2b1c8`  
		Last Modified: Fri, 13 Jun 2025 18:48:56 GMT  
		Size: 5.2 MB (5210564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead267f2a84f708e15663a00a18a9066005b02982ef93243677e80c3a5e3a4a2`  
		Last Modified: Fri, 13 Jun 2025 18:48:56 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:81e3bbdc97f270f9cc8f8ab48c3f33e42912298289cf3aa91d689d8b99163af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141447542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf97b0d5292033fcf4aa8f80c92bac96eb2767a31e45da26c0db3dee81b0d52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f844ec97a89280e7af60c493460aa49b5619b2d6067a03b0402e4e6967ade2a0`  
		Last Modified: Thu, 05 Jun 2025 14:39:32 GMT  
		Size: 88.9 MB (88881805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:07ee254999d55a5ca4c73c076535ec8e3867b826616dc25a8690541119a0dab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6beb4b92e4f0e252f7413d98680360dde06d3f7aa9e3eeffa6efb8275d726f`

```dockerfile
```

-	Layers:
	-	`sha256:3e6133c8f58f886c4bc7f1c457ec0153af81ce75a5bb5af60965021570c6405c`  
		Last Modified: Tue, 20 May 2025 00:49:42 GMT  
		Size: 5.2 MB (5206343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2593e638d77ab1cc05dc46ba53dca91e02af772f40b085aa6c3abfbaac4f5a3b`  
		Last Modified: Tue, 20 May 2025 00:49:42 GMT  
		Size: 9.0 KB (9006 bytes)  
		MIME: application/vnd.in-toto+json
