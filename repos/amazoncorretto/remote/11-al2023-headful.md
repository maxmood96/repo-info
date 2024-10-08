## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:942440a27cb2543cf71c0b8c85bfdaeed2bee64c91c136ad7d19fc43426b103a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e08b618bb10fa3ade95aee2c77395a8cfacf7af0b3cbb674d71c340b8da09068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129168816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03be03176a936f2dc628f6358070a199863af851705516e7d7a65af62f7b5b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940d9e8c54f1ad4941d570a09ee40af2cf9b77600d75ab898732f171d0ea5e88`  
		Last Modified: Mon, 07 Oct 2024 23:59:56 GMT  
		Size: 76.8 MB (76843511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da589bb75794a260d1a2580a087594ca3fa92b18bd99bbaf4195094c99b93bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b99ac9e2c6cd18d80952842335a951f908e1f87a05199455e677a1b1cb03fa`

```dockerfile
```

-	Layers:
	-	`sha256:3f9060fc063b1cede5d8140c2d70d17e359977c0d088d1247e8ae43f1bfa1ba5`  
		Last Modified: Mon, 07 Oct 2024 23:59:55 GMT  
		Size: 5.2 MB (5223625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4804105bdd583c48b70e67e4539dff9186ee606b4a7ceab34809025a4eaec147`  
		Last Modified: Mon, 07 Oct 2024 23:59:55 GMT  
		Size: 8.8 KB (8759 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b0c4225a191297cb3a17f94741bbad056de891325263a6bb65a3b06813fdfebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127427764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e105791d4121f374d62a002d21ab8b11b1ca8a9a31dddad2dc2dee103c89f5d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85721c68c49773fce59670d3470ce36fef963e35a0beb74e3c12fdd9e0bc559a`  
		Last Modified: Tue, 24 Sep 2024 02:32:55 GMT  
		Size: 76.0 MB (76001772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3cdf70941d1f02a2dda356795c10dbd66a75726020c5af1c242a18154399f2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cacdf950ebd0c229dbaca85bd13671e8a7b9d1c55f7b4fa3f641acf8f1b573`

```dockerfile
```

-	Layers:
	-	`sha256:ec58dacb2298070c03724b5d54fd385136e44dd6bdfb51d15de10a602bf1f88d`  
		Last Modified: Tue, 24 Sep 2024 02:32:53 GMT  
		Size: 5.2 MB (5223232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e0a026e630144c54bd615e7e1acfa1e3524ba69d69242bfa099a9b56e8df13`  
		Last Modified: Tue, 24 Sep 2024 02:32:53 GMT  
		Size: 9.1 KB (9115 bytes)  
		MIME: application/vnd.in-toto+json
