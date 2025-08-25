## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:54db3dbfa07f29fca7755de7da9f4a4d836ce388dc631e43021f59f178fe7aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6f06944e82e6825165bf9f4677331c6e80db9ff30378c399f31ff5e2a53ffaca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130240505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2a7bb7d260b0bd4517d16c89d24484617820947d21798ee2fa9270ed1a4aec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711434c5cf4bba42e565447e42347a80c03198db2e6716127b7c22fab889ec94`  
		Last Modified: Mon, 25 Aug 2025 22:02:53 GMT  
		Size: 76.4 MB (76371775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cbeed785d04123d3dcf34b2e00d9e242d751706f54a19ff41d1cba188a3e510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c44a58e36dacacc8e8db361cd4b373bdc56047b4c9ddf1e9db3862e8750866`

```dockerfile
```

-	Layers:
	-	`sha256:56246b829fe746a2e8152bac4138ad874b29548d0e256d10d784b5f72d5ec205`  
		Last Modified: Mon, 25 Aug 2025 21:47:39 GMT  
		Size: 5.2 MB (5196743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ef7d6c2fcdce30efbf663859195700bc2f0197fcfaa952e6e530425fd0cf3c`  
		Last Modified: Mon, 25 Aug 2025 21:47:40 GMT  
		Size: 8.7 KB (8651 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bf2726ddea80ddd85f610310bbec8ac25a8d41d3547c0a0331a7684c76cd90ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128312557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6141834f4a9b08ff1db476b2b5fa9ecb0e26f05ff7259c76e1dd707f969229c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562dbc18aab5fa0628a686c7b3915c0092a0f044c137be15c61e9ad2c0411c01`  
		Last Modified: Thu, 14 Aug 2025 08:54:04 GMT  
		Size: 75.6 MB (75586163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f3e7ce9fe6c571dc0e3c33cb5fa80412c06c7c3601b326511fedcecfba5e7799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7b26868ae754d5e2aa3aed65af37d3e0d09f9704794c34e476335d5d49e9e6`

```dockerfile
```

-	Layers:
	-	`sha256:899266d0a46145f1ad4144789fe91430e7b48296053852858ecf902ecfafab2e`  
		Last Modified: Thu, 14 Aug 2025 09:47:46 GMT  
		Size: 5.2 MB (5196361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fcddda1da211f0895e58833984721d06f48cd38a47ae43f50ce39124cbb0873`  
		Last Modified: Thu, 14 Aug 2025 09:47:47 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
