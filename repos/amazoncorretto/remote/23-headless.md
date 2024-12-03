## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:a6f78531f67ef57ceab862e353a9c90014f09f958fe7ead4810f3e8ed90e0a30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:83579e22c0cf7e753f6f214ba36d5dc1d4923f2bf94bf01b00b009d0a950d6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145460113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a392fa63cf92a7921e8a26742a9324e76770dc8b0509ba3bb8248b02e5ea77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:4a665eb63bc8cddb90e1e74e3ec745a1bab733c919dc4b2d648b43459295464a`  
		Last Modified: Sat, 23 Nov 2024 01:38:06 GMT  
		Size: 52.4 MB (52377532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0353792426c4c30e95dd748fb707da7e9f5fc68a30b96717be71fab64e4b08`  
		Last Modified: Mon, 02 Dec 2024 23:23:30 GMT  
		Size: 93.1 MB (93082581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:64df0a1cd0bb17988088fda0a8ba5101c0080137d4849f2d86c6377d0b78069a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dba8a97ef85ee05eb1b2d026d725c8ffb672a2536a32d00347fac134b26c2c8`

```dockerfile
```

-	Layers:
	-	`sha256:913e3861c3db86ce5d77556761e879761f73d5217d026fd2eb692384b59695fc`  
		Last Modified: Mon, 02 Dec 2024 23:23:29 GMT  
		Size: 5.2 MB (5188972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73e7ecde7dfe3034e9e21cc29a34ed756cc7fe87f68ad82b6473a62e59f637a`  
		Last Modified: Mon, 02 Dec 2024 23:23:28 GMT  
		Size: 9.1 KB (9071 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c4edbde4cc9d43a53ff9d71f604b8456c1a240c900e3b03bdfba822fbe8a9f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143512146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edbf7d427f9cde172623e1c38c1552b501066451da4c022fdb21907d5502721`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc945fc601cbc50fc30bde764119a6aee592d2a53d19ec9e0f19aa3af76ace`  
		Last Modified: Mon, 02 Dec 2024 23:32:08 GMT  
		Size: 92.1 MB (92056302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e38276635c12b41895f916e93c2d1484ef1a479ced1a2a315a56bf25cb4bed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2121b7afab7fb290259901e5fb0a0d1c0ff9b594c5d9eddbdfccf6da779526`

```dockerfile
```

-	Layers:
	-	`sha256:9cbf89671312f2851ef43fdb27949ecc6d869e6399e3d9c342d2cdd18a29b2d1`  
		Last Modified: Mon, 02 Dec 2024 23:32:06 GMT  
		Size: 5.2 MB (5186958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47824776e08be2a988b5813c354d66bd7886a76a48c72997a81770fc7c19b361`  
		Last Modified: Mon, 02 Dec 2024 23:32:05 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json
