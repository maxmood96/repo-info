## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:7eeda994112f3a341b58c38f9392930e07d6b61d687c0663825813baabc8a2a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9ae40fc4383686bc5d7e00dca49043d65841b909af95fa1a82bced4efb5eaca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145386157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ab05c3951bff4f1f413d93381aa15408a6809f51ca152885a3bc6439e31864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
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
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63ecc0f8b1832f802bdcbfbba8570ab8bcdb7f32c9a5aa59d20b0b041fc924`  
		Last Modified: Wed, 16 Oct 2024 17:57:38 GMT  
		Size: 93.1 MB (93060852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:709f2907a67adbc5acb213c05f753c48684142e4f791c65504c2a737b6bf7544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf213054c93c5c0a416c032a73e8f403fb2b2a79155e85e85fbc5742bebc5dd2`

```dockerfile
```

-	Layers:
	-	`sha256:4363bb1a3de5328e9b6bb8b32f56fe6b7fd5dd4f4b960d6d0bd2cddb8b170a32`  
		Last Modified: Wed, 16 Oct 2024 17:57:36 GMT  
		Size: 5.2 MB (5189015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43ba1c84d2a334a7e100f52d99b7d94c1102e3fbcc31e8d4f3b3da0e16bc1faa`  
		Last Modified: Wed, 16 Oct 2024 17:57:36 GMT  
		Size: 9.1 KB (9076 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0902304535d8ca0727c8bb6de6e51473bb53d398b51311f557fe6c66edd9c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143413040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193e889d6e158cd23c79c431f28c6dc8013c3a05bf33bf11e361a321c910398f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
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
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5715d1f42aae9009f8530d413e085db04bc4c35e797557f00dafa86c66ac6520`  
		Last Modified: Wed, 16 Oct 2024 18:42:16 GMT  
		Size: 92.0 MB (91986676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d7bf3f33f58592c8faaaca15e0c732b4ddc838745cef4eff0237cb7acdacea93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3c106283f00bb14aedbd5c0fc3812121a5573c89b517e6b526097e45323c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b06f5b672d1ee715aec551bd595624e9ad5afb349e11425dac33cc7c43c6e7bf`  
		Last Modified: Wed, 16 Oct 2024 18:42:12 GMT  
		Size: 5.2 MB (5187001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d46b684389ba8725a0a4f4021e5c234cf14c6f922992059520860dfd544508`  
		Last Modified: Wed, 16 Oct 2024 18:42:12 GMT  
		Size: 9.2 KB (9167 bytes)  
		MIME: application/vnd.in-toto+json
