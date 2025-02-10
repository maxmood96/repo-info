## `amazoncorretto:23-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:d41a425326f67c13caeffd800119cfc33af4766d69aec85f20a6c67b2502885f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7883aa5a7dd2fa229ac1625742c828206888ecf0b83fa691e327f5974c342025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147001843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a605cbbd37abbd30d3dbeffdb9a3bd6c95d36fd0c0480d28a0b9348dc35a2a59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d20994076bb072d4a3c138b0ad339da49183391a43a64c121520c0af009915`  
		Last Modified: Mon, 10 Feb 2025 20:08:43 GMT  
		Size: 93.9 MB (93851260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e27c1e5a65c35738a893a7a41419a7bd7eb4f2c034894444fc29fc36fb83c6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d3a750a5253dd2ec1e9e1fae0658271b5d89343359ce0a11fc777be7eadac7`

```dockerfile
```

-	Layers:
	-	`sha256:9286eb4df189ada6c0cf550dc71c64e42a50ba1bc805d30dda19a2fc5198f4d0`  
		Last Modified: Mon, 10 Feb 2025 20:08:42 GMT  
		Size: 5.2 MB (5189400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad653598ece26bb19525f7ffc02c7e2f60372ca26405b17d7a3076caeabaff6`  
		Last Modified: Mon, 10 Feb 2025 20:08:42 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2afa87f78a6390dbbbe6378cab7428b581edd266c3197c0c0e931c2c7dd5d8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145136171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c03664abade60f02c172bcafc41cfdde60998ae52791781ae46f9b681b13c2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e0019fc701733026aab99a1b5d56357fe1a71a984142a547bff34166e5a368`  
		Last Modified: Mon, 10 Feb 2025 20:31:16 GMT  
		Size: 92.9 MB (92865220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:422eedaba99ff7eee96e3cd688c61c62f4ff116ce4c79c4ee477345d056c89c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ed2f18ae12a1f0b39c582ee504ca4f345f2782e3d1013bbdc0cf3074899bae`

```dockerfile
```

-	Layers:
	-	`sha256:0742ca1d809dc7854d507fc94283ff41efe67d4585c1ba5d9c599a86a1d68146`  
		Last Modified: Mon, 10 Feb 2025 20:31:13 GMT  
		Size: 5.2 MB (5187392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0889b7b3e925108b8eb2bd53be4fbe61f615a65e8504cea252763e3170ca830f`  
		Last Modified: Mon, 10 Feb 2025 20:31:13 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json
