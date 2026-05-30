## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:64614322e27d77a3dba41f510894adac7ee8ebf2829a9724481f7c6e4d3bfc34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0a38925cb2bd1115c373392923617ae1444b1cda805e23276e9e2a2871e0cbc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131333985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e4afa5bed1315b830a26dc42c50151b837f3973a29739fcd943ec58fe119be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:00 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:00 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:00 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ea376adc11d08cc7dbc43141a27734ee3e1b3ad81f228d8b3d56f8df183652`  
		Last Modified: Sat, 30 May 2026 01:11:17 GMT  
		Size: 76.8 MB (76762829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e95a262dbee0025fe6ae45e7856bd108cad99e3f34cc303b423683892c9a3a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b025f079a6dcd49eaccaf1db86dc40436fcc524d8b259dad19ce64612ab4dd99`

```dockerfile
```

-	Layers:
	-	`sha256:4d7096e552bbbc2f55a932f98408370af27ad0ffade6568bd051f92957c9837a`  
		Last Modified: Sat, 30 May 2026 01:11:15 GMT  
		Size: 5.2 MB (5228698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802d8950fd0efd7e6629df37c8277d962e58277aa3480c8e19f3037a0d1b96cb`  
		Last Modified: Sat, 30 May 2026 01:11:15 GMT  
		Size: 8.9 KB (8907 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:384f2aeb948b415c146ab65098b37c5e2f3bf8d39ca833bfc019c42da57ea01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129472067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e9a2dd02f10bf3f7c7d6b182a55dabb2f4a2c985c3e4e7976c3f590fcb8ee5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:06 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:06 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:06 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ef5fd4d24838936c14c3fc0822101f69e17bcaf7b7cb4ba0aec890bd6eeb15`  
		Last Modified: Sat, 30 May 2026 01:11:24 GMT  
		Size: 76.0 MB (76014240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:472efd7a0692f7609db6b3f41ef9d1e44e526ac56baece83630d09fcd6acd172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcf9d05e3cee0eaae3f766311cb78b6ac4ae1c16fbccc36d85f579cf62ef716`

```dockerfile
```

-	Layers:
	-	`sha256:723dba04836652e8d745509635f0273d23ad95bee46c1ba685f89ea62cd736b9`  
		Last Modified: Sat, 30 May 2026 01:11:22 GMT  
		Size: 5.2 MB (5228319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c31d3fe846ba67baa31d516c4e2ab44847beb0358f34ef955dcee0e39cdcd39`  
		Last Modified: Sat, 30 May 2026 01:11:22 GMT  
		Size: 9.0 KB (8987 bytes)  
		MIME: application/vnd.in-toto+json
