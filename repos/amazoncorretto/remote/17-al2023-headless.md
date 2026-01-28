## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:1dc1e3e95d98526489eb3f529ed624a3dd920b12927d4ce0f8395a06447c64a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:43a6b9b4601d0b0392e6dee53d5ecf9e6f5c3e950010fc64659adae12cff93d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136382896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e694c42ace33d280c7c544cfda652db280c61265850140b62eb8a0a0593e932f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:08:02 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:08:02 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:08:02 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:08:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:08:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3982db546e33a1fa42d818bfb16fc08d7bffb3ae5e6a6f63ad73466c19bf98`  
		Last Modified: Wed, 28 Jan 2026 04:08:21 GMT  
		Size: 82.4 MB (82359060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b749acf52ef9a800fcae13cb20d7d9dfe3c948384f72823345d8fa46f1be4dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b538f971e41f8b4dadffb98d0cd4b45a55d7638399ed081d4451eedb8151eb`

```dockerfile
```

-	Layers:
	-	`sha256:c4df5b8f6f949b50df8bc9c96dd2f5c36e201b6d372c2db801dd26e64f3fc80b`  
		Last Modified: Wed, 28 Jan 2026 04:08:19 GMT  
		Size: 5.2 MB (5182896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4bb510ae7f87b5ef841701eda89d4ad8198edba487e52124288814c18c11638`  
		Last Modified: Wed, 28 Jan 2026 04:08:18 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:891768f34cf823c46f82ab637b7b3ebb503c0af6a6faca0ad8d2a1d68c9b26f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10c2dc45f7e30024717802cf9a3ef334f4d6c38584926134b871d731ffef64a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:28:46 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:28:46 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:28:46 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:28:46 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:28:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84849b171b6ad7133d50a1aabab0e99d9071174bbfde45907cdb917658ed275`  
		Last Modified: Wed, 28 Jan 2026 04:29:04 GMT  
		Size: 81.8 MB (81764901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40173b17ed98e9bc4f1571977fa640397748db2e946ab78e06b6e48da79ac75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59da7b27f83191a480ba911457c63588f9ca0c78d21b4963a81f460b0be279cc`

```dockerfile
```

-	Layers:
	-	`sha256:60bf4da873ef79c81c39f77d3d10b8a87807bf422cf03e17dade8b9016e67513`  
		Last Modified: Wed, 28 Jan 2026 04:29:02 GMT  
		Size: 5.2 MB (5181684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd80f95f076289153892c8f2c6c8de8804fa60e94828fcae33b948487ede7499`  
		Last Modified: Wed, 28 Jan 2026 04:29:01 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json
