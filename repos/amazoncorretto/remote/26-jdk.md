## `amazoncorretto:26-jdk`

```console
$ docker pull amazoncorretto@sha256:c68fe7fa937feda33a37ee8edc2a3897db1fc62949e2b1d071de6aecdc65818f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e39dd13287feb23529a6face5d995251c2e7db3be88459dac39dfd718d884ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.0 MB (248019620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802ea5085fb2554933672c5e51158b5d3869a282ad4d384f9e8cfd148decff4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:13:04 GMT
ARG version=26.0.1.8-1
# Sat, 30 May 2026 01:13:04 GMT
ARG package_version=1
# Sat, 30 May 2026 01:13:04 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:13:04 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:13:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6cd6b71904ad0c9f44845cd2e44e84fe94b5bd028fe58243deb1a28cff2f00`  
		Last Modified: Sat, 30 May 2026 01:13:28 GMT  
		Size: 193.4 MB (193448464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:64e76308873d93919a55c8008a981e7bbdfd8ab8a44a9bdf2a26290fc2b84840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d30fb83defe95499c2c30e2c993a58f11028ac585c4257d134e9139f5ece3f5`

```dockerfile
```

-	Layers:
	-	`sha256:78aa89667f9ed525dfbd0dd0820a8e00181da86d7c06c8fec2e718e146f90908`  
		Last Modified: Sat, 30 May 2026 01:13:24 GMT  
		Size: 5.3 MB (5332742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddccae03ab80b08c20dae550ff988549377f6d1516b415c096f9962a463876b1`  
		Last Modified: Sat, 30 May 2026 01:13:23 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:18a41bc690adfd4252f64a4765dc9106408f160eb81734c599ab4ceb3a133e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244728178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b412f3a9b0b1c9cf1475f06765c9914b8315016ef9d91a0aa7ed21bad7229c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:46 GMT
ARG version=26.0.1.8-1
# Sat, 30 May 2026 01:12:46 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:46 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:46 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cb409cbc386a378ceecf3534bac8fa8d7648e86970cac53af9892dae6c57e5`  
		Last Modified: Sat, 30 May 2026 01:13:11 GMT  
		Size: 191.3 MB (191270351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cbb2744e626e8071a9cef944d8a6d61db9f5968a91952c4a9120fe6597a97fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c547d71632b534eadad9b9b8aba8003def083c2d65b7cc71ca87bbfc2302ca`

```dockerfile
```

-	Layers:
	-	`sha256:8623e29c01639e74da406e053271cd042e127a400cb5ad3a312d8c6613196ce5`  
		Last Modified: Sat, 30 May 2026 01:13:07 GMT  
		Size: 5.3 MB (5331718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd0c1f2f13d56ba05f48387a4cb325889a8b5724628f35d487acd150eb4de6d`  
		Last Modified: Sat, 30 May 2026 01:13:07 GMT  
		Size: 10.8 KB (10778 bytes)  
		MIME: application/vnd.in-toto+json
