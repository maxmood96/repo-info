## `amazoncorretto:22-headful`

```console
$ docker pull amazoncorretto@sha256:e6c2e6cf8f70fd29efcb9b6f319fac30ffc9dfb47d7fa393edf70d96e6d43db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-headful` - linux; amd64

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

### `amazoncorretto:22-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8dd837a6c96350b9201c56aa85d523eba7de32051a6d1e345279a85db0783d90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139684101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbd5654ebad84f6c54f7d3afb1964b75567eca1d8bcff5ec8162828ec9d7953`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:29 GMT
COPY dir:0c9326c957c0b22895e223bbba2686fb8615da2af32396db3026daf720546255 in / 
# Thu, 20 Jun 2024 17:39:30 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:29:20 GMT
ARG version=22.0.1.8-1
# Thu, 20 Jun 2024 18:29:20 GMT
ARG package_version=1
# Thu, 20 Jun 2024 18:30:23 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 18:30:24 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 18:30:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:15e2a4581bb8a27d0865d7375063b10dc543dbcfa6a288911a297aaf754984d9`  
		Last Modified: Tue, 11 Jun 2024 02:05:34 GMT  
		Size: 51.4 MB (51406731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2120113d4c376572b27f73666be696da8bd0e97ac94e7a12c07e5bf3026a9d`  
		Last Modified: Wed, 26 Jun 2024 16:56:02 GMT  
		Size: 88.3 MB (88277370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
