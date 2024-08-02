## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:abdab8a6d72dd4695f630fc2f250e888c62989ba163c9ce8a065b1bef0986322
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b4a5672b914cb451845554d867a58b204719bf7aab070b9b582ede7b0b34e929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128477857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98e8a01a90af0c74e3ed0536786067f985256e0463a6a641c18c28a631cd534`
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
	-	`sha256:cb6230c89c15ad3884b7222b06322338ef758165e0b4068d1270a3c8141a3e43`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 52.3 MB (52313926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d927b74d09e02cb946a03a497fb2a21f22e027b2876430161ff9c8e0fdda4c22`  
		Last Modified: Fri, 02 Aug 2024 14:54:52 GMT  
		Size: 76.2 MB (76163931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da0ad3d9f988973897619b99897bd2144da19c4450a76f6fb904c4cd650ef66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f1290510fa20dc3ca14424edd68f6ed87801c5fdeecafe228dd2824026739c`

```dockerfile
```

-	Layers:
	-	`sha256:fe540700b0c6d157f4be42d542252730d683dd86b9736b1150fd0ea7a5b65cd0`  
		Last Modified: Fri, 02 Aug 2024 14:54:50 GMT  
		Size: 5.2 MB (5198365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace9d9271b80d040d69db044f61a8908bf4da8b9b0685642a34616d402a0964c`  
		Last Modified: Fri, 02 Aug 2024 14:54:50 GMT  
		Size: 8.6 KB (8618 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b0738c71beaa9b511a1cabc5380d67c91cd5b8c115ef6c5dce4c251029817a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126703369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a738645f85eeea0914baa0dd55a7cc10936251b86d487c839c0055cb700311`
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
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a73da9273803a21c85a9026e9b8dcf3ee76acb6bbbd155c265b103619a5d9b`  
		Last Modified: Fri, 02 Aug 2024 05:44:21 GMT  
		Size: 75.3 MB (75301357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0ea46997d1ed7c74db6f99fecdf6160b858157372179e35c251774230fdfeea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd34cb2cbe3ad78d3fdce97268b0daf2568e97d5c64169610870f7b24517e480`

```dockerfile
```

-	Layers:
	-	`sha256:688729f51b4e73962d616b1d5b761f45121e98751e0ef1fb9940e5ed832575df`  
		Last Modified: Fri, 02 Aug 2024 05:44:19 GMT  
		Size: 5.2 MB (5197982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615a1703efa2a2f871811a4136f4bc679cbce564331a0f1ffecdf74f0ee7f34d`  
		Last Modified: Fri, 02 Aug 2024 05:44:19 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json
