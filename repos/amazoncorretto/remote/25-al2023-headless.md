## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:fecfe19164841a85d4e4933581609f3e1882f3b1f20756b2f55b975506b7374a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8ad705d12a415b153a665e726894a1e440a3620f7237dd8c30103a6e80f19f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157556375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76390f831627bea43689a22f6d6e52a7fbc515dc6db89813270ad9ffd13b3ab4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:44 GMT
ARG version=25.0.1.9-1
# Wed, 03 Dec 2025 20:24:44 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:24:44 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:24:44 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4969c8bd2230ab29e72e682ac41fa8640bed0f79ba791fb5aff2148304c69503`  
		Last Modified: Wed, 03 Dec 2025 20:25:23 GMT  
		Size: 103.6 MB (103587354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5218cdd358ed50abb613c8ceb5cc19168176090c12ae2b394879775eee6d6357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3838961bd3fd798a99c62dfd84f109a98cf235336c6c66ec6fabbb64f96c5d`

```dockerfile
```

-	Layers:
	-	`sha256:76da3585d0cd78d1e8541c29bbae83453097073d686c879d1810869fd8a22c8b`  
		Last Modified: Wed, 03 Dec 2025 22:50:56 GMT  
		Size: 5.2 MB (5194783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68983d89cc21a59260feaa19de63cd73392f13479cdecf94b8026760404d7c45`  
		Last Modified: Wed, 03 Dec 2025 22:50:57 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:403854178a3397bb460481903aa156d6b1c6e311c5c1ab8d2490279d12b3a6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155399397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c7055ede35d60e829a018e028158b5436df48a036c2549dc1e5479708cb5ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:29:05 GMT
ARG version=25.0.1.9-1
# Wed, 03 Dec 2025 20:29:05 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:29:05 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:29:05 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:29:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1751295948905a7b3315365ea71a95cb84676aff96ddbcb2fda5d87b7c15dd`  
		Last Modified: Wed, 03 Dec 2025 20:29:39 GMT  
		Size: 102.5 MB (102529976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6fa43041a3fdea43e40d6215e75458cb289d45d4df6b58a19f806b12d88c7d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aea37ae4a2c4c460482c397b8816dd47a758a2ff482b61b9e73bfb963edef48`

```dockerfile
```

-	Layers:
	-	`sha256:0d09f311298664f0d6c28133fe3e1ba6bdc46684f968eec4464f1617cc2af5c7`  
		Last Modified: Wed, 03 Dec 2025 22:51:03 GMT  
		Size: 5.2 MB (5193594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300f868c70dbac5cb28860175366da7469d112f424e1fa6119886e398f89ee27`  
		Last Modified: Wed, 03 Dec 2025 22:51:04 GMT  
		Size: 9.1 KB (9122 bytes)  
		MIME: application/vnd.in-toto+json
