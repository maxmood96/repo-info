## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b1c8251373cce39e0350b667f45acfd71f93b9ed3d2d9d5df82a4e028a68e7bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:50e54a8bdc9ef61a82f111f54999f2f05cc20092f4312663e5c043b29d4cf2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129384201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c7ed9b4796816fa1ad33ebbf9410c2268e2830d15ad0058e0bf35f2a74ce0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f661c1cf50d5a2581abf17f2334730f18217719f7f70927fa7fbd8e9c9abb71d`  
		Last Modified: Fri, 20 Dec 2024 22:32:18 GMT  
		Size: 76.2 MB (76227888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cd5b1790c5234e7acf47c4c269cd8883266ccf8c9753614945a37928131d4f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f7dc9ae4c9fd20b6f82a9c8e5dc060f811dffd3d540a2d322f21695eb159e3`

```dockerfile
```

-	Layers:
	-	`sha256:adcc01bc27ac0ea15162a5828a8e309acc3b7fcb88428eacb4117b8063f54893`  
		Last Modified: Fri, 20 Dec 2024 22:32:17 GMT  
		Size: 5.2 MB (5193347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c006e12a8d8f6e92f3f420e1d18566e5f6e93d6aba1deb9bec36caf3c31637b3`  
		Last Modified: Fri, 20 Dec 2024 22:32:17 GMT  
		Size: 8.7 KB (8652 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:48b925466979ca6ea462b058ef6ccdd07d65be20a30c3532371591c55c84f62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126829334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9bf6e284ef487c9d00451debcd7e686b124242526f84bb8eb9b5c3ddb29ca5`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b2e3006b01144f6c69caa79ca7aed16b737b5b6cff0bac29fb1841d839690`  
		Last Modified: Mon, 02 Dec 2024 23:25:03 GMT  
		Size: 75.4 MB (75373490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a43095df2919e61686d6ba7925b0bf4851d3a0ef5aad5f50c2662c2a68ccea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770b87c3680ea3b61b96ea5349db3f09ea32e10cbc9e1527c28fe6ae472ee382`

```dockerfile
```

-	Layers:
	-	`sha256:edabb07009f8d23fe6648b4646634c5693e387dfd84d0ace292ef76d59f866be`  
		Last Modified: Mon, 02 Dec 2024 23:25:01 GMT  
		Size: 5.2 MB (5198086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0dc469ddd8add94caf6cad92ac626f2588c42ce2d19444c460473c3a5f7be4`  
		Last Modified: Mon, 02 Dec 2024 23:25:01 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
