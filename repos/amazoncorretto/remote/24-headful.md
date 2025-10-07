## `amazoncorretto:24-headful`

```console
$ docker pull amazoncorretto@sha256:a0c167638cd42d990a384430692a0183b4c0e2f3212b475c4725a905293af565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5a65a579bf539be80d6d49132599546b235bca32d1a85eb0abbd21dfa25565a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157170286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ddac4116e47ce3ea14fea2de89ef968dfa478fc021980a255b3cf979794c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ed7e3e19dacc5aac640ff48afab62be5e4a03bc211c52e0cdec0f6f26fe640`  
		Last Modified: Mon, 06 Oct 2025 21:14:09 GMT  
		Size: 103.2 MB (103165155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:167c29be75c7ab2e15b0d8017899c8ce50db18cc6eb2a1f448f66f0d085e44c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57416c2d9da9946f73b76f34b8ad416df94fb84a07184766004d880d26bcc41a`

```dockerfile
```

-	Layers:
	-	`sha256:ce7693e2a02a67209052c06bc6b0623c4cc4fd8362a050ff4e6710c948fd2a41`  
		Last Modified: Tue, 07 Oct 2025 00:51:03 GMT  
		Size: 5.2 MB (5220128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e9ba1c79ce6aa64ad96b3b80407ddce9fdb15df9a2301f86f9170fe4cece86`  
		Last Modified: Tue, 07 Oct 2025 00:51:03 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d32c74cbd948b716d7e3f640d43c0665ed56ad6e0b60e2fc887cbc0c5d1100ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155065610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788c7f4f2697548857cdb0ed64b74a3864046ef7982e4e1afa34ffb759c0368f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d37521d79e15a2a3e1bf1784d9682ab6e4f250d988e3117261158c9f3880c1f`  
		Last Modified: Mon, 06 Oct 2025 21:14:36 GMT  
		Size: 102.2 MB (102174407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4b089cd9cb22ad0905b52537aec0a1d979b1317c56a1c2afdedffa618baf81b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45025fbd70e384d7576cca40469056c06546e996e1e35687247f94b9577b63cc`

```dockerfile
```

-	Layers:
	-	`sha256:b64d90f0ec74abfee6cc0cd726537f61a27f21fdc1c47363b0416f0f85bb925f`  
		Last Modified: Tue, 07 Oct 2025 00:51:08 GMT  
		Size: 5.2 MB (5218942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4e697912e599a471798c95c5a52e53eb7552f903714689fe50d5ea709b06aa9`  
		Last Modified: Tue, 07 Oct 2025 00:51:09 GMT  
		Size: 9.3 KB (9344 bytes)  
		MIME: application/vnd.in-toto+json
