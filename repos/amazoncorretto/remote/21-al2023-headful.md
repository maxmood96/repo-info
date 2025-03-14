## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b1bcd9036acadcc5be73b07e108be88ace8f3fe34d56ebd59d2d49aecbf01dd5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:04d92c23a4dc105f34b253d4d11e17d9b988f791dbbaafd94757bd924be5a03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142830991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b5dc2547f2938217d7ee64a3ebbbb2007cd551d53c71de0a2ef7404f780383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3821c16409786f1ee4132fa3756ee9d21cf2179e76c5031fb90dcc0f38500c51`  
		Last Modified: Thu, 13 Mar 2025 22:53:09 GMT  
		Size: 89.7 MB (89704115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c59c5abcef1276486349e7d59103df2fbcc4e7cbfa05f0b2731731f77ac14b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776d2491692fc43b3b9b7cf0337baa495641f0a7b6c8583adf34210402880adf`

```dockerfile
```

-	Layers:
	-	`sha256:e87d6ae74a0ed86cf924d82829b54e626a195924e3f01f30142c01208b2b208d`  
		Last Modified: Thu, 13 Mar 2025 22:53:08 GMT  
		Size: 5.2 MB (5186578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff827d7ba172cd436f4e2d88c7b0cd005f3915f2cb1e95ca7d0af7c77ae02d44`  
		Last Modified: Thu, 13 Mar 2025 22:53:08 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:34801a748c56794fb843300fc8990ade3ed756abbcc9bb8de5806da613936cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141118124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314fa626c633d9c81b054f152e179bc5c5efa287b40ca110bf94394f96c9e438`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d02eb953541c2ff90ee6823eed21e190b64fc35f6038a407ba5cfed5ac783`  
		Last Modified: Thu, 27 Feb 2025 21:24:00 GMT  
		Size: 88.8 MB (88846854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba9dd54492c31d5511b96bdcde1ea24a26ee3a90e9d72008c8d3b86821077ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e8768fb283b2136b8065d7f2d263ab7723e734ab13a673e36225a15d5f8776`

```dockerfile
```

-	Layers:
	-	`sha256:56c4c68a2ac90c8ad2b3b17e4f0c89af38edf53d2faeff4c44fd6bd69ad96e72`  
		Last Modified: Thu, 27 Feb 2025 21:23:57 GMT  
		Size: 5.2 MB (5185371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a3472448c49acd0b59923e2381b1c99f7f27e0f2dac020ddabac153f4ae0e4`  
		Last Modified: Thu, 27 Feb 2025 21:23:57 GMT  
		Size: 9.0 KB (9005 bytes)  
		MIME: application/vnd.in-toto+json
