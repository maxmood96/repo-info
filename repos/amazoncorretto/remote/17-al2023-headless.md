## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4283c0312e21a92998de56803d5ad726940e3d30c5436847e8174b892f24db2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eae65f0f34ebed5f5a2fad71355d940eb61c31ba66507d71eee5f8b00ab8e96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136336387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30841018d0227ba3093b3c3d2526f7d3c2cabda66648dc2d4ac70fe97590880`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:23 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:16:23 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:16:23 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:16:23 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45ee8ae5f7317f897f1f0225271d9b23c7971128464c5094d7735626a8a0b26`  
		Last Modified: Fri, 14 Nov 2025 02:16:54 GMT  
		Size: 82.4 MB (82359672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0434e8cb8517ce7374cc6f42c1f3cc01477de9ecc70ce3917430220eac55e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f6583a61690965c3736e4e291fe1577a51d0c335a8a1cd730dc1a5ad90303d`

```dockerfile
```

-	Layers:
	-	`sha256:36e504c9f8e11c20180032d9baaa8e836e026c37996aa6f89225656ca8a29742`  
		Last Modified: Fri, 14 Nov 2025 04:49:16 GMT  
		Size: 5.2 MB (5182896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16196665fe88501b82ff61efb17dcc4cc71680f13a49aa048c11ea0f48cfe6ce`  
		Last Modified: Fri, 14 Nov 2025 04:49:17 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:18c78ff94bf6f04fa2fc99043ffda5b14c8129d33bc9b14c527ed9927593ad18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134653971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3483ece074bf1f10f9f56cf66a8de269931779bbda096d50f6c45b9818247011`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:51 GMT
ARG version=17.0.17.10-1
# Fri, 14 Nov 2025 02:17:51 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:17:51 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:17:51 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41af769ff5d4f18dc7690150cb67d2ba72b608032fac8090822b02cda43e6839`  
		Last Modified: Fri, 14 Nov 2025 02:18:23 GMT  
		Size: 81.8 MB (81777315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:56e664fa7e5ea4470a81eea9168ed795a4a4335a100eb684f41080d392cdd22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87dbd78e633383e9f9a8ca67eba21892faf40559492f0c440e9ada07727798bb`

```dockerfile
```

-	Layers:
	-	`sha256:0ee77c9292827145203470450267e837470c18ceb18a22382622397dcdc31cd3`  
		Last Modified: Fri, 14 Nov 2025 04:49:25 GMT  
		Size: 5.2 MB (5181684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bf3490499995279c76d67d974b30e70dfbfd47ee193239ce2c2bbc0d89f882`  
		Last Modified: Fri, 14 Nov 2025 04:49:26 GMT  
		Size: 8.8 KB (8793 bytes)  
		MIME: application/vnd.in-toto+json
