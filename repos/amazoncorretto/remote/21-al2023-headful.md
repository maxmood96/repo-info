## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:34ae9cde37c4fe692c3670f3e73549c6a3df53c56f5aea2d1a9417b86e85015e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2852fc69b0574355ba6ec812bd28a914f562115a69e20bb56c442251a80df96e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142564957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fff3fe6055b9f48bff220602c3752d7f879af61bb4cf5a55f45db06a7f4b87e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 23:50:11 GMT
COPY dir:d7da6e069b79aa8b51b20a889b996a9bea020932e2948f46e1e355ca42d78f77 in / 
# Mon, 11 Mar 2024 23:50:12 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 02:58:24 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 02:58:24 GMT
ARG package_version=1
# Sat, 16 Mar 2024 02:59:32 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 02:59:33 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:59:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:89b8a841604356b93248cef633e19448985a8a9e86277f3b31c2e3860eabe2ad`  
		Last Modified: Wed, 06 Mar 2024 01:18:19 GMT  
		Size: 52.3 MB (52337114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4323ca6dcaee391a043f1ea1860c4f50902bfc95abb96176f7bffebbd0dc32ba`  
		Last Modified: Sat, 16 Mar 2024 03:16:08 GMT  
		Size: 90.2 MB (90227843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2887d739ff5727d680eca798fed274131484ed2a6fbc337c286ea436fedf4f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140724385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbccbfee007b7d5d9a42d730b63eb2304cc000b6ae9271f978d4ebe426eea66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:05:49 GMT
COPY dir:df28b18edcce192f5e6601a1f5352535de64369eb71fe3f006ea8b6aa29b9c84 in / 
# Sat, 16 Mar 2024 00:05:50 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:46:56 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 03:46:56 GMT
ARG package_version=1
# Sat, 16 Mar 2024 03:47:57 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 03:47:59 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:47:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:dd798988746a347b32a9e843088ef9c56978b6beca831a29a02bcd2ca002cea1`  
		Last Modified: Wed, 13 Mar 2024 20:11:17 GMT  
		Size: 51.4 MB (51414586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2166fbeac9ba80edf9dfac13b1a3a9b18df63807ebed266b9ac49345761c45a5`  
		Last Modified: Sat, 16 Mar 2024 04:01:56 GMT  
		Size: 89.3 MB (89309799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
