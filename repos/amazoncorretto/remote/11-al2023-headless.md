## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f7342fed429c78528be68aa033fd06bce9f8d7f3e6bb267acf121d62e39c923d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:62e48655aa14a14b8a9f89465a5bb35186785cd7cd0ea4fde0c3985cb44dcd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130630999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373257eabdfe7153f7735b4b10a5095471f9c12c18dbe6a7830e4d4edf436962`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:15 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:15 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:15 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8caa325ff8e5b3a90bbfd6a4c8abdd4d9388900a17c94093d7e2a453fd67305`  
		Last Modified: Fri, 22 May 2026 21:11:32 GMT  
		Size: 76.1 MB (76058559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:abacb5448d9e71e0f4dd79c2c45a436554bca160d917dace9fb4e742271e69de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bde131a535c741c129786f0ebf97b833120e23fddf8daa0b3d742421028b09`

```dockerfile
```

-	Layers:
	-	`sha256:e4c272906db8de24778d125728a28779e8b1c819a439350076bb602334336617`  
		Last Modified: Fri, 22 May 2026 21:11:30 GMT  
		Size: 5.2 MB (5203271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd43adaaf602131dc4eebab0978d9795e55ebeb43b727b5051fd327dbfdae6b`  
		Last Modified: Fri, 22 May 2026 21:11:30 GMT  
		Size: 8.8 KB (8783 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f8cba1a828435a4b3212523c8d09f83c2340cbfb421c04d414aa3cce8de74b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128758621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0ebc1c2b63e25daf43942a7bb7af9a7ad60af921c0751a5d4c99ec2db9eda0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:11 GMT
ARG version=11.0.31.11-1
# Fri, 22 May 2026 21:11:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:11 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ed6c3df03f12aa665d055dac841928bd04354adafbabfe2f6e9350775e8d8f`  
		Last Modified: Fri, 22 May 2026 21:11:29 GMT  
		Size: 75.3 MB (75304206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:62f4241a3d8e0bf091e0b7d4db38e627a36dbf5810e233c94dd900b65aa3fe63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7a14f63051ca4361d8a6b9ca1947ba86d17d871c46ea22643100c72f4af5a5`

```dockerfile
```

-	Layers:
	-	`sha256:6ed1e8a752917e88aaa8b14972fb472203a1dcc7e839f8fbe8f97f614d925a7a`  
		Last Modified: Fri, 22 May 2026 21:11:27 GMT  
		Size: 5.2 MB (5202889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:000e3fa821db406471be34940284c730dd96dcd9eb7d327f86dd6617874b961b`  
		Last Modified: Fri, 22 May 2026 21:11:26 GMT  
		Size: 8.9 KB (8863 bytes)  
		MIME: application/vnd.in-toto+json
