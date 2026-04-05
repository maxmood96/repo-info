## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5e141e88a80eb4c5fbf6a84d5ce10cb52afa4eaf78ec10b12afafd9b82a10fa2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5607bf583c88e2ff6a41e6bde555f4f6fdda4621488d2453890fdf13dc86d64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143808791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b0f593ecf5c70a9c126f6f9d4d70a0512a73b0c3482957648e3137bb7a21e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:56 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:56 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:56 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:56 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce3203ebb02f7fff61cfdec81fda11c85f4152c2d7f75d1e8b8427565500439`  
		Last Modified: Fri, 03 Apr 2026 22:15:15 GMT  
		Size: 89.2 MB (89237488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:683c31e1e569c7d6607328121c90ebe9a150dda888a781a8109d5ab71a1df756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39a6f3d1b71a6767aab1f8eb35e47682752c7c793e86f770e5505bbe84cf77c`

```dockerfile
```

-	Layers:
	-	`sha256:dc03f1d9d4fc8cda4eb7f278211ba29fbd8a8f0b3800221109af7f6de4aacdef`  
		Last Modified: Fri, 03 Apr 2026 22:15:13 GMT  
		Size: 5.2 MB (5190966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d181d5c2140554f876562542680329346f5cf0ba817715512672ff7544c3385c`  
		Last Modified: Fri, 03 Apr 2026 22:15:13 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:596215452088ce70ff1ff5700c8010b31a3c5622cc18f2e5ed83907bd2b00204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141818256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89724ecf109b54b6c4d024a1db65512f3f847916cc2fa77d5f2cc8eeab0c5d40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:35 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:35 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:35 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:35 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cbc24183fd8ee250a216e666d1a6de014eb169faede62fba880bfb3853c885`  
		Last Modified: Fri, 03 Apr 2026 22:14:55 GMT  
		Size: 88.4 MB (88375431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:62e8f0c06713d1d66b44e4c388e40e2b39263de43c7018e28e9d336311965a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe189f47f7ae465b175a5959ea5e8e837f2f7ba16ac55c3de31843d07868bbf`

```dockerfile
```

-	Layers:
	-	`sha256:07f8df323932713ce21bb535ce8d2a68ca281cdcc3395b8fd8c1f0425a32db9f`  
		Last Modified: Fri, 03 Apr 2026 22:14:53 GMT  
		Size: 5.2 MB (5189756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58beabc04916852d3fac4ee11dc9298f4b9bdf213780e307177e6f971213a28`  
		Last Modified: Fri, 03 Apr 2026 22:14:52 GMT  
		Size: 9.0 KB (8957 bytes)  
		MIME: application/vnd.in-toto+json
