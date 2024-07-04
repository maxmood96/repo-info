## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:74d68dcc38a2e228b204f4f18bfcba328acc16f81b7949d4d8f32751a020fe32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:95714bdca1c7ca748e434bebf74c1d974f555a56e7e3c988be2fc2771fd479fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142588781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091013a2ba99356700490fb83587223b7e8297575a793c408b1280d2939f2cb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Jul 2024 00:19:47 GMT
COPY dir:1c9e0f4db95e1ae683b8f16b1ecfc5d8693ad4e5e379a2386e2870f38383c7d8 in / 
# Thu, 04 Jul 2024 00:19:47 GMT
CMD ["/bin/bash"]
# Thu, 04 Jul 2024 00:40:05 GMT
ARG version=21.0.3.9-1
# Thu, 04 Jul 2024 00:40:06 GMT
ARG package_version=1
# Thu, 04 Jul 2024 00:41:16 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 Jul 2024 00:41:17 GMT
ENV LANG=C.UTF-8
# Thu, 04 Jul 2024 00:41:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:860904071dc658e37de73aa1556e7badfb13bef4747965ea3bd1049e8ff87dcd`  
		Last Modified: Thu, 04 Jul 2024 00:20:13 GMT  
		Size: 52.3 MB (52319623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13e4b5333c7576797a4369693cd8915f016bc7d3636bc0b73c5779b5f5c6e14`  
		Last Modified: Thu, 04 Jul 2024 00:47:58 GMT  
		Size: 90.3 MB (90269158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:023749933613b5df6ad4a3a8a70dec47dabdf372177b958b4cc654f6f77b1ce3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140720031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b5cbc1d08f886343a00488c5bbe0db79b6aebd8f1a85a77423744cf45f502f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 Jul 2024 00:39:25 GMT
COPY dir:a2f5453af1f2210c7b49fadc5acdaaa335139ac35c64847d2f5879056f91a03d in / 
# Thu, 04 Jul 2024 00:39:27 GMT
CMD ["/bin/bash"]
# Thu, 04 Jul 2024 00:58:23 GMT
ARG version=21.0.3.9-1
# Thu, 04 Jul 2024 00:58:24 GMT
ARG package_version=1
# Thu, 04 Jul 2024 00:59:21 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 Jul 2024 00:59:22 GMT
ENV LANG=C.UTF-8
# Thu, 04 Jul 2024 00:59:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f95af119e05065dbdff89fbd219657362e32f7ec50d632e28754e75b5a13806e`  
		Last Modified: Thu, 04 Jul 2024 00:39:44 GMT  
		Size: 51.4 MB (51407040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359b8f4b5da5205bfbdc54556e79eb027453400f115fb98517dd4f2a530a4392`  
		Last Modified: Thu, 04 Jul 2024 01:05:31 GMT  
		Size: 89.3 MB (89312991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
