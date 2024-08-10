## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:2cf8ba14a12dee67a941f9adda4c552aa373089089e1cfba7fee5713eb11e47b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:648332e35f9501008174772bae158006caa8f108634094a5e0a5607b4db7002d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129161957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53527332fed85df9b322086f5b2f247af1e5446657b5c3f07b864e6c021c5e49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef8a535bbfcda46ed662e5ef424bfaca1272e0ecaa0bbc88a23f34806593bd0`  
		Last Modified: Fri, 09 Aug 2024 20:49:37 GMT  
		Size: 76.8 MB (76844054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2dadc9d35fda053f8aede1a8214d48df6ff68a53b4facbb1323ad9787fa3896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b410d5a5a765398bd446bc2151641c294a460aa49694edbe78791580fc4f840`

```dockerfile
```

-	Layers:
	-	`sha256:ead32c14dd558ae8f511d884792dba3009c31ab0875a56b0b0513223dcb933b9`  
		Last Modified: Fri, 09 Aug 2024 20:49:36 GMT  
		Size: 5.2 MB (5223524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eccb11292f2ad0da7ded6e28d81db48fa3776d6a9b2ee92c5b83fdf418bddde`  
		Last Modified: Fri, 09 Aug 2024 20:49:35 GMT  
		Size: 8.8 KB (8753 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3878a837328a5b14037f7f1da0266c8bd6ecc2ba44c02712156456a76406219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127411715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b076a780f5321884abbad4baffd724da3038ae75ef47ca0ab387fc1997862e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b06976c393839bcd82e2bf2c08477d57f1ef88baefa9224103f856ed179a8`  
		Last Modified: Fri, 02 Aug 2024 05:45:06 GMT  
		Size: 76.0 MB (76009703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79c5deb5084d2eb27d3532b1d4a1653f835ac78ebe736bb9f55ad66246d0be82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d965f93866a02c092f17b272ba097481365c4d4e9104af3dcf0a5c06d3858d`

```dockerfile
```

-	Layers:
	-	`sha256:5aaf434cde2f19e0d7326d7051939d79c56829cf289a342f62150ed6f8cc0f46`  
		Last Modified: Fri, 02 Aug 2024 05:45:04 GMT  
		Size: 5.2 MB (5223098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460a1c9810cf07856c1bf2eb1406c62d0e361cd02559b99cd4f7ef4c9c5538b0`  
		Last Modified: Fri, 02 Aug 2024 05:45:03 GMT  
		Size: 9.1 KB (9115 bytes)  
		MIME: application/vnd.in-toto+json
