## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5e1e313fa6f5902241ab3075c782d44fcbe347134d403f09e130d321d36aba46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bce2f678818c06a8d3fb6a0cd71e56c96a46888bf7fe15c7da9e0827933d292e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136007787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33bc66c3b3a7c8ea3ed52699c26a1b9987a87a1e7b1a2971a455eaca949cb77d`
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
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225cacbf11da4978380bc5d4cb18b0a2e2f70527dec6874feb36801dfe19588e`  
		Last Modified: Fri, 20 Dec 2024 22:32:56 GMT  
		Size: 82.9 MB (82851474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d09a59fc3ed066fdd0e55ce097bd00e6feb4c20af20990caa5bfa16ff2429104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e26f9a9b0a89fc99273254030513290a972d9558894c67c3806c79a25447ae`

```dockerfile
```

-	Layers:
	-	`sha256:a7198229da7c78c5002229f49e3e3d9e3b589219e07ff21f08d6a92ec8328bbf`  
		Last Modified: Fri, 20 Dec 2024 22:32:54 GMT  
		Size: 5.2 MB (5204676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a358ba6f32c3ded1f6c14a3fc86ffdeefb1135c2cea17a961e9193c8969f29`  
		Last Modified: Fri, 20 Dec 2024 22:32:53 GMT  
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
