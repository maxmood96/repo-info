## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6ae78462cc68ccf644eab377dfdd32ed19b6807ba0a522416b4a90f8a14acac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d89ff8b1f66cecf8430a9c60b0d779b574bb0ee6b1e0b98a9d746db871c6e7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131278734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b56b50b15ee40fe02b8e4a25ecc057f7d8a79c7e27900e43866f414081c9c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:51 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:51 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:51 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd2fc15795ef3db48777565fa5522688ae19a733d9ee18c7f86862811632007`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 76.7 MB (76707431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b5ad0303d61f0958fb9e436bf0c17063ab3931d3695cf75e9057a57e4da32e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576669770fdea1800923e8f273295f47c93bd40be7f6a090e16a8b413605b3af`

```dockerfile
```

-	Layers:
	-	`sha256:288fc2a76491e622e0b467b2a852beafee7556a30d02876f929e8d7c640972ac`  
		Last Modified: Fri, 03 Apr 2026 22:14:07 GMT  
		Size: 5.2 MB (5228692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e09b64c6cda1b8035f4f7f26fca7114e563fc32ef74386f890b21feb245155`  
		Last Modified: Fri, 03 Apr 2026 22:14:07 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dd2af19ebe3e2e7204b737fbb40c79d4f03477b1e7534867c04541057ab1971f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129398975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1329e7ec7160c9e9754ededd7ab577d044b7235f0687ecb39f66af6707c2a169`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:51 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:51 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:51 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7385e296d5617cde7ed632263378a04c9b937e588c27cdbf34f7fa19f514e3c4`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 76.0 MB (75956150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cab0e2a01e224fe78197f09c41309f57a27f220562ed85a1d3733aa702624cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07533e5efae92a6bc7263e72b58abcc07a0275fcb77a649c940918da8c5529ad`

```dockerfile
```

-	Layers:
	-	`sha256:da36c3809f7a64f51cbf32869f603118a089fcaf397d31a59272a31dc33aee45`  
		Last Modified: Fri, 03 Apr 2026 22:14:07 GMT  
		Size: 5.2 MB (5228313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a55dd3849fa5a607015c6d8bca8d422bdb620c806940e97198e0430eae39990`  
		Last Modified: Fri, 03 Apr 2026 22:14:06 GMT  
		Size: 9.0 KB (8986 bytes)  
		MIME: application/vnd.in-toto+json
