## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:58ed1bf5476791269df02bcd57dfaa386f6cd88c734aa215db127fda9213117a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f454be55b4f039e9239b57c368ab6bc290f6ade8f929022cfc3624f6e206a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130635766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd184bf6d837087fc1ff60baffe5fcee08873869f162c9a7301967620004429`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:40 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:40 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:40 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8e7379d6b779d4a3ebaf76220f40cce67546da04807ff79e75695c7a7ab331`  
		Last Modified: Mon, 04 May 2026 20:11:56 GMT  
		Size: 76.1 MB (76059013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c3c87924fe5d592cd32f1a95d0dc5a1c16ccdcb612332a92efbb90e7a26b7009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9634101ff5746f0bb0e6a5ceca67164c9d24f200629dbeb4988bd7caaf9c375d`

```dockerfile
```

-	Layers:
	-	`sha256:244afc12be35f455cedecce65d0f932e360165739538e01481b8e6c445fe98cb`  
		Last Modified: Mon, 04 May 2026 20:11:54 GMT  
		Size: 5.2 MB (5203271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce939a6d4f81d0ecb1ed8777f3bcf502d4cdc89e68ce778c7a80b0e8b2042933`  
		Last Modified: Mon, 04 May 2026 20:11:54 GMT  
		Size: 8.8 KB (8783 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:583074f744f6e31f0df7d86a2c3ac1a5ebd5cc6ba8cef204f0cb9c28699cfd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128761112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a09b49d31389a8b4d3858492dfa2be49d4267477f190645baf0bfb2000943c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:27 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:27 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:27 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7358e3658c02a05ca4eaa2d7458a04db8ac706d0f211b82531f695957b62f29f`  
		Last Modified: Mon, 04 May 2026 20:11:45 GMT  
		Size: 75.3 MB (75304342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3472832f94822b320bff2808dd244ee2c4921666b441a082f1f7b799c1f3d9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c1e746e61584372415192ceeed0e2708405a7bd4533c01a243c8a19c00d19d`

```dockerfile
```

-	Layers:
	-	`sha256:841c664d4aee153a25291072e7030c3ded01f87f4d0ac22ea90232f180397d11`  
		Last Modified: Mon, 04 May 2026 20:11:44 GMT  
		Size: 5.2 MB (5202889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2638212aea933829440b9a7928f70b302130adfd6bbbe66cc216b059f3c64965`  
		Last Modified: Mon, 04 May 2026 20:11:44 GMT  
		Size: 8.9 KB (8863 bytes)  
		MIME: application/vnd.in-toto+json
