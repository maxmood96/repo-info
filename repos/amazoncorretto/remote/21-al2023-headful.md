## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:78f0deb5b87f0b50654e705ef07674020bbdc1ef4ddb2590de9b573bb11fec9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:940410366429cf015e3950abf0328313ae402ff70beb32f9204197b94274fe49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143943732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f5ff52ba3d4f5c255b1912c13b873d3e4855ee72f6a83aea65ef00b6b81aca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:20 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:17:20 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:17:20 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:17:20 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf5bf1e995e6dd4d18e9a2afa95db20917ac9dba858b0f4b6b29b5b783b6bc`  
		Last Modified: Fri, 14 Nov 2025 02:17:59 GMT  
		Size: 90.0 MB (89967017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b21e79d1ea8d5764fb2acb944f3d8f42339a42f1fcca8318361e91d3ca55c521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a22c2ccd6deb03effbf0fc7221c50bd594f59be6b5ebf85254ab84c26d604e3`

```dockerfile
```

-	Layers:
	-	`sha256:66ff047c529bb44071021d10e0b6ffb7b1a3d5e5f6832cec840a522f8c663287`  
		Last Modified: Fri, 14 Nov 2025 04:50:10 GMT  
		Size: 5.2 MB (5209943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:374dc225e9e1ed7426d67e90276481c7aa4e923915fc02205d330a3618d65e38`  
		Last Modified: Fri, 14 Nov 2025 04:50:11 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6ffd6870b62b9171da96230212e63c81b1760c5c425a53803171449dcf3ed40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141982543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898ae8c349c2f6902cd349766eab0dcafc61e9b78e672a76e94e95bbc8193d66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:21:26 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:21:26 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:21:26 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:21:26 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:21:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363024fd5b991b6c1cfb6c8c7e8261fbba26332fc11f9cee6b8cebbe4e633e66`  
		Last Modified: Fri, 14 Nov 2025 02:21:56 GMT  
		Size: 89.1 MB (89105887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9841114cf63de7b18a65105e5f842ac5064ae5e4c7d7a7e187c061359cb8c2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7837216196bece5073473e8b695efcbbb545bb6d2eab6695248a7e739bd4f401`

```dockerfile
```

-	Layers:
	-	`sha256:bd24ecb09434504176e6031a3ee4beb7f620c0ce0df1e62ef976a724257bba43`  
		Last Modified: Fri, 14 Nov 2025 04:50:37 GMT  
		Size: 5.2 MB (5208736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace6063cf0088160af851277a79dc8400a0da2b329dc37e4c67e95b3d4e656b8`  
		Last Modified: Fri, 14 Nov 2025 04:50:37 GMT  
		Size: 9.0 KB (8969 bytes)  
		MIME: application/vnd.in-toto+json
