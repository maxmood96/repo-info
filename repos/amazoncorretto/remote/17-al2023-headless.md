## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f3d2c795740063ee41c746121d45892852b9c4f3b4b44bd5b10eec2c0be968a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5ef1d67f4463472d99779eee56b8e6945de3fdf584a409475c32fdab6dc2ec9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134757478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f141c3f40b46f5452524b2bc7f972f8588210e368d7e0cb3f8003e64297605`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f9dd052e142d6bbee3556a17548362b00b044603d859f7ff1a81d3ef6d64bd6e`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 52.3 MB (52325199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cc857e9d0658dbacc50b54c9de3207e94185afafcaacc3dcbcf51d1893f381`  
		Last Modified: Sat, 07 Sep 2024 01:05:47 GMT  
		Size: 82.4 MB (82432279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a986f1c412478c13e56d17d8283305d84dd7f4aed37e15c54406a79de20074f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f3a582b54a1d971781ee27ed5e85af53e203de9f4f9a6489aaeb7ace27678b`

```dockerfile
```

-	Layers:
	-	`sha256:5a654b7c3945e010647231eba9b40d780cc93d382e4e856a735a545c37f3bcf1`  
		Last Modified: Sat, 07 Sep 2024 01:05:46 GMT  
		Size: 5.2 MB (5183727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561b7658d97d33a79cf017e1312b34a0291fb338c6e8b0593f912d59531b5fed`  
		Last Modified: Sat, 07 Sep 2024 01:05:46 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e51f2033ccd861e57c4fade30fa92b736b31c373bef24117dc6fc6648a73d474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133176011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97576f8e500621061b2a7f121d97e2b237dc3efe286a3d12a4b8d74b7d7d462d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5df0cce0a70b576e00cfe75d45089073c37754f2920c4a7a79f3ed6e6500982d`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 51.4 MB (51426143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdf99573e8519be0f0f1f493ce99f526db97d17b26e0072d6cc1d619a64b35e`  
		Last Modified: Sat, 07 Sep 2024 13:20:32 GMT  
		Size: 81.7 MB (81749868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0cbefc6d7db63ba41c4b629a795bba15d7f2d0d6c2574c51266be72608554c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5356aeed7df1a28db4c1df3fe09a7bc21ba4538bbedc74d9ac1c35037886e059`

```dockerfile
```

-	Layers:
	-	`sha256:6c293c280fcf5b73bf7f60222a86e3dc93eedf44f2a006fe2e3d7b25bd510f18`  
		Last Modified: Sat, 07 Sep 2024 13:20:30 GMT  
		Size: 5.2 MB (5182512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470a646a207708f740f3b506d492a60a8aadd206f40f0a5fb025683bf16f4c9b`  
		Last Modified: Sat, 07 Sep 2024 13:20:30 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.in-toto+json
