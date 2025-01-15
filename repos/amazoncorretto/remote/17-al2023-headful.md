## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:9989272619372711a1235945d2a8c43075b32c22007645d536aa16ae2ca1bfaa
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
$ docker pull amazoncorretto@sha256:5e3bae0f83f5168433b37a545949bf888fb652ee3d2a5bec52de4c149ca8f6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134514860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fcee0aee980492f3194e2a07d3e9cd3fadc177c02fb36ce7d5849d124485b9`
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
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Tue, 14 Jan 2025 20:39:04 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc69a8ff4accd30473b8736c0f128664d1c23c00e039591990d08dc3a1ba5f00`  
		Last Modified: Sat, 11 Jan 2025 03:05:59 GMT  
		Size: 82.2 MB (82246664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a883517f836b31cba78c1993d9775ab87b20d9fe62e0b14afea66aa5d6d8693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8547db74b6dc4a5ae3478737ad4da89449afe3d1a6f1f6f049b64af489e798b`

```dockerfile
```

-	Layers:
	-	`sha256:040e00a668170fc097d0a774fef5c5b320190e2c55e1a08d1ebea0e5e68975ef`  
		Last Modified: Sat, 11 Jan 2025 03:05:57 GMT  
		Size: 5.2 MB (5203467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f59b3dba1ab14b2570b74f19dfe3a90efe433bf4798a4b57f4eaf83ecc05bd`  
		Last Modified: Sat, 11 Jan 2025 03:05:57 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.in-toto+json
