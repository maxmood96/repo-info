## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:7504fb39f94678a83b7484a1ebfd2f6ba999b800b1f5614c45f2dc7e0ff94008
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2e28ae7c808607c792013d45d38ae308ca30f402c6071b230a6af594a615e44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142612093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc13f2b39d93a7d95f2931b849c52860298f6ba06a0b71c4df1ddff133483007`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b496102f35925938ed2bf2a60201103bb883a0f869ab47e8b90e706ed58e39f5`  
		Last Modified: Thu, 25 Jul 2024 21:02:18 GMT  
		Size: 90.3 MB (90297914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:023e69f9562ab32d8b7ef708ca9fa7d6d4ed591f939106bda968093d48a501ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6fe81faec0cf139c7dcdf12750721ae9a2b3e9239d3c87aba33cf615d3abd2`

```dockerfile
```

-	Layers:
	-	`sha256:f1f8bee2cc3c32cf451c038863589421a5e64d28ff758a8cca6ec26811d64bb5`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 5.2 MB (5210076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd9be5658c055254b8a1ea81a6a6bf294df8cdecb4434cbd129f9f30b35af91`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 8.9 KB (8893 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c832debfccb6cc3f7a41c138b9b8a3dd9bf478b049680ef48f3cd1afaa9b2671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140754228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331eed29b7802bc7982016ff17735ae7a6acb645c9b3d212ddb83d3234e6bae5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75135ae2bcb204d3424605d578f60133d664f4068ec9d44703196e31fb3b38`  
		Last Modified: Fri, 02 Aug 2024 05:50:18 GMT  
		Size: 89.4 MB (89352216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4c7107e97e462ef86bce98cf35a75a5fb20d35fff5377cc19b183227a991bce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02af8255749463ea7d76b5e32f4aa3475eee58e4a9698f1ffad69c5f78d8c0d`

```dockerfile
```

-	Layers:
	-	`sha256:e3505b74fcb4719a0cb59667ecb9a143946f4655be904ac7b87bc27b015052f6`  
		Last Modified: Fri, 02 Aug 2024 05:50:16 GMT  
		Size: 5.2 MB (5209947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a9c4af94c0b385c539935c501f01d6873b91edce574f9dbd131d4c9f08c665`  
		Last Modified: Fri, 02 Aug 2024 05:50:15 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.in-toto+json
