## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:53dbf1045ef03f502c00f6b347b35d9f4ff9345504711ebc292e3634054a5b87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4a83cf4bef783bfa8f647219c6140b44b8e4aabb7686663e33a9f78c91b48423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136388200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a57a26f05111d7e5d74b0378380f3354dbae7e3b53fe34b4aacc580c194fada`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:08:12 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:08:12 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:08:12 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:08:12 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:08:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c3eb4b17e2dce9e34d6a09b328e61ec2aa9584435938904e915d944aebb9d`  
		Last Modified: Fri, 03 Apr 2026 17:08:28 GMT  
		Size: 82.4 MB (82355110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8629851106cfdf128e3240ac76df5855f5261311d7c356c825134a643c12874f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637e8ab97582479a42bb1ea147fac75e4d1c39b122f7f47d83fc325d7f4791a1`

```dockerfile
```

-	Layers:
	-	`sha256:9dfb260bc07a59764a1cf7a9dbad19229bf528a3148e20ebba2dbba9195d2759`  
		Last Modified: Fri, 03 Apr 2026 17:08:26 GMT  
		Size: 5.2 MB (5182966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf162b931a244e8e8d519d601ed62587ef8a079a3ec99ed976e2731e2023d7a8`  
		Last Modified: Fri, 03 Apr 2026 17:08:26 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7bacf7ecf1f3d3e8fd586dbf1587fb86a180331ec7e3eb4eeec0c3ee75c4ba5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134707037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d41ed1abc3826d1b6a81a69724f3584e7ac35ce2267f89b26d9b263c821127`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:15:54 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:15:54 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:15:54 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:15:54 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:15:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b9dab28a830f0b4a3bdf41601f05be703a34739d12c3908b207a74a96c78fa`  
		Last Modified: Fri, 03 Apr 2026 17:16:12 GMT  
		Size: 81.8 MB (81765662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f52f50cd9ac3193832d57c78c6a01d9c8e91c5d8aa40fdc62314f1dec01dcb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a3f184e5b72f43466c32b4fe7e4b7a12b83ed6c98155fb57af041de23a027d`

```dockerfile
```

-	Layers:
	-	`sha256:2327678c90d1e8d3876eee6d2ab2191e7ae613ba7a8d8aae08270b0442feb045`  
		Last Modified: Fri, 03 Apr 2026 17:16:10 GMT  
		Size: 5.2 MB (5181754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a9894e8c5df99456d0240e38569db2bc67cfa1d5ca0597e4d2460d9b4a2133`  
		Last Modified: Fri, 03 Apr 2026 17:16:09 GMT  
		Size: 9.0 KB (8957 bytes)  
		MIME: application/vnd.in-toto+json
