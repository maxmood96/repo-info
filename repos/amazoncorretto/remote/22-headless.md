## `amazoncorretto:22-headless`

```console
$ docker pull amazoncorretto@sha256:dbafe04bccfcaed3775845c56c70c63c7b89d98ea1d2402be85864080d81d9b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7d207b9cb6175314fe42090d759e45d20ca930564604d50cfa7ce5eae63bbb04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140659043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24da9314ff7f36524c466cb62571d736662268a72a996ec896972fab554a7b38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:cb6230c89c15ad3884b7222b06322338ef758165e0b4068d1270a3c8141a3e43`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 52.3 MB (52313926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d393177e2310c4286d057db6217312970c20fd4fe83318f58b26944e125e4857`  
		Last Modified: Fri, 02 Aug 2024 14:55:38 GMT  
		Size: 88.3 MB (88345117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5add51e46a17cbfb748bff5560da5fdab9a25dda755a4cf738ceb5c6108685a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c451b558144bcb053734ec77b0637630b9973e13b416290165a430482a0e878`

```dockerfile
```

-	Layers:
	-	`sha256:2a5c2cf201a4b61ee663c22cf38fc5c9ceb7708250ca9fe71a9b8edac7601dbb`  
		Last Modified: Fri, 02 Aug 2024 14:55:37 GMT  
		Size: 5.2 MB (5187181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949cfc6ac3c44cd4c486a2fa9800d63d17f691862fe3de954c6bccebaa63cbf9`  
		Last Modified: Fri, 02 Aug 2024 14:55:37 GMT  
		Size: 9.0 KB (9038 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b9786c0abb3535f7e632020adaf9e0c0ebbf288546393e1f69c927869b544c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138706356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c0a73bab21fb836cab5e7a7047334674e0043aeba48ac6c30c0f12a1ea8d7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715e5b190e65c54028238e22658401c6f1b720aa8827c5adc4432d688cbd4c0d`  
		Last Modified: Fri, 02 Aug 2024 05:52:07 GMT  
		Size: 87.3 MB (87304344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f341139e7b699cc003b14c728a6ae78e7b6d3c424882f133b9ca8c328644f466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb548475b78d8ed551446fa568afa685524da5d801656b1c3876ee4c3db8729`

```dockerfile
```

-	Layers:
	-	`sha256:1922c3cb5521f4fc0f3f53ba6d33de58eb248d113674c2ecfdbe724ce3bd9cee`  
		Last Modified: Fri, 02 Aug 2024 05:52:06 GMT  
		Size: 5.2 MB (5185165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5fc1ecb6a62f1adfd42fa34ed5cf91ef8f9c6e32eab3d699a61c32e60449891`  
		Last Modified: Fri, 02 Aug 2024 05:52:05 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
