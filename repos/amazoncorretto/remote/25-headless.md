## `amazoncorretto:25-headless`

```console
$ docker pull amazoncorretto@sha256:4c73e5c3b697dbd7d181dc4d02258d29e247c7f6f611d80eb74fffa9462f9341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce2aed7fad891abc98e4c20d403d18367181ce93e21b3a9013676099f4951482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157622058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06287726bd6723989248c40413ffec71e650c53362ad56948baf1bab351ccc86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:44 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:12:44 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:44 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:44 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72b93a14791c7a9beedec34cc9a57f19405495b431070d2ef8df9614332cda5`  
		Last Modified: Fri, 31 Oct 2025 00:13:24 GMT  
		Size: 103.6 MB (103620823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:58986ed63324972e68bd9b171e4559dc43bc2bde482259cbdbc6375d30267e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c833d01d70b56caf1460963d1e5528ece53276b3927f680114f1ffacb155dda1`

```dockerfile
```

-	Layers:
	-	`sha256:e0d1ff3ada7f20fb5faf5da8f2000517c2827c272b3ed44774ea25fa13b1df2b`  
		Last Modified: Fri, 31 Oct 2025 03:51:03 GMT  
		Size: 5.2 MB (5194783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84590b3bca1c059c78f9ac55013cd7e420f1e5c4e13e048227e03c82843bfdeb`  
		Last Modified: Fri, 31 Oct 2025 03:51:04 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a65711680f61c2f2691bfb91aec44cc39410f5cb83cd1cb4d9afd935f62a1aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155464168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab17c1bc907b38e8c51b7c1f3167c7e59a1537e3a76866b32f4e86e2b1bfd47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:13:17 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:13:17 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:13:17 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:13:17 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:13:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82bf4c95a8c8da4a8d6084ca79a225387eb47927f9b8c208a09b926efb13401`  
		Last Modified: Fri, 31 Oct 2025 00:13:53 GMT  
		Size: 102.6 MB (102562317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3424da436e23682f3d8258dfba357c27f37e2c0905e6ba04669111586928f85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82955a3afe5be3b5d58f110a81d31ada37efa2e3e3eb859557cd3f30aeb474f9`

```dockerfile
```

-	Layers:
	-	`sha256:4ae44df7363f0a4fed2a307b404f52a932cdf0153502522350977022de03ac70`  
		Last Modified: Fri, 31 Oct 2025 03:51:09 GMT  
		Size: 5.2 MB (5193594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fee41e4589ddeb956601499b38e1f7c3e78fc727ff672715a22599afa5c0652`  
		Last Modified: Fri, 31 Oct 2025 03:51:10 GMT  
		Size: 9.1 KB (9122 bytes)  
		MIME: application/vnd.in-toto+json
