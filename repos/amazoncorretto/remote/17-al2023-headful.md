## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ed8394a455b55f7b7ac0c40e5c65087ec7f25c291f6b6c8bafb6158e1297e8cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f487db82a00d4a0431bbbc4c8c883b7ddb014c9d9ca4b7d97f51cc60b80be39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137790282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd23b589df87737adb65d7393d9092098d6ba581e1808ec490f5f9f19515317e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:03 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:18:03 GMT
ARG package_version=1
# Sat, 09 May 2026 00:18:03 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:03 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0877514ce753bae5ffdb1df679e5c16551e26d764343cbe32671dd1fbd097ab`  
		Last Modified: Sat, 09 May 2026 00:18:20 GMT  
		Size: 83.2 MB (83213478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b3a64801222d7ea132e9caad886284b834452758de78603fe17f5cd0ba3bffce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd7cd9ee51320bdbbf421d3a96a78d6e516e7187de76b44c1eed27fb4edf5a9`

```dockerfile
```

-	Layers:
	-	`sha256:605d5d93c3be740cd3ae77c04f4ace638afaa2f0e352a0639bd7b2de67684548`  
		Last Modified: Sat, 09 May 2026 00:18:18 GMT  
		Size: 5.2 MB (5215594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:001c2e2fb80ab812fc11fcbcdf6dad9d180e0e5f7fcc5f851352e09ed9106cf6`  
		Last Modified: Sat, 09 May 2026 00:18:17 GMT  
		Size: 9.1 KB (9052 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9af1f731fad782dc903acc2ceedb6b0b3bfd7c9a9b724553b7c6c6cfd1be721c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136094824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe324fc68d6318038262c4820cd1115c0f6b2a6c37889b8f62616f22e57921da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:09 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:16:09 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:09 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9de5c85070ef6f71370a4275d49e875491dc48c8400b81da05ac43bc2f0299`  
		Last Modified: Sat, 09 May 2026 00:16:27 GMT  
		Size: 82.6 MB (82637849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a5aa565c46234351e6912ff810a2e2031d00db88e8a781402f2a2d2ba15cd577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b100a002b6dfd59f6061e7b4cd9ad723d2153d55fd66c7eaf934cdc1dd14ecec`

```dockerfile
```

-	Layers:
	-	`sha256:34b89523444ba46a9f25f83d24817d464c44adb22689fcc60bcf13894efd41ad`  
		Last Modified: Sat, 09 May 2026 00:16:25 GMT  
		Size: 5.2 MB (5214386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:536071a04f4ef5040616b2353730dbd5655cdda4788a47877bd31ca9fde19378`  
		Last Modified: Sat, 09 May 2026 00:16:25 GMT  
		Size: 9.1 KB (9133 bytes)  
		MIME: application/vnd.in-toto+json
