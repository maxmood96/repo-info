## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:cdd2c2e590b98c0005c987c9ed88829df3b47ec98d630b3cfc1a14d25d6adb69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16cf16bcccfeea0d8b1bf284613bdba0f8f2de8ba799408ce57dc9e3a73ae3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136154314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e14f91347a55c58b039b20dcb4d5475c04e155e24bdf311d027030d02dfe9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52456cca82162ac2720f5306c42d4f71e47306411fcc6e5da8b8d179bbff728e`  
		Last Modified: Wed, 13 Aug 2025 23:02:16 GMT  
		Size: 82.3 MB (82316355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:089f521531fb57ec6504b35b3587defabaa140359f2800229e1c4f6cd0cdfd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01b96d5c9c936d286a3a6645c3abb2c3f55a10d61d79fb9f77f6b8c74aaa8ca`

```dockerfile
```

-	Layers:
	-	`sha256:6046b15ac8b09ac751c0fa857d71c645d42ddc66017474724e6c8bd2c7401ab2`  
		Last Modified: Thu, 14 Aug 2025 00:48:30 GMT  
		Size: 5.2 MB (5182816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aae8daf2dd132cf85ed2a9c618e425f96c2ae60d8676e134998c71bb25992c`  
		Last Modified: Thu, 14 Aug 2025 00:48:31 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0e66845d05827b94e3e0267943edf0a26a27e1cf1bd0d03481537e183cafd669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134461414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98abcc064a154bdaef5665d9cafce5351fc84359041e166b2bd7f02d43a206f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7ab21410d3c6897ebe4e1535d0adceaf2c5deea9b3f52f69d26bed6b7712ff`  
		Last Modified: Thu, 14 Aug 2025 09:22:31 GMT  
		Size: 81.7 MB (81735020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97c0cf482d361321b885fa0501ae913f2382838c1d8c4b4d04979a6a6f4f497b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba031c0cdfb1c7e23406a0d39dd420a78816297bb73386d10cca99c1a137e78`

```dockerfile
```

-	Layers:
	-	`sha256:aa7187f9aabb6e944debf2de83e3c461b3027821527422f30badb926fb8ccaff`  
		Last Modified: Thu, 14 Aug 2025 09:48:30 GMT  
		Size: 5.2 MB (5181604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc2461c356f8d967545ed71265e5f281901e47331c3c1f7858fec9a342e1706`  
		Last Modified: Thu, 14 Aug 2025 09:48:31 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
