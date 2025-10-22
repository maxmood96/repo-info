## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:c4ac7c2033e9b978e5bec7389e9e1637b2056592d8d3c20e8a60afe7951c7bbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e387781cbb76540cc8d49fac834d12539d172b845e780d09376abcad28c24d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158343450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bddd5e2bbdbbd6cb46ba23b1cc66236662f98a252e48ee7d8013af910dd3ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:56 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:56 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8-1
# Tue, 21 Oct 2025 20:48:19 GMT
ARG package_version=1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2451a3b05a7ce769c2354350d26cb40edd3aaeb990478dbdc5b03039f34564`  
		Last Modified: Tue, 21 Oct 2025 23:28:50 GMT  
		Size: 104.3 MB (104338319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:357df4c66748e67adbcfe7ca0db328e20eaef8d84c17dd9b15a29867edaa6257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb332ec64ef02e1b9f457e5c0455a6dd9d84bd033a2d937bf383cbe2dbfa06f7`

```dockerfile
```

-	Layers:
	-	`sha256:b1390ca30445fa4e41ccaba164c8551d99a1d4e303d29cb546391da86e719e50`  
		Last Modified: Wed, 22 Oct 2025 00:53:23 GMT  
		Size: 5.2 MB (5220132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c0fe724a2bd71a0a8698ad1cea201a57394928310b63a33e768101b8dd3ead`  
		Last Modified: Wed, 22 Oct 2025 00:53:23 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1a1aa71d3d7c13d1243d32b49abb13ee82c6b335ed5b30ffb35ee96fac1db644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156175349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429beb6185f08081edc8a1c105a3bae8c4a742df990cc92008762e148bab3ec9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:59 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8-1
# Tue, 21 Oct 2025 20:48:19 GMT
ARG package_version=1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde5d5c9123bd88e19148c34b0eeb16af05560c8d205879848eff0d22248d882`  
		Last Modified: Tue, 21 Oct 2025 21:52:01 GMT  
		Size: 103.3 MB (103284146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b02e7c0717609b3b8e7ac307ff6e403bf5ad851f517f76e6b6e30ab2e4781e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e369bc3ead9b0f81b81aaa065a405c53d9ee28a9eedff85d6eb937fdeb619631`

```dockerfile
```

-	Layers:
	-	`sha256:faf6ad4ea282626c9b0bc3bc0a5290ef212949dc4b3a088427f3cc068559ef71`  
		Last Modified: Wed, 22 Oct 2025 00:53:29 GMT  
		Size: 5.2 MB (5218946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42a55128af868445d4101d8eaf026dad7d1daca6dfbce7ef9747cded287b94e`  
		Last Modified: Wed, 22 Oct 2025 00:53:29 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
