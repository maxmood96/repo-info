## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4502424fbd217d66554802aab4b43a8751ce4b78d3b09321817c4299e9aa35c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5ed77363d5290c3b66a2d80e1494e1afc86fa01b3528a28025c182e1f743fc2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143097814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea9f43b16bfa8d1b8b228320f8ef8af800a42c6f1a5857fde636f7623b945c3`
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
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5711b9dc6b27171b675e95f7c69c34a179416ffc5ce52452b79bf90c7b9acb26`  
		Last Modified: Mon, 25 Aug 2025 21:49:16 GMT  
		Size: 89.2 MB (89229084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f50cb13755b33f13181ecfe4209615adf3580a7fb149d6528608df68bc4dc084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7810ae676560982f72f1d081f2591a9e6966ef63d6e9d0553ead15a8f3c83b`

```dockerfile
```

-	Layers:
	-	`sha256:ddf3f9056468a9f79e036508db2d8a09d11e32fa5a39ca349c12be79eb7fd513`  
		Last Modified: Mon, 25 Aug 2025 21:49:04 GMT  
		Size: 5.2 MB (5184434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef54840141a4298c9fe7b33166dc37b93b719c34ee439d1de6d977753a3b931a`  
		Last Modified: Mon, 25 Aug 2025 21:49:05 GMT  
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
