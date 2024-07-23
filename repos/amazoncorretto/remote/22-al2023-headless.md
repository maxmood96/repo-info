## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:1c6d6785f06dcf96244d14bcd3211a43a4ecdf9fc54b4f8763b643b8a037fa2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c72d6a41083c473b1e433630bc2479cb6385b146efbaa2734516280e71842843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140658999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1953ef7419ac603495c2c6e2c4883b9b93d7e89ed89f73859bc661d7a83af6b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Jul 2024 20:01:54 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Jul 2024 20:01:54 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:f03636e672ba797137f2f72e64c7fdf7947397c0880ca5f9e9962a85462a7875`  
		Last Modified: Thu, 11 Jul 2024 02:05:27 GMT  
		Size: 52.3 MB (52313836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a745bde6001ec8c6e665a590211739705b51c484471aa432ed9f5c5e1ec7bd8`  
		Last Modified: Tue, 23 Jul 2024 00:08:52 GMT  
		Size: 88.3 MB (88345163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4cc6e4cfeff1e71513acf70bbad04e1ed04f989021d94bce0a4723e99fd0ff3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca03bc448a382f2952317b7fe02b789ff56e01cf4affa6afbe3d7115e114942d`

```dockerfile
```

-	Layers:
	-	`sha256:fd0cce0b8c6e050092752de3bb06dc6571019b1a1fd34920a5ac0bdf38dfa212`  
		Last Modified: Tue, 23 Jul 2024 00:08:50 GMT  
		Size: 5.2 MB (5186101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31563c762b1a82b78cea55bf6274ebf493f90f5684b17f1b6acfe381fe07e612`  
		Last Modified: Tue, 23 Jul 2024 00:08:49 GMT  
		Size: 9.0 KB (9038 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2739240428474563f7c7401334f1c0e6c88fc329f84243f9c3f55f5c9c339bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138705640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c662835727ff750b49979cdeb98fa3f30221090f55561b5d93aa1c1e41fb2d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522d6fa6cb69d823eeaf813fe2b11d3998e530030b5d73a933c6fe0263a897a7`  
		Last Modified: Thu, 18 Jul 2024 01:27:06 GMT  
		Size: 87.3 MB (87304502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7dd9f113f5edcfe48c68dfb13f3c639ae89fb4c25f30ad9ba07766ab86bf5e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f1a5eac9af822dd89e2af367b7e7858a12a3881af6f433d999ceabf98bb5a3`

```dockerfile
```

-	Layers:
	-	`sha256:f86fd93742928a880bc725dfe3f9c736c0c10aa05fc01182e40f6973b878201c`  
		Last Modified: Thu, 18 Jul 2024 01:27:04 GMT  
		Size: 5.2 MB (5184085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0268fb19a209d5bcbb0a7d0d181d3e39ddb6295c169a81f0a66515d7966d008`  
		Last Modified: Thu, 18 Jul 2024 01:27:03 GMT  
		Size: 9.1 KB (9135 bytes)  
		MIME: application/vnd.in-toto+json
