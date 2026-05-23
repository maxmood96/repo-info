## `amazoncorretto:26-headful`

```console
$ docker pull amazoncorretto@sha256:f82f7064532b75ea2202048d503fb7f15a33d8e9621eb9696b15536b01ea7e8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a679bf86d9020e3d06e2cb5b15ac06133f2ae88a02a23df058bf93853a4e0dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161113499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205eab1a3014ee7b230817a1ef6af8d933ab167de07f4aea290091447b6d0b31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:58 GMT
ARG version=26.0.1.8-1
# Fri, 22 May 2026 21:12:58 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:58 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:58 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c10ec00beb857087786b9e616ee35ed9b8358143eb43cd9580326809a0952`  
		Last Modified: Fri, 22 May 2026 21:13:17 GMT  
		Size: 106.5 MB (106541059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5bec8260ed250a22632fcaafc142350dac435ab69c48f56e7bc3a5de8d593a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69757677aa03856c5542542859d5153ba701a5391e612de1844d2a7321601c30`

```dockerfile
```

-	Layers:
	-	`sha256:aa9fdd61dc94d3923c4c8976a925dc28497bfa0f76ba9aecabbbc3023e799e85`  
		Last Modified: Fri, 22 May 2026 21:13:15 GMT  
		Size: 5.2 MB (5225833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2693d2e4bc3cc094c1414d05aea36e7a8eecb6f043bb8ec013b3af2b5dc705e1`  
		Last Modified: Fri, 22 May 2026 21:13:14 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:21c6b4809e185ffbee2c7b0e561af3a913cddd4b26139ffe33d1e239548ce017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158885522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ebb6eebe0e222745fccda25743738716e2c6f3cc07a85e5391aa35d3368c07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:42 GMT
ARG version=26.0.1.8-1
# Fri, 22 May 2026 21:12:42 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:42 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:42 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52cb62bfe04da12db6ff21ef4011c9216e717ad7ef5401276798aa665ef5cb53`  
		Last Modified: Fri, 22 May 2026 21:13:02 GMT  
		Size: 105.4 MB (105431107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:988e110f7025394cacc1ce85450784e4bca408b4a51fa74026f338679d4c8074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac45824b7cba06e14647401555aac07fb1e70f3774d480f39e695b8f4cbb99ac`

```dockerfile
```

-	Layers:
	-	`sha256:490619c661c9c11e44f9898cc8b433350bd97ca4f8b09302435034d74689c432`  
		Last Modified: Fri, 22 May 2026 21:13:00 GMT  
		Size: 5.2 MB (5224646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dcdce39f0ce392163fc8c4a6823ddb1a8cc14634343b2525311b9c1996db19b`  
		Last Modified: Fri, 22 May 2026 21:13:00 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
