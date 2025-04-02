## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:6c2f82069b0383a845e08a868e8a32c10b8a9732675cf41b7016d0c30d3fc228
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e939855d870fb4c214e656c9cdc37f24d3cde35b834f4d5c3880a62834ef53dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (144978652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7721757bd18c4a5b2702e873d8a363bca1e1f240746b08e9edd6ca88b9e13c83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a3286bd9bec83bebe73074cfb78535138d76fbee37470904a133467c3129d6`  
		Last Modified: Wed, 02 Apr 2025 00:01:25 GMT  
		Size: 89.1 MB (89071599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c206ff4884be5b1b993007ff9e21a914b0d341fc9deeac0192e9d89dcb0606eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5436142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be5cec3707429e5160bb63763ba92ec947120341e753c6b3f29e150d8792c41`

```dockerfile
```

-	Layers:
	-	`sha256:0c1779b3ed4b3f5528f63d41006778488288539b83315e1faf4e6a5a53fed910`  
		Last Modified: Wed, 02 Apr 2025 00:01:24 GMT  
		Size: 5.4 MB (5427394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a342c7205f153873db88a05f24290bfff2568bdc0b9d3188f55e32e24cc0a3e8`  
		Last Modified: Wed, 02 Apr 2025 00:01:24 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:67d9633abcf6b802cdf5f7383c1b256d67c10f024f8d019af66d7d114966a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140354023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec77326ed892124f194c2740c290f5a955ab67b85e2c9b303cbf69b9b45b803`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78541e6db98594811543fa73b3e4b93928418742dd80cba3127f8a56b8da9b63`  
		Last Modified: Fri, 28 Mar 2025 00:21:17 GMT  
		Size: 88.1 MB (88106033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cbb2ddd5413a94b84dfddfd63da5862622959c00a3a43f4307a9b5c419728088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7a1a890c9f56d92994b2d41d806f2a1af8120e943a430bd3346bc4c2ece702`

```dockerfile
```

-	Layers:
	-	`sha256:fd13de99d9cd981e3c05ecee7df650804263e640639803253e8f828756458c2b`  
		Last Modified: Fri, 28 Mar 2025 00:21:14 GMT  
		Size: 5.2 MB (5160120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6843a405c369fb69f83f6b8017f5453e7f6cf9d439f46e84b30f6065006f22`  
		Last Modified: Fri, 28 Mar 2025 00:21:14 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
