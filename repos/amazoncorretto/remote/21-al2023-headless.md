## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:8e0c31b2e8b1e594e685e3899e80d0c11c42070ea7cc4c5874186df1be0c9895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:84d19f364c9bce0a312279030100afcd1e00092328556cb5c73bbe6ed0f08fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142112571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d4b4a55a94ae7370844f38181f795dc6c809f5991fe7ed369ac1f998898c12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8382d2da9d1fb8a1afedbe02877c04151ce009cf527ae12aedd9f83cf26e88`  
		Last Modified: Mon, 10 Feb 2025 20:08:43 GMT  
		Size: 89.0 MB (88961988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:edc915399b43ee9ebe6f0529c9f0a996d1e42f25e88690ed8e75978e8b009a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd65c178104c0f30d2da5512aa971e9100f8ecbb453c5b0aa5972457bb8c56f6`

```dockerfile
```

-	Layers:
	-	`sha256:979a771d958d1da7c89ce9e008a78adc40b3233e641467c36027b834a6f3c447`  
		Last Modified: Mon, 10 Feb 2025 20:08:41 GMT  
		Size: 5.2 MB (5161330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7200f21e68eb4b1613c79698534128696c4d0499f16b5f4f88a9d45288183a29`  
		Last Modified: Mon, 10 Feb 2025 20:08:41 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:691a8022f9b99a49e9f74da1b72f3b509309cb0fa2ac705cbc8b3dc8386c9380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140369358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89743ee0bb0798ca7abbe4f2d1592a3c51ec4e4853d9995388c8fd0f7e93fbae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c056a0ad6ef34f129146204a318131b1b9830341223341657ff72f51a9721e22`  
		Last Modified: Mon, 10 Feb 2025 20:27:59 GMT  
		Size: 88.1 MB (88098407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ca9112d1e90fde9f00dcd9c919b4b2ab2dfa9415fecb2ad2b2fcb1ddc30735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523d5e9c21ea15ceaced91cd6334a59f39f8fc587218454f9ecec429082028d7`

```dockerfile
```

-	Layers:
	-	`sha256:f0111093e16556e58e693166e3a0ecdefd577a655b2b463b702d541f37dedf23`  
		Last Modified: Mon, 10 Feb 2025 20:27:57 GMT  
		Size: 5.2 MB (5160120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599484c481df48f81c2de2f79e109e31e3301e330f1208526c6108ccebb7a546`  
		Last Modified: Mon, 10 Feb 2025 20:27:56 GMT  
		Size: 8.8 KB (8827 bytes)  
		MIME: application/vnd.in-toto+json
