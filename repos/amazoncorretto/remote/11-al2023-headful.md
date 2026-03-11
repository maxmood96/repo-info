## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5c3c06bacf014548b2f5ff6c166740963ad44a35c0fa83547708ed72544ade9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bb9435c236ecf6419ce1ad59b3b42c86cd8a4f78cd5996487f946514e062f2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130739117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8ae1f3f2c3d8f5c409529c0382935c526e7b6dbd84c7a83f28128fedf40f87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:03 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:33:03 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:03 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00888442dd486f57129665f8dd24b58527ae59ca2a4380767d7cd9206a2482f`  
		Last Modified: Wed, 11 Mar 2026 18:33:24 GMT  
		Size: 76.7 MB (76706027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6876a561983acca7bfde5c559e7656bad1d309b31d130a76499b2627a2468367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99ba8f9885d2ec5dadf5eb2d861866fe21d1c95a5547b19eb17531f1e4010f8`

```dockerfile
```

-	Layers:
	-	`sha256:250443f3263070096dc48177c79f56b9bcd4f7d7a9ddfbcf055b7d8ab236bc12`  
		Last Modified: Wed, 11 Mar 2026 18:33:19 GMT  
		Size: 5.2 MB (5222318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e35327fe685474c9801c5928d1f6402e291f501969d0c8aeb7c792548a17fd8e`  
		Last Modified: Wed, 11 Mar 2026 18:33:18 GMT  
		Size: 8.7 KB (8745 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:32dc7d001be5a5be378b912e168f5927d153f57bde15189f62f2700ca49dfb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128897784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ddd9b5414154a328a3a45ee16ba5a5ed97a7eae3a8952204a98433be1e87db0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:32 GMT
ARG version=11.0.30.7-1
# Wed, 11 Mar 2026 18:32:32 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:32:32 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643d1e23b7f6cab9dee743785dae26e1b5566173167d1bcc90a705b49797dd15`  
		Last Modified: Wed, 11 Mar 2026 18:32:50 GMT  
		Size: 76.0 MB (75956409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f5739893f7fd1b55b3d10d369e8010562dc681ca7098cb414b7457f2a539c62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a3eac79a440f2661db388b95437415fab79723949ae99ca44e99b511d73310`

```dockerfile
```

-	Layers:
	-	`sha256:f71b8822e8ca7b17ebe22422f958c2951d1d826d81143e5e02bd4d7fdef05f5d`  
		Last Modified: Wed, 11 Mar 2026 18:32:47 GMT  
		Size: 5.2 MB (5221939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf3cb86ef1dcb34a4e2ebe5f6ff2b67f2f9ab99ac6b293e6c3af77f06c56553`  
		Last Modified: Wed, 11 Mar 2026 18:32:47 GMT  
		Size: 8.8 KB (8825 bytes)  
		MIME: application/vnd.in-toto+json
