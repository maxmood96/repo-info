## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:be8effafc4e1dc44ddf2927c6828a9277aa9134f45e1b2b44b9cd3f2b002e402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9717d74923307e4967a5d0441bb82ce8843418a57295e3277a7a24be85b8c270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141368659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc290e589da191f499e12b19303d25d6aa4d330d781da38f8e81ace2404ab0e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60498a819144d3dfe5fffbf1ac087a5d6d723d7404328cd44140aba86649baa3`  
		Last Modified: Thu, 25 Jul 2024 21:02:14 GMT  
		Size: 89.1 MB (89054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27cd2d197c0c0eae68df1bee39339830a1c7826fc6b25c18b6796428900ca644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fdeaaae7bd323386f7eff05674e1828193ebd85414d15edbbee8c67e789a61`

```dockerfile
```

-	Layers:
	-	`sha256:eb268ec904017d3ac05f8f8b9d068b9b02aefc424aa52bf0294a9b882b8743b3`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 5.2 MB (5211214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e254fdeee1c585da44150525fecdfe64dc14e841cac75e7fffc63a571c9b99a`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2f363af6678faed595786c3cfcb5bc605535595feb8e09ac3e4defe044e670e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139424080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb82e2f993d68325c7bb337b30f437d215b2651970f8a00f073ea53df1646ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e62da9c23f6c2bc63e5e53d65284a42bd5bdb7038cd9e7f242023ff4ff0a18`  
		Last Modified: Fri, 02 Aug 2024 05:53:02 GMT  
		Size: 88.0 MB (88022068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e60bfd0aff791e732793aa567a97d71eafca80770586f5a5ae63b9b4da3a0858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d487d50071c5970df7b6e471d5be6335906aaac7fc72e477e3ab788099563f`

```dockerfile
```

-	Layers:
	-	`sha256:8d37fb0056bdce8a04144f83033946bc7ebc0b57863efc09e3a1aeb2051ed307`  
		Last Modified: Fri, 02 Aug 2024 05:53:00 GMT  
		Size: 5.2 MB (5210281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6ed6324189ebf47e9eb3f2edfce532fc7fac6125482d0f87fb96a6f1717182`  
		Last Modified: Fri, 02 Aug 2024 05:52:59 GMT  
		Size: 9.6 KB (9588 bytes)  
		MIME: application/vnd.in-toto+json
