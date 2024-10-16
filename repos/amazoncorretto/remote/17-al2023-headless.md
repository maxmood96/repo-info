## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4a8dcd4ff127c9d455b334a0e2cb845c5e126f7debe95e123742caa110bcce4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:198c6cc121bd6a4ac2219fda07dd8d2092bd11befdfbdd4828596593ce8d52a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134385194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bea5ed49f24cb035707e9950de34196d05b449e3d56847555f32fe88220cbd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ebb2070e9f36b50f9f6728ad97b8c19d879a127ed65a9b11a838dc4d4d6c73`  
		Last Modified: Wed, 16 Oct 2024 17:57:36 GMT  
		Size: 82.1 MB (82059889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de73e48a2ad76d7248d4046391119c49d1b5a5d4366d74274e44fb6f9e8ea4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2a4f5854d23ac16b3ae31653b22b9724b3b49df82ee1479d2d1c9bfc441dc8`

```dockerfile
```

-	Layers:
	-	`sha256:eefc1a703cf4203eee54f3aca24d8c055db7a24768c78516c110a5613c928612`  
		Last Modified: Wed, 16 Oct 2024 17:57:35 GMT  
		Size: 5.2 MB (5184572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6935b7ddbdb10dd8301465438c68fdb62a9af9f1fabce2f227842587b34a4a8`  
		Last Modified: Wed, 16 Oct 2024 17:57:35 GMT  
		Size: 8.8 KB (8760 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7a0dcc8d7013f0d6e9d1d6890bfed0d2981123f5ffa0a07023ac4e2fde997832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132842352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5948682506fd811532b1e8fb53a1922d0e924ada27d069d14519c82571fc101a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e92aa254e1a67c13d683d937c1539c1980d4aa51dd154127a8f9e642d81bd55`  
		Last Modified: Wed, 16 Oct 2024 18:22:19 GMT  
		Size: 81.4 MB (81415988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f227bf2cef001524da3ac4b5c54c443fde8c44e16400e4fbb15e697c0b469ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91416862c61ec82c2422dbab990618ea1417e8f7d17c60aad319e9bcfe37452e`

```dockerfile
```

-	Layers:
	-	`sha256:172cf5b1f7c16f2a1a5dd37e8b53fb0cf38c0f2755f1010c2936e3a74601a66d`  
		Last Modified: Wed, 16 Oct 2024 18:22:17 GMT  
		Size: 5.2 MB (5183358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb1584dfdc8bb6fb34ca785ab5d496356dd28b70d4c722d8b43df7132979415`  
		Last Modified: Wed, 16 Oct 2024 18:22:17 GMT  
		Size: 8.8 KB (8840 bytes)  
		MIME: application/vnd.in-toto+json
