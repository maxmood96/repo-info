## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:589579bb26f1e369d56aec5d6f5b26d9724fdf1c8f6003e12f89eeb78868c6fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9ddcec998ac008e09bc5efca8823923a3e3f3ecf3a54199cf4b186570b5a41a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142839246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787e7a8d60225e835af1bb0a14d090c0f14a2a0b5080dee184845d3211ed559a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992d654545ee878002456801bf12ac5bce4f77f108c4f113b42b5345b2c3bc30`  
		Last Modified: Fri, 20 Dec 2024 22:33:41 GMT  
		Size: 89.7 MB (89682933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b1c75d0617381e2ff09c813e612c26a3b53a2db79b01ab0524a7c1842eff8e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa83e1d43fdfb63877a95e7515bb45500cfc2efc4a2573772529d5614b8aa99`

```dockerfile
```

-	Layers:
	-	`sha256:15b371681409b8e34a98612a56a7d282eebee2a32aeb3b2c8940cdfc6cf2849f`  
		Last Modified: Fri, 20 Dec 2024 22:33:38 GMT  
		Size: 5.2 MB (5206292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54c034782ef6870aa2b8970ba1ee404f75342503ddebf43224ea54cd743e2f1`  
		Last Modified: Fri, 20 Dec 2024 22:33:38 GMT  
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
