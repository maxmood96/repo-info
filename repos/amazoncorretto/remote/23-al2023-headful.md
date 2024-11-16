## `amazoncorretto:23-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:7575107784e84387658672f0a8a62aac00acc31bbb21455ef11c7e0d5b1da071
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:019fb6c8939833d8ee901e70ee73a16fb8b8fd0b5193e30f703c60b4fd72db24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146185560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733ccae8610224263b0aad0d81dedba468b7eb7ad1a75a907c22a94ca801887`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:46453255c2f610c1cb9c8197635e6d542bbd326425a9898df0de76e5bb566461`  
		Last Modified: Thu, 14 Nov 2024 23:11:22 GMT  
		Size: 52.4 MB (52379519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8b04b47e137ea4e09cc9e450e94086e3570eb93f8944ce06e67bec57bfe80`  
		Last Modified: Sat, 16 Nov 2024 00:48:42 GMT  
		Size: 93.8 MB (93806041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72683ed71f4ebcb742b2c214371296902e4666cbe2eea98d6d8bc7e0b7e2798b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3f35a0b7da5e8004bf2d91aa0f07dfff3b2fb40dff12be772a19e73f246896`

```dockerfile
```

-	Layers:
	-	`sha256:6f5e63a38bcf0974c54daeebb07b2a5393e474215346a04bd58633c1d489e7a3`  
		Last Modified: Sat, 16 Nov 2024 00:48:41 GMT  
		Size: 5.2 MB (5214297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3545dc36fd272c621e844cfa4fce94f7aca93bc4eae6b6e9f1f480122896faef`  
		Last Modified: Sat, 16 Nov 2024 00:48:41 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5223cca7446a237df5856c9047260a2d1c763479a01de90b19f9b1c6de360a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144246598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd59d032ec8f14c663d6b6ec2ab4f998c993db558d974a29b3ba33ccf4683e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:aa4cd91a180503f7c5ac34b85fdd22c27356599a1d700f978c6d2fa5858867fd`  
		Last Modified: Fri, 15 Nov 2024 02:20:08 GMT  
		Size: 51.5 MB (51456561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778c1c2cbe5cade92e8d1f0ac52010fa129e4682d455f420fad2af11d2ae0509`  
		Last Modified: Sat, 16 Nov 2024 01:12:53 GMT  
		Size: 92.8 MB (92790037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7b34d2f3256b0060fa1839cf1f2fbfdff69622853643f6a1d724ff71db3ecbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9ab74728d68b0c568b814356d0fde57cb1f03c1a09d1e422c3a2e43ac917c2`

```dockerfile
```

-	Layers:
	-	`sha256:e7d232ec8bb4960145de004a17ab94f77e3b90cc3682c8d67681408c7d5f6d15`  
		Last Modified: Sat, 16 Nov 2024 01:12:50 GMT  
		Size: 5.2 MB (5212286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a4ff17b0227ba4c21c01ad8a17866eefd27c8633c6665e80eb5aa9263b2e5d`  
		Last Modified: Sat, 16 Nov 2024 01:12:50 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
