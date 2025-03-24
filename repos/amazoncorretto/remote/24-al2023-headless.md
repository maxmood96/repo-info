## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4dcbef751932e7759e606e861236f8a7dc1067c76f50753607d09d2fab6d33bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e406c3f2b118409cc6e0a80b67c12e8610feb6aa5573afac3e969e6ea76ce67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155399108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59159760578c658e98206c89a7c82ce92e8e78d7332f7a920a9d535d855a436`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Mar 2025 18:35:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 07 Mar 2025 18:35:37 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2f5360010c821e6961bd41930334b43ed8db5e71c9478170b0676b669f5a02`  
		Last Modified: Mon, 24 Mar 2025 17:04:16 GMT  
		Size: 102.3 MB (102272232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1f5d912482c1869b7b4d69eddd8751f86cd0ba05e5bcad2a0447228199ba1c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5180663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee73930e77679d0efed8b658adff10440b719d60614e0de9d3b206c779058efb`

```dockerfile
```

-	Layers:
	-	`sha256:e35b8148dff87ad46a59531dcb1dc2bff511c6711ef8d43feadf730caba97482`  
		Last Modified: Mon, 24 Mar 2025 17:04:13 GMT  
		Size: 5.2 MB (5171589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c61b9276af8862d6a1ee9d3215d6afd9fc69f5ba1f696b0331ba4fe4cdf2e7`  
		Last Modified: Mon, 24 Mar 2025 17:04:13 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c1447c313e7c67148783b472903e383ed22d4f8fd6e0ac5cc05b4bec99f4c469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153511949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f91888b085f15b1df9686d1b4b83f492fc3e8212c0c4b325aa3039ddbc2e99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Mar 2025 18:35:42 GMT
COPY /rootfs/ / # buildkit
# Fri, 07 Mar 2025 18:35:42 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8491ca965b68d39b6dc49f0a0e34bfc83346de889ce4d67a9d6f1621f0a2fa`  
		Last Modified: Mon, 24 Mar 2025 17:34:26 GMT  
		Size: 101.3 MB (101265971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:096e39619bbd1c65f5733c5a83e697f763a568c97223edd804d2ed9e877b3b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de27bd4122fb020cf49b4abb0890fa7a6fed4e816a443ba98b16abda0471e0a`

```dockerfile
```

-	Layers:
	-	`sha256:0246f345e35878d48111d0479af570b9213b6afd619fbdc1cf28d9647c43237b`  
		Last Modified: Mon, 24 Mar 2025 17:34:23 GMT  
		Size: 5.2 MB (5170400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c82b1ab828b03f681b30ce3ec66c55f65e757287509d0d6be373ff3af51f415`  
		Last Modified: Mon, 24 Mar 2025 17:34:22 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
