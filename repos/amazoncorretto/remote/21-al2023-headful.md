## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:9494c68f5023c35581544324dfde2b5edc35f668c4c0d41a64b58d4097c2bdd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2e28ae7c808607c792013d45d38ae308ca30f402c6071b230a6af594a615e44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142612093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc13f2b39d93a7d95f2931b849c52860298f6ba06a0b71c4df1ddff133483007`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b496102f35925938ed2bf2a60201103bb883a0f869ab47e8b90e706ed58e39f5`  
		Last Modified: Thu, 25 Jul 2024 21:02:18 GMT  
		Size: 90.3 MB (90297914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:023e69f9562ab32d8b7ef708ca9fa7d6d4ed591f939106bda968093d48a501ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6fe81faec0cf139c7dcdf12750721ae9a2b3e9239d3c87aba33cf615d3abd2`

```dockerfile
```

-	Layers:
	-	`sha256:f1f8bee2cc3c32cf451c038863589421a5e64d28ff758a8cca6ec26811d64bb5`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 5.2 MB (5210076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd9be5658c055254b8a1ea81a6a6bf294df8cdecb4434cbd129f9f30b35af91`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 8.9 KB (8893 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9472a0eb321c8ff61b8835aa8b31100296300a92f5c4b7bbf6bae494e458b2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140754281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4462bc168cf1e5f92e44fe5143f95cc8c0033ef6cf70fc9d4be0bf3fc6050ddb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:69f1520adb0e35dcf91717c80b7867ab26fcf8ef8506b9831fcca72a1b38b618`  
		Last Modified: Tue, 23 Jul 2024 01:08:54 GMT  
		Size: 51.4 MB (51402016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8fd16ef06ee0a748ef98ccefc90b68a050a9d94d91a4fea54fc4f663bb7c9d`  
		Last Modified: Fri, 26 Jul 2024 02:04:48 GMT  
		Size: 89.4 MB (89352265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f10e32624d10fd0e4912d89b67af85c389839a3ca0a8eec17271621e243f03c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f9bd58d3f2cb7cd39a85c0993bc0c40e5416ea312ccc5e1b4331664a3da861`

```dockerfile
```

-	Layers:
	-	`sha256:6eecb70fa92ba350b7e0b69e6641b7fb84db818652b37b58de7307af38abd805`  
		Last Modified: Fri, 26 Jul 2024 02:04:46 GMT  
		Size: 5.2 MB (5208867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:735c243bf09a8a0419ff1f222049047db309091d2a476c308841d0dea1ca9de0`  
		Last Modified: Fri, 26 Jul 2024 02:04:46 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.in-toto+json
