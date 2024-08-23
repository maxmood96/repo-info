## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:3e2fb0783e428f83b462ef7ee9a9d3cecfdb82cc6524f932667902c44a2a259a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a67ea159ae698cabc047647ea8cbaca02d2a3083b8500bf30c5c3c13d676f8c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128481584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47475a430873d49a1a06c09404724ec4d92d346f72babe5c87e0a4a00c2e5f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b60b6c892280988095a2507a148439d3b5fd7b108e66565a91cbdb1f0e543fa0`  
		Last Modified: Mon, 19 Aug 2024 23:08:46 GMT  
		Size: 52.3 MB (52325078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c04ec44c48abebce95b5198645754d0e46c742df599c3b6cf5be9135dd0ddb`  
		Last Modified: Fri, 23 Aug 2024 01:50:18 GMT  
		Size: 76.2 MB (76156506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b87b0530c93aa5306bd0491f10f7c942d38d63962fc575aa0984984e35a922db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492df54d83124484a647fddb035b718a0df72e5f01a8b7d79d07e0912dbc8094`

```dockerfile
```

-	Layers:
	-	`sha256:7e0574e8efdfec40a1d5a5be43ac71211d97128a94a416870eb3b734a67a246d`  
		Last Modified: Fri, 23 Aug 2024 01:50:17 GMT  
		Size: 5.2 MB (5198499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983bede98a66c7cfc946f2938ae044dd8f3ff06d4fb82afebd175f011f94fa75`  
		Last Modified: Fri, 23 Aug 2024 01:50:17 GMT  
		Size: 8.6 KB (8618 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2858325e7323700883f5c702df1f8a2cab80f824e79e5895d8214185597d706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126724264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b870deb4c6d59a13311e37c4fd9a32bf6d712016de3886a90b721398094a6818`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd814e880ce321502206a77c374545bac039a590667ed0b82243382d7adf0992`  
		Last Modified: Fri, 23 Aug 2024 02:21:27 GMT  
		Size: 75.3 MB (75297966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75626ccf8b39a274cbfc6a8ac546a9b4edc99673221b084bf42eaa381359f5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2ff81b0e2b58c4a52192418e9f2ac385ee25652351d629a8eceb72d4ae962e`

```dockerfile
```

-	Layers:
	-	`sha256:c751f60d8102cda926b794aff6790311e9fe1e7aa0a7f96223641ea76fb71db5`  
		Last Modified: Fri, 23 Aug 2024 02:21:25 GMT  
		Size: 5.2 MB (5198116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2df96e22457d3eff59073097ad902d6cc29b60450792d53c20fde59e5ac7740`  
		Last Modified: Fri, 23 Aug 2024 02:21:24 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json
