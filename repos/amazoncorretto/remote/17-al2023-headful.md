## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b50767810ca5401188bcf3b5830f943e5e0365b0569942a51dede523b71e33b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6763a717b2f66189c691b506add0593379911cc5765b6dfcc1bae3c6aa992701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135984129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078ac67e55fbeea5339c056136ca69cefe8dc0752a087389a89f07fe728c087c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23128d959f48eab55217469d736065adc665e1979f3ba481deaebd7350a6bf18`  
		Last Modified: Thu, 13 Mar 2025 22:53:04 GMT  
		Size: 82.9 MB (82857253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2e27e115d59d2f060021896383c2ccfdbe94fb63c13e93d1fa3ac974a0630f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff0dc0ff0cea6f354fe4b004fc29cb61ca2623153175076dc61c72bfd9dcbf`

```dockerfile
```

-	Layers:
	-	`sha256:b6d2160fdd81fc735021d133e6c5409637991818607cfbaf6d6c115033515bd8`  
		Last Modified: Thu, 13 Mar 2025 22:53:02 GMT  
		Size: 5.2 MB (5184962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d3f23ecb371321d870e9b268d3fb03c1b652f2cc53a09b9a9e9157e6381a5e`  
		Last Modified: Thu, 13 Mar 2025 22:53:02 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:84a297d8eadba97c07791e245b0c4a4e45414077104f28cdb94697f32bf0212c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134547654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdec45a9c6aa71299342ae60ebe6a2d15b795d133923885b0f06edb85b157006`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ab750feac752895d7d179c4ea7bed1e98b0f15dfbc12c1c080209851aa00e`  
		Last Modified: Fri, 14 Mar 2025 01:13:43 GMT  
		Size: 82.3 MB (82301676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61d10b8a59b37f59e40ed01dd3e4ab4f9b134ad85a28d97afa3b578ca656eaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faab3333e624155c3bc160546f521fd4007a33dcd065b5f34fc64344f43630b6`

```dockerfile
```

-	Layers:
	-	`sha256:0ca61c51b79e4e0b2871d61fa84b221e872eb3c27f70105811a079b82932e03a`  
		Last Modified: Fri, 14 Mar 2025 01:13:41 GMT  
		Size: 5.2 MB (5183753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02086cae6e086bef2c2283a0ae2731978b7dc6c8607e72b08a5e93f16d9833b6`  
		Last Modified: Fri, 14 Mar 2025 01:13:40 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
