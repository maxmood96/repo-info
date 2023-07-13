## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:9c9520050d143e553fc6ed839f05cbb154b2b27f6a2bdcaa6e81278b8cc1ee83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:65eb6ac7f22d300a1c442943101aba87b0cf8a139ddc436401ce553fa86d02b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128160040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30794ad31032c5428c0df5884f91ccc6656a63e22661990dfc7a3870b8362e06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 01:19:51 GMT
COPY dir:6bcf60f30d73b947ca07a9033109632c5faea18ed42743e2d6374e73b77d7d3a in / 
# Thu, 13 Jul 2023 01:19:51 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:40:26 GMT
ARG version=11.0.19.7-1
# Thu, 13 Jul 2023 01:41:04 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 13 Jul 2023 01:41:04 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:41:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3b8efe8e8a66806c25259c3f18e066eaef344018f8fb28a90db73bb2c2379601`  
		Last Modified: Fri, 07 Jul 2023 03:04:17 GMT  
		Size: 52.3 MB (52314023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0930224145f16b3337a65713ae9ef70451b30a59cdb0dd0a26a3f8a49d2436c8`  
		Last Modified: Thu, 13 Jul 2023 01:51:42 GMT  
		Size: 75.8 MB (75846017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:44fe1f7420a667e0f899a06d12ca55db8ccdd9afece4037732c5814aa2479f9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126383999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079c33d21fec0044586a8536e0196950aac356024c4319dcfd8d44da93b989a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 00:39:43 GMT
COPY dir:c971849a42f287ec4e3f54148631542a63e55183107bf0088e1c6913d556d33d in / 
# Thu, 13 Jul 2023 00:39:43 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:06:13 GMT
ARG version=11.0.19.7-1
# Thu, 13 Jul 2023 01:06:48 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 13 Jul 2023 01:06:49 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:06:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8df4f3b6d932cf6e3c467c8f32011fb41de2120bd82bf33f3469b54bbc38d5c5`  
		Last Modified: Fri, 07 Jul 2023 03:06:46 GMT  
		Size: 51.4 MB (51360865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcc1ff6331729f7a0153cc818274b1a47a1f822d8ff425b074fc649f5fbd207`  
		Last Modified: Thu, 13 Jul 2023 01:15:01 GMT  
		Size: 75.0 MB (75023134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
