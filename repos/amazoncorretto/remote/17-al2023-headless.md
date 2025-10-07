## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:cc9aa22edb27353414af68dc851f1d6fefbb66e4c48e75275c886ad9d888e670
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1d10b05bc9ec08dc267162646ccd1c81a8e6a8f013dad0fea20cca50937d447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136333594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c7c3c5bbddab10d7f4f1294ea12e584e885722c7b13b5b8092205a43150041`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2c40df73655937de08a4d687f05cc07c2787631ec026c6d9492dd66c410a33`  
		Last Modified: Mon, 06 Oct 2025 21:12:14 GMT  
		Size: 82.3 MB (82328463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0e2d3dad8bb28f4d1b0c97cc73fd30c32842dd51f1c848de377ef96a64c7bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7f586677823c39783cdcc3becbfc2baa409e746c618b47de20f904427b8b48`

```dockerfile
```

-	Layers:
	-	`sha256:69fba64024490ee1d20f657d5f16d73f13fb23b6d18baa900458bb4d40757983`  
		Last Modified: Tue, 07 Oct 2025 00:49:19 GMT  
		Size: 5.2 MB (5182816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa02ec4e5555a7b89a902e33f807a38c357c98df984651e7b8b084224a7d6dd`  
		Last Modified: Tue, 07 Oct 2025 00:49:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d8f72d6752523defd20679afebf1bc19ed066d0ad496645f052ba9f1435329e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134640044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6906cd429612b110add8f6b84680f72c7b16dd6c6bf0881f2e1ba720ab0d10ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb76deb5d0021ee30b60db09955b9289c4b7230de78a2ca2d82773b642e3f1ae`  
		Last Modified: Tue, 07 Oct 2025 00:52:32 GMT  
		Size: 81.7 MB (81748841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b382e1009a25abce31910bf79cecc650def91d6f5903fc77807433a04a822c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f75d73fdab304b562d1eb0a6087ab5358aaf52e4ed23f129b1463669911ba65`

```dockerfile
```

-	Layers:
	-	`sha256:b9600d9f37c267d3fc0d503fe6417bc5dcab51db16de803a420e50e682f4f589`  
		Last Modified: Tue, 07 Oct 2025 00:49:24 GMT  
		Size: 5.2 MB (5181604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c239af0ab587a381483207ff4949897d78d49182f5263740bb640aada338f57e`  
		Last Modified: Tue, 07 Oct 2025 00:49:25 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
