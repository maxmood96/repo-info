## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:bc736d638776862ac650413a51c7175f36cd11796f5c231a271bac94b67e9f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3ceb62f944cf3189f21b9678134ae308e5b817a221a355261a97169217fd812b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142836028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03a52227d27b736d4198e1c9a20a24a35d4a594d0f27cd1a3116b47b2bd502a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a2e8122f4c852d604a3ff5e6650100665488cf1de3c06e5533116d32d5aabe55`  
		Last Modified: Wed, 29 Jan 2025 02:05:37 GMT  
		Size: 53.1 MB (53149711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f465de462a5452e69e924b799bd1f9827d77f0dcd089ab3faa78afe9ec95384`  
		Last Modified: Sat, 01 Feb 2025 01:08:51 GMT  
		Size: 89.7 MB (89686317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6936008891998a2feb52e4a88006bef39bcf97387216db207e867072360f4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c073381ee210abe5156d5033b319f0ddc711bdb0ba052eb4c97e2e36173ae11`

```dockerfile
```

-	Layers:
	-	`sha256:bdaf74bad8d4889612cf51708794334fe350cccda1f76ceb46f9111626de4fb0`  
		Last Modified: Sat, 01 Feb 2025 01:08:50 GMT  
		Size: 5.2 MB (5186578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ed937c374c6186b82297d51013a0c0b3febc58aac90d223e3d02c9ba5a4376`  
		Last Modified: Sat, 01 Feb 2025 01:08:50 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:196e625958d257df3d58902f8983459f4da39af0a059c4efe48995098a395670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141101672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36707e2f91ca2f95a234d5abea4ef8aadf07c94c9bb3f80834e5196c492db4c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:523a6b03095ed77c021e90dd9cc9c96374240d01b0165f628a7a82b4d9acd585`  
		Last Modified: Wed, 29 Jan 2025 02:15:16 GMT  
		Size: 52.3 MB (52269024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f68744fe837dd0f8ff198f7afcabe8e82dc16814d075fd1371f8edac4a9017`  
		Last Modified: Sat, 01 Feb 2025 02:25:16 GMT  
		Size: 88.8 MB (88832648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cb9090df517e5535d7ebe9ba40aa0e85a8ba0b97c0990794e4bd5bb809b6e557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48ab8953bfd979dfbb42bc788a1d9ce97896c9cb09f83bfeb3c5ccd54120920`

```dockerfile
```

-	Layers:
	-	`sha256:714ff089c47c138a04aa2572c2e29ce2a92682e0ce5dac5e21e20eac751b3969`  
		Last Modified: Sat, 01 Feb 2025 02:25:14 GMT  
		Size: 5.2 MB (5185371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a718259a93e9971d90832868afd37f08cfde5db0a5f3548fe69e4b9dab7cc3`  
		Last Modified: Sat, 01 Feb 2025 02:25:13 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
