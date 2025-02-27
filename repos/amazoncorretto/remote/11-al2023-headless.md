## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b3e5a5272ba6dfaf97924a70141554f7e7ef638bd3c3d6ddfdcf70952b2065ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3fb5944c2548c35f26dcfb85c012ba6ef5d14e8b9d5a8dd72d88d15abca48585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129389086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759e05835811dba2e3a36fba500b77d31dfa9cce1d2dc5ee713e9c735c105d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f332b02855205e16af91ca1c4366245f818ae4ed0d8225976ce342e5f4192a9`  
		Last Modified: Thu, 27 Feb 2025 21:08:09 GMT  
		Size: 76.2 MB (76237353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f4255e62d18566144dcb8b8189b0b5cc6659f0613b910bfdabbaa4b63860c6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607a274a96ad228ad8b6751615ad52926d1232dc6aa07af390a0d7c657c59387`

```dockerfile
```

-	Layers:
	-	`sha256:251fddab941bb0fd8c27eda1e974659edc5670e5c547988d7a1ec6c7fa4ddcb7`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 5.2 MB (5173639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f681c5f8a62d3f63d066bd402be81b533a185bb74ffdc8127b8a510fcfa432ae`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 8.7 KB (8650 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d615973de183df4379640f0a6b57df1c88936852afd4dff9596c68c6491ff6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127682399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214bb781ebb82b36a32cba99e63c1c15f745e00dfbb0b625118e512f55666f8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa1bb1903ac84e2861db527a4d9a4ed72d79846e402c821c0f6488b6c905568`  
		Last Modified: Mon, 10 Feb 2025 20:16:45 GMT  
		Size: 75.4 MB (75411448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d28d75fa1065e8d33af2066ab48f31a2cdfb64b9bae9ae095ae96a2d5c27f196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5181989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f209f75d0c13dc55436c948edcf3fb926c956697644198a0178310ed2278f1`

```dockerfile
```

-	Layers:
	-	`sha256:f8d93a4f9352fa710cb5b5bba5f1a0fe5da48badfd4bcddbe276bb0f986fcc86`  
		Last Modified: Mon, 10 Feb 2025 20:16:43 GMT  
		Size: 5.2 MB (5173257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5542e5c41950d2cb92c6627aff290708e8b15eed6b3689d6e4f5c78e38172907`  
		Last Modified: Mon, 10 Feb 2025 20:16:43 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
