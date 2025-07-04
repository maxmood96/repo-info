## `amazoncorretto:24-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:608a74a76f97d6a287145751533d82b9d0544b27edf3c03c489d184b24091920
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d43bc14494e9c385d850949453da300e74ed322a775f0bcd4e81e9d6305d78ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156838519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cad112e46dc1f8c81838ad48114aee57126a1dfb281beaac8b46f096c17d2a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58159b2d64bbd25e98358c41c8c668901f20190486975665ce63c0a4fe2ea47`  
		Last Modified: Thu, 03 Jul 2025 23:08:42 GMT  
		Size: 103.0 MB (102998308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:451d1a497e321bf9bc83b6d038112e6504dc17d1dca65bc7ab17d205158d0f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e43ec1ef7f8081505a65d2a602f813272e70269757bccb89fea41a87d78139c`

```dockerfile
```

-	Layers:
	-	`sha256:6e09f004ff00057897615b8bf584c8ed06146a0d28d6d5fcf0cd3987ba382cad`  
		Last Modified: Fri, 04 Jul 2025 00:49:24 GMT  
		Size: 5.2 MB (5220831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efba9197e2cbf60446080e9e5e4f6b00354026653bcd78a20b01c9a86a141f60`  
		Last Modified: Fri, 04 Jul 2025 00:49:25 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4042f31c3cdd7b3d97178607e23f7a250be01d532079e03f39fece2a16564038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154713207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3043131c99fbab94952fe0f0c06d8e5decf0be426a05464deefc47db47e92bc5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:0e455f237a70326021a937388393d9d7ac6f9ae1616673300f248aeb280add13`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 52.7 MB (52717557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b46435bd926ab26293921f2538bdfff5ce6f733062e7fcee915565fd833c6a`  
		Last Modified: Fri, 04 Jul 2025 03:04:45 GMT  
		Size: 102.0 MB (101995650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17be95f8542ae783587a79f8686f91d538ac5e4475ab149c30625dce44ad934f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9f9a5e0ac00a7b54d50dbb21cbf513a405959c5b0ec43002e8ea458f2d9408`

```dockerfile
```

-	Layers:
	-	`sha256:0adc7112bc41b42b50dd833c59d6dd899c58c2b0bbd483985246ced8b65ea7ae`  
		Last Modified: Fri, 04 Jul 2025 03:49:25 GMT  
		Size: 5.2 MB (5219645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc17b1d9465c084a0c7c530ab8e0c4cc3909bc7dd5f863e5341bd8ba2bf520c`  
		Last Modified: Fri, 04 Jul 2025 03:49:25 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
