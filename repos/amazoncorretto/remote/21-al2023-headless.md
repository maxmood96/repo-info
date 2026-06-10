## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ad6da26bd1ef19e82dedbb7f43dff8e632f9f02a0ba74ad496819908aaab33ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9d8ee6ec0c34c61b1205bd50f0eff421fa0a393c4f03cac6f17bc1ec404a9b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143929528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8854e5056a860a0cafe4327ee1c687d0dcc2c628c90cd7a4bc2071edb0a115f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:37 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:37 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:37 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab62a2d5442919434d827d8908c440b973361ad45881f7b0b478e32f7816bbd`  
		Last Modified: Tue, 09 Jun 2026 21:12:54 GMT  
		Size: 89.4 MB (89358372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8142c028e2872395d4c92f569bb3b5a8c03d6e62f77d9c79e340fe255bdcf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b0ec9f074b33696a85c643fb8a3d13635e8ef4230e86b560cf1092f8bcdcfe`

```dockerfile
```

-	Layers:
	-	`sha256:b3cebd0698cadd58051869c88ddf02e8b73ab9de304a934e89d5a8de3a18ae70`  
		Last Modified: Tue, 09 Jun 2026 21:12:53 GMT  
		Size: 5.2 MB (5191789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c903b828ab55f9ef5d2d6a39c7303bee166116f80aa896a00e950d0c0a95e610`  
		Last Modified: Tue, 09 Jun 2026 21:12:52 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:046d8dbb03d9ae875fec2a12c47372dc83e21560d3d70ef73dfabdc890a4f6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141949403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905787c5c03772326ed6d75f9ddae044965f0fe7d92355035bf35698092bbb54`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:29 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:29 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:29 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67065a4547c82735a36a7ca20fc7cd9bd948c6fffdce1b5c31c51df7b11bd6c2`  
		Last Modified: Tue, 09 Jun 2026 21:12:48 GMT  
		Size: 88.5 MB (88491576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ab722212a847dc759b9624f96c43d59ed811f3b98ef384c6a27b7c507fc5be7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da394ff39b37237335483f404bad85673f04c90625da47bac9790aadc9a16ca8`

```dockerfile
```

-	Layers:
	-	`sha256:1475427d531bf75002a1c301d71a4c1213e884f888536ebae21cc6704f63084f`  
		Last Modified: Tue, 09 Jun 2026 21:12:46 GMT  
		Size: 5.2 MB (5190580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:706d07047c9f53fb809d6f6b600b487d5be5420b7930d97b714d20601f9f3066`  
		Last Modified: Tue, 09 Jun 2026 21:12:46 GMT  
		Size: 9.0 KB (8960 bytes)  
		MIME: application/vnd.in-toto+json
