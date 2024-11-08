## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:14234ae843ef4ef24066244e0f90c3fbdd1b43d98ef85cf558df766ecfb36948
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:578f17bd9c22f3f34935e2660ff16ee1bc57cc6ae0fac3400fd0a6d99d529ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129222152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8b246025f900aaa7a9c410e4ac09e62cd6602480ef50452b4a7b892be49aa4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5f3b500dc43eba4cfdf8e70913f712bd20874deac837800a822eb046b9b8bd01`  
		Last Modified: Wed, 06 Nov 2024 19:16:29 GMT  
		Size: 52.3 MB (52344739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6324c7e24320e5033e76d41ebd2c932f888193e68a47494bd40b32058d2e760`  
		Last Modified: Thu, 07 Nov 2024 21:47:58 GMT  
		Size: 76.9 MB (76877413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:53e892d4655385b9fd7cfd64d8ce9d7312c936274f5a94d1f5e94f3d436a4092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b842981dee899abf05e3610d8b249af6b6bd4f9e8e505bb96c7f9463ecbf66`

```dockerfile
```

-	Layers:
	-	`sha256:429992631ba93d28d25531a53e6c0530ac8d281139daf9a11c51b3f6d093f75b`  
		Last Modified: Thu, 07 Nov 2024 21:47:56 GMT  
		Size: 5.2 MB (5223795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246ff38107d967897e1b9b5e6f3ec96f84f9f16ff4e9a0e90d4559e6c1c14469`  
		Last Modified: Thu, 07 Nov 2024 21:47:56 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:babc5f015d99b4b10c28f803655df2de5d95a3ca347e3cf6ae2fcb72701d05b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127503786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5177a19db4c06c0f6b24a2c9e5a277e0c15171d781342161a66bce5fe737767`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74aa4f73a8a12623c696d6800d1ef253822148b8ddc659923758d65d3297747`  
		Last Modified: Thu, 07 Nov 2024 21:53:28 GMT  
		Size: 76.1 MB (76079785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:94bd64edf24a71b59e0b7433242b2fd65538574c1dd5cb749c08aa0a513245b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77fd182a067ba740b0f650e58b914c6d6542aaaedfa160149421cdd00ddd313`

```dockerfile
```

-	Layers:
	-	`sha256:90d0e609a48e1c1f1af38bd5800a2cb920dc6ecf52f1006be28d0caa2f9a76dc`  
		Last Modified: Thu, 07 Nov 2024 21:53:27 GMT  
		Size: 5.2 MB (5223415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80baf273713a35b57cd844d206f11a0081ad0086ff6422de0fe9be80600a810d`  
		Last Modified: Thu, 07 Nov 2024 21:53:26 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
