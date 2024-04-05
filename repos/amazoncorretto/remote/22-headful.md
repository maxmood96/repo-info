## `amazoncorretto:22-headful`

```console
$ docker pull amazoncorretto@sha256:ff0e691b4ec61c37e019e2d18f00b0978a72d0613ea233388e266f6c74eacadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9a6ee66a9ceb579c0ee6e8a4e01bcdda9def33ec8f2c120f96f1bcadd0f4974e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141628455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d3ccfae25004f412e45ec47e5473d0479a01c9689946dfb469ec2f0b54ff4c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:31:55 GMT
ARG version=22.0.0.37-1
# Fri, 05 Apr 2024 19:31:55 GMT
ARG package_version=1
# Fri, 05 Apr 2024 19:33:08 GMT
# ARGS: package_version=1 version=22.0.0.37-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 19:33:08 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 19:33:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c36025e044e9d7eca8a7259ec50f41c45ac3879da00c081cdf1b080e2107f7`  
		Last Modified: Fri, 05 Apr 2024 19:44:56 GMT  
		Size: 89.3 MB (89304550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:057f05c4859c9fd1aa11ce61d26d60ad697a530dcbb6f1c54e1576590d40c737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139682341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6640bf72859b2c6cbbfca927936c7496bc8944e0e212fbd5664f0e5f330bf3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:52:33 GMT
ARG version=22.0.0.37-1
# Fri, 05 Apr 2024 18:52:33 GMT
ARG package_version=1
# Fri, 05 Apr 2024 18:53:40 GMT
# ARGS: package_version=1 version=22.0.0.37-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 18:53:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:53:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf8a500a937baa6ae85069c7818a979e6671c6f51705ebd2cdc35dbae3f75fd`  
		Last Modified: Fri, 05 Apr 2024 19:03:42 GMT  
		Size: 88.3 MB (88274016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
