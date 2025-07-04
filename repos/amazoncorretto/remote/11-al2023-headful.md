## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:54d55005c489cb076667fbd2ebb5261560fd5bb993cfbfdc08e0557d3c41e69f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c54eff4d09330046808ac1a7cd942b68f106ef59abbf197d1e5995bcf6dd72ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130793875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1240488ad2b60566c48fc5eb3a671883acbf3b151d3dea7646ae12a4b16047c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93f6cc8c0ecf0e04c304530682f4a61079aa543c88b8550421ef308d26d31fd`  
		Last Modified: Fri, 04 Jul 2025 03:20:58 GMT  
		Size: 77.0 MB (76953664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:90101366c455740b11946b31ac12b49128624390d83a22c4fe0655e034f28f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc0e97cdd7e33b2feed872daf802c4a330415c06308425a7da7da8196e13a1b`

```dockerfile
```

-	Layers:
	-	`sha256:b832219ebb97f1f6660f1aef018c048dc79271b2e98d572fef5ea88057a3e95f`  
		Last Modified: Fri, 04 Jul 2025 00:47:37 GMT  
		Size: 5.2 MB (5222877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c88f4666d75638efd74bbc63278eeb0c6c91b1519430f693dd560664d1965ca9`  
		Last Modified: Fri, 04 Jul 2025 00:47:38 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:70d3c1c0a455877c8d18bf12464c0b819682f0a27cd710c14a497e29e1ad20fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128890353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1074480874203a80b878e1878fe06ed3016dcbcc590f8ee9c2453ca844fdf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0e455f237a70326021a937388393d9d7ac6f9ae1616673300f248aeb280add13`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 52.7 MB (52717557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a33c968b1f7e2a9a81ba488b56c799344657fd943738d5312651fdd8bc5bfc`  
		Last Modified: Fri, 04 Jul 2025 02:51:21 GMT  
		Size: 76.2 MB (76172796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:054da77e1fbf94189cb18d322ff3cf3b4ba878e9defb231f041429995455b238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae1607a8dac1b03152bd25384eac438a73a75889b36526fa273787f89357008`

```dockerfile
```

-	Layers:
	-	`sha256:26a34f1b6ccf4f5d3abdbee5cfb757a4038b7ced2ea98df11ffa989581218f91`  
		Last Modified: Fri, 04 Jul 2025 03:47:38 GMT  
		Size: 5.2 MB (5222498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d9f1bd10a6384d92a92477b550d9eb574a6fd7908cb4b2d540bea31dd42c25`  
		Last Modified: Fri, 04 Jul 2025 03:47:39 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
