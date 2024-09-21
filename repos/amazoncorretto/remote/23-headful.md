## `amazoncorretto:23-headful`

```console
$ docker pull amazoncorretto@sha256:a0f62a4d9cd1e00cd6a0d97b1c16417c53f207e655983719b9f19d9700132d99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e6e5a9a98cac02749eccf235dc40ee9e052ce2e91c49a71556424946d86ea75c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146092330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b16c8b3ecd68ed0d49888ca80873b2d5397a2683bb410b0ec18dacd0b8a32b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:17:44 GMT
COPY /rootfs/ / # buildkit
# Wed, 04 Sep 2024 22:17:44 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:f9dd052e142d6bbee3556a17548362b00b044603d859f7ff1a81d3ef6d64bd6e`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 52.3 MB (52325199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b314f1052a4d83ced088dff81358f1f4bc688daa6c027a105aa2a23cbdc683a5`  
		Last Modified: Fri, 20 Sep 2024 23:56:24 GMT  
		Size: 93.8 MB (93767131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24e6281ace03a048e1db8dec0a16eb9bd12c04510bc672cdb6e3f6e50f5fa7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 KB (11265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc7e9d4aa96f6a70a1b455955d3dc34ccb7d89169443282fc7c320bc4509fb0`

```dockerfile
```

-	Layers:
	-	`sha256:8a919a847f8258a719f3c4e5b26d3b532b61567f5b88622c161c6a0fe7eee058`  
		Last Modified: Fri, 20 Sep 2024 23:56:21 GMT  
		Size: 2.0 KB (2045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9da1c7a5eb799e17b4564de866eb0eb69db3a5e40f0f906f46217c3e6cbd362`  
		Last Modified: Fri, 20 Sep 2024 23:56:21 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f0f214536fd433cbc12c6b1bc6f2a52c231b95acb99f44eee7ec7b2743e79fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144133996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd27028c623c94211f0324a2174afc1c7891b58a3191ee250ecffbd0a5f8b0f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:17:48 GMT
COPY /rootfs/ / # buildkit
# Wed, 04 Sep 2024 22:17:48 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:5df0cce0a70b576e00cfe75d45089073c37754f2920c4a7a79f3ed6e6500982d`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 51.4 MB (51426143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9badf427612f39e525cc37d72f9c353b073c8bf4b1a1461cfd0384f554a6e3b8`  
		Last Modified: Fri, 20 Sep 2024 23:57:59 GMT  
		Size: 92.7 MB (92707853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d88af880fa8a8222d8ec91cc8d01f6b8715dbc1615c7b65324362ed1bff5ae7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c84850274410f83b89674cec13281c2fbf87fcf3ee58127602442e4797d5789`

```dockerfile
```

-	Layers:
	-	`sha256:372d8663efc8840dc9f0e452b5d78f671f3206f80c7c70338c765e4f66f17333`  
		Last Modified: Fri, 20 Sep 2024 23:57:57 GMT  
		Size: 5.2 MB (5212102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48bcd0bf93c5029bf3677eb0c8b2720b00610d5a2fcd66e3fb8ba91cfe288803`  
		Last Modified: Fri, 20 Sep 2024 23:57:57 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json
