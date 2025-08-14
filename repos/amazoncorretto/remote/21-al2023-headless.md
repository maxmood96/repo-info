## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f5ae7191c2dc5fbb4c2b00779dcc40f54e6a0c0e1ed3e0042fd1fa2e68be5bf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e3b0295d4415f5b4e5b1f438fac14412c24f236cacb29fca40045ae13f764724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143068207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2c43beefc71d4169f64afd78e46ac7386d25b263c1a9dfa7d04fb369e7ea29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f6170370102aa9692c4df9514e9ce17245d32e6f92849c963a9e24cabd8b1c`  
		Last Modified: Thu, 14 Aug 2025 00:54:41 GMT  
		Size: 89.2 MB (89230248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a85b48e6383cd22580723711c7696aa6319daa6eac9da89ccb667b907aa51d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932a31b364cbefbcc1a91c14b13bb668e376e15d63ef181dd3f460288fc1f67a`

```dockerfile
```

-	Layers:
	-	`sha256:e789b1d046514dbf9e47f183437c238ecb914dfbb216abe70cb0bf7b2f70f50e`  
		Last Modified: Thu, 14 Aug 2025 00:49:10 GMT  
		Size: 5.2 MB (5184434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c103ae3152d65554627f9df60c92c2f7363b8784c69c239a70e922fcb201b30`  
		Last Modified: Thu, 14 Aug 2025 00:49:12 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bae06668323cdec592ccdc494b7e495f069f2c0593fdb92421c1b825b095f5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141080565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20634b5e1b6334016153223900c361c5caae74091f72cf87e679112c711e7351`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c03b86cc710440b317287d149939b8ba397df2c03631ffff68e5467a19e310`  
		Last Modified: Thu, 14 Aug 2025 09:05:17 GMT  
		Size: 88.4 MB (88354171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:844c1a91d6ec0d58ae7ce6e63f71d01f0061aa6a11c063835095f211e42a7c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf61ed8559727430b02ba0ecf02de2497460c8019d97ac4ea9d2b346586bb7e`

```dockerfile
```

-	Layers:
	-	`sha256:cad9e09a2133fba9c0104238c3de10e27e52fb45aed8495aa2959843a63bdef4`  
		Last Modified: Thu, 14 Aug 2025 09:49:07 GMT  
		Size: 5.2 MB (5183224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4db49aa50467c597ca73e9d72e2d57d456b7b2dddc1b72b74e1d8e9d00ea471`  
		Last Modified: Thu, 14 Aug 2025 09:49:08 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
