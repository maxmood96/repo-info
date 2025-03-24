## `amazoncorretto:24-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:10d037fe7a8c2d505fa51649d9122715d32db103fe9b9396bed7b6a32fad4a51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9936ff64c75d826180aaaa4ade27fdcfc92b6d8aee1d2e798f86fe11d7d01b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156117475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ec8f33bf7d8a30db875aafd158d0b32bf4111ac9dddead20f58b89daf63249`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Mar 2025 18:35:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 07 Mar 2025 18:35:37 GMT
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
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d03b60e9fcdc382327ccd9a897044acff0657e03c26737fd20458ab4feb64b9`  
		Last Modified: Mon, 24 Mar 2025 17:04:13 GMT  
		Size: 103.0 MB (102990599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:313c1203406d9c592ae6b667d1826240abb7dd8c67fb29c40eec4e2dec304fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0bc7f491d95209868e23e566659f2235e99a076dcfadaef0b41250c65ac915`

```dockerfile
```

-	Layers:
	-	`sha256:614a61ef42481d6b4fc4f30f8196a82f077878d54473491775f6d725c136b7e8`  
		Last Modified: Mon, 24 Mar 2025 17:04:11 GMT  
		Size: 5.2 MB (5196837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ebcda02256e0863ae07908c5042a18ea61e3f27e60d626496af325f5612e09`  
		Last Modified: Mon, 24 Mar 2025 17:04:11 GMT  
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
