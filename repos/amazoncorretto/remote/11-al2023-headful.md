## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:9d46e1a370939a20d89247adea6bac95821356c4cb86a4afcde63396c29bb883
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:feeafc7a8ef1fadf3b487b8ff7926f32e1c497f9b4fe662baa5054fb626fb323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131336380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877ca04d402d11bbf57d66d758dd28e5eb57b85e3aa3fb8a4e083e2e48cc2ddd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:03 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:03 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:03 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4672eece356df59eee4b43c7eb004edf1c4099dd6af8d6367a0035585049225d`  
		Last Modified: Fri, 22 May 2026 21:11:23 GMT  
		Size: 76.8 MB (76763940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a7c71945b6afe033521f797409a4d021169fc9a559cf7cbe5c2fa02f27b2dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7b1b03f09d9bfe38d12d325c81e5a6d60dfe4b332c6716c5c6d876fe83e3a4`

```dockerfile
```

-	Layers:
	-	`sha256:f60aff169245d92f9432e94869fb77409201cbbb638a5803e095f6700baefd10`  
		Last Modified: Fri, 22 May 2026 21:11:19 GMT  
		Size: 5.2 MB (5228698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe1bab23ac4dad2d4e874ec6a3bcf7729c54af7c8165da386927da2d06b420a`  
		Last Modified: Fri, 22 May 2026 21:11:19 GMT  
		Size: 8.9 KB (8907 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:70366644718f7e6d25cb5484a9fb78d57439de45d533ee12622fd426fb82b38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129469163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1807d527b1a91cba6becbc81d1105cbc4295968f89880eae8852f156fa29dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:14 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:14 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adce90130ebbc3dfb7a139b28163f372c141f7ca970d34b370bf0e56353ef4a`  
		Last Modified: Fri, 22 May 2026 21:11:31 GMT  
		Size: 76.0 MB (76014748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f9ce500b6e767139540321d62816eaf1957ae42ad777a3921fc9b440757f2a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a07cdca1842dc2a8df7c7e2d423f63fcb94e4a79b58bd5e23d674f92be11d1`

```dockerfile
```

-	Layers:
	-	`sha256:9603189633981bc8ae875cf8024e8f3047610f65b53984008573c571192859f2`  
		Last Modified: Fri, 22 May 2026 21:11:30 GMT  
		Size: 5.2 MB (5228319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c6d31417fbdabae355ac53da5d58dd719cf3ffbe6887010a10d470a624338ea`  
		Last Modified: Fri, 22 May 2026 21:11:29 GMT  
		Size: 9.0 KB (8986 bytes)  
		MIME: application/vnd.in-toto+json
