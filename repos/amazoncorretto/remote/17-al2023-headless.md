## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:c34872cf3860e48e895c259ff6a484bb31f29eeeaf2938b46376cdae472ebe8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ae4c47efb913014c98aea2f9ab5581e26e274926f36318cab97c88369108cb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135262039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1d3806194028473d6888e317b90556210ab8ca12245f7fe91102e29ba92808`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a2e8122f4c852d604a3ff5e6650100665488cf1de3c06e5533116d32d5aabe55`  
		Last Modified: Wed, 29 Jan 2025 02:05:37 GMT  
		Size: 53.1 MB (53149711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f678ee54b195590cc486ed2f3532d1687415169698baf4d095a1407ce1c2420`  
		Last Modified: Sat, 01 Feb 2025 01:08:46 GMT  
		Size: 82.1 MB (82112328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:097481c3d028452cadc4c5974c9ef1731f48c4b2dd767c2e9c4c950a9422930d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ee937a2efae7212b8e7e95b742ecaf37a0ca57f71ff0e74a9513384913d57f`

```dockerfile
```

-	Layers:
	-	`sha256:963dd8be5a10e3ba326c4236945cb2b8787a94c5ca35b29b81c86aeafb15e080`  
		Last Modified: Sat, 01 Feb 2025 01:08:45 GMT  
		Size: 5.2 MB (5159712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8456c4e63c548654cc49273ee95f27a094294b8a130c10d9459f8fad73b25298`  
		Last Modified: Sat, 01 Feb 2025 01:08:45 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:09fd9bc62a04d0def5e877a0e012e80b63481eafa6882ee6f92956e6a697319f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133819937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d904b76e351d3bde55b0c3b64d61a838f033ccd50b3a04822fed6705e47d90b5`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:523a6b03095ed77c021e90dd9cc9c96374240d01b0165f628a7a82b4d9acd585`  
		Last Modified: Wed, 29 Jan 2025 02:15:16 GMT  
		Size: 52.3 MB (52269024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee67f0e71dfd34f63815fbe7110c5088a1edb5113b77acb491d28467c43b2a87`  
		Last Modified: Sat, 01 Feb 2025 02:18:14 GMT  
		Size: 81.6 MB (81550913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0619b8ca98114ef99afb95b9ab2cd9fe8f1ae737c94f2f38d7354c95814892af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5300f35a5fbb3a57acb3c31f7d0d1420dd2ff3cc1626f5d6120b41da881dbcde`

```dockerfile
```

-	Layers:
	-	`sha256:939416b00feb9466216608c25576094d4936899d5dfc758e9aea7e3548b854a6`  
		Last Modified: Sat, 01 Feb 2025 02:18:12 GMT  
		Size: 5.2 MB (5158500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff6d6bb7055882d23ab4d8ff7fe53a91e88814d1e02556e647414eb1c379fa5`  
		Last Modified: Sat, 01 Feb 2025 02:18:11 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
