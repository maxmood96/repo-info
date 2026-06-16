## `amazoncorretto:26-headful`

```console
$ docker pull amazoncorretto@sha256:26613e745000c2d24d6b61ae16eb93339448981ecaac0acdb99fb795d7507615
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cd3846fa5a2bf986aba1dafa2ef9535a3245a315e6228560f4d983089461c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161109025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46f60cd3db63e6dd7c2d790f6cdcfc34c99310e085342a5563bd763532f199`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:35 GMT
ARG version=26.0.1.8-1
# Tue, 16 Jun 2026 01:16:35 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:35 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a21a12247d9e3c4c11e6aa55ab4ac8dd4535006f50cf1c6222136ea5e2bf62`  
		Last Modified: Tue, 16 Jun 2026 01:16:57 GMT  
		Size: 106.5 MB (106537869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0de73d9f2b105f65d8a0d5037188d31eab1a8fa514d2259aa7ecc1dbfde21bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b240c58a12ce9a34093caedf66d1eacd6e0c725aa9178b5b3075e253f5712dcc`

```dockerfile
```

-	Layers:
	-	`sha256:fce8639e13e4b4098fe6eecd3d51917f9fd110a301cf96b2a441aee9f2c33376`  
		Last Modified: Tue, 16 Jun 2026 01:16:54 GMT  
		Size: 5.2 MB (5225833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10aef21a9b72837eb099a69b2ffdc219ef036aeb73b9e5eae524aeafc3829578`  
		Last Modified: Tue, 16 Jun 2026 01:16:54 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:67508f4fd8a2f5384d55cf23f0a7b3f37cd98dee274d200cc187c9e614705dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158889194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a30b7dab1ecaa65692521255bfe09ce564083a96fec03f280887314dc8d0f68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:17:38 GMT
ARG version=26.0.1.8-1
# Tue, 16 Jun 2026 01:17:38 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:17:38 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:17:38 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:17:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdb56dcda08b123be7ac2312240f08cbbba442ea2a48a5894813919b5fc2714`  
		Last Modified: Tue, 16 Jun 2026 01:17:59 GMT  
		Size: 105.4 MB (105431367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d21c1a70d50ebe2079527350e17ed2b289c3b69fdbf2861203c802dbbc60d167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fb8c8f2c70109c67ef1a186ccef0948260629b85c1c6dbdd9d963463e2e12b`

```dockerfile
```

-	Layers:
	-	`sha256:087939dd6825b6e8935e30924ac027495ab5ffd467067dbe8e83016df101d84e`  
		Last Modified: Tue, 16 Jun 2026 01:17:57 GMT  
		Size: 5.2 MB (5224646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbd56a661aa8fac8b2a8b153a7e68d7a45a2aeef443589d35177d5f5b1451b4d`  
		Last Modified: Tue, 16 Jun 2026 01:17:56 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
