## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:87b7802300cc346dc4edd52679d87c72bdc9483b01531a1906c34ef456021dfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e93c1de85a05c95e307c8f80951074185745c6fefb3d7a79e96ee05acc246855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142628599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827ce9e38529e3ffe163a143a00725937f8b62de43e8fbef13b415cddd548481`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870286867a9add402c0d2fc6da5a1e6aeb1c4fa402c9c562f7ba8d0fb1f8952a`  
		Last Modified: Mon, 19 May 2025 23:37:06 GMT  
		Size: 89.0 MB (89013897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5ce6dde1db1c83ccf3c0a05c50d15792d4d2dcee1621de8a8add8abda21f2955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882172b3c4ce6377824c7d9a46d9216a8128d79c2e6a1b079275337abc196e46`

```dockerfile
```

-	Layers:
	-	`sha256:0694bac77706a391cb5dda0b4215ddfada7d2b7fa300f7c023f42832962602ac`  
		Last Modified: Mon, 19 May 2025 23:37:05 GMT  
		Size: 5.2 MB (5182123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7160b0eefbde1b61307c5a3d1009f464b2f87614fff3d49ce721a06a34137667`  
		Last Modified: Mon, 19 May 2025 23:37:05 GMT  
		Size: 8.7 KB (8747 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9dc2f0b02244b4d81fc90d78c770cf0003be7a54435f8f09c6aa6e5c365ca823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140724596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1741549d97609238482f406647af3d58e38b4f0361958e1b1c1479be3d3b5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c30e16f9b3cc4c9880fff60fa80c7ee25130055d06b4267a24de73602fe9226`  
		Last Modified: Tue, 20 May 2025 00:02:20 GMT  
		Size: 88.2 MB (88158859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:daf1e2ba4553312b65b11921f3ccdc4f6ebe39ee006c9cb6a1b096cab8ef8c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1c57d11168177b381c3443a199cee786dbffa80bfa959f8ce3987ab48c47f7`

```dockerfile
```

-	Layers:
	-	`sha256:26c42aeeea9fc217c4e990b1367bae2e9b9ed4514f30bc5d7eb2a81e8a312399`  
		Last Modified: Tue, 20 May 2025 00:02:15 GMT  
		Size: 5.2 MB (5180913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:468dd62daa05e7ce04f6c877468a0f725ce84f76898f03d705b5cbac4a3c1acd`  
		Last Modified: Tue, 20 May 2025 00:02:14 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
