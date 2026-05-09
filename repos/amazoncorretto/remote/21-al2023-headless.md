## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ced6aea9ba173a4485ddc9cea7f3dd4c1323fe213eb28414a7777d54fafda5b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1b34f2f02915d7658ce89a7a56aa53548ae93bbbe0b99cd5a7b4356010e14f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143934567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66fa3c4fbb342ec0db70fe98228d8aadf3a3c97f30bee46227af6e935702442`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:53 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:18:53 GMT
ARG package_version=1
# Sat, 09 May 2026 00:18:53 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:53 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b803bec748a3fd492a9f74322f0002f2ddebfaf4ee8ae3df6ce30e1b2a2ae97c`  
		Last Modified: Sat, 09 May 2026 00:19:11 GMT  
		Size: 89.4 MB (89357763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c16ecbfcada35532144dbb082a62e5c3295c60535bfd24ba9c5d217aaf39cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f2709bef9e44989ce0bfa6e28aadba026d7d0a31c32c535344e6d001b6a12f`

```dockerfile
```

-	Layers:
	-	`sha256:9cc069f98f1f3058d8b8a1846f30f59ad40a3e45081ceb2403bf6ebbd9f231fd`  
		Last Modified: Sat, 09 May 2026 00:19:09 GMT  
		Size: 5.2 MB (5191789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe6c88a2592035ef0c4d4eec67a9f4311cc50911adb00bbae1f7c19165de439`  
		Last Modified: Sat, 09 May 2026 00:19:08 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3cc49d6517c7a130db68fb372aa58ccc09979e0e9ea18cc2cc75092b0a02754c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141948609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1e740f2139a7144bb831108ab08159109fd5594c7cd3e138a94e7e0aa6bad8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:34 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:16:34 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:34 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae9674dcb92f78de846c012a48ed49e06f062ed5884b9b458f5dfab63873b08`  
		Last Modified: Sat, 09 May 2026 00:16:53 GMT  
		Size: 88.5 MB (88491634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2a3c7bcaf9296b78e6800220b0f5e9c088c21ba3d559324ba7f23af25cecd07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab160432ec5c7524f268a6b3b0baa54937d5e29244d0cbfef29ae9d56d4574a`

```dockerfile
```

-	Layers:
	-	`sha256:1dfad109c24d6e804fe50997bc85b5e135fc71a459ff15f6ee2598ca955a0693`  
		Last Modified: Sat, 09 May 2026 00:16:51 GMT  
		Size: 5.2 MB (5190580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd797845ec82d5ebe52bc0ea4ab3d58fa661283fca6733501cbf7b4742f61550`  
		Last Modified: Sat, 09 May 2026 00:16:50 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
