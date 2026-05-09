## `amazoncorretto:26-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a0945e1b8c0dc79a6cc37191ffb503fc3f1f374c32918458c4eb14aeb2b0edfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1217877f6a075d5312fd56b44711b9b49252d2ea4d1712c09e14e469152ccc4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160400590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a1f8c6182b6a673f57660a5b3c0783d201eaa8c6d64566b5d1d82200a235cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:26 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:19:26 GMT
ARG package_version=1
# Sat, 09 May 2026 00:19:26 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:19:26 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:19:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d319d3a49e87bb917718925eebb13fbdbf7fb4e741a5975a313448a0296bfb`  
		Last Modified: Sat, 09 May 2026 00:19:44 GMT  
		Size: 105.8 MB (105823786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a96321bfcfe7e885d6f3771df815c2dd24af253d7a779f945d76598a73912671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660bb5245b890aeb73a3f0b94abe3ecd871fe5ab2776ea33091835f405ad5219`

```dockerfile
```

-	Layers:
	-	`sha256:a11f572a11704b9b7a209daa62919771cbcfe7aa192823e5940cd94c91e1b80d`  
		Last Modified: Sat, 09 May 2026 00:19:42 GMT  
		Size: 5.2 MB (5200408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dabec293809d74ea1589b1d153d8561be40b1c7092246eb6e0b5700a2355aabc`  
		Last Modified: Sat, 09 May 2026 00:19:42 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9a80c7f8e29bc2616ff7153086d68f998b5cb1aa6f867dddd09f7ef815c15784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158165086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238bef8167ac2106cf960a3b55957e4d05a1467a5514435ac1b29b93988170dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:56 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:16:56 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:56 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:56 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9636a1dff9272ab4da49ccccd0a26297d8ee8ad7d0ce2ebb2549732b8ffbce0`  
		Last Modified: Sat, 09 May 2026 00:17:16 GMT  
		Size: 104.7 MB (104708111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8f4bea8faf76eb1b4adc63124c5acdc1664f6f9f91354ebeb12127949a50a79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11dcd7c1529dd81fe33d8cccd15b02a335e1ca23351f6b8dd71ea7237afc452`

```dockerfile
```

-	Layers:
	-	`sha256:ef6f2995fef03849047cde4aaaca03faf2cbd05088ffbe0ebdd338a4fa70deed`  
		Last Modified: Sat, 09 May 2026 00:17:14 GMT  
		Size: 5.2 MB (5199218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01af69d7f6d00a00b7519f35e8095e4ba3958939e80af29e32a5b980ea891ca5`  
		Last Modified: Sat, 09 May 2026 00:17:14 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
