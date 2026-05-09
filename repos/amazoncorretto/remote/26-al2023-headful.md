## `amazoncorretto:26-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ea0dcae1445c156ab6f4f565d05057ec7ddbe21a0452ab85fdb55b0cbda892d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:27a3c38be58b176a7fceb22c339ec8e7103a904a5bac465089f2f00523214a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161116598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616d6a1e79721fe917883ac28f22b1a415762979433e9460efc805a716ccefb1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:32 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:19:32 GMT
ARG package_version=1
# Sat, 09 May 2026 00:19:32 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:19:32 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:19:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67a3fde67c3b75d189cf3d4adabcfc25d64e5bad361c285cb521800982455e5`  
		Last Modified: Sat, 09 May 2026 00:19:53 GMT  
		Size: 106.5 MB (106539794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a559b69606650f4ddd0cd3c0c77e62ccfeec8ce81d2afd43302dcc975ccbe10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68909099861b6349245200c52bb87d49d087f20a342942a5ec3b71e337da80e`

```dockerfile
```

-	Layers:
	-	`sha256:2b21f1e40de3e01be718d7af85fce6194034d1ede864156b9915a0dffb7bfb1b`  
		Last Modified: Sat, 09 May 2026 00:19:50 GMT  
		Size: 5.2 MB (5225833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27fcedc7da552d45bfec192e4663feaea1a3bd5ec0af671efc1afe9546e4ebc4`  
		Last Modified: Sat, 09 May 2026 00:19:50 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ecd29247e99025121fb3ee1ac73923ca972b37221f09bb958193848ecffffa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158889836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a58142a729e79b7020e37a4caae80c687dbb2d835ffb656179067f5282cecc2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:57 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:16:57 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:57 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:57 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270ae2179cb058fe4846103d0f6659f5ec4bfb06d209072784883cbe8ae28234`  
		Last Modified: Sat, 09 May 2026 00:17:18 GMT  
		Size: 105.4 MB (105432861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6426d9cb885f12ee0ce3b6c65a956f6ccfc6bba67214bd3a0f73ae9dfa2c262f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d6a010a15a9af3e37e1d1cfdf482bcfa806826ee121dd1f0b0b141c1f63e82`

```dockerfile
```

-	Layers:
	-	`sha256:5c3affe6cba90a2bb33bc53bda0ff829680391e138c478f6b1ae1c351d8604a6`  
		Last Modified: Sat, 09 May 2026 00:17:15 GMT  
		Size: 5.2 MB (5224646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa996396e5b16a9e30c93f8a298cb5524dc0d768c357a4055c5e5c2c3148bca`  
		Last Modified: Sat, 09 May 2026 00:17:15 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
