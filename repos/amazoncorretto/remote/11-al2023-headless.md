## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:51cda1db4a319321c0cfd967ae4ba0df962ab309037cc2da8274bd523852206a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:54c6b61c95d003d8e0416b1d818db3912e079751bfe420c7c70c09366e91af6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130001158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9350b9463a1b2e79425fd82a81deb940b83112abe5529ecb6f09fc9021e1b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:06 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:09:06 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:09:06 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20f46cb7090dc1e3f37c4de92651b56e4746521396a6ea0b865c7a942a5e7b0`  
		Last Modified: Thu, 15 Jan 2026 22:09:28 GMT  
		Size: 76.0 MB (75979954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:065e0b9109b506d67f7777faadb123f518e5a53d95148e7ec651a27efbeb7dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a2cda157d78994e18dbf7f18a103d18e332baa5e9f4117943fb54a0bc607f8`

```dockerfile
```

-	Layers:
	-	`sha256:131bcb8a18fedfda13fbeb07c0f17c22e936e572cb8579cc879bb9409e8b0e6a`  
		Last Modified: Thu, 15 Jan 2026 22:48:46 GMT  
		Size: 5.2 MB (5196823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b03d159f1917a1fff4fc6371d92d9baf289d84212ff3d0b4fcaa3b1eeb17666`  
		Last Modified: Thu, 15 Jan 2026 22:48:47 GMT  
		Size: 8.6 KB (8607 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5db615c1b2e4c7eebc4e01d590a4ca692b3af3711f400a649c2c36166fadf911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128123967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813dac9b037cd2208461d5979703f5d5744e745f2d501ac076a27ca2334b7d4e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:36 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:08:36 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:08:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9950ebd341eb86409ad0a3aaecccae49a4d3b1dc2cd2c62be14a9ffeb83b7bb6`  
		Last Modified: Thu, 15 Jan 2026 22:09:17 GMT  
		Size: 75.2 MB (75209610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61cd80e05fecacee17e2bd7fcc19f13589d1b02a869df5ff9a576d3a9790a1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f008f29316b27ef4fc099b6238ad4bbfe53ada78a412cae87fa73135a2937ea`

```dockerfile
```

-	Layers:
	-	`sha256:b7261c2db4162a70242749dd038cf1455876c8d86758c8488ee65175bf2ddb1b`  
		Last Modified: Thu, 15 Jan 2026 22:48:53 GMT  
		Size: 5.2 MB (5196441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f0359f861eebdd8166a05d9fede804c351959db1d6293b60204e42a543cdda`  
		Last Modified: Thu, 15 Jan 2026 22:48:54 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
