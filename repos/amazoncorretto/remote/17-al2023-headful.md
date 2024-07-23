## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:77ef6227c37a02c9aaefe6daf94d65b161812a9a180598e2f5682c1eb0e83a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:969f81848b11c3294bec6f8921eb9ef58c3ce271708e840e45cb4541bb07972d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135438492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5132add51ddcb3c6b764f88b2982ae5fcb6940d080ee0749b7f417a2992a3cad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Jul 2024 20:01:54 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Jul 2024 20:01:54 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f03636e672ba797137f2f72e64c7fdf7947397c0880ca5f9e9962a85462a7875`  
		Last Modified: Thu, 11 Jul 2024 02:05:27 GMT  
		Size: 52.3 MB (52313836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f4502b246777d59c10dee92d9fd0f3cf029aa50526d64e4d764b8f00d4fa0`  
		Last Modified: Tue, 23 Jul 2024 00:07:35 GMT  
		Size: 83.1 MB (83124656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:93add4407061d9e29f5f4e5abcb7774e84013e6118bed1ccf405e4d86cc89705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79c2214dfffd4bc7526a4be3013d6bef69003123f3ccb968a347aad5c257cb1`

```dockerfile
```

-	Layers:
	-	`sha256:704e3034057b17b8ce50fa54990763b0c6d734f5cb23ed46669d4aed2575ccd8`  
		Last Modified: Tue, 23 Jul 2024 00:07:34 GMT  
		Size: 5.2 MB (5207630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78927695654ab093890bdd5e91257dd034822ea360c7e703bbea85d687f97bff`  
		Last Modified: Tue, 23 Jul 2024 00:07:33 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:babaac00c4a87d7995de95e94afa5926e1f36619a35cd688e18a4d273e4bc6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133851443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b5aa2ab496f601e1846dc0e5e5c34aa4c1e74f814fdf2c9185ffd07eb51927`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a871d782436d0e8f31d42a3b5f7b153bc9596aed6bfb1e904baa659a919614`  
		Last Modified: Thu, 18 Jul 2024 01:12:44 GMT  
		Size: 82.5 MB (82450305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c620d9284672daf8ba557389d624dc30852d5570ae9b3887515577b4efb9b11d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bdd53d8272e9c729f7d907afee51419fde0f9d8fcbeb93c02525cda1078758`

```dockerfile
```

-	Layers:
	-	`sha256:2ddea54e6048c74f68b1f1dcc44daaa103b3419ff4e651d7f25269673d5a2762`  
		Last Modified: Thu, 18 Jul 2024 01:12:42 GMT  
		Size: 5.2 MB (5206418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb7e1c035b78b21cf6fa528a4243c1c798711848f07b929a2906d5299db2cf0`  
		Last Modified: Thu, 18 Jul 2024 01:12:42 GMT  
		Size: 9.0 KB (8985 bytes)  
		MIME: application/vnd.in-toto+json
