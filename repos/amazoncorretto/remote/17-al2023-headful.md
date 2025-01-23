## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:46d732bc433b79cbbe3e7932f791fddc9ad74960bccf0c6e1e80ac663efa93d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:14eccd637b46401f89247c67205b489547a2ca0d7c86b814278bf1e5828f8811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135995122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b48ec0413f9a12c2cdff63c5a8fda11b1d8eb0596df4f454c0192339369f0a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c6e20bbc059e58de19d0240a0f6e2f9f7b6589a46fd3205e347599be586921`  
		Last Modified: Sat, 11 Jan 2025 02:29:23 GMT  
		Size: 82.8 MB (82844647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fe9e9b776a51deec557da4c315c517c0e1d86b5c9af3f84b594b298bd5707f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2f3f415b337c862ef45f97cd0dbc47b19fa468853b9adc4b6dab5f8347ca11`

```dockerfile
```

-	Layers:
	-	`sha256:dcfa0ac76d1102fb8373c03cd8363c34e6ad35ea72f227a776e992fe84bdd6a8`  
		Last Modified: Sat, 11 Jan 2025 02:29:22 GMT  
		Size: 5.2 MB (5204676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7f6767e629390378334b36bc5bebe285059b5f8a4ece8d117b2f8a476a2e94`  
		Last Modified: Sat, 11 Jan 2025 02:29:22 GMT  
		Size: 8.9 KB (8935 bytes)  
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
