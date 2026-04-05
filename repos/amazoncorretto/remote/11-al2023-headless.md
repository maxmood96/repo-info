## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:8121e868a1c8aa8bbbd63a0664b86b63cad4ebac47c158d51fc64175f9aa5698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:82909754bfc1fd9b9268a6489bfb9c50626f4aba40b19bfcd947f7a9e29bf09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130575278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd5480adfda022975a423c22bc4ab89fd13f5e5f99234cae4741d76a0fcfc81`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:50 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:50 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbc62bce3eec7eca8d9cc46a64a1915118ff0f74b1868687ec8dbbe79479d8`  
		Last Modified: Fri, 03 Apr 2026 22:14:08 GMT  
		Size: 76.0 MB (76003975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f2e4bb54a1bf93f8a0c8edf0d3159bc976d5243d25cc9c981e5cf8c46ceb7d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b492d69b185684262811df8089847ec45c4bb095b20a0d34ca839fe35effb35`

```dockerfile
```

-	Layers:
	-	`sha256:bcf51110a542c50d6892e2431f79904070d35ca82f502d7d440d62c26ba3522b`  
		Last Modified: Fri, 03 Apr 2026 22:14:05 GMT  
		Size: 5.2 MB (5203267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ea054b01bd60947c78fa9d2d9c2cf9e7a5a57ff1906c691f8943a6d7ef1b0e`  
		Last Modified: Fri, 03 Apr 2026 22:14:05 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0138b34cefda0488bf845f2062e26cf58490cd0e4a8baa64291784b398dd2243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128678546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ec00e47cf2a6a4f6a3033ca0a039e97752896ceab376058058f2a74817027`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:43 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:43 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:43 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6854ddd49b2a51e1db4884f4dc8d1b206b1999f91b4b4fe1f8a08e04099bbeba`  
		Last Modified: Fri, 03 Apr 2026 22:14:01 GMT  
		Size: 75.2 MB (75235721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14c24cfaea895ebd6ce2b9abe3526a5affb8c4f3c72b863359cdce31623a3888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e1b19b6229ca984f3e860ed2ff990a9fcf194b468e0a7adf353397bd9504fe`

```dockerfile
```

-	Layers:
	-	`sha256:5c6f1bfaf8de12a48f9b5e26598c6c98e0989142d070c8651f7812fdeab194b0`  
		Last Modified: Fri, 03 Apr 2026 22:13:59 GMT  
		Size: 5.2 MB (5202885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf43234b37db854c207a9b20abb331dbe0731d43cbf8119b0ee679c1c544bef`  
		Last Modified: Fri, 03 Apr 2026 22:13:58 GMT  
		Size: 8.9 KB (8858 bytes)  
		MIME: application/vnd.in-toto+json
