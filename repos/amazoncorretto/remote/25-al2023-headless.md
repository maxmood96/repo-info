## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:25cd90cb7b2b8d50561d374ba6f01e73688f084847def2622a73ec8acfe7f11a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9f3c2d26c3c2a07613b784d98a1fc5a61371e0be4c2cd09d0132007515596d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158298372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b8a915d7c4f68f228ba9aee1ac86f9bea2f3bfd4a96057d48e913f98aa8660`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:57 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:18:57 GMT
ARG package_version=1
# Sat, 09 May 2026 00:18:57 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:57 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88e93c48525db95b3113b1dbbb1431a1e0d4afd093cc5199c2cee332a11e2d6`  
		Last Modified: Sat, 09 May 2026 00:19:17 GMT  
		Size: 103.7 MB (103721568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef6c93bcd904e85056ac730cdde995068fa16c3eb9be8c429bf78d568f14d36a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f899f6ccb9b8c995779c4be8e3690a6f64dfdc2bd2336687977945f2e1e3356`

```dockerfile
```

-	Layers:
	-	`sha256:af41780edcd073362b6cfc2440466f41c55329f32d2cddc6ba0df80ba5fd018c`  
		Last Modified: Sat, 09 May 2026 00:19:14 GMT  
		Size: 5.2 MB (5202050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26fe1c7f773c55aafffc793911170a90d1313989249dc1f126ee63a4d16af72`  
		Last Modified: Sat, 09 May 2026 00:19:14 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a87f0f572622bfea4a5b4fe74c3aa68a7b601c54854cf851e96d20b6cfc7a3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156108024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56d145dc1d010099646c89d0a6cdb07c1f268a7c53386e0f6ec982c0f61fe15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:43 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:16:43 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:43 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:43 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed0c9b64bdcb5e23e5e89c2f3c67b756bd6818991d5ead120a6a90128c730ed`  
		Last Modified: Sat, 09 May 2026 00:17:04 GMT  
		Size: 102.7 MB (102651049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:acfcfcbe08ea0604a041a8bd6e9cdfac31aa02330b4cf63b8c922f625566b866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc58c0396a9841ba4880dd969e65542cc5a3764218a0e04405bdd4edc2f9aab2`

```dockerfile
```

-	Layers:
	-	`sha256:873b5bb0f7b2da32154203bec9741efd76c2dce18b2eae60c1a397d71cbcf37c`  
		Last Modified: Sat, 09 May 2026 00:17:02 GMT  
		Size: 5.2 MB (5200862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a6b96cb0e32295ab7455ce6cfdfcafb46c0cdf8ffba4e1685c7758c397d099`  
		Last Modified: Sat, 09 May 2026 00:17:01 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
