## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:8e58f6d7f0cb502704e69a9b25eae68c6c7d6d4ea48e8a15b4d8c52de44a694c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:322bd3cd5a8982d516eca424b6d5a8cfbb1908d1dae5e22077a66c75f06b5bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158365349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9549ed3611a265a3050f8b35fb9f84ef6447e2875984520907418d051f94ba8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:32 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:32 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:32 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:32 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194f5d09c745dafde52fad728278aa024150867740279ffe76e26237d9a11283`  
		Last Modified: Wed, 11 Mar 2026 18:34:52 GMT  
		Size: 104.3 MB (104332259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:864f2c9d02753993c6852b245c8183e4bab8b7eb5cbb9caa25f3baeaf20b660a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83e6b18ea38606cc1716c8ebdb67829879dc53a7c842e18edd1faca19692f02`

```dockerfile
```

-	Layers:
	-	`sha256:d7af5552453a5bcb2c1ebf02a4b8230dfe560c5d7458e34023397b8654f96d4d`  
		Last Modified: Wed, 11 Mar 2026 18:34:50 GMT  
		Size: 5.2 MB (5220288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c1c5f942bf74cab2aacd18218d3f8fc333b34fa1d820111fda4cb13226c2694`  
		Last Modified: Wed, 11 Mar 2026 18:34:50 GMT  
		Size: 9.2 KB (9212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:632f7b4b77a29c2ba5ded9d703a20518c403e9c3203d8ad865298ac00539c24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156201938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3051925511ae42a274c4205fb0688c25c9a1ca6cff581c98af786822506b44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:04 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:04 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:04 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:04 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055c6975a4f239e5ec59f92923eafe7ef567dbe411ede60f933e6f5884c8717e`  
		Last Modified: Wed, 11 Mar 2026 18:34:25 GMT  
		Size: 103.3 MB (103260563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ca2de9a9ff1608c9b986e24b9ef6f6659191c632e9417da44355430221267b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ee51c01eaaa4dd4e8f9fb3b81f9b456bb43ea52a0b39a3380468d814a97647`

```dockerfile
```

-	Layers:
	-	`sha256:69173846bfe5b2a7b1a96c96c824636a452a0a8e6a823f7423169af6b02e5c9a`  
		Last Modified: Wed, 11 Mar 2026 18:34:22 GMT  
		Size: 5.2 MB (5219102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f3ba57431c1cc6fc35e270ae7073b815746f23c0c3248aa8b0305f02c23f01`  
		Last Modified: Wed, 11 Mar 2026 18:34:22 GMT  
		Size: 9.3 KB (9302 bytes)  
		MIME: application/vnd.in-toto+json
