## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:75b67e018d88479b76972cbf8b0aa99cd88aaf47f72f3b40fadb8bc0b5437a1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:562f5e7302f5da3dccf68f14df37204c173f0f489d9e1850ccb4f5aae4727ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143838919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ca56287a256928743995c5429974943915137d5854fccfd89d2da41409e3b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255ccbebcc63dbc5105c24701d7eb312b27e48f0be8e85aa2bd33ddf7a0472a7`  
		Last Modified: Fri, 12 Sep 2025 04:34:57 GMT  
		Size: 90.0 MB (89963213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:556ce765a3ef1842679605926e37c9dd77bbc0d523c617d28932873efbd2c320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e067360ea630d5a8fe3c67269d56904e21cfa03c6b3cc1c31fcf81d7612e81`

```dockerfile
```

-	Layers:
	-	`sha256:1025337b87ab3dc6587e5b7a40e81268f539d1378b99c31136617be5bf6ef840`  
		Last Modified: Fri, 12 Sep 2025 03:50:14 GMT  
		Size: 5.2 MB (5209861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e788ff228980e229987876794f9a04061297cad0bd743bdccb0cb028f5aed0`  
		Last Modified: Fri, 12 Sep 2025 03:50:15 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b8207fdad7c83a56a514909315b93d73372c3256d135bef925bc7026d99d3741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141874102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ffea7043c1c48ae6e15d702bc29331a1018404d8c45c0353cdc9ee99d6c21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133a087c6c9df50eb0168f15251695ef76360a53a9fdca86b1768eda52b820b7`  
		Last Modified: Fri, 12 Sep 2025 01:12:41 GMT  
		Size: 89.1 MB (89098991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:643131dc9219e38184b3764e8af61431171776dbb7e969f1ea802b9bc71ca55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0d6ba9b513a997f56c21c8ff5359e558af200f7de20c087b76837cfe4e058f`

```dockerfile
```

-	Layers:
	-	`sha256:d795e211a2ea31167bb3b32e8d09ec4665477500fb750d1bd703993f55dcc4d7`  
		Last Modified: Fri, 12 Sep 2025 03:50:19 GMT  
		Size: 5.2 MB (5208654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945316b9174a7e441dd6f7a8700eb169057a2867a21ed882858ca19904c75bec`  
		Last Modified: Fri, 12 Sep 2025 03:50:20 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
