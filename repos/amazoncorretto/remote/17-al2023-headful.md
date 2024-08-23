## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:cc43448d25586734922a6c8353e0286da3b867a7f63abc41589a3b69c1ac6a88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7ae6afae9f1a0d9bea27e5ead9584e5849e5fe02374ebb029d4e778b25f7171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135428307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf438e2b39f67fed6adf0e85231dd9aa5721f8193b13eb5d542196c6ac00a0b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3143f436089bfda0392c767d573d6a5bc5147ddb7ccfc956e824c5cd318d9449`  
		Last Modified: Fri, 09 Aug 2024 20:49:31 GMT  
		Size: 83.1 MB (83110404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6e40a9855b6264f9563604aabf86282c08e877d9ee23fd337ae9d8909721829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaf6ddac218bfba419f4056a1a2e4194c094b1f2c0b18ac18d38ecf471a7c28`

```dockerfile
```

-	Layers:
	-	`sha256:8d4611e23b118c846b025474a5c17e27df092147f161a296ea0197fbc7e9f1cf`  
		Last Modified: Fri, 09 Aug 2024 20:49:29 GMT  
		Size: 5.2 MB (5208756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ec22309ba33c633817f25fd6bc5449ea3d8a56e123cf58bbd7c40d003aa940`  
		Last Modified: Fri, 09 Aug 2024 20:49:29 GMT  
		Size: 8.9 KB (8900 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a4cead9b1dae2262096c2fc9e124349cb00f8e2c959929ffb5026c7ca9e5ce3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133868696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cea47ca96b7712930c27e32a10ff44637d4f8e0841ed7c2be933f0534788c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0019787f9568484e676b8cb167c8e517fc09246b5c6db2cdb7ccaa0a6483fc`  
		Last Modified: Fri, 23 Aug 2024 02:28:59 GMT  
		Size: 82.4 MB (82442398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:839b3327262aa7de37c192feab480c5732c97f01205183229a8932734ed68f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86439d5617d56abf6f08a6ad41ac321a1c39205cbca3eb05f3f2cef4157a282`

```dockerfile
```

-	Layers:
	-	`sha256:0894dc37d7519f1f05706261ee98064e0e796acbe6d1e35abc29f331405d9d0c`  
		Last Modified: Fri, 23 Aug 2024 02:28:57 GMT  
		Size: 5.2 MB (5207632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fc09c58e1acd19e0eef16bb1cc79dc1b36080b7d7603b37fea25b508b1c74f`  
		Last Modified: Fri, 23 Aug 2024 02:28:57 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.in-toto+json
