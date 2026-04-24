## `amazoncorretto:26-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b64ddf5ec446ab503fd9533a8b7d153d39677487247eeaa1cc3952272541b0c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5aa6fc7b88682be8886ac80a8493845548f2ebced5b002504c3b5abac8cfe630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161110522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7de0a2dec09463624f2d9922fb97f931efb0afbb0362ee144d1ef9a368f9520`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:14:10 GMT
ARG version=26.0.1.8-1
# Fri, 24 Apr 2026 00:14:10 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:14:10 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:14:10 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:14:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27694c540c776ffe61ea55324fd259ba83b0fa4675f415db4510b65d7e72fc0f`  
		Last Modified: Fri, 24 Apr 2026 00:14:32 GMT  
		Size: 106.5 MB (106540817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5af841245b41d77b2bfcaf8f226e1482afc4d661f7072f80279ea48c60b7f237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0af467723f3afade3fbeb1f3eecf493eb7446277d8b1ce0e1b81559f2652c3`

```dockerfile
```

-	Layers:
	-	`sha256:ccd771303e03dd566b70a6c3f5510de3cdc3ad2c17c8c91335c12aa8f2f9d952`  
		Last Modified: Fri, 24 Apr 2026 00:14:29 GMT  
		Size: 5.2 MB (5225833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54698b7ac08eacdaba58809c8b8838aeec6b2ac885cbb328e57452f80a37735d`  
		Last Modified: Fri, 24 Apr 2026 00:14:29 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:38e5de68d70f45935ea6a8644bbb60fc11d8b943b857df806c3a31e987a292ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158883331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5eb46b35c1dc0930568e1507dc5807dce725737b30c6a8a03f5bb30760a0d96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:14:02 GMT
ARG version=26.0.1.8-1
# Fri, 24 Apr 2026 00:14:02 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:14:02 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:14:02 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:14:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037897fa96c14f2328b9d5ae341987e4027b04b9cf3df6912eb5fb50b6eb1e43`  
		Last Modified: Fri, 24 Apr 2026 00:14:23 GMT  
		Size: 105.4 MB (105431078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:577b15ed1ba60f57b0cc58dab7bc63da6965a7b2057b2d5509ef1580afbfe56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def8aea13db78483cc1eda2efdbf1dd91fcf2e2919c5827724e5eac8012704e7`

```dockerfile
```

-	Layers:
	-	`sha256:f1cdc4752c5395ef1d0dfdd8cb0098df245890c6c7507247bb581dc61d558986`  
		Last Modified: Fri, 24 Apr 2026 00:14:20 GMT  
		Size: 5.2 MB (5224646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d915af41d5f4868c080739f217ab23d0e756969af9675f97e73fcb76ce80a63b`  
		Last Modified: Fri, 24 Apr 2026 00:14:20 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
