## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:47b86a81a83e4c87c67475824c5d7049f6f9f114b146d20603a71ef932fd0893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:39eafc65dba4d75259fb44e2ab8bbc01fdcd13c29646889fe6f4c240e172b147
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134737211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e344746fbf150f54a0eede07104bfb3e9cdb0003313ce05ab12674eb05a37a1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:35 GMT
COPY dir:e6df6db8aef540204b86452a41cadd353e4d48e223134b5e21dfa05ef97e1d88 in / 
# Fri, 28 Jun 2024 00:19:35 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:10:41 GMT
ARG version=17.0.11.9-1
# Fri, 28 Jun 2024 01:10:42 GMT
ARG package_version=1
# Fri, 28 Jun 2024 01:11:27 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:11:28 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:11:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:81678b13f6c636072eda0120bcac08ba9702bd3303e400ae3c7400ab681bbeb3`  
		Last Modified: Fri, 28 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68754c2c3b9b7d30e35b230a3cbc5228e793fad5ec09e75844ef0a0b152e55dc`  
		Last Modified: Fri, 28 Jun 2024 01:24:18 GMT  
		Size: 82.4 MB (82417438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aec50f932bf7cf4f5310deaeb6550b7a55b51a2e08d1c94d2a20e87cb0ec7878
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133146947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6aa317e59644c6747eacc813edf7e8508e91029144854193bb3edaf50c2413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:39:45 GMT
COPY dir:e916198a9a0937e23f608a553229a3149679983e31d80cb67d2ef3b5d0279cb6 in / 
# Fri, 28 Jun 2024 00:39:45 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:18:41 GMT
ARG version=17.0.11.9-1
# Fri, 28 Jun 2024 01:18:41 GMT
ARG package_version=1
# Fri, 28 Jun 2024 01:19:19 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:19:20 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:19:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5e58b9ea919d57f6ca8b1b6a0eab735cb9ec385acc5ae1ab6fb46c492771cb2c`  
		Last Modified: Fri, 28 Jun 2024 00:40:19 GMT  
		Size: 51.4 MB (51407100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e855eda52de45d9b5b86c10d5628abff390651ab4649f20ac20802cb8f72d816`  
		Last Modified: Fri, 28 Jun 2024 01:29:34 GMT  
		Size: 81.7 MB (81739847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
