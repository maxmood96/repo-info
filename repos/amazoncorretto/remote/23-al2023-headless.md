## `amazoncorretto:23-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:6f4f8c3f4e202757133955743ac9f7bd19f27bb6cc695222040512934c9f6658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c0a30542b5b093a7e134a4474db1f1bef02dd159b3ee813946f98fc6c6667d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146283506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba7570d22f56c1a50dac4436ccddc8d4710c29c4c8b1f17dd350c4261f36eb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99232b3fa37edda1a2ec9bd4deed4d5d1e98e718ea5c97023d0346c9420a06c2`  
		Last Modified: Fri, 20 Dec 2024 22:33:36 GMT  
		Size: 93.1 MB (93127193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:46d4943d34ef1d74389e8f6a4202274a7db8d9c83ebd028ceae27e6852a4c654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcde5e90b3690544b424a08708b5bf2735c3f74afd44676920e7008f777b622`

```dockerfile
```

-	Layers:
	-	`sha256:ca9ed1eea6e2386feadf49fe5c74903fce6a491a40f33e24821933040b6561ec`  
		Last Modified: Fri, 20 Dec 2024 22:33:34 GMT  
		Size: 5.2 MB (5183862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8c46507883be69b78d498dd190791b15824285b982b96661408a254254fde1`  
		Last Modified: Fri, 20 Dec 2024 22:33:34 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c4edbde4cc9d43a53ff9d71f604b8456c1a240c900e3b03bdfba822fbe8a9f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143512146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edbf7d427f9cde172623e1c38c1552b501066451da4c022fdb21907d5502721`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc945fc601cbc50fc30bde764119a6aee592d2a53d19ec9e0f19aa3af76ace`  
		Last Modified: Mon, 02 Dec 2024 23:32:08 GMT  
		Size: 92.1 MB (92056302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e38276635c12b41895f916e93c2d1484ef1a479ced1a2a315a56bf25cb4bed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2121b7afab7fb290259901e5fb0a0d1c0ff9b594c5d9eddbdfccf6da779526`

```dockerfile
```

-	Layers:
	-	`sha256:9cbf89671312f2851ef43fdb27949ecc6d869e6399e3d9c342d2cdd18a29b2d1`  
		Last Modified: Mon, 02 Dec 2024 23:32:06 GMT  
		Size: 5.2 MB (5186958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47824776e08be2a988b5813c354d66bd7886a76a48c72997a81770fc7c19b361`  
		Last Modified: Mon, 02 Dec 2024 23:32:05 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json
