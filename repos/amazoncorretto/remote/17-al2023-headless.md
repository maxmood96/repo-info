## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:729ae266773a8e4f9e60333689cc11d7591179bf6b011d188d99bf47fde6a69c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0b06e1c125937ae5b0708d3110e925e857bd470ea5df042f59dcd5590fe4aab9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134750082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997b424c82817ab0a6be8ae19d2c55625fa544426347b8eba4ca5bc0f035d6ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:00:10 GMT
ARG version=17.0.11.9-1
# Wed, 17 Apr 2024 00:00:11 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:00:55 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:00:56 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:00:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285617a00a257b52cfa3174528cf68b0ef29a9c938f07e3f422aeacdf79bda47`  
		Last Modified: Wed, 17 Apr 2024 00:20:05 GMT  
		Size: 82.4 MB (82426177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f456d8b6c60c674b6ecf52987ce3452dbf2e32a676736e4086ea93a8c242967a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133155693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0107b2e9e4a82d94d24f365ba131ea30c4daf8d4427258ee720174408aba0ba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:10:07 GMT
ARG version=17.0.11.9-1
# Wed, 17 Apr 2024 00:10:07 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:10:44 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:10:45 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:10:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4417974d60d01f902e1c5a0917f4fe958e8f3f13a0ac47b03f2ff504566c808`  
		Last Modified: Wed, 17 Apr 2024 00:29:36 GMT  
		Size: 81.7 MB (81747368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
