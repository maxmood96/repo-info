## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:435da00e2ad4dc5702911a17fff707747f5e40ee0fc0df145b5a85367df0a061
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7b0f3dda708cafa2db83bb411d5798610b692d95a30cf5fe1babdaf5ce41b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145416961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb6d9deda938828fc45fabd9f82af5b3318dec9ca275e9b22eb1d28a0dc6beb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35755d8f66ac15027316dda0745f0f2a20d833b3c053bb1fa52c4c9be5aeb4c`  
		Last Modified: Mon, 21 Oct 2024 18:57:18 GMT  
		Size: 93.1 MB (93073129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a038600b2f2650cb4c6fc4e0a8af1b895399ffe2df56c405be184a6293ab0fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c0117314cdb60612dd3ca0d6322dc6a519c8d6c812d5552c4cee8fcb496df4`

```dockerfile
```

-	Layers:
	-	`sha256:0c69b14fd24a8d6e5a750b3c6f2649dc459d9070d2a4992494bab483c49c7acc`  
		Last Modified: Mon, 21 Oct 2024 18:57:15 GMT  
		Size: 5.2 MB (5188973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37989e0b334e0fce81778363e7abd624e75eb634e90753599dd9d0176b015c46`  
		Last Modified: Mon, 21 Oct 2024 18:57:14 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d31f95c74ac3114fdbfbdcc20994b825fcd9e3f008ebb5d1c87854cf6904bfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143470516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c9b34c308746ce756894cbc9f14a5d2e626e7ae816145f80bff554e546060`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0975d76ffd1599a89e2b8c2b243284961af4996625256fdfbefe803ad1e6aa9`  
		Last Modified: Mon, 21 Oct 2024 21:07:40 GMT  
		Size: 92.0 MB (92045989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c27b236950dcc99dbf8ac12e489a469e97ac38ee0fe7ae5f359bbb8a943bede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4044fba7fc29ca1cfb344887b0744f307e82c2ccc391f61001f30f35b09b5289`

```dockerfile
```

-	Layers:
	-	`sha256:1aa7f2a56106486c78306bbe5ae9eb2112d3c5d76d2288bca2f42b4d2b9cac7d`  
		Last Modified: Mon, 21 Oct 2024 21:07:38 GMT  
		Size: 5.2 MB (5186959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309c9a5132f6fcd9451698480bb8a3234075f6f7d981c3204fc098f7436a62d7`  
		Last Modified: Mon, 21 Oct 2024 21:07:37 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.in-toto+json
