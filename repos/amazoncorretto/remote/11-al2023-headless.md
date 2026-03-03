## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:7dd2a35e6eb844f3b2e87846319a91dfd779a7ae4a2dc5c61ad6e906801bb938
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ef8ea4a2774040c7f51c64a55cf8176604ec134c4501065d87e07dd70f367e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130035677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa91f9ce2bc61df72cc8273edf3fd8f3f347d55dc50266b37bb428497c4b802`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:11:27 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:11:27 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:11:27 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:11:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1015cde23517c6140f5843938f2ae097bb979ba63b97535dfd5a74f5b2a82e`  
		Last Modified: Mon, 02 Mar 2026 23:11:43 GMT  
		Size: 76.0 MB (76002837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:430a22024eba9c261fba8ae1c035d318bdd5e8c7c78817d3cfbef999356149c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5868aac273fa3d97742b4cd2ef7d9f45932b2059991928b27d80e7464c3d852a`

```dockerfile
```

-	Layers:
	-	`sha256:d1717bfb7499ed8211b852f3c215dce1783073267ffc40ae17cbd4a1e52b30bd`  
		Last Modified: Mon, 02 Mar 2026 23:11:41 GMT  
		Size: 5.2 MB (5196893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f8bd5f1511f039a40b53b4b6b81c3aa917e56f445be314b286d7ec47fb06d4`  
		Last Modified: Mon, 02 Mar 2026 23:11:41 GMT  
		Size: 8.6 KB (8609 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7dae0d8b353a2e35c9d562939da5a7f14e0225545553596a45393da053ef1a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128178738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e684dc04d80dc92e5fad478d44762cc3b786940d9f252bc898f280b6aa8c2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:13:19 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:13:19 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:13:19 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:13:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8220fdad27709816c119419f31aba7e60bdd1d2abd9a41cd6b5eb385843a575`  
		Last Modified: Mon, 02 Mar 2026 23:13:36 GMT  
		Size: 75.2 MB (75237419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9193823762e2a67cf740e6be0f161407d320235db047b3e51426583d480b407c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e8bb03e97c52b7314a390560b4dbec966668d1b243efc2ade2178fe7938a3b`

```dockerfile
```

-	Layers:
	-	`sha256:389babdbe0b2455e07997fc4d08b44b453006c29ab56d354007f8130dcfd9a5e`  
		Last Modified: Mon, 02 Mar 2026 23:13:35 GMT  
		Size: 5.2 MB (5196511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662988c22b98b424dfa6f25cf4cdc9ae1efa1596c0b5e4898758ce91105bcb83`  
		Last Modified: Mon, 02 Mar 2026 23:13:34 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
