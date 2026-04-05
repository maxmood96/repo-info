## `amazoncorretto:26-headful`

```console
$ docker pull amazoncorretto@sha256:0c0a22bc0c05c6cdfd8b9c716af3f6cd8ad562f99b95c24eabc32ebd28f3d62e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:041ac466bfb47f0150ecf7d892118f65eb67ea90ea3eb34f3f35d2fe8d80fc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161111781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc96955ac74efde161f99ef93e229ba4da9cde4238a88f8880c8147f1f39b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:51 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 22:13:51 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:13:51 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:51 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3873ade7d61d96a32594b2b03b966b77c7ed0de15f125c4ca371cf03cab49ed2`  
		Last Modified: Fri, 03 Apr 2026 22:14:12 GMT  
		Size: 106.5 MB (106540478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:78f510fb06689d13971f85225c9769a3923eced667c540a815deda8f06ae1575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce77cd47cb2ae5c3c6cd658fe12e7c9ffc414eb6b9a9c3e2c55b50ec1f009b1a`

```dockerfile
```

-	Layers:
	-	`sha256:9ff5d5b2edf93a07456feaa6dc94a018aee4952d0cb8cf9dd73db96580f81ca6`  
		Last Modified: Fri, 03 Apr 2026 22:14:10 GMT  
		Size: 5.2 MB (5225831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27b5336738de9ed55bddee011ce2ec48dda5c6ab4847c38130aeca6b8b5185f2`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:391790530f5d2f4ad705346fcffa59653dc979835ab058272361ffe7138f1ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158877138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94c4565e484368eee1a25f1bfa5c3efaff3a945d7ec311d6bb0bd09befa0c79`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:57 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 22:14:57 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:57 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:57 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c042c16295eb88085e9c1f1bb29e0de424bfada9d852833a7b6a291ea17f58`  
		Last Modified: Fri, 03 Apr 2026 22:15:18 GMT  
		Size: 105.4 MB (105434313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:241f16af4f242ed564e86429e365d944f201bd4b61c179cd0b6c9f728ef80f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3a29c40b6fd85e7b8b037e73a90f8942454c5a9f1165045fba707598a6296d`

```dockerfile
```

-	Layers:
	-	`sha256:abf5c34289554c8097c2ce079809154188f578c519ac56a9b11153f18560cc06`  
		Last Modified: Fri, 03 Apr 2026 22:15:16 GMT  
		Size: 5.2 MB (5224644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9bcc234dcc04b8fee637f569bda661820a499e5216f1a85da1a84723f89ff3`  
		Last Modified: Fri, 03 Apr 2026 22:15:15 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
