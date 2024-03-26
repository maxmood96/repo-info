## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:73a19f6b0a643845e915d6ee4a38a68afc0e623135c17603f81da398c7ce3225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:940bb56771c6cee6ebe01e4d590ff1f9d04aa38696a0dcb898fda403fbb5509b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141649080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ba565136d6cb261c13052ee7d6bb3496a17888c32284c89e92e39e654ee383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 07:58:56 GMT
COPY dir:a3b34d0fa41c44f27db0e1cc5fb85c42e2d376f97e37c993883bc79b0ac16bdc in / 
# Sat, 16 Mar 2024 07:58:56 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 17:53:17 GMT
ARG version=22.0.0.37-1
# Tue, 26 Mar 2024 17:53:17 GMT
ARG package_version=1
# Tue, 26 Mar 2024 17:54:24 GMT
# ARGS: package_version=1 version=22.0.0.37-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Tue, 26 Mar 2024 17:54:24 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 17:54:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:47a7782bf36730e29aeeeb2bd36b1fc2a9d8b97f2ee4990a6ad2300602de69b0`  
		Last Modified: Wed, 13 Mar 2024 20:11:15 GMT  
		Size: 52.3 MB (52334338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1e7606db9936cc5ae56404faf5f7393959493201abd56233d4db6e195ca741`  
		Last Modified: Tue, 26 Mar 2024 17:58:21 GMT  
		Size: 89.3 MB (89314742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:756b7ef13fa44f9c8d447d89a36b81486d34f5e4ff11c70d4c687459c9a8e391
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139703520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c072a1d5fe6240bafaa96f58be67b554787b66db59ac7a3047643a6d5b5cf97b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:05:49 GMT
COPY dir:df28b18edcce192f5e6601a1f5352535de64369eb71fe3f006ea8b6aa29b9c84 in / 
# Sat, 16 Mar 2024 00:05:50 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 18:06:07 GMT
ARG version=22.0.0.37-1
# Tue, 26 Mar 2024 18:06:07 GMT
ARG package_version=1
# Tue, 26 Mar 2024 18:07:09 GMT
# ARGS: package_version=1 version=22.0.0.37-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Tue, 26 Mar 2024 18:07:11 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 18:07:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:dd798988746a347b32a9e843088ef9c56978b6beca831a29a02bcd2ca002cea1`  
		Last Modified: Wed, 13 Mar 2024 20:11:17 GMT  
		Size: 51.4 MB (51414586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db4be52ed07c603e3d89db2ebe80aed1e2db1e8997ac52633c289a2e8b52819`  
		Last Modified: Tue, 26 Mar 2024 18:11:20 GMT  
		Size: 88.3 MB (88288934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
