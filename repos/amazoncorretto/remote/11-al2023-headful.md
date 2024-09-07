## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ba9b2ec70986fb93cec7668e15a31a0e2d36b6d3c7c5c29beac8bef1dffa6c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a74c0b1a3290044352f33195220898c195c87c30e98e83d04332421e8aedad6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129168638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfad7a01da0f1547488f75f06cd7cdd921ca6594fe6c8c6fae5d9f0704a40e4`
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
	-	`sha256:f9dd052e142d6bbee3556a17548362b00b044603d859f7ff1a81d3ef6d64bd6e`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 52.3 MB (52325199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46dad0b61c357dd9858fe441455c573417f87048596b18372ffdb376ff4956f`  
		Last Modified: Sat, 07 Sep 2024 01:05:51 GMT  
		Size: 76.8 MB (76843439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72be71f9cf1d847be168d32eaef56c4fbf08bc8f0e4fcb69a8bb358a91ae8f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f12289a48936902421b207a7c5f9e279a32c1a991c6532123a237a0b6e615f4`

```dockerfile
```

-	Layers:
	-	`sha256:9d53bea21d4aba1a8639e88b3b74459afd9ce8c36dce5faae7818dae68c7ce73`  
		Last Modified: Sat, 07 Sep 2024 01:05:49 GMT  
		Size: 5.2 MB (5223612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20ffbc629064e38d189921f9beed7167fc2450619d163c890ce274e1f0843f73`  
		Last Modified: Sat, 07 Sep 2024 01:05:49 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:31dc250529fe22e53838c0d6af69bbabde6680c7817fa6ba1f686d9debcc039f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127428207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355508bdc83ab6ba613237a24ac4ee5ed54fcdc7f5398f952b3b753803433278`
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
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f279fa847f04d29d016e724b1ba864ebe5c82541cbf63b84fc671aac78d79ea`  
		Last Modified: Fri, 23 Aug 2024 02:22:16 GMT  
		Size: 76.0 MB (76001909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4a6f26c15a03cb12d1205c5aede1dcf8aff8020da1e36f9bae6ee7343cac88b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df26e678970b302635533dff497b5426caf7beab684896fcc95f4b60597aec2`

```dockerfile
```

-	Layers:
	-	`sha256:5b262c9ba8b6186d67e35ac48d5ff773f0b651b31776e6e5fa66cfbe91977b79`  
		Last Modified: Fri, 23 Aug 2024 02:22:14 GMT  
		Size: 5.2 MB (5223232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e77125f3e4d9c4e3ca2f31d0046066d6fdf36dce6d4c13f227c03747209ccc5`  
		Last Modified: Fri, 23 Aug 2024 02:22:14 GMT  
		Size: 9.1 KB (9115 bytes)  
		MIME: application/vnd.in-toto+json
