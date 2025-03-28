## `amazoncorretto:24-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:f4ad7b2671144aacec95302f8f52b93e3f25fb0ff1fd905c26a63298cc00845e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0078df6d5a3c8af04779d7cea72bedb1f114a86c93005476de8f0976f2327305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156105413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69eed137527f6e49c90ac4fc6ff5e77674fe34aba024af21f108860b86402b83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16eeb06655d8beeb7ef9d74e1d43c7a49200aec0524f1ef0e9af10e58d4d683d`  
		Last Modified: Thu, 27 Mar 2025 23:58:59 GMT  
		Size: 103.0 MB (102982124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7bbd793a788043fa11a3bc8a4d4217f1206444a816c26f55877f374274e18ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca9a8ac57ccfc0fc743b67ee4b19cdf1656095f58160f57d924face2f4a0736`

```dockerfile
```

-	Layers:
	-	`sha256:b9a7dc50bc59997f6773fb0cd7da74feeabc8036a5b6d4ff0c6e48274b35f355`  
		Last Modified: Thu, 27 Mar 2025 23:58:57 GMT  
		Size: 5.2 MB (5196837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25eb26d801d2ff6c58ba90b0b37b8b163e596b623dac3317e92c4809fcfd748b`  
		Last Modified: Thu, 27 Mar 2025 23:58:57 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0746ed3d4cc1fc7e534dccd567f59e9ffca6ee0c9825a7e68095537a4f201565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154231077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78cb2eab465a9eea932fa06752f37483a5e02115a357c191ebe614a9f14e246`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Mar 2025 18:35:42 GMT
COPY /rootfs/ / # buildkit
# Fri, 07 Mar 2025 18:35:42 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147cfc03d795e7f541f92bd82b66a81ca8986434389a634e51911572eb479c13`  
		Last Modified: Mon, 24 Mar 2025 17:35:14 GMT  
		Size: 102.0 MB (101985099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3046263fb35f2a0da0f494145b1edf40033742c78b7b138153036150c6c22c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14b31c17a69e30c69a440f6bc98106dec8fe7025c15a8d97e1a97a1c8c7db81`

```dockerfile
```

-	Layers:
	-	`sha256:8c3a985f6433668ad3d7db2c294ed0ba1b7b796c299b2f0f958290d2815559b6`  
		Last Modified: Mon, 24 Mar 2025 17:35:11 GMT  
		Size: 5.2 MB (5195651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa68424c196fab5f2cfd00db8d497c57888982a9d2d8810bcd433d3bf6a8d134`  
		Last Modified: Mon, 24 Mar 2025 17:35:10 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.in-toto+json
