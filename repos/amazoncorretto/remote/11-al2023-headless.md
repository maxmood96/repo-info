## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:c1be55626f973343613f8e1e18b645a480e18d7e385ac5eddcea020e1a46dde0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3bbca534540ed2d12cddf1416cc93cab4eb827ad917e3f11268539648ac3c76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130087408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a98adeab406c34bbc1cba557db42535d9e505aa9af8254b27b95ab9f20997f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eeb4e3721f160dafedeb41da303018cb405b7d5ffce058841166d4d9936acba`  
		Last Modified: Fri, 04 Jul 2025 01:17:25 GMT  
		Size: 76.2 MB (76247197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c97cd73032a693c09e66471c1c01af32608ce194cb780588597d1ff17f7bc0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69c5f79c193cf53d4ab188610b0f0a693c7f9da570ccfc83456da16a346bf3f`

```dockerfile
```

-	Layers:
	-	`sha256:984dc6adb4496f4e402c256fbe46fb107aba64de87a146fbab51e0f2b65c5a08`  
		Last Modified: Fri, 04 Jul 2025 00:47:40 GMT  
		Size: 5.2 MB (5197452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6d4a6e4a63b8d44c4fdb2cf7d61c02d37766841b454176fb95e7fe4a7ed8844`  
		Last Modified: Fri, 04 Jul 2025 00:47:40 GMT  
		Size: 8.7 KB (8650 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bd5812adb9c5b8ddbda3a556251eeebecdee0f66dcb10b8d0f1a70c769995d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128180840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc824babe932e1be297e2a6893d633f90c7c6e7f0b8791872f8363bd5b6cb4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0e455f237a70326021a937388393d9d7ac6f9ae1616673300f248aeb280add13`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 52.7 MB (52717557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9517554877657b8f151fbcf9b55f0f1895491c94c1df0d4fb3b6f77a291014b`  
		Last Modified: Fri, 04 Jul 2025 04:09:52 GMT  
		Size: 75.5 MB (75463283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4276a9d7a4d67e954994239622516d917560cae6f8f9291cf2093855ff9f5a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ac3d6fa16d2137186bc5a28058d38b25b11142fc9f272005eb31d236d715c6`

```dockerfile
```

-	Layers:
	-	`sha256:4751f1450da225bc8e8e77af827470e2a3520c0f8f61e4627321dfd87a61c7d7`  
		Last Modified: Fri, 04 Jul 2025 03:47:41 GMT  
		Size: 5.2 MB (5197070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc09e09011818e889fa1822f57cb93a38cddece1fed5aeedb6858f5da540b46`  
		Last Modified: Fri, 04 Jul 2025 03:47:41 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
