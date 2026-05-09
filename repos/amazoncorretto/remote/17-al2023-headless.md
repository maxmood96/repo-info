## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a6200d647c386e207f9a99fec82be5b57b011c1f38b3fa5c3375d88e410628b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2cf765750d327ec1f004617e55ec04bdd848d4a06cf26eb2985862dd4c5b8bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137064218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a09396a413e3232bfcea9b01469986a89104ec8782dd9fa70aadd532cf98959`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:13 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:18:13 GMT
ARG package_version=1
# Sat, 09 May 2026 00:18:13 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:13 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3439b45fcfefb0fd43ffc64d17203c3cc83e620ea41f7e9fd1f723b1c2a3e2`  
		Last Modified: Sat, 09 May 2026 00:18:30 GMT  
		Size: 82.5 MB (82487414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f47ea562dfaa95d2647168e36ad6e328b8d5bd47d7aaaeeb343c7ab2590d345e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1772f33bc2b4acbe5f4a216651c17a71e42b11d68878a9aea49694e8b57d9bd3`

```dockerfile
```

-	Layers:
	-	`sha256:c0de5d784a5094169bde24619a689e6e89520aa2ffd6ea0eb03ee5aaaa05e720`  
		Last Modified: Sat, 09 May 2026 00:18:28 GMT  
		Size: 5.2 MB (5190163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc9b7e0fecf852c21687b5fc6bab71bf7ad50b6f54ba1d121efb50435bbda01`  
		Last Modified: Sat, 09 May 2026 00:18:28 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9a876312dd9c8c11d6b4e552da8e85bbe1de761c8974afd73066b8a1374eb597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135354679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c35ecf95a51d14d828641fa2f9de3edc8b303a9c4eedf3154058ffc0758cf6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:49 GMT
ARG version=17.0.19.10-1
# Sat, 09 May 2026 00:15:49 GMT
ARG package_version=1
# Sat, 09 May 2026 00:15:49 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:15:49 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d117dc4acd4566b1c1a8d02e09985fc206975152064fbdf3b1f0f118c5a22100`  
		Last Modified: Sat, 09 May 2026 00:16:07 GMT  
		Size: 81.9 MB (81897704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d0386ed47134b0d173bfb36b0a611b1f967a88250bd6a732bed4d490b22dc502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5197912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca8aacef9e31d0999260a4570fb5239697dd4afeddd1f9bcaa717ca5048ca85`

```dockerfile
```

-	Layers:
	-	`sha256:88fd6737bc72373b41af1ce9222e8a8055a81c11d6c6e5acf208e522a1a0240c`  
		Last Modified: Sat, 09 May 2026 00:16:05 GMT  
		Size: 5.2 MB (5188952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6eac325b366faf00b1ce01804a9b2d206dd90629e58a9e1ddd5e843401f00d2`  
		Last Modified: Sat, 09 May 2026 00:16:04 GMT  
		Size: 9.0 KB (8960 bytes)  
		MIME: application/vnd.in-toto+json
