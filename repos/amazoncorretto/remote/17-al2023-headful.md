## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:98f191e724d855dcfbc7924e5c25b886674702beaa767bc0bea2c47902688854
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5c7eaa6eacfa31508cc98e22818d07750903017c936ca5efff3dea93c3c67377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135184109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e118933b5d6c4160847ed26fb66232c24d051ae729a1c857bc42602f4eca1150`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:46453255c2f610c1cb9c8197635e6d542bbd326425a9898df0de76e5bb566461`  
		Last Modified: Thu, 14 Nov 2024 23:11:22 GMT  
		Size: 52.4 MB (52379519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3273880bf88e1370087b0564375803f6b06b3460be94f295f39aa16f5fb4c427`  
		Last Modified: Sat, 16 Nov 2024 00:48:03 GMT  
		Size: 82.8 MB (82804590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d93c27dff00d994ff703b1923a99c56384682f50db1ea2a41007819a857fd2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dd071cfceaeee97f3f56113d556ab3c47ffe0b376c788126e6ba8d5ca6ff9c`

```dockerfile
```

-	Layers:
	-	`sha256:dba5e2c6a2dbf3cdb0d32b363e6bc66d3f3f65242d6056cea363870eb6bbe294`  
		Last Modified: Sat, 16 Nov 2024 00:48:02 GMT  
		Size: 5.2 MB (5209860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e4c997468f4f186decc2c534a9c072e3dc2edc3200b3c88bebf8c07fd0f1289`  
		Last Modified: Sat, 16 Nov 2024 00:48:02 GMT  
		Size: 8.9 KB (8935 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3f97097b8081536c78c42a6bc169aa5a0e018ecac5b470f5c629ba965fff1ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133664886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4df17aec7650e5fffbeedefd1194dd4917033d953401233bbfb3de679440d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:aa4cd91a180503f7c5ac34b85fdd22c27356599a1d700f978c6d2fa5858867fd`  
		Last Modified: Fri, 15 Nov 2024 02:20:08 GMT  
		Size: 51.5 MB (51456561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213f9e982778cd85d3245f65ca2d7850d86af3f8a2c5685d882dc02e930066b5`  
		Last Modified: Sat, 16 Nov 2024 01:01:14 GMT  
		Size: 82.2 MB (82208325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7654cc7e83e15eb8e6f1133be3ebca14784d3bc5676c8e48fec1e68c53616bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d6968c1894099febbc8184aab0198f142bab3763c799413df204720f4043b`

```dockerfile
```

-	Layers:
	-	`sha256:dfc81bed4603ac23798eda3528687caaf65e63776dd0bdfb5f82d0d80feab611`  
		Last Modified: Sat, 16 Nov 2024 01:01:10 GMT  
		Size: 5.2 MB (5208649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d8b609330dcae4e65d9a62575fc0e59aa83437b9ee4d6267ccd3de8789d4c31`  
		Last Modified: Sat, 16 Nov 2024 01:01:10 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.in-toto+json
