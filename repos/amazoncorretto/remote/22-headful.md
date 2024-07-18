## `amazoncorretto:22-headful`

```console
$ docker pull amazoncorretto@sha256:0048f9a4d92668d5f04b6ca6c8c20eb03ef2c67d22e279829254b2a3fefb5461
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ba779f35431558f79715ff2dea69c68891cd3af06524d1a6e88fbe4508582c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141368119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3252a2ba48e444d0010217c7da251ab95b9435b8b8aaec1601136b4c4f44add8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:19:33 GMT
COPY dir:8edd892881e79c0c11996c1a60e2c04d066537e06bdf88e1def994a6148ea23c in / 
# Thu, 11 Jul 2024 21:19:33 GMT
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
	-	`sha256:ee5ee70789863a32f444d11d47a2849acfc6089e3e8c78d196f63475ee994293`  
		Last Modified: Thu, 11 Jul 2024 21:19:58 GMT  
		Size: 52.3 MB (52313695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab27719f18036072ab240939897b7a2c536841641fa11f7b6e0b3783cb233b3`  
		Last Modified: Thu, 18 Jul 2024 00:56:12 GMT  
		Size: 89.1 MB (89054424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9c39916d62bb4d81a19306fbd6cac29b8cfb9ff493671b8e5999bfc955860135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938149f932a37ec0f01e7b0c15406645955fec6f749e131df9b27faec5e5d5ed`

```dockerfile
```

-	Layers:
	-	`sha256:9100d4c17fcf205ccb168eadedee172435553ffe0745adc0534ef27c3bc4c75a`  
		Last Modified: Thu, 18 Jul 2024 00:56:11 GMT  
		Size: 5.2 MB (5211214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac60b3219a996a8090aa4497483e8d82c9c609f671f3a75454767e08ea4544bc`  
		Last Modified: Thu, 18 Jul 2024 00:56:10 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-headful` - linux; arm64 variant v8

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

### `amazoncorretto:22-headful` - unknown; unknown

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
