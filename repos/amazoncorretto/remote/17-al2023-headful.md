## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:50e1c3bbfce556745ab9070dc85169c00f6f4c0338d040f3a49a30e13280dac6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e30f083f384a4bd6d8e0c3359add5573034ac8e88931622c74cee12ec94c8db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137782773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621cd4f0f1e42ac32181a866e4b66ee2917152fbeb8832c80631829f9fd8f5c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:02 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:12:02 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:02 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:02 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76423c9813e40fd651f029c129c0d97911d8e6d7b091ae2946dba5c073843b32`  
		Last Modified: Sat, 30 May 2026 01:12:21 GMT  
		Size: 83.2 MB (83211617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d62b2fbbc308abc58471c224549bc2757c3c6fcb14d8db609c33928c0cdf56e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54437b272427cd7243a1bb6a2f5d79a105b24a401934f33c45b6da9d7668009a`

```dockerfile
```

-	Layers:
	-	`sha256:5887808cc7980210a7e2cb48c462052c96dfda35647f30c5a08ea0b2524c1d0c`  
		Last Modified: Sat, 30 May 2026 01:12:19 GMT  
		Size: 5.2 MB (5215594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3051baf7c585157203e224421a401cd45d97fb3d826205b3e1642c4f529680`  
		Last Modified: Sat, 30 May 2026 01:12:18 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:abe74dddfd28cb978f7f406b6eb34ca7fc00feb5a0dd219e9ced3f3043440586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136092851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c4d3e26c79bcbc7a5c9f71f1b58d5ec7398fb4998de3d311d074665da38c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:53 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:53 GMT
ARG package_version=1
# Sat, 30 May 2026 01:11:53 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:53 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f711dacb2cb18e2f64382baa083af040f723502ee5acd9e613f3887b9d9a6c3`  
		Last Modified: Sat, 30 May 2026 01:12:11 GMT  
		Size: 82.6 MB (82635024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a579bb6a33493644b6ac2eb6cd319a59df6c0fac4f0d24f666f0527de3e15c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c05fd6ab223e15aa904b15cc45c9782b621049ba5cd1b4336781e6c067a54b`

```dockerfile
```

-	Layers:
	-	`sha256:2d1f1b98f878aec1b1d557138a4868be95e825b320a8d145fe620bf8f7502799`  
		Last Modified: Sat, 30 May 2026 01:12:09 GMT  
		Size: 5.2 MB (5214386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8edd3631d5941ad897de94413a52c27d0d4f6a3b0f8aac0b57ef911d3e0aeb`  
		Last Modified: Sat, 30 May 2026 01:12:09 GMT  
		Size: 9.1 KB (9133 bytes)  
		MIME: application/vnd.in-toto+json
