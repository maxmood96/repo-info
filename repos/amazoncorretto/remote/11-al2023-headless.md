## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:3b6dffb23c776c2332d5ec0a4611a6c3920ebb6f22c449f661cfd74a36899753
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c7a69478a51de3fc9b74c82cce739fa4e9f9a69237da1f8e25b4196ba4ae23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 MB (128559442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03bb0d22d9159eab7bcd164791e280f3f28a13cefca91743b97063ca8babdb0b`
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
	-	`sha256:4a665eb63bc8cddb90e1e74e3ec745a1bab733c919dc4b2d648b43459295464a`  
		Last Modified: Sat, 23 Nov 2024 01:38:06 GMT  
		Size: 52.4 MB (52377532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb56600720120d6f0293cc4c6db0cdea3e196e793c7ec5fd9b053f1b602b35c4`  
		Last Modified: Mon, 02 Dec 2024 23:23:17 GMT  
		Size: 76.2 MB (76181910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5bc3658b47459e7372d61f8a950e766aaf0b7bf0e69c90308261fbeba92ec324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df00c4ae307382a28a78a62b2b7cad01dd52ab0674e71baae1a2e95d98f89259`

```dockerfile
```

-	Layers:
	-	`sha256:4d18dda70fdee394a0001fddd9f7f1ee7fe5235356c3267b7b69c094e212302b`  
		Last Modified: Mon, 02 Dec 2024 23:23:16 GMT  
		Size: 5.2 MB (5198469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b810c4df989681a3288ffe2183f43b6a1a88846c6a45fb9febf4f5d9bbdacdb9`  
		Last Modified: Mon, 02 Dec 2024 23:23:16 GMT  
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
