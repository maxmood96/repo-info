## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a0c6c1d97f020aba664c6e29fb5d1de5deba9e8380a40d169c2dbfd474b6b53e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fb5cc0afa48bb423b129950da74a1246effbd677d1d4d723fa6b9e16f7e05df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140653256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3323a77a21e95689fd24106a9ab73936667c36a108e8fd224aed3d6c866ce03`
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
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639b5f3bb2c63bf61e8e5ff8d070e00edd7ea59884b64fe8ab8c29f5436b27e`  
		Last Modified: Fri, 09 Aug 2024 20:49:32 GMT  
		Size: 88.3 MB (88335353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:735a3c273069a498824db31f4890c46409bd04558aa1306ed88efa6848ce2ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494227d41e35d8c331a4e1f2a62e130f04d5652a88fa729232e5d73284e11196`

```dockerfile
```

-	Layers:
	-	`sha256:6aa45f4a80ac36f7e308e52337630d553a1aa26fe62deafd8254f45c7bba92a2`  
		Last Modified: Fri, 09 Aug 2024 20:49:31 GMT  
		Size: 5.2 MB (5187227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6498315039e64ae765e682bccb5efa39a2ebaad614ad59069d50c5fe3a70c879`  
		Last Modified: Fri, 09 Aug 2024 20:49:31 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

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

### `amazoncorretto:22-al2023-headless` - unknown; unknown

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
