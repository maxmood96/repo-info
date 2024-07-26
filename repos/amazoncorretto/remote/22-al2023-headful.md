## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:f736d619b958f66498457548de6d1d5a0447099d8de8a088f48b7dd1f0be0708
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9717d74923307e4967a5d0441bb82ce8843418a57295e3277a7a24be85b8c270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141368659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc290e589da191f499e12b19303d25d6aa4d330d781da38f8e81ace2404ab0e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60498a819144d3dfe5fffbf1ac087a5d6d723d7404328cd44140aba86649baa3`  
		Last Modified: Thu, 25 Jul 2024 21:02:14 GMT  
		Size: 89.1 MB (89054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27cd2d197c0c0eae68df1bee39339830a1c7826fc6b25c18b6796428900ca644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fdeaaae7bd323386f7eff05674e1828193ebd85414d15edbbee8c67e789a61`

```dockerfile
```

-	Layers:
	-	`sha256:eb268ec904017d3ac05f8f8b9d068b9b02aefc424aa52bf0294a9b882b8743b3`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 5.2 MB (5211214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e254fdeee1c585da44150525fecdfe64dc14e841cac75e7fffc63a571c9b99a`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fecae1f8f9212c3503de8acff4bc5356f1b470bc75221f0b68bf3cbd3a491666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139423260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e7379a3f581cbcbe4b057b7c14a3f30a0ccb7bbfcb205d650c2d69d2aac79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626bdd6328ce27065899fc38380690a8d1b07c2928b8b1ebfd90a8b922510732`  
		Last Modified: Thu, 18 Jul 2024 01:27:54 GMT  
		Size: 88.0 MB (88022122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28b97cdb70d791a6695063d7c9353aefa674d4a62d6bbabb1bda5e1bd94f3b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5243f021caf5a25957034cf15e51a37ef1898f8dac7561ea657e8f1f7465cf`

```dockerfile
```

-	Layers:
	-	`sha256:55b214c23a63d02be4d61f1527d7f8bd53c3d3cad8db5a3419701743fc393f66`  
		Last Modified: Thu, 18 Jul 2024 01:27:52 GMT  
		Size: 5.2 MB (5209201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fadce740067b44976b8357317752ad67314b89e318df025833b75a524203ba48`  
		Last Modified: Thu, 18 Jul 2024 01:27:51 GMT  
		Size: 9.3 KB (9312 bytes)  
		MIME: application/vnd.in-toto+json
