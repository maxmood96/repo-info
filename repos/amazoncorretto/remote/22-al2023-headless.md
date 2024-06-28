## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:32a1bc8ee1ca2603dd14afbfaff8e1f7b3971c8960d8951f928c7d0981cceaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:df20b8d1bc335d08cd8d005f0856b5b35831cccf4f9cfbd155ce80b64b6a4a4c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140919041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e54cf5f13a5e937025e8e859a951643cc8e54fb4a352a827b308cad309a84d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:35 GMT
COPY dir:e6df6db8aef540204b86452a41cadd353e4d48e223134b5e21dfa05ef97e1d88 in / 
# Fri, 28 Jun 2024 00:19:35 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:16:06 GMT
ARG version=22.0.1.8-1
# Fri, 28 Jun 2024 01:16:06 GMT
ARG package_version=1
# Fri, 28 Jun 2024 01:17:22 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:17:23 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:17:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:81678b13f6c636072eda0120bcac08ba9702bd3303e400ae3c7400ab681bbeb3`  
		Last Modified: Fri, 28 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bdf9a267f871c03b0fe8bcde2eba078aabb078415fbfeca965a276381bd4d65`  
		Last Modified: Fri, 28 Jun 2024 01:27:59 GMT  
		Size: 88.6 MB (88599268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:61ae8cad5a2cf61597d232843d5b178fc444fb62bcaf57f45c3213783be308fe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138964031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91436b08abc787f736f909dcaa25b423f198ac3f08259e1817f3657d2c35ee8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:39:45 GMT
COPY dir:e916198a9a0937e23f608a553229a3149679983e31d80cb67d2ef3b5d0279cb6 in / 
# Fri, 28 Jun 2024 00:39:45 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:23:10 GMT
ARG version=22.0.1.8-1
# Fri, 28 Jun 2024 01:23:10 GMT
ARG package_version=1
# Fri, 28 Jun 2024 01:23:58 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:23:59 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:23:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:5e58b9ea919d57f6ca8b1b6a0eab735cb9ec385acc5ae1ab6fb46c492771cb2c`  
		Last Modified: Fri, 28 Jun 2024 00:40:19 GMT  
		Size: 51.4 MB (51407100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652fdcd898abee8a2462272439f9d9ea35ba8ae222868bb7d96888382409b8a0`  
		Last Modified: Fri, 28 Jun 2024 01:32:50 GMT  
		Size: 87.6 MB (87556931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
