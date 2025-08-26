## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:09cc9a61d4375176f0939a504716427e17d1a86860dbda898e26ec4052c496cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:33f22fbaecd331199a16ddbd79ac2c3f8cf6e89e2e5a58b95f5bd234fae33167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136911027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e574db354f8dccc69f73021ef3d870689ad6df250afefc894756700f1c85de3`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a9ccac4fb23ffe24a344fb5fd65ed114654873f47b58299930bb693a443d45`  
		Last Modified: Tue, 26 Aug 2025 00:01:14 GMT  
		Size: 83.0 MB (83042297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:234f231aaaf29b9620c97f147aabe1a40aab7fe01e94691247e2f3f7cbdf5390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c0d50f9c4efdecca26cd241cb4b31a636415ea5c31d17b096ef20d695d4e4a`

```dockerfile
```

-	Layers:
	-	`sha256:a9950e49dc32ee33e351db45db123a3a39be2574735e45f7e10792a4bcb2ecdd`  
		Last Modified: Mon, 25 Aug 2025 21:48:23 GMT  
		Size: 5.2 MB (5208245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6196a8fdbf9e81e751074a9c08b0afc3a9111aafcf716f83564506a9c779a626`  
		Last Modified: Mon, 25 Aug 2025 21:48:24 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7c6f9df5848b60fdd8ab0fab7fa71af4f27ee08fe85ec1ef5adf780cead4a962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135237660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45722cb43f46014252d8642033199fd62eabde26c584a7a13d98c7aa2125d973`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f0b7d54214a6f9c2c7698f71fb06f2128097c3f9d97269e3d449f7639c142381`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 52.8 MB (52768497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ff00489304db01c8c160502de70c3456dbf8f38701ceee23f1395321d8d546`  
		Last Modified: Mon, 25 Aug 2025 22:19:00 GMT  
		Size: 82.5 MB (82469163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a7e3e6663fa1f084dbef43b416d236206228dfd2e5743b50a9a49778189db631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eddf683edc51ec6e8242a892fd626b645b99ba2309769eacaf58fe351def641`

```dockerfile
```

-	Layers:
	-	`sha256:f5e56478ddb2ca1399f6980f271403e83f4a83d9a9fb75566efa58f459cf3d2a`  
		Last Modified: Tue, 26 Aug 2025 00:48:24 GMT  
		Size: 5.2 MB (5207036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47284fbce2b3b09422dc588a13fec7ff09413c6638977638d321750da0b56ddb`  
		Last Modified: Tue, 26 Aug 2025 00:48:24 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
