## `amazoncorretto:24-headful`

```console
$ docker pull amazoncorretto@sha256:4959c67e31c9719b390d84f0c6d3e7aad71af75d435e0711d4a7ac0ae72608e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:53cfff58e59c6128663485788257e6ab63ad363e7b13edf86737f12b963a9bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156602690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f576485fc50c7d9da4926b477c1f44a4e98366bb138a5cbd14aac0ea7d59f6e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5ec2452bbb0befb78df47c3914b76048162ddb5303ea079ce4270950b5179`  
		Last Modified: Mon, 19 May 2025 23:37:10 GMT  
		Size: 103.0 MB (102987988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6b86a7f31bd4e391a1978a5f6ba47a04bbda387d59e347ff6e284283bce2563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af097ddac6d14ac64d88181c59aced64282873b95c8de8cda617901775998724`

```dockerfile
```

-	Layers:
	-	`sha256:cd1eeb96c902c4a4fe56c15131f324e2f54b81e7e2ef4daba60111570237e080`  
		Last Modified: Tue, 20 May 2025 00:50:08 GMT  
		Size: 5.2 MB (5217811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21af1698962362db9f049e6962d34bebb04ef495697de222850c6816621d67d7`  
		Last Modified: Tue, 20 May 2025 00:50:08 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e1e4af2fac56fd4f11da5fd82b908153ff490b8a695e61948ce346873a946e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154556339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5546ab0e6bbaeb8ec82b6617fdf98d43177a94e7315ebb3f4a92ed14f3a7b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a413cf7336732e2a0c07ea910ced5fa8805da65c1c95660bf0e0db26f8867b`  
		Last Modified: Tue, 20 May 2025 00:05:37 GMT  
		Size: 102.0 MB (101990602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1795c590cc83458f7fe2599ae34c9a0012f48113f55664a51b4a79f6b7c418e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169ea7bddebdac4797063dad9bd86d08c57c0ad5a6bf09c971530d7ec6362d4b`

```dockerfile
```

-	Layers:
	-	`sha256:b198e415430cd9b01a46670630fed222b6db30a089ebb14257244d38a7366a15`  
		Last Modified: Tue, 20 May 2025 00:50:12 GMT  
		Size: 5.2 MB (5216625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f974ac46ed1c49b26b4b1c4a8b95117c174ae680863fa48bbc2808512de7d0e`  
		Last Modified: Tue, 20 May 2025 00:50:12 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
