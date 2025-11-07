## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6905365ce0fcab63f55e1578fb6426fce901f9c923886933588a8bb9c5551711
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:26467dabb88e6641acce930cc216581904c2c713050debdceb692aedb2265a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137118715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e1ff54da55881e2fe26b7fee3dfcf9222c2d91a4840162d22e0ec103f4c5da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:06 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 23:12:06 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:06 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:06 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4faf0d14d6e12eed93fd56a69e16b776b64ec31cb29dc70cc2364383b7b6a6a7`  
		Last Modified: Thu, 06 Nov 2025 23:12:36 GMT  
		Size: 83.1 MB (83118212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f787b5b565e20d1905204eee39e124302b7ae8d369f1713e3e1558463f817076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94938219eaf45faaaaf4942fa70ee20542fc4e02d5069f1793b42894f988d671`

```dockerfile
```

-	Layers:
	-	`sha256:0770f77f9cbc4e50f3fc7f26941c5cbe62bff3d3c5652d05d8386526a5a0e9f3`  
		Last Modified: Fri, 07 Nov 2025 01:49:19 GMT  
		Size: 5.2 MB (5208327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e051eb541ea1be6f2e2a19f6e37b034623ca90b2c73b45903e0ad84553a418e`  
		Last Modified: Fri, 07 Nov 2025 01:49:20 GMT  
		Size: 8.9 KB (8892 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ec9b47d7275b39b943ba430ecfb1fee98a0bba539f732b5fedec794f56c2abe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135436502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6edf071acf1515813a6e47ee6134f6f14f00f2bc80b5e30bd10566c3b094a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:26 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:13:26 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:13:26 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:13:26 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50d2d20daf1fd79b491d6a8de1d5f082273a51b8361b701406581f29db0bc6e`  
		Last Modified: Thu, 06 Nov 2025 22:14:06 GMT  
		Size: 82.5 MB (82534818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ea5baec65f2f6bc0bea7579f1d5e5a6e517fb0ad464582e86a2c0f5fcab9f698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f77ee15cd9b6fac5b2db1d4f96a59138198d2db8d61e0e70e9a297234e1b65`

```dockerfile
```

-	Layers:
	-	`sha256:9e0fcd9252d1344e3d7e4ce3533757bf915028908601dacf447d2f9160e50a9b`  
		Last Modified: Fri, 07 Nov 2025 01:49:26 GMT  
		Size: 5.2 MB (5207118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df48214a46f896284cbb356d2f419138e256b253e32227bd03447eca5b054ed8`  
		Last Modified: Fri, 07 Nov 2025 01:49:27 GMT  
		Size: 9.0 KB (8972 bytes)  
		MIME: application/vnd.in-toto+json
