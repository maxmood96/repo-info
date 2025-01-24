## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:1c4586daf592dbba3e5a38d3422cbf2403823296e5c997c891c0472dc4320879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0ad77966e5bcb2a0f22859c544d53241119c933216992f70fb5f31d5603cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135988629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f23fc828acc1dcf7983e899bbdb58a24e6be085282124006389b0f80e56903c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:33 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:33 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79df155ff2f95e615ad3ae11a88425b4f6f8c1d837046d38833fdf2946c7ea9`  
		Last Modified: Thu, 23 Jan 2025 18:27:40 GMT  
		Size: 82.8 MB (82838154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:23acb82cd667642d10ca13cbd1193c5256ddf142327548b0d6fb77cccb693ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c958580478b3707040362947e118bfdc6a7d7477b2a93e996e13f62f6617d3b`

```dockerfile
```

-	Layers:
	-	`sha256:d100cad2a100e479669dbd451d6d42ec6b6542f1c7403304c68e4abe3c9e0717`  
		Last Modified: Thu, 23 Jan 2025 18:27:38 GMT  
		Size: 5.2 MB (5204670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703a0d28bb422b3d787ca79e0cf3cf612895b67c109a86011e45d117bcd69b6e`  
		Last Modified: Thu, 23 Jan 2025 18:27:38 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f01aa57003ff1ed827effbde75e4f9c5ae38a442189f47a1e6c9504a24add2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134556961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784ae3101316d9d46a1cdfa1a9df33fdd9ea7b0d8e9e419de44db1a71f3f62e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27487226e55c8d81e0ec31f24b2291184d184dc17e4734aeca09383bfe480625`  
		Last Modified: Thu, 23 Jan 2025 18:44:18 GMT  
		Size: 82.3 MB (82288765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8979fae2b3fd02f8190a50045f31ef71048700a60e41be902d05c0e6120a21f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5f13917feb459a3bd405f6e7f29c682c236c8dbcf3de95e1486bac6d2a9896`

```dockerfile
```

-	Layers:
	-	`sha256:8808cde4f82398a9150e6f23c087413683f38c22328eca503acd0d3abe710e17`  
		Last Modified: Thu, 23 Jan 2025 18:44:16 GMT  
		Size: 5.2 MB (5203461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:668b6a0697edcc72e79dc9f82a142ba358e8be87577466db1cecc1193d3d3749`  
		Last Modified: Thu, 23 Jan 2025 18:44:15 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
