## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:f3403ef94864ca92b6603bdf92a00f1d8329faf40f0b28852085624c6727466d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3ed413627a09175b1022b471f27ffb3f726c5ebecdaa3d2707485dc48894d7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129220635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548087554c1cb89a6f9c78d09928c14c3be316c19d3902edf8ef6c06a9e06196`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff2305fb8f7460912ca0851a59aff893fb1932e58fcd3fb56e9e9bed654ae5c`  
		Last Modified: Mon, 21 Oct 2024 18:56:55 GMT  
		Size: 76.9 MB (76876803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a412b7e047144162715e1cad58849f6e79fe0f3267cbd1f40a8c469aca1e7803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1d237f57a39f1b37094c68e9bcc1172b3e389d244a9dcb0345a0fa415d1294`

```dockerfile
```

-	Layers:
	-	`sha256:142329e982afa85a5284af11c5c098066d25e01ce9bb4c9c3512297432453afb`  
		Last Modified: Mon, 21 Oct 2024 18:56:54 GMT  
		Size: 5.2 MB (5223795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6373243a0d67cded23efd99106eade3e39e57e5e3370acaa72a9d5b06b5e67d`  
		Last Modified: Mon, 21 Oct 2024 18:56:54 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a9d8aec75b396dcad55f2a154cc54e92eeccc37c90685ffa94bc666cce9b2f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127502805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ebd8d9f6dd7e51e11d7c48b4fc2b77b88288ff9cd7c6c52ca39048c5cfce53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab351925a4543ccc590d8621e51f5b58fc630000d5851140b9a20086b99b5ff`  
		Last Modified: Mon, 21 Oct 2024 21:00:21 GMT  
		Size: 76.1 MB (76078278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8dd457ff4b96e5afb7928e07b4ecb9586f1f9a6139a3e9ed602747a78641fd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f200a42cf81a58c29b581fc44988a0bd9500dba076d9fa73a024c58e4559b3`

```dockerfile
```

-	Layers:
	-	`sha256:65618fa0aacf286a00c62c41603d9b6c0cce3d7a3dab525325003bca0a990b72`  
		Last Modified: Mon, 21 Oct 2024 21:00:19 GMT  
		Size: 5.2 MB (5223415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76faf48017caddabce1ea6e78c3c28da1d9cc35119ae49cc7d1ce0cd69f7444`  
		Last Modified: Mon, 21 Oct 2024 21:00:19 GMT  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json
