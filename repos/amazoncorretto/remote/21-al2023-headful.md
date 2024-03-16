## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6ad343b779a6686fd86fe464ceffa5abb7bcad37bdb429ac488e28b0f2e9dee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:42876c33d3e48fed9cb777467d7a574da3817838655d3a48340d2efa816a555f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142558510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9175f0f4247895fae32bdb036b87b2427f332c7ccc3d1cad5b3504635b55fda3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 07:58:56 GMT
COPY dir:a3b34d0fa41c44f27db0e1cc5fb85c42e2d376f97e37c993883bc79b0ac16bdc in / 
# Sat, 16 Mar 2024 07:58:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:41:53 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 13:41:53 GMT
ARG package_version=1
# Sat, 16 Mar 2024 13:42:59 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 13:42:59 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:42:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:47a7782bf36730e29aeeeb2bd36b1fc2a9d8b97f2ee4990a6ad2300602de69b0`  
		Last Modified: Wed, 13 Mar 2024 20:11:15 GMT  
		Size: 52.3 MB (52334338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf8570f3057ae8f1ea5eae8b7f68569004cf23af13808117e85e4aff0a523ff`  
		Last Modified: Sat, 16 Mar 2024 13:52:13 GMT  
		Size: 90.2 MB (90224172 bytes)  
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
