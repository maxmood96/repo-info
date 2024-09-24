## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:213b0c3b27e8e6e905f673fc5ef0db6b7652023fbfc23f038da10b55597fc07f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e1a3422c3d18faf25a5a597bff0430944ba2d5d1d6dac1d318b88949783af09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140663070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7fde2f1b774c71a44e68e3bfa78c636088bf303e88947531073e0554e388d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:50 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6371cd6a0c1d0eb34c8fa9737d76b2af4f1589ead6763171b1e4d3070da989e`  
		Last Modified: Tue, 24 Sep 2024 01:57:46 GMT  
		Size: 88.3 MB (88338112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e802ba2f8b8313e6f35f75d3b7ce9b57296a4010a11442dc97ebe1ae7425d0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a469b9b0bc535adeed731dc8d144608a1d1bea284a240e48aaee5ab367cc574`

```dockerfile
```

-	Layers:
	-	`sha256:f604ee4feea3ee3f691029ea35cc5d41eaa584183e5a275784be8910e51fa849`  
		Last Modified: Tue, 24 Sep 2024 01:57:45 GMT  
		Size: 8.8 KB (8819 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:25d9c075d2fdbaaa46476ae5e9d4ef620930dbb3c16cd0fbb202893b2a4a66d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edec95ab14f652ae44da0b506b7fb331cb71f3692a7ea10bed51e29c59cf1d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b3182c2bf4f49b83ffd7963b1f32d7746c8a8cd6c283e4e96e1f641e03de4f`  
		Last Modified: Tue, 24 Sep 2024 02:47:18 GMT  
		Size: 87.3 MB (87290202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0dc6ff0e790aa36309e578014b2625eec1632b63dcf1b9233323d06399b2e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a011756f71783471d2a51f02bfb3389de0f98b5adadb504a37e808fc64ca50d`

```dockerfile
```

-	Layers:
	-	`sha256:06b9015a23bae471409672eabe86592a1229e9584aed9d718eb91d0ffd532f0f`  
		Last Modified: Tue, 24 Sep 2024 02:47:16 GMT  
		Size: 5.2 MB (5185299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c776681d4d6dd74ec4edd2b028acd23cad0e21c49de2c4cfb3ed1186ccafcf`  
		Last Modified: Tue, 24 Sep 2024 02:47:16 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
