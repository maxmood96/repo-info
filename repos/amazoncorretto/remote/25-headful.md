## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:7675398c77f1a93cba604079657d016bbdfa700eb30446081bf7690ba3ede38a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b95826327354a9a7c575cde57827fc33ed2f71b7823c8a5bef21ff5cc9335e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159008704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f07846cbf08dc89482f817b5450cc9e56b44e780901640b38d26241f773779`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:48 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:48 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:48 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:48 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9495634c07cfec8e5461355c2213d760485691827a55cfb1d05e5695587f5031`  
		Last Modified: Sat, 30 May 2026 01:13:07 GMT  
		Size: 104.4 MB (104437548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:528c14629a300ebadcdc7937d4bdd64fa915472535e60064d6e5f854b88a5fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd0746be0e5cfec16d99f0c250b01619e5f8ac5038da17bd6afdba55ebbfe76`

```dockerfile
```

-	Layers:
	-	`sha256:5af11f1a420e274d95736727927ffc421371f1f662fd790d31f6f0ffe8239ed4`  
		Last Modified: Sat, 30 May 2026 01:13:05 GMT  
		Size: 5.2 MB (5227475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3e409277d0b2ddb248652506ee3b7edc8e714fa67a055001c1d5a4ad8d7a13b`  
		Last Modified: Sat, 30 May 2026 01:13:05 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:592641947f2238857d4bc7aa4c7a9cc3725ae91c6ce950205543e8df79c1c131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156846053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65ad2ced72e3bc6265ed8d2dba63021d2491ad1eaf68b0c3367a61c0067f0e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:37 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:37 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:37 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:37 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e08b84d5e6efb1523976ff01c8e2e957264f525c392e5b2563776990efc880`  
		Last Modified: Sat, 30 May 2026 01:12:59 GMT  
		Size: 103.4 MB (103388226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:448039cead0a8e9731ae8848f1e387d53442bc3c39810314befacedd0735800d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2444d040c425009f11d021340ef8dd1be2211a200eb0f7aeb616e59a24d0237`

```dockerfile
```

-	Layers:
	-	`sha256:5edb02e1e10c0d28b643144d98ffec037ea5cbc6a7c5573be0478f8a3bb55c71`  
		Last Modified: Sat, 30 May 2026 01:12:56 GMT  
		Size: 5.2 MB (5226290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da80934837caed2db9e52e5a75dc13844a7533ca8019c4db07a208474f4cdf89`  
		Last Modified: Sat, 30 May 2026 01:12:56 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
