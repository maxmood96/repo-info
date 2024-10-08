## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:f0e77cca53ffc49d6c1911846ac0f232a994f5dc0e911cc6496474963ab3a0f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2a31dbdc8e8a89d86ca8d3e4494519bad510313a61d961d381ffa350a4b18eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141367929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739a3e72bb97444f209cf6f880d3b6fdd0409529538d86c3fd0e8f8f593d699e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf8e9a9fdf6d601d62aaecbd7b1d0e51a18b697c0e7e68968d02bbd66a34ea`  
		Last Modified: Tue, 08 Oct 2024 00:01:09 GMT  
		Size: 89.0 MB (89042624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e1ba5e7b766f1654e392f5d3bf5513a1fa7c6f21fcd0e8715f971fd81f08409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48fd505c1ebf6d646e8271f7f5e145fffd976ddfe6ccb4a8901a55d81215ac0`

```dockerfile
```

-	Layers:
	-	`sha256:fea84814fcc65107a57d2fa5fbc32038bcc6960ba2575339154d80c8942f2239`  
		Last Modified: Tue, 08 Oct 2024 00:01:05 GMT  
		Size: 5.2 MB (5212441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f8e022908b9f4e1f2a893c13a8f6313aaa0ffbab5a826ee1eacb05a2b4558e`  
		Last Modified: Tue, 08 Oct 2024 00:01:05 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5c02a0fe25611327f631ef5b9910d6d6ee8a83ff9b6d33c5b0d78aa1e37b3edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139434759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096d6e8ee199aed2dac32f1dd0ff047f56714726ac534ff1a28dfa6dd58f1d93`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd6c281fd648f0e0358f0715c63821d43ea376a20f91612509a8653fe96cd3f`  
		Last Modified: Tue, 08 Oct 2024 02:16:36 GMT  
		Size: 88.0 MB (88008395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7335e83db118fede51ef1488961d08087db251e15878f830723ff32f3dd0e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016355ef89b60d4926fc9a84d7dedcd033bfac518506f60a8eac49f190037fb0`

```dockerfile
```

-	Layers:
	-	`sha256:200ae48bd66c779436d8a181d6870b497107bde862b6a0b4800bb04e077b9cc1`  
		Last Modified: Tue, 08 Oct 2024 02:16:33 GMT  
		Size: 5.2 MB (5210428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59564edf5de913ade587caec5050c891504f47376f6ab848ca49677763deee95`  
		Last Modified: Tue, 08 Oct 2024 02:16:33 GMT  
		Size: 9.3 KB (9312 bytes)  
		MIME: application/vnd.in-toto+json
