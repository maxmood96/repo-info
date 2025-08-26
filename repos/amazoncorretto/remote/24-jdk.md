## `amazoncorretto:24-jdk`

```console
$ docker pull amazoncorretto@sha256:257f1a9dbd3b07aa5719ffaad1377fb464379e87764e695c217a8d7c2d840f49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6a99da95336d09c9a6e770440bdabd4faf1d4e1751797983f19a119db2928ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241253483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5865742c2a48af8ddbba915f30b7805caf594417e4475d43a9571411657fa6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1514838d081fb5e63a66fd4fbb6c3b2e1096e3a522459c8cef3c5e0d4069773f`  
		Last Modified: Mon, 25 Aug 2025 20:54:53 GMT  
		Size: 187.4 MB (187384753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97528d0508aed5a25f3fa0dbad5778821b47b56ce815789b511ef7564433f02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5463179e45c89f84a3b85f3dffd37d087f2f77e8cee7089e833263afa26c3ed`

```dockerfile
```

-	Layers:
	-	`sha256:6bb131cb82ad8e16867a48acc10013fa0f7938c9fd24268f82459dc7f324deaf`  
		Last Modified: Mon, 25 Aug 2025 21:49:24 GMT  
		Size: 5.3 MB (5329176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954459293bbb02790fd4e29ca2026bb5511c98edb8fd160017a853584aca802a`  
		Last Modified: Mon, 25 Aug 2025 21:49:24 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:caf4b21b6b36bc971b15f5e66293049d2b0db933a0a24fabc78b1c98f754b15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238195174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b1ca7183505aea4ece2ec6009d5165448f6808bf9a88a0c15a27e55a0d94de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:f0b7d54214a6f9c2c7698f71fb06f2128097c3f9d97269e3d449f7639c142381`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 52.8 MB (52768497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3757bcfa7490d81cf91f8e40a946b5e9b5fb6ef23be79baf6e450f183a8b11a9`  
		Last Modified: Tue, 26 Aug 2025 00:09:32 GMT  
		Size: 185.4 MB (185426677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db1753930473dd96c87d8bb519ede2081e0ae128102b5c611f5b794686429526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b774e310bbe192e4306686dcee05bf9a689105f07d9672a4a859b82b77c665`

```dockerfile
```

-	Layers:
	-	`sha256:abe563aef0a75992741c2ead924f4e04e6f958448987e1c138e1363c9895db00`  
		Last Modified: Tue, 26 Aug 2025 00:49:23 GMT  
		Size: 5.3 MB (5328144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8efbaeb0f8c969a933379dfedf1e9b30255dc9cfa12f13f2de2fc470e2f4821b`  
		Last Modified: Tue, 26 Aug 2025 00:49:24 GMT  
		Size: 10.4 KB (10355 bytes)  
		MIME: application/vnd.in-toto+json
