## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:8220ed59991adb20a54119ad5c686c17bb4da6c6c77a44f5af81e1296e021730
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:33f22fbaecd331199a16ddbd79ac2c3f8cf6e89e2e5a58b95f5bd234fae33167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136911027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e574db354f8dccc69f73021ef3d870689ad6df250afefc894756700f1c85de3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9ccac4fb23ffe24a344fb5fd65ed114654873f47b58299930bb693a443d45`  
		Last Modified: Mon, 25 Aug 2025 20:18:05 GMT  
		Size: 83.0 MB (83042297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:234f231aaaf29b9620c97f147aabe1a40aab7fe01e94691247e2f3f7cbdf5390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c0d50f9c4efdecca26cd241cb4b31a636415ea5c31d17b096ef20d695d4e4a`

```dockerfile
```

-	Layers:
	-	`sha256:a9950e49dc32ee33e351db45db123a3a39be2574735e45f7e10792a4bcb2ecdd`  
		Last Modified: Mon, 25 Aug 2025 21:48:23 GMT  
		Size: 5.2 MB (5208245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6196a8fdbf9e81e751074a9c08b0afc3a9111aafcf716f83564506a9c779a626`  
		Last Modified: Mon, 25 Aug 2025 21:48:24 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a77a7a202842ee53c094df74d890124972f4f5ced8ca5c3cef3e70353d102d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135196222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7da93087e148248f5104e790bae7322b6d7a66e11c3581ef77a383f4e13b2b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2b8cdb25345f5d486ceb7d91dda096b5aadcf28ac74ec2e935e287201f2e75`  
		Last Modified: Fri, 15 Aug 2025 00:02:14 GMT  
		Size: 82.5 MB (82469828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb32e62917498a189472462cdd14fa182c48425b3f0fee13be167d7deade2391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fb1890438b001093f6f1bdb0898518e779f0f088cb5b80173d93c36b764f14`

```dockerfile
```

-	Layers:
	-	`sha256:63a6666ab11ed8dedfc5ae43a7b4df9cd8ff2b9b2a31bdb157bd555022b17194`  
		Last Modified: Thu, 14 Aug 2025 09:48:26 GMT  
		Size: 5.2 MB (5207036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0992c11581822c280301a3bdb14fb9426207e0b6e891f7c2d88a199df69d6ea3`  
		Last Modified: Thu, 14 Aug 2025 09:48:27 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
