## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6207f40bcb840db9af949815547db9e8aa30152c7b6956bd2e0f0f68fcfa8b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:89244862b2c14b861f15bc3c527b8da423464180bfdd4b2c8ae381a009038192
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142588930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e668945b8b4e8603b54573f2bf4b3acd60626e2c0251dfb7606fc857bd90331`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:35 GMT
COPY dir:e6df6db8aef540204b86452a41cadd353e4d48e223134b5e21dfa05ef97e1d88 in / 
# Fri, 28 Jun 2024 00:19:35 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:14:42 GMT
ARG version=21.0.3.9-1
# Fri, 28 Jun 2024 01:14:42 GMT
ARG package_version=1
# Fri, 28 Jun 2024 01:15:49 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:15:50 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:15:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:81678b13f6c636072eda0120bcac08ba9702bd3303e400ae3c7400ab681bbeb3`  
		Last Modified: Fri, 28 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a6abd30d38bf3011e2becffa544c1ba8e4c9dfe180528ceca35750d1abdbf9`  
		Last Modified: Fri, 28 Jun 2024 01:27:08 GMT  
		Size: 90.3 MB (90269157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1c4f5939192ea6c1799d50bbc7ada464e1b5bf418d7b63a782931b714f12a280
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140719919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4af31c8015bb01eb079899439e54b690cb3e5067184b2f0f99acdfcd5b91fa8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:39:45 GMT
COPY dir:e916198a9a0937e23f608a553229a3149679983e31d80cb67d2ef3b5d0279cb6 in / 
# Fri, 28 Jun 2024 00:39:45 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 01:21:55 GMT
ARG version=21.0.3.9-1
# Fri, 28 Jun 2024 01:21:55 GMT
ARG package_version=1
# Fri, 28 Jun 2024 01:22:58 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:23:00 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:23:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5e58b9ea919d57f6ca8b1b6a0eab735cb9ec385acc5ae1ab6fb46c492771cb2c`  
		Last Modified: Fri, 28 Jun 2024 00:40:19 GMT  
		Size: 51.4 MB (51407100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a66ab14b7c795f43a7dd5884cd8b44991eac6a6e6d157a8e37887310a671b4`  
		Last Modified: Fri, 28 Jun 2024 01:32:05 GMT  
		Size: 89.3 MB (89312819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
