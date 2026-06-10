## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ba9be632d4cba9fe9494a56a0acfd3722431e9c18c52a36b3f33de3059d32e90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5d8967d65ec01f32ba43c1055b62a9afa1fe97ff98784fb14fb5e9bc680c06fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158292821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58e440e30c9f4a7614242800cfaddb92e5f9f8cacea5bb7299cb869ba81c12a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:42 GMT
ARG version=25.0.3.9-1
# Tue, 09 Jun 2026 21:12:42 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:42 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257089fa6ae995a3d3e33481866937b94748cf5a282598791d390c82ab2a16c0`  
		Last Modified: Tue, 09 Jun 2026 21:13:01 GMT  
		Size: 103.7 MB (103721665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:54c7976edb3e67584a195c7154b1019742351dee45a853d8389e2810eb8cb649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db2af72714694d0c1f2a681ccf6a4c7b33afadb6242da0acb73101d2d9f11fe`

```dockerfile
```

-	Layers:
	-	`sha256:63b24a5e10be1e874654c035ff094283407f853c24af86811e6adc3d3b7204c5`  
		Last Modified: Tue, 09 Jun 2026 21:12:58 GMT  
		Size: 5.2 MB (5202050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:606e70a8ece04790187cc08f8cde583d6af9590beff9e31bb17fc8992a2b704b`  
		Last Modified: Tue, 09 Jun 2026 21:12:58 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:15a4cf1a4b5612e1d6eeadfec45c563861721941fe20ee8b5b715abf3a881af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156109415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb99bc62115e76f66874e54de56b48fbbafa12b4e2c3ced48f79898df09ab5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:32 GMT
ARG version=25.0.3.9-1
# Tue, 09 Jun 2026 21:12:32 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:32 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:32 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6955c43911b153ea94eb924e78fef55c1558c0d407522177b9d0b8896e26679b`  
		Last Modified: Tue, 09 Jun 2026 21:12:53 GMT  
		Size: 102.7 MB (102651588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4f1037d1fa27ecb8a90a65532fdab251141b13ee0999923e9b8a4e9c190181d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc4c8c9070fcb8500a67ae4e95e6a13a8411db9980de09594635b03a3bdbef8`

```dockerfile
```

-	Layers:
	-	`sha256:259eedb1759ff0d10959729528610f0499187421a9df216c4709b0d69f0e7a96`  
		Last Modified: Tue, 09 Jun 2026 21:12:51 GMT  
		Size: 5.2 MB (5200862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01e374209e499ff5dae7c1b5b43578a5f039491c55aeacf873e21cdad6f0274`  
		Last Modified: Tue, 09 Jun 2026 21:12:50 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
