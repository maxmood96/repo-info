## `amazoncorretto:24-headful`

```console
$ docker pull amazoncorretto@sha256:1252938e2bc79ac71d4986df590a76c3b0b663db729e4a97bd919d1035b5c9cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cafde2e3305db7a67997c40619e33a2d8ecd2d4cf8c0822696dded9ca907a4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157169381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a02018d8d4060ba85f7ecc1865e56f2160c46aa7216aa0ba141b405bcea523d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef46825c613d2a0d047f4e1297eb26efc7313ed193f7576fc7492961a63515a`  
		Last Modified: Thu, 25 Sep 2025 02:17:13 GMT  
		Size: 103.2 MB (103164101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2abae3781b6a173044c49d2b8afd72c49756e4584a91cc6b7613fc78d3f42dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ad8dfb8bf6dfdc978f8098bc953fc75dcca6b2acc0e3ef5aec922fd0deb176`

```dockerfile
```

-	Layers:
	-	`sha256:06fa618421657448a3d307e20aaac252bae4003f619bac17289bebde4c5f3ecc`  
		Last Modified: Thu, 25 Sep 2025 03:51:09 GMT  
		Size: 5.2 MB (5220128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9a25768ad76cb49346e9102ddc3857c748a4a8579d5c9934086ca2236893b8`  
		Last Modified: Thu, 25 Sep 2025 03:51:10 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:afeff3cc75df6f7ba2c3928d46c521c61f7a0916b60f069bf1eccdfc38e37cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155075915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1383537f90ca566bfdb9a5b945d2d7c5a76df6098e81ae1f28a659cfdb735d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcde7b9793da81d7ead0fdd942e7837863a7f638b53bebf1a1770065ec0d538`  
		Last Modified: Wed, 24 Sep 2025 21:14:23 GMT  
		Size: 102.2 MB (102176477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73df385b828a247e5c5286f8cc28e2023d44261dff2b393b3a8623d6cc4af2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4fd8a79b9b55f098a605a0b52f77765f032efe936303641aa7c66011f56e78`

```dockerfile
```

-	Layers:
	-	`sha256:00c2d547bea2cf3d4f02023f295bbc1105a118a7e8f6dacd7d7e7459c4fa6fca`  
		Last Modified: Thu, 25 Sep 2025 03:51:15 GMT  
		Size: 5.2 MB (5218942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb42cb3a3eb77cd6e558baf0beaac913aa2e2bed933d1b6483fae0a9a93c2d87`  
		Last Modified: Thu, 25 Sep 2025 03:51:16 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.in-toto+json
