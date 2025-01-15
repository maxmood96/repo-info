## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:8eab6b2ca48cc3fd01a810dc6a8c56ff4f9268fe8548a4a78f7c095d1d968fff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:de773be460c13951d9fdf5dec55c96dee9e1ec3ab5239a0db3344ce6cda6bb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135270096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c1ac5524b7b8be6669644b09c48af1e75234e98e1d8d6977e7b768007bb37f`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:99f84128d778e956fddb954bbe0f89122cdfedee57e71adf038440ac68cdd7e2`  
		Last Modified: Sat, 11 Jan 2025 02:29:26 GMT  
		Size: 82.1 MB (82119621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:315672c3165a8a1b6673466b61720b9b0bca7519eb71f6e7b55b5f531bfe6928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d052c59970b5ed03e88432092f4bd7950b034248d1853a319918204c7f91e9e7`

```dockerfile
```

-	Layers:
	-	`sha256:cf3835b5d3d1b9d408aca8f49596a6ddfb248379b0e35260c7a405a6f84a40ea`  
		Last Modified: Sat, 11 Jan 2025 02:29:25 GMT  
		Size: 5.2 MB (5179424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07aabea1f74cc67ba3bdf79e64f69590b5ecf9f4d35cfdd52ad4ee643e1cdc16`  
		Last Modified: Sat, 11 Jan 2025 02:29:25 GMT  
		Size: 8.8 KB (8756 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aab8a908893eb8ed8f345684f76215a10aa18838fcee6fc1d7afe7a80b5c4951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133779305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0161cdda41522641c9a0248e92cca4d12154c8e4f57784a776639358837c1c2`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190f51cb08051cdba7081365a4a5103eef58b526cb6d8c35b61ccb02b6adde5b`  
		Last Modified: Tue, 14 Jan 2025 20:52:36 GMT  
		Size: 81.5 MB (81511109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ce0dd0123ca89b5366c1d9f543f8154e44757b19fef63d7be7d62df30edfdb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238e1f294f383c6719db095b6b028b050ed1bc675758ecf97e48de7eef4f751`

```dockerfile
```

-	Layers:
	-	`sha256:d0f055752ccb1bf2e33dcd2c48cbab663d734cf1ca5d3e7cb726c2dbd036cf6d`  
		Last Modified: Sat, 11 Jan 2025 03:05:15 GMT  
		Size: 5.2 MB (5178212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d3a2f6ace11d96f40ddd37e56b2d85fe8b5c77b1e97ac5d41528c530f7f721f`  
		Last Modified: Sat, 11 Jan 2025 03:05:15 GMT  
		Size: 8.8 KB (8835 bytes)  
		MIME: application/vnd.in-toto+json
