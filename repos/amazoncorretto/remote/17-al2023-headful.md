## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:04a8002ef12f9b4d2406f9e92bd5c41ce50e0289e0169bec90405f4cafca3b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a03a373f280f666d3dc9b14a444e9a3e0e20234b0343cb62e2a520b509b5f5e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135501572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7269a2100329e1c0c3dae04b76eb608008b19e2f94de3e975915fe53afbbecc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:20:08 GMT
COPY dir:acd83a6b32519bdad84d6a4d016402a3bfbd7ec8056e92d01a2222fd4cc63d9d in / 
# Wed, 26 Jul 2023 19:20:08 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:19:26 GMT
ARG version=17.0.8.7-1
# Wed, 26 Jul 2023 20:19:26 GMT
ARG package_version=1
# Wed, 26 Jul 2023 20:20:22 GMT
# ARGS: package_version=1 version=17.0.8.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 26 Jul 2023 20:20:22 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:20:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0ccf2bf65eb109135ce4e32ed827c8fd4df1396c406122da0b40d4fd7f088839`  
		Last Modified: Thu, 20 Jul 2023 17:41:27 GMT  
		Size: 52.3 MB (52310872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b85fb836a282a6ee3520b21d2f16425f594e02604a33162d3751672d948747f`  
		Last Modified: Wed, 26 Jul 2023 20:30:44 GMT  
		Size: 83.2 MB (83190700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:58d783aa45e788ba2a9601a41fb5f6c804340742f7acd6bf5afb3788672a16ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133866584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379d86e2c5637366ffd0e0fe52fbecf919587e207852e95106c9771032c2659b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Jul 2023 19:39:44 GMT
COPY dir:ab5df2603dbae327b5eecbb1ba196f5a1f17cd096f7248968ddb73809ff1f45c in / 
# Wed, 26 Jul 2023 19:39:44 GMT
CMD ["/bin/bash"]
# Wed, 26 Jul 2023 20:21:53 GMT
ARG version=17.0.8.7-1
# Wed, 26 Jul 2023 20:21:53 GMT
ARG package_version=1
# Wed, 26 Jul 2023 20:22:41 GMT
# ARGS: package_version=1 version=17.0.8.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 26 Jul 2023 20:22:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Jul 2023 20:22:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:91b7fefd504f27afc9eac17100f8e7fa41446c3fdfe003e74025c20a9adb95f3`  
		Last Modified: Fri, 21 Jul 2023 03:06:49 GMT  
		Size: 51.3 MB (51349707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ce23842d88fe35ec11ba05ab90e52f3e02c89fb88c365c72c4b4caef22d78e`  
		Last Modified: Wed, 26 Jul 2023 20:31:02 GMT  
		Size: 82.5 MB (82516877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
