## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:124bcae35eb2eab97b00dca1f31f9a89e07e6ba1f666d032848a3f3345837796
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:29ba11b55f6252d1f5bf751d464c1266c6fb82f873a0cb2a92d6a45e461aa410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141910728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efafca2b35dc3efe0f4198318aeab981f6c229064c77710e177acca6ce2ea8c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b60b6c892280988095a2507a148439d3b5fd7b108e66565a91cbdb1f0e543fa0`  
		Last Modified: Mon, 19 Aug 2024 23:08:46 GMT  
		Size: 52.3 MB (52325078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364bdbc2605e0d41ed56bcdf2773206d9f27dadcbcbbd33f9242cdb29c193388`  
		Last Modified: Fri, 23 Aug 2024 01:50:31 GMT  
		Size: 89.6 MB (89585650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cc6492b97459451cde92cf1d3bbff8fa8375a3fe09e2323950eea359a41d8b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86272d3329212aea6e96c3005e5de38efcbb68c8c6cfd31d6c806c5c65c6eb7`

```dockerfile
```

-	Layers:
	-	`sha256:0c9405bbefd1218f73dfb1a6a9a000d95e3c2d4afc33403f4b26f3e14c99d8f2`  
		Last Modified: Fri, 23 Aug 2024 01:50:30 GMT  
		Size: 5.2 MB (5186175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438ad9214b0efb7984f71da420c7bdbd842635544fe3aa2a6a30b49b88d20504`  
		Last Modified: Fri, 23 Aug 2024 01:50:29 GMT  
		Size: 8.7 KB (8714 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c53bc333973d20d7a2967ad531c6a4853fc35a509f5bf16db64c99e58aa0ef95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140037679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274c995261e4f2432598173eb9d26eef304039a21aec1ba3ca15b26fbb56b23b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c479b56f866bd8d002a18ada6876b2e4a3b28ba8c5f1eac58c8eef909e874c5b`  
		Last Modified: Fri, 23 Aug 2024 02:35:19 GMT  
		Size: 88.6 MB (88611381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9756c0f247dfaa7405e536dc3eb2527f46cce101f29b8cf540bf6b7c769e4a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:905e6ed701fba6b079380f067b985850e585cceb152436fe7ea1c863899b9162`

```dockerfile
```

-	Layers:
	-	`sha256:7e4b03e47343a9eb36e49acb5ba6357da032b27bc6786fcdb3ee1e7e7868d719`  
		Last Modified: Fri, 23 Aug 2024 02:35:17 GMT  
		Size: 5.2 MB (5184963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3b08969cbe29452507c6e7aba537088015d4d74710830f16e766737c749ff4`  
		Last Modified: Fri, 23 Aug 2024 02:35:17 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.in-toto+json
