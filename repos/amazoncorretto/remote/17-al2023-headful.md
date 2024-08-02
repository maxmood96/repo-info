## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:33f0b30370d562b7fd5adca50c62d7bd99da51db92c74f1a0f7b3455c205eecb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be2d6b54ad1603dd291780f8e59fd944e822b2295a13dc6418a78d1fdf6fa0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135438676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2c35a736aaaea44ff502407784f7260e62898ecf5d3b3216f0883867538e36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:cb6230c89c15ad3884b7222b06322338ef758165e0b4068d1270a3c8141a3e43`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 52.3 MB (52313926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f432582fc1201b7bbbccc20a23df141bcc6c93ccd87c6601fbb541af1805bc2`  
		Last Modified: Fri, 02 Aug 2024 14:55:10 GMT  
		Size: 83.1 MB (83124750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8953b528bfa7fd1aa59f77a7eac44391e7fb37fdf6207a21f61ee0489a87ccaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f330187b3fdde0f150c95797d5b3bd6775c5605405a6da56648b13659c6f76`

```dockerfile
```

-	Layers:
	-	`sha256:c40f4c857457edbbb12ff1b41981aa78ea69f7a16cfcffa950c4392d069d6b17`  
		Last Modified: Fri, 02 Aug 2024 14:55:09 GMT  
		Size: 5.2 MB (5208710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce4f5f26c2cff2475fd20c30f2dfcdb00a798d5e0baab37d3fa5577dd9be6ce`  
		Last Modified: Fri, 02 Aug 2024 14:55:09 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8640cbc587778ef852eb39da1041c1d071f06f3713305fd8390db03b91d9d938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133852153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea00c7d7362c57ada869705582d17907c5932cfdaa5f8dc3864f053cf98d934`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e9a36a4a60f0d38a6d8a27b903506a10c95c2da2b94bbb5bc16c52025a0938`  
		Last Modified: Fri, 02 Aug 2024 05:47:39 GMT  
		Size: 82.5 MB (82450141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d798dc3277c930cc522b8293b3168460db14735ef95f832f0c086fdaf1e4690c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d016a682117c9faa650d742eb6d971746b2ab74f6ff7c433bebf07042abe5657`

```dockerfile
```

-	Layers:
	-	`sha256:8ea94cfa696dd35c1bb9bb5ada28966fc826db83af5370ab5a04260dff7ef22a`  
		Last Modified: Fri, 02 Aug 2024 05:47:37 GMT  
		Size: 5.2 MB (5207498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17751459516631e5c293e5a0e09cce6973c81e49a990752202f12d237d29b30b`  
		Last Modified: Fri, 02 Aug 2024 05:47:36 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.in-toto+json
