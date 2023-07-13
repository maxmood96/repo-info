## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:046ecdfd9526bf228adc083a89db346c62b37162fcb917f317d294310fad6a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:55b0bb1a5614ff2d8e91c850ca4b43dba79764cd078935b2bd0f5e06dc3b4b39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135277874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6267b9018a01f42349a2086d4dd75a176b761a518001f532f17594e445856d28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 01:19:51 GMT
COPY dir:6bcf60f30d73b947ca07a9033109632c5faea18ed42743e2d6374e73b77d7d3a in / 
# Thu, 13 Jul 2023 01:19:51 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:43:33 GMT
ARG version=17.0.7.7-1
# Thu, 13 Jul 2023 01:43:33 GMT
ARG package_version=1
# Thu, 13 Jul 2023 01:44:29 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 13 Jul 2023 01:44:30 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:44:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3b8efe8e8a66806c25259c3f18e066eaef344018f8fb28a90db73bb2c2379601`  
		Last Modified: Fri, 07 Jul 2023 03:04:17 GMT  
		Size: 52.3 MB (52314023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97787bc995acbc296b8bcd5bf4f19faf4b9390876cafec94140e3d67d69e31c`  
		Last Modified: Thu, 13 Jul 2023 01:54:26 GMT  
		Size: 83.0 MB (82963851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f8d5161f2991bf8b325e39dcce0435b9e85fa5de300d6e5e62c3adc4b5002ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133672020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d04ed4da03dbca623c1ec859f7326ba348b37f770a7d280092f0e2bea6c176`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Jul 2023 00:39:43 GMT
COPY dir:c971849a42f287ec4e3f54148631542a63e55183107bf0088e1c6913d556d33d in / 
# Thu, 13 Jul 2023 00:39:43 GMT
CMD ["/bin/bash"]
# Thu, 13 Jul 2023 01:08:38 GMT
ARG version=17.0.7.7-1
# Thu, 13 Jul 2023 01:08:38 GMT
ARG package_version=1
# Thu, 13 Jul 2023 01:09:30 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 13 Jul 2023 01:09:31 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jul 2023 01:09:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8df4f3b6d932cf6e3c467c8f32011fb41de2120bd82bf33f3469b54bbc38d5c5`  
		Last Modified: Fri, 07 Jul 2023 03:06:46 GMT  
		Size: 51.4 MB (51360865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e8e3deeebb7c8a7bb67aece3b8e15d0f882093bed0039cf0bf7b9ca32398e5`  
		Last Modified: Thu, 13 Jul 2023 01:17:19 GMT  
		Size: 82.3 MB (82311155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
