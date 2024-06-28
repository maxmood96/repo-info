## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5ea5f073f2a9208a4775676de070f5676d38e757c724d30aca82c260c013f973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1bbb20902a134d10ffa5387de727e55743ab341ca805e20f0a04343c3e7fdb0b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141881872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b575f1527b3c8c13c55dc3daa17b42472fbbb49bffb6f49795d263b6818ced37`
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
# Fri, 28 Jun 2024 01:15:28 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:15:29 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:15:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:81678b13f6c636072eda0120bcac08ba9702bd3303e400ae3c7400ab681bbeb3`  
		Last Modified: Fri, 28 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e0aab3a259256260410a0e0816208574165164739b4e570f1eb091eeae93bc`  
		Last Modified: Fri, 28 Jun 2024 01:26:50 GMT  
		Size: 89.6 MB (89562099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c2a597c7daa92771f58f646dc14cd6bbd869e6885d29e4326913f8d1a97e31ca
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139995101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24769f0388de4d06f312900ef00ce1bb5cd69b8eab570a87eebb58c3da1207c0`
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
# Fri, 28 Jun 2024 01:22:38 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 28 Jun 2024 01:22:39 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jun 2024 01:22:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5e58b9ea919d57f6ca8b1b6a0eab735cb9ec385acc5ae1ab6fb46c492771cb2c`  
		Last Modified: Fri, 28 Jun 2024 00:40:19 GMT  
		Size: 51.4 MB (51407100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8d38e31c24bce4138f78dc41f8c17cca0036606b6cd3a47435631f1641fd71`  
		Last Modified: Fri, 28 Jun 2024 01:31:49 GMT  
		Size: 88.6 MB (88588001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
