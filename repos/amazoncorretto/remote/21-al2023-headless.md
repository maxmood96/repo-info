## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5d33ccaab0b2ad69748a75a784030be90e1c69c1a365ed57baa43b51b26e979d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fe27964281a3624d0114f0ffd20ab1f10af05ba2fd32c91b7c9a6f2267db0401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141249467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32dc5fe37cbc80955579e47b281e47d3a0e41fed4ca2542a54c9f5f901d190a`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:e6830262bf4ac13870b0dcbdb3a21b1522b04ae6fb8890d97520f1a184e11605`  
		Last Modified: Mon, 21 Oct 2024 18:57:04 GMT  
		Size: 88.9 MB (88905635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:90f1f259794d7c5d284cd774ae3af2ee1a9679609b7c8957aaddc655827c548d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2653121ba55c37e273c993d4771d1cfe61efda0563536d31d47e9e4da1620674`

```dockerfile
```

-	Layers:
	-	`sha256:31741fd64d9ba11c705a4b035808ef5d44ea90fa6a648d883d49466287ce2db2`  
		Last Modified: Mon, 21 Oct 2024 18:57:04 GMT  
		Size: 5.2 MB (5186150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5533249d4e6d8f8a9a6c7f22a71e973ce98c5fdfaaf3139ddcf490e9cb21a5`  
		Last Modified: Mon, 21 Oct 2024 18:57:03 GMT  
		Size: 8.7 KB (8749 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3fe4f7fb028f9a1fc919d0216ad6ecb364cff73bc50eca4c8e46e414da99965d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139383672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18d40a522cd0cfc50a8933acaecb6626f618d4b6460800fa3354021b6fc70b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b87362a34d915674fb8e37ee736d0e621f1ca0eace2e3853bbae6f3c70dd48`  
		Last Modified: Wed, 16 Oct 2024 18:34:39 GMT  
		Size: 88.0 MB (87957308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42c13d4c24971b081db70364c562426d0a3868ffd5c62a3ce1f077a5f217e1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63239b72fe9e6d92837d77ad36028a31859520c1f4f24d1f574fdf31a1eb2047`

```dockerfile
```

-	Layers:
	-	`sha256:ed672c94357ee40c11568e7b5cc56134c0799ca215e296ca9b540eaecba91c65`  
		Last Modified: Wed, 16 Oct 2024 18:34:38 GMT  
		Size: 5.2 MB (5184980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1495f3e98b2c2f88bb91e66845acaa8c62289cd0d0592b437cd4b84a665ed6`  
		Last Modified: Wed, 16 Oct 2024 18:34:37 GMT  
		Size: 8.8 KB (8833 bytes)  
		MIME: application/vnd.in-toto+json
