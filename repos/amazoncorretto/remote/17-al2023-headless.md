## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2578c8a541ec8aec45d10dfbdd460f55e62a8d5f201118a2836d1f34329cf98f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6507f0f7671fdefce24b1bd16c4fa304a148ba5941cd3ffd00eb8125e2b3093c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134757216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8b34a570ef159e77746626adf64949e4ae4a21038a9acd6e028e41f4e8635c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:50 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80f48e91b3459d0974b44b44726e282e0c3e9ab8c3c5ec0b9563c9e4c05ed7`  
		Last Modified: Tue, 24 Sep 2024 01:56:43 GMT  
		Size: 82.4 MB (82432258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28703029219748164911c67dabdcdd3be9a86d1bf6b6186e04f9c67386f4c768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 KB (8497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afe2b7c2818a209ed7713dabcffff14cc587714aa5c82d38af94263360fa0d8`

```dockerfile
```

-	Layers:
	-	`sha256:212b856cadb2eb3b3ddba0547d12fe126f25765fd6134800f6bf64dd4cb7beef`  
		Last Modified: Tue, 24 Sep 2024 01:56:42 GMT  
		Size: 8.5 KB (8497 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8a3b05299396bd1a91bb417760185ab282ceb48f08cfc2db06d66331cc9b83c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133176106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b31779a59fd45072bab88896cab385b19881213ce816bc4a3ffa6e757dee20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cd59f7db0c8de954444ea8dad313695dd88c8f1164ba3089f07cb878760dc5`  
		Last Modified: Tue, 24 Sep 2024 02:37:53 GMT  
		Size: 81.8 MB (81750114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0b0e6dff16b5f0f902755d06470264ab79c3254e3d40327c73ddb88e3ab8c34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8470d2022df6fc9468d46101700115559bace2f72be28f05b21cc5e4da9d77`

```dockerfile
```

-	Layers:
	-	`sha256:267b9ebaa6bbb45ea3f5cd171df6f32facb3a3f9659fd57d41ee9ea436246d34`  
		Last Modified: Tue, 24 Sep 2024 02:37:51 GMT  
		Size: 5.2 MB (5182512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a04c7ef6775bfae00b1e9db2cda25e48c0dfe2318b69dbcce9d4a416e0e84c8`  
		Last Modified: Tue, 24 Sep 2024 02:37:51 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.in-toto+json
