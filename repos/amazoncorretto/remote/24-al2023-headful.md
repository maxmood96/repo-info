## `amazoncorretto:24-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:10d0e3587efb6832dc12e233ff80d8849a22d29e3cd12273ac870b56b27da380
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8ca28dcf084e4964f8604b44830a822b09391453cb872b1954c9982499a8d194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156566441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9da72e7d1aff4d2c2f3e9d7f57ef033e3d48b1d9408aa5a91d8de9d84c1462`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05226987f7e12d95f54ba886f7e5560bec87e093f8c787189dfa4a9d8378df64`  
		Last Modified: Fri, 13 Jun 2025 17:03:49 GMT  
		Size: 103.0 MB (102996081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d4eaaa00fb44838f537a5d7425178593e19cbe3aefd808131ecaefc608750944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ee89bbbec2c8ca0c0476677cd5222cab1936f3fc9df96b4a6aa173e6beef87`

```dockerfile
```

-	Layers:
	-	`sha256:95253999acd9b68ad65c6b78865f1bdb29be82790cdf5eff63a9bbf55ae2da13`  
		Last Modified: Fri, 13 Jun 2025 18:49:22 GMT  
		Size: 5.2 MB (5220825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b0bb15664b0b5ccbce6424d4d7f0a3bd4db3086416a96d746ab8999a8452415`  
		Last Modified: Fri, 13 Jun 2025 18:49:23 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:00a95e595ff3aad8b35f73740e7823aec48e283f58d891f596a7a0008179fa28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154477256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cb983f5910b1633531c2914b3e0050d72c8d3e1fdeec3c5df2f97ab7f2e48e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de23bbf3b111dfa3c6c184d229e45333655a55d8742a45c29eb95210d791a07`  
		Last Modified: Fri, 13 Jun 2025 20:08:47 GMT  
		Size: 102.0 MB (101995564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ecf747def3ec3d6e18367540bf194cd661557e03ed45fab2e61267b1068cf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb29b228bb1cdb4a1d4d76d65eceaf99853c0e2c828ef069335c70fedcd96c00`

```dockerfile
```

-	Layers:
	-	`sha256:587015ca12d935bb68a1c50781d533861737c7c36e78eda170e6bc09a3989971`  
		Last Modified: Fri, 13 Jun 2025 21:49:22 GMT  
		Size: 5.2 MB (5219639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91d8560728e9cabf2f461b27220a624e701bf17e36be3f85ea2efa45ffe52d6`  
		Last Modified: Fri, 13 Jun 2025 21:49:23 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
