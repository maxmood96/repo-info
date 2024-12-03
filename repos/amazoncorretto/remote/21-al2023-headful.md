## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:2416bcd59eb7742fea2b1400c206cc49fb6a110563a7fee18042108b3187d07f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8be865872ec89523fcf4fedf993ad0471ce4558e6dad553f832bed6801e591e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142016047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61598962b52c0b0781b1b095ab0bb9f626de2cc826a8b568c8b0e1ac19bfb9fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:4a665eb63bc8cddb90e1e74e3ec745a1bab733c919dc4b2d648b43459295464a`  
		Last Modified: Sat, 23 Nov 2024 01:38:06 GMT  
		Size: 52.4 MB (52377532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f0125ee54ba2f2ed053e82b8240b54f5ad887c9a8378c705c38e29f16d70b2`  
		Last Modified: Mon, 02 Dec 2024 23:23:28 GMT  
		Size: 89.6 MB (89638515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f2a909b8c0170c6cf56e09052a0a35bd637fd88661d452389d75b50845e6d30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b2448e98c1d65042561e2466ab335b3d4be3b6e25ea9236d43d8dab86be412`

```dockerfile
```

-	Layers:
	-	`sha256:c49b2b92e0f3d6ac5ef0432f6321b8e88d7691321ddac2d8f949790fa926067a`  
		Last Modified: Mon, 02 Dec 2024 23:23:27 GMT  
		Size: 5.2 MB (5211478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22e813ba31bae2ebecf79d9e7fb07425250ed0c5a74c8d30c146a84f109e8e8e`  
		Last Modified: Mon, 02 Dec 2024 23:23:27 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:284009f891f5cd3f603f7954d7b4455e85894356b0a087cb5101b41a4bc5923b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140211695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031d61056db44d6290bf320e522e588a6f49a30b2c23b76d19bfb36d90caca1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e552b86f661d58b9525c69a3cd36085e1d00900fee75d9124b41da98fd039e9`  
		Last Modified: Mon, 02 Dec 2024 23:30:17 GMT  
		Size: 88.8 MB (88755851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:635997bae6260f88e9aa002cf57bf7357529720d4e7710b33b21b0617227ace1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa48869e2ac5f2949b28af6fae0525ce81b4e122403f1adcca9da82e9056dc`

```dockerfile
```

-	Layers:
	-	`sha256:8cde17cd4de6b9906f48af940678663d23b29e659300055932451cc9a2d6e798`  
		Last Modified: Mon, 02 Dec 2024 23:30:14 GMT  
		Size: 5.2 MB (5210269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93916bfb2aeddff18c076402204afbe9b91787fe8372f032fecca8cf615df89`  
		Last Modified: Mon, 02 Dec 2024 23:30:14 GMT  
		Size: 9.0 KB (9011 bytes)  
		MIME: application/vnd.in-toto+json
