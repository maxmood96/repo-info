## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:bf67cc69c9cb9edd3bfc97f670e8ae6fa38c3afc3b939bef5d64270312666e8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f4c71d0ad74fed8ec68ee253834b85200961614e79d5c615b1d19234455f33f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156296231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cca33339db97816c12e5bf98366244088e1d0f241cafcd44e08ca1aa16594c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb06a3d0464fd8eaaf16e694314b4ca4ebc4a2c76b5eb249bda87f0e19e17032`  
		Last Modified: Mon, 25 Aug 2025 20:18:59 GMT  
		Size: 102.4 MB (102427501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2d1bbf0ff33e5b4b006c71c1c8d845eb6aa63678d0529b0353358d5312cf2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c986c4abbdcf619318835259fa8671e07280ff24f8a7690666230cdc94cf32`

```dockerfile
```

-	Layers:
	-	`sha256:f6f851ea0ec16d3dc35bad2537c87437bd075900e9689ac659bf28d91d23a93e`  
		Last Modified: Mon, 25 Aug 2025 21:49:31 GMT  
		Size: 5.2 MB (5194701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e936efb93734908f6d82b0539cf9e1585056e82dfc99e786d4b7ad0c1d9e19d`  
		Last Modified: Mon, 25 Aug 2025 21:49:32 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8d1539e4af7ef9e0fb5d1902ccdfe0d333a302d0729b67e3e4575ae9ed7d412e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154213795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70750f5cd6e9b2ac8fa67df1923099244489c38fc20e6df5a44fe906a67458d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:f0b7d54214a6f9c2c7698f71fb06f2128097c3f9d97269e3d449f7639c142381`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 52.8 MB (52768497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a7fd396baf7af17584aad5afed98b854bd4be4fc2559923bb309037e716946`  
		Last Modified: Mon, 25 Aug 2025 22:26:57 GMT  
		Size: 101.4 MB (101445298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8af8829fb4b8cbd89a3927dc42d8d5532444e1d71d34c6b136931c5376856d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feeeda1609da6f31b3936622213e60e60c2c63163b5dd23bd34e0c50393a232f`

```dockerfile
```

-	Layers:
	-	`sha256:6524baba1bae2ea0d44e6c6fa9ce3e938e8394e1ebbec938df913474b87dbbed`  
		Last Modified: Tue, 26 Aug 2025 00:49:33 GMT  
		Size: 5.2 MB (5193512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cb5999cb722ae1ce6a83f5c73cc2b59f7656a8c18ab183f2408a3a587938b9a`  
		Last Modified: Tue, 26 Aug 2025 00:49:34 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
