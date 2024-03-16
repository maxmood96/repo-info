## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:59eadae257ae3831970b7e2dd09d47ecd9c66ed23a4c465596b98b73d3413842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bb52c82444aec8d7e218009bce96ec384777be9751b5e8c0e55a1aef37c6dad2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134677202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e62202c0b4212f572e1fc6a59bb315b1c63bb6ef7327b217b56d8cadf3ee897`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 23:50:11 GMT
COPY dir:d7da6e069b79aa8b51b20a889b996a9bea020932e2948f46e1e355ca42d78f77 in / 
# Mon, 11 Mar 2024 23:50:12 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 02:53:22 GMT
ARG version=17.0.10.7-1
# Sat, 16 Mar 2024 02:53:22 GMT
ARG package_version=1
# Sat, 16 Mar 2024 02:54:14 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 02:54:15 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:54:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:89b8a841604356b93248cef633e19448985a8a9e86277f3b31c2e3860eabe2ad`  
		Last Modified: Wed, 06 Mar 2024 01:18:19 GMT  
		Size: 52.3 MB (52337114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab3f2efa460692b4f7587d5178fc19af1a1c2e060f44dc6a37a9e854d2516a`  
		Last Modified: Sat, 16 Mar 2024 03:11:19 GMT  
		Size: 82.3 MB (82340088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ab073ccdd96a1392a3913a2beeb822b5ce13068145722df6ac23c239194d2016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133087991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adeb2001e56929919b926413c36ad6e6dfbf7b3908cefdf86b4ad6168eeceed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:05:49 GMT
COPY dir:df28b18edcce192f5e6601a1f5352535de64369eb71fe3f006ea8b6aa29b9c84 in / 
# Sat, 16 Mar 2024 00:05:50 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:43:04 GMT
ARG version=17.0.10.7-1
# Sat, 16 Mar 2024 03:43:05 GMT
ARG package_version=1
# Sat, 16 Mar 2024 03:43:47 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 03:43:48 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:43:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:dd798988746a347b32a9e843088ef9c56978b6beca831a29a02bcd2ca002cea1`  
		Last Modified: Wed, 13 Mar 2024 20:11:17 GMT  
		Size: 51.4 MB (51414586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18ec65fa30ac9dcf4e2b3fd541170251d73455a31395a48d980197060bd551c`  
		Last Modified: Sat, 16 Mar 2024 03:57:44 GMT  
		Size: 81.7 MB (81673405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
