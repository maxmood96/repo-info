## `amazoncorretto:26-headless`

```console
$ docker pull amazoncorretto@sha256:00c56c96577e1c3605fa774d1d86e27c421d9d44f0c5214c250e4dbe34c3dee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c2821a4e437a4c1bf0fecfc67f5a32345506635f0dd6b8d1d339ea15532e6201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160396748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4aa7d603f84f258e517cccbaa1efc16c5842c2eb67eb039f9a06837bc4df94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:48 GMT
ARG version=26.0.0.35-2
# Mon, 13 Apr 2026 22:49:48 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:49:48 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:49:48 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddaaf20ea5fc7c7ec04d1ebfd53b10c59cbb38097d5e49861acbfded979e24c6`  
		Last Modified: Mon, 13 Apr 2026 22:50:08 GMT  
		Size: 105.8 MB (105825494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e4f63bc4a3fcad7da5d62282b5f28c19119def373302912011d086ede9a96d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a13eb368dccdd0974fca63a17dedc454110c310d2a391cb2000b167d01d60a`

```dockerfile
```

-	Layers:
	-	`sha256:aed6646e70b7f6a607cb784b10c1e95d50d845944f5550771b0e2ed948c50346`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 5.2 MB (5200404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b36af7e9047b742ab91efa81fdc9bc4c73d677f0b10c20d905fdf857149c689`  
		Last Modified: Mon, 13 Apr 2026 22:50:06 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e279023669e076db26876f043539577fb0671f43d31aa3abf688cb70d03ada49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158150805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a704bcfc6ff8d2e1f0f22c49f993d8236a8c32034c108a20ef75e4016274cfb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:12:36 GMT
ARG version=26.0.0.35-2
# Mon, 13 Apr 2026 23:12:36 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:12:36 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:12:36 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:12:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd0a6f664ed6d41f2ec752fad92e71046bcc9024112a9e1bfdc9797362ca59`  
		Last Modified: Mon, 13 Apr 2026 23:12:58 GMT  
		Size: 104.7 MB (104708066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14f0f8bb774eddfccce7d42761cab98ae2d72ce41a174f000a40f5b942a02bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadef888ef914752416a47865d901979f88208504bf565ffa196da738777d8b6`

```dockerfile
```

-	Layers:
	-	`sha256:e6337341fe32216f9efac118fb45d0eb12ccea77a6581d6dc0f69d2db0076090`  
		Last Modified: Mon, 13 Apr 2026 23:12:55 GMT  
		Size: 5.2 MB (5199214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7543f74198dc9cf62f648393f061e1ec48e37f42cf2afade97da0d9c9ba7ed65`  
		Last Modified: Mon, 13 Apr 2026 23:12:55 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
