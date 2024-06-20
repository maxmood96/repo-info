## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e023ef9c685a8d05648c054fb05e48608e90dd1b90173c87c8ccc34cb4d87004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e6dc5f228ac8ab3900e6f38312bd61833bf2f9b10b06d08c57734c54b55c80b2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141627480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5423db9bb66701be96243f1ba72c3a1152d79308106dfead268e3611ad66c274`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:08 GMT
COPY dir:1a64694c076f4e5a1aad0a3ea24080e6520840f532ade5fd6b4f5f6a7cd949b9 in / 
# Thu, 20 Jun 2024 17:20:09 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:53:17 GMT
ARG version=22.0.1.8-1
# Thu, 20 Jun 2024 17:53:18 GMT
ARG package_version=1
# Thu, 20 Jun 2024 17:54:41 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 17:54:41 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:54:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7e582939a50b073a670e38ceb36c4598b61fce79b12e6021b137c4dcc465cd`  
		Last Modified: Thu, 20 Jun 2024 18:26:21 GMT  
		Size: 89.3 MB (89307967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:814ae6a766e8b36e9af0f51cce427f7c3113c979b9a36dcc5ac6c84606b8a7f5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139674163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a269db82de973f9765ef2f43db62f0f25e42811978da5cd76afedb3335f6fe1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:37:36 GMT
ARG version=22.0.1.8-1
# Wed, 05 Jun 2024 02:37:37 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:38:49 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:38:50 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:38:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a38be4e967dd89cae6c13cdacd3d7aba1b8f96b03401d0508e0d59e89bf845f`  
		Last Modified: Wed, 05 Jun 2024 02:48:03 GMT  
		Size: 88.3 MB (88270285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
