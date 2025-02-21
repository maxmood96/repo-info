## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ce4255c0dfd71698adcc0a1d53425ac810a9b7021035070ae95b43404246fac2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:978bf0538832132aae2bc76ede1f9a8bb50e9aefeda6638260b1f1197c6e6b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129369865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a54bb1a02e27d83d71d4d8f01c2f3930b98551769016f0ab8813f369de01b9d`
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
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf4daab45bd70277d23c5936b6f268ab0dbe3926da96460a132e93260b6e792`  
		Last Modified: Mon, 10 Feb 2025 20:08:33 GMT  
		Size: 76.2 MB (76219282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4ae6c089a22541fadf2b6f59cf682695c21599e70d3b421999574d53a7addf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ec56f93e79beabf37c32c2754e72184495ebf48d7873c02085f33b98169164`

```dockerfile
```

-	Layers:
	-	`sha256:3b060241edfd11e10ce8b75e968aabab24935cdea3c9f1348373fa9d10ce8b6a`  
		Last Modified: Mon, 10 Feb 2025 20:08:32 GMT  
		Size: 5.2 MB (5173639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74fda413956b9bece3ab88fe26735fbf33d218b59f5d146e268212d80c0bf86e`  
		Last Modified: Mon, 10 Feb 2025 20:08:32 GMT  
		Size: 8.7 KB (8652 bytes)  
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
