## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6a8467b30d63b6b7b4ad748207fe6046df6b3b513e4ba507c79677efcefb00d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f14cd69306582419b4c77e1bfad72539f039dc9cb77e40e5ffe9760c922b96e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135181907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956e23cecfe386efd8751232f20cf4c88002863e33efc3c1eae51b097c7b0297`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4a665eb63bc8cddb90e1e74e3ec745a1bab733c919dc4b2d648b43459295464a`  
		Last Modified: Sat, 23 Nov 2024 01:38:06 GMT  
		Size: 52.4 MB (52377532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b102a172eaf27ed6c97ed265e97977134e6ffe7af309a8f0e665f43cf6f2cb`  
		Last Modified: Mon, 02 Dec 2024 23:23:30 GMT  
		Size: 82.8 MB (82804375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:155868e2ac86a00a66ad4b1bae2fbedd230610f3408a37f4dcd520bf10b2b11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3873889d9d0a31b951fc8a785a10e42317296cfbf84a81162001c70633f7b`

```dockerfile
```

-	Layers:
	-	`sha256:9bb37f228b8d8e00c810a48b8956071cca69618ae741b67574f48e770a4f4353`  
		Last Modified: Mon, 02 Dec 2024 23:23:28 GMT  
		Size: 5.2 MB (5209860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49430d3023540b668269c9a93482295bc5a237c44b151b91d5565557365c2d1a`  
		Last Modified: Mon, 02 Dec 2024 23:23:27 GMT  
		Size: 8.9 KB (8935 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9e52d619aa6c1cb9ff1f1c92bc6c2db6ef3d32b3d2f3aa1226c272e219302b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133664032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d196ea9c245e00996fbb9fcddf94c0298f9f974a6584a9d6c9943ef855518b34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803c4ecca88ee6ecca1c9ff65d480fa0dc3bd06eb44f958a9fc2025395b75caf`  
		Last Modified: Mon, 02 Dec 2024 23:28:01 GMT  
		Size: 82.2 MB (82208188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:727c321d66021115de55f6c426f9144df18bcb02dc23eb6036507de44abcd8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d5fc48cd8bdf663417acab930d1a1aed05aec0bf8adb2f59bc2a38b1d91e81b`

```dockerfile
```

-	Layers:
	-	`sha256:dc1fcd364f24d49c8b83d2cc56be568c9ac8d08409bfb1b320afac3a6c91e247`  
		Last Modified: Mon, 02 Dec 2024 23:27:59 GMT  
		Size: 5.2 MB (5208649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca75f4b23501dc5f2965ec9522d87f53ffacfa02237537d5652aef9e772b0673`  
		Last Modified: Mon, 02 Dec 2024 23:27:58 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.in-toto+json
