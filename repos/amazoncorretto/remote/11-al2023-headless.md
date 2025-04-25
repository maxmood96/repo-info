## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5284633a71ac0ee8a7ce229e8d45d4996e706c58c55403cdb7e0e2fe39a7a6a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8c898ac7e6d761d6b8cae4aed06ff3a0c2413cc60a3e82b611c97cc7ebfa64aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132228977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0962298bf100efaefb7410b369bd0b1d93e022e183506472780bc95a8238332e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1cf9fb914831ab202ad1756fe44227d7c88c49394a5cc9749ad863e76989673c`  
		Last Modified: Thu, 17 Apr 2025 22:49:09 GMT  
		Size: 55.9 MB (55906521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f6031122d45393e876a51d6f50ad14f2e9a29d424ded8c81af1857686ebb2b`  
		Last Modified: Thu, 24 Apr 2025 20:08:07 GMT  
		Size: 76.3 MB (76322456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:86db6d985b7bf4105919137a6cf78dcd0d57876a485f99d001ce580a5be72ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c3fa27e362e1b50d5296c14847c752fbdd87434722ebc4b3951a2c16ef68b2`

```dockerfile
```

-	Layers:
	-	`sha256:d1544cd94ef91b1755e0f69bb7fa4f1302e3559fd04a15dcc1e05d4493d4b676`  
		Last Modified: Thu, 24 Apr 2025 20:08:05 GMT  
		Size: 5.4 MB (5439703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0fd41a48a5de071825f7fde967ed01b01ff0a12b999892f327eb3d8dab32acd`  
		Last Modified: Thu, 24 Apr 2025 20:08:05 GMT  
		Size: 8.7 KB (8651 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f99308b08c5d824927a9e0cb1994737be0cccd9547653a0e3675011a14c5cbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130496118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeaf3936def249f7cc2809caa32dbc61102bb63c6ea982499b0711fac73801b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3851c1e87439f4d250c3c0908923968a64dd743e1e5cfc05b798a52dc5d1e215`  
		Last Modified: Thu, 17 Apr 2025 22:49:07 GMT  
		Size: 55.0 MB (54961479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a876749eb88cc078354ef2b1825c8a88b1ce7b9b7f78bedb933d6dff194bb`  
		Last Modified: Thu, 24 Apr 2025 21:12:28 GMT  
		Size: 75.5 MB (75534639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2f0dad1587e8a6bb764498cadbf5b751a72edc9befb54facbec10d65f499810f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f006e000f26d55c231ae1b81e13b0822c89852d3ddf98fc3d425c856b8817024`

```dockerfile
```

-	Layers:
	-	`sha256:3d5890c5d15d93951bf5fc2b83dfdabee086ad45e6c298b0ed3353379c203a2c`  
		Last Modified: Thu, 24 Apr 2025 21:12:24 GMT  
		Size: 5.4 MB (5439321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5bdaff0dda4dd8c7e2fb53e79f50e18b5dedd9245362a2e9081a81742b3b697`  
		Last Modified: Thu, 24 Apr 2025 21:12:24 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
