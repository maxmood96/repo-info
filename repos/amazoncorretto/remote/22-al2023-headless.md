## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:e1688717a56f4af4132fc114bbb6f93ae14d5fa34bf2f64d25e4141435466f30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:28fe13e2a7b805657e6a42d2f735c025e9304623ac63c5a7fd754a0a276489cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140659500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4346af328bb87862d16ee7176bbf04833b7f61637c3c573231507653bbf3538`
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
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff750bd26ab71a46c3b8ad5fa384df48e6dda50dcf63f864208a3754a071181`  
		Last Modified: Thu, 25 Jul 2024 21:02:24 GMT  
		Size: 88.3 MB (88345321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:338656c0d7ab6af44e837ec0f624cb06e52b73f096a7f2291b6023541391c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca6f7005d371b6a7d2113ba2cc7d579ee7ebb3725ca62f9017188e462f10592`

```dockerfile
```

-	Layers:
	-	`sha256:a455f34761990831bad75f07a19f719f40be2b05427291257db6287e84ed4e09`  
		Last Modified: Thu, 25 Jul 2024 21:02:22 GMT  
		Size: 5.2 MB (5186101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdd31ba510a8f1cba12087f663269017b47d31fc1f73d303da6073ea85d0a0db`  
		Last Modified: Thu, 25 Jul 2024 21:02:22 GMT  
		Size: 9.0 KB (9037 bytes)  
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
