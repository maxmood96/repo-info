## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:06f62ac2069335fd69e3345ea192b5f87479ea2c2bd7681e41040531df255b74
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
$ docker pull amazoncorretto@sha256:cfaf9e46a65e43da442fac61606695d8d093baf25ba14403d27b8f73430803c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141125099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05639fe1abb6808f94cdf6da0bb099adc902cbcda699fe5379e3075a14336dbd`
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
	-	`sha256:f0b7d54214a6f9c2c7698f71fb06f2128097c3f9d97269e3d449f7639c142381`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 52.8 MB (52768497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759810c159c83dee248baa36567a78857c73fc9add8ffe19ceb1e6eb5ff886cc`  
		Last Modified: Mon, 25 Aug 2025 22:24:08 GMT  
		Size: 88.4 MB (88356602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0536232c250b326541b02e33cf4a344dc405d8a7eecef4560fee7b43a2455fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce7fb6d4e995a18dc07a707c441dc46a6bbfd44b7c1560130fca0e6a605c5d3`

```dockerfile
```

-	Layers:
	-	`sha256:50418cce5bd399cc58f67f61b54b3bb74e841f176ab627cc674bbe8437a8eba1`  
		Last Modified: Tue, 26 Aug 2025 00:49:05 GMT  
		Size: 5.2 MB (5183224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4a53c6573c2d7cfb9c593a9c167a33406cb017db98cd5a634e366b31a62128`  
		Last Modified: Tue, 26 Aug 2025 00:49:05 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
