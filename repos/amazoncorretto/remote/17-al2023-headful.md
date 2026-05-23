## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:1218e57ad0812dd56a22223f9ea80fb8b320187520017e4167d891bb83f8a22b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a3d5950c535240f65020e927b6f5207de3f7fffce885c9e3ee997523afb78e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137787236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55d2bd54a9a8d57f61ff423c152b4ac424f251001118bb8e813406064e0d613`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:48 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:48 GMT
ARG package_version=1
# Fri, 22 May 2026 21:11:48 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:48 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976eed1494020cdc6ad10bac948e3b4b4a756f4277c2a4fab41e1dd9dde2ff0f`  
		Last Modified: Fri, 22 May 2026 21:12:05 GMT  
		Size: 83.2 MB (83214796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13287ed8fc18db9758a360bdb8047516099a6912dcc2785e458f0f5b591024e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0de999f9f51fb23ac78d87062d40744a3f7cf8324063811f673678041c80f2e`

```dockerfile
```

-	Layers:
	-	`sha256:16f3409acf42f5cf3c84b95ec99a6afed72fb7c0667034bbedef3ab6c967362f`  
		Last Modified: Fri, 22 May 2026 21:12:03 GMT  
		Size: 5.2 MB (5215594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc43ef3c1d3b12f56547f1f744933e0d3e74fd36b8c4158634e6a35696966ae`  
		Last Modified: Fri, 22 May 2026 21:12:03 GMT  
		Size: 9.1 KB (9052 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:261c63852cea6eda9211d7185f15e1b675b3c05b51561dbacfb700015fe8ab72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136089786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d191b3a5adf9df12ac8df89c89acd1cc6f548c42ffb2a726ee806dd560374d6d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:30 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:30 GMT
ARG package_version=1
# Fri, 22 May 2026 21:11:30 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:30 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f28a535e47add892f442c7fd7ea097ab13f82cc8fd372a1acd6ca250a7a8cf`  
		Last Modified: Fri, 22 May 2026 21:11:48 GMT  
		Size: 82.6 MB (82635371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7d77ecc2d7424fc6f41a755f88549dd05c2b86ecf87a157a7371aee88e5ada7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b893527882fa1bd26b632895159b5fee652c1518ff7e288326c020698408c6e`

```dockerfile
```

-	Layers:
	-	`sha256:f55c551eccd24ffbbfc26f3981d6c890212444c29bc9c078fa4ccee43a1e65aa`  
		Last Modified: Fri, 22 May 2026 21:11:46 GMT  
		Size: 5.2 MB (5214386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a305c956c649646f83e7c428ae70e10b1c9f3e3f83f75eae4fe25f28eb0243e9`  
		Last Modified: Fri, 22 May 2026 21:11:46 GMT  
		Size: 9.1 KB (9133 bytes)  
		MIME: application/vnd.in-toto+json
