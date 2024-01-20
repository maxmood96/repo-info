## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b844dee9d3045a6d0e1ce651ab1562894a093ef6dbcb28dfb57715b295e6c85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e1821be7a5f0de856aef6d1ff4166466d8307357ec7cf5fb9b674d0a61779ee9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf06448b68167be52a6c166bc0beb22fb6e695c6cffe9081e3e0eef00fd25107`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:41:37 GMT
COPY dir:8f7245a97c061726fd1f5e8ec557a254660d588f51008b0475bdcdcce3a48bba in / 
# Sat, 20 Jan 2024 03:41:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 03:49:17 GMT
ARG version=21.0.2.13-1
# Sat, 20 Jan 2024 03:49:17 GMT
ARG package_version=1
# Sat, 20 Jan 2024 03:50:02 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 03:50:03 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 03:50:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:cd4602cb0e84e00e8b7d38510ab92c4d091288133108bb74e581c22d31377e8b`  
		Last Modified: Fri, 19 Jan 2024 19:08:42 GMT  
		Size: 52.2 MB (52244936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93be71f0379ee019636832f24b3623b93844273558d90d5f1940d2b84843a78`  
		Last Modified: Sat, 20 Jan 2024 03:59:42 GMT  
		Size: 89.5 MB (89514747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b888662d90a85bf9e3c60e78cef980f2530018feb5505d819be111caa01e5e32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139874415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f319fee5a6e0d3062c7402c706546d3e1325395d9d2063d8b0d668058ab3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:07 GMT
COPY dir:80de4926459dcf07edafbe2044439672e4fed6bf5796881b9953e9ffab3571d8 in / 
# Fri, 12 Jan 2024 21:49:08 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 23:46:03 GMT
ARG version=21.0.2.13-1
# Wed, 17 Jan 2024 23:46:03 GMT
ARG package_version=1
# Wed, 17 Jan 2024 23:46:40 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Jan 2024 23:46:41 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:46:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:6126164e178e3570337610ef0b171038c4426a730623557513d2ce511166a065`  
		Last Modified: Tue, 09 Jan 2024 02:25:54 GMT  
		Size: 51.3 MB (51303151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfd54103dc49c317b624eebf3889d76ae9342ef225b244d86da5aaf9c7d0a4d`  
		Last Modified: Thu, 18 Jan 2024 00:01:47 GMT  
		Size: 88.6 MB (88571264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
