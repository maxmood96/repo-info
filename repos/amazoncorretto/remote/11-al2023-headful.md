## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ee68206de077b21c132eaf859387ae481ddaedc6324c7e953ee18a7d09dd7e64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d78b57ece48f6263c97206a01dc37f33a196b17eb97bb82f5a83511cdc89887b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131336959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62787605584feee4250307de7473454dc200e6a027c869a749ae757762244ff0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:02 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:18:02 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:02 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a538e64cafea11f4b180ce0ceda92558004385a2d405ff3730e83438f9502944`  
		Last Modified: Sat, 09 May 2026 00:18:18 GMT  
		Size: 76.8 MB (76760155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc9824e1101620bff4c88a3703bc2dc954f9f4b230afe72c3dd209325e9f0d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29449674918449a31aa47c60695d67f6cd65efca0872d14ef765c78e78785ecc`

```dockerfile
```

-	Layers:
	-	`sha256:c81e319d2fa59041ce317a3155fb243fce5534dae8e99cfb075699a49c02c7a5`  
		Last Modified: Sat, 09 May 2026 00:18:16 GMT  
		Size: 5.2 MB (5228698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff568e3136ba86479919896a446afe2c854562b2afa7a0767baa1b648ce1af26`  
		Last Modified: Sat, 09 May 2026 00:18:16 GMT  
		Size: 8.9 KB (8907 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e98f299dab9f95b9c9bdf34dca4d78b05b6536a4ef8ff1684133276ef9a1f7db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129473515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0529b706ffb34c854d902d5c85258c045d6b92e231427fdb4df93cba8e87941c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:14:56 GMT
ARG version=11.0.31.11-1
# Sat, 09 May 2026 00:14:56 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:14:56 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:14:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843093bd03ee9a73a188a3c1e716908bed9bcb7deb544e372e1d16cfc95724c0`  
		Last Modified: Sat, 09 May 2026 00:15:14 GMT  
		Size: 76.0 MB (76016540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:11f7adf40c4fcaa7a02bbec9ed14e1aa669c10e84491a849df14173bde278da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dff6f104e3589a2acb213376b3f8e4b4afb85c372ca9d5ad17efbaa24dfa6b`

```dockerfile
```

-	Layers:
	-	`sha256:f4db309840e21dbf4dad02fe7e9294024ff60c63c80b916efceca97ddd8ee703`  
		Last Modified: Sat, 09 May 2026 00:15:12 GMT  
		Size: 5.2 MB (5228319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f36949471579fcfbcfdc67e1614afcf8d5591e0455295ed19beee67f9e26fe55`  
		Last Modified: Sat, 09 May 2026 00:15:11 GMT  
		Size: 9.0 KB (8986 bytes)  
		MIME: application/vnd.in-toto+json
