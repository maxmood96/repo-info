## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:3f65c742894f11ab77089ad9d7f0b3bb610f9b154458c741479681f59b73d027
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f6988061f71dac7bb88ec25b1e19a03619b8e717aaeced0e2dd1484e0ecacc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141367256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81749227f3c9a0907baead9347f0687ea0e09872e71e9af3d849406681fe047f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:f9dd052e142d6bbee3556a17548362b00b044603d859f7ff1a81d3ef6d64bd6e`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 52.3 MB (52325199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead405905eeea110c1f5ad89f69b3485cd5db70405f2581c230df45b25b66c16`  
		Last Modified: Sat, 07 Sep 2024 01:06:05 GMT  
		Size: 89.0 MB (89042057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ac921484a7a9a810576a48c06c48b074695f639884b61a47263a1da492e76a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5c75cbbe86810722d36a8e07f046f2e573c0e9445b1054300dfcd962664e17`

```dockerfile
```

-	Layers:
	-	`sha256:f83ccf1f06c0709c00a1c9ef0ba496b92dc0476745d16e5f31e5d79cfe96265c`  
		Last Modified: Sat, 07 Sep 2024 01:06:03 GMT  
		Size: 5.2 MB (5212428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:076219d7cc8c895ed152ff3b4b69ed24b6a84f91a5b1e80cb00aed337bf1fe81`  
		Last Modified: Sat, 07 Sep 2024 01:06:02 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1c9f4c77bd53380bf51595a95d0b56601f99291672c1344879c9a3ce8b04dad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139434510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e033ec9c1790eff3e108f2d878f44eb6b3301f784437769249cf7b37938effa2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:5df0cce0a70b576e00cfe75d45089073c37754f2920c4a7a79f3ed6e6500982d`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 51.4 MB (51426143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc672f3e25279def10eeafd2d1fd4fd1aa5f9acedb4f7cd620a23f88565a7285`  
		Last Modified: Sat, 07 Sep 2024 13:33:36 GMT  
		Size: 88.0 MB (88008367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8e6f2463a0a1d4325242ccc06ac582cb39028e2145703210dd54b56e1562b415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d87415e4549239fa391481a054d9b2de92eff403dc4c6dc17d144d7baed2b2`

```dockerfile
```

-	Layers:
	-	`sha256:6a3f3f7576b048a46c1610bbc884915979d8736c7efdf276127c6ea1e2c870bf`  
		Last Modified: Sat, 07 Sep 2024 13:33:34 GMT  
		Size: 5.2 MB (5210415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0e35be2f8864aaac809a2796b248653a869c7743aca9334cd5764255bae6cc`  
		Last Modified: Sat, 07 Sep 2024 13:33:34 GMT  
		Size: 9.6 KB (9588 bytes)  
		MIME: application/vnd.in-toto+json
