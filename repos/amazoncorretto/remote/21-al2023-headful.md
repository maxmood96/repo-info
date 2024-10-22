## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:04580fe011438bc098c0b5a3a167240811b589c801701c722201649d2bdbc37e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e0d9293f1f9387c1a1c7eb0eb90c5bdb6701c64ce404d7705dec708850b26047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141973457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2531be504461f58f540c01bca18b0adabe43417756cf67cb86bb56f3a783bda`
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
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caba7b0b101b6f0ba33b2a048242f79d103d0c7415cfc59e606484c8db01cc58`  
		Last Modified: Mon, 21 Oct 2024 18:57:09 GMT  
		Size: 89.6 MB (89629625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7717826a91b8f22dba21d9cc8a1b74c5eb8fd103640d0dde9cbcae5b7df3b21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cd2ab4bfbb9d1ed9cfdf1fc1543f1477ce3712d4a9ad4ab9ae5d835607bf36`

```dockerfile
```

-	Layers:
	-	`sha256:d44e450a1d299250081e52cbd4bdbcf367de6c14ae8562bbd29bbd69593596db`  
		Last Modified: Mon, 21 Oct 2024 18:57:07 GMT  
		Size: 5.2 MB (5211479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37ef037a39e4d153afa5145892b7abd20d98cce382c577ca6971e0a094d3b90`  
		Last Modified: Mon, 21 Oct 2024 18:57:07 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:de50d9603161162f2d3cc067d9d4764ac3e706998cd1b07f2f195f963e70191a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140172432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eba4760a7379d3d5a7fcecde251dc6f3a75867a1e3cc147e4baf493f5d1a2fb`
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
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dda976ca47dee24ae14db44d26f46824368a9883f73f3480577652a37c7ca2`  
		Last Modified: Mon, 21 Oct 2024 21:05:44 GMT  
		Size: 88.7 MB (88747905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aa1558a4fc2c987956bb63b57582f787949239f3f9e0199ca27e37735db99cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033715a02d35664fa10cf5a0375cf00bb51e4acf9c6f6ff633d9c5f8098f0300`

```dockerfile
```

-	Layers:
	-	`sha256:dc05603837439e043dfaaefbed4e700042060773df6b9ed304d64e851d39030b`  
		Last Modified: Mon, 21 Oct 2024 21:05:42 GMT  
		Size: 5.2 MB (5210270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce76fbbc719d927d13ba0eb48c2aedca2a246e53493a6e4f687e0fd17f67b8ef`  
		Last Modified: Mon, 21 Oct 2024 21:05:41 GMT  
		Size: 9.0 KB (9012 bytes)  
		MIME: application/vnd.in-toto+json
