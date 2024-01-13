## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:8dcc7eaf5b7e8178ec97fdd0fc67d2e4be813822d1a4600392cd7837aea98395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f816df0b8fd143332365c8d8899be7df77a94d7325b5fd32f675581eae25b626
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128292165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1f3a2da64fc6b6a2615d6bbcd870ad8a9fcd1e03b1069f6c94d26eb45c63a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:33 GMT
COPY dir:3d1c4d9e1017e7de559aec6b3779bdf6668d0e4f73f6af00952a84abd805da43 in / 
# Fri, 12 Jan 2024 21:45:33 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:18:00 GMT
ARG version=11.0.21.9-1
# Fri, 12 Jan 2024 22:18:44 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 12 Jan 2024 22:18:45 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:18:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592fcbe9ebcec6e31ad10b3d219e4f61ce8e39180e215fab37ae75bc7ac4c0b7`  
		Last Modified: Tue, 09 Jan 2024 00:19:51 GMT  
		Size: 52.2 MB (52238109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6833b2393a02b4b6be027f99712ae3a0c85c0fe08356066247716d128dd0001a`  
		Last Modified: Fri, 12 Jan 2024 22:30:37 GMT  
		Size: 76.1 MB (76054056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7e01cb8b686300ef3a34f869234904c8a361fa4329a6e89e0b0ad8811a888a6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126530596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92c6d5cfcd2c456fccea9619689865d98ee3dabe99fddc573ab1aad5ba11b4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:07 GMT
COPY dir:80de4926459dcf07edafbe2044439672e4fed6bf5796881b9953e9ffab3571d8 in / 
# Fri, 12 Jan 2024 21:49:08 GMT
CMD ["/bin/bash"]
# Fri, 12 Jan 2024 22:31:29 GMT
ARG version=11.0.21.9-1
# Fri, 12 Jan 2024 22:32:06 GMT
# ARGS: version=11.0.21.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 12 Jan 2024 22:32:07 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jan 2024 22:32:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6126164e178e3570337610ef0b171038c4426a730623557513d2ce511166a065`  
		Last Modified: Tue, 09 Jan 2024 02:25:54 GMT  
		Size: 51.3 MB (51303151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa915c8d5ceac91eaceff78d062b684409a995e3b57d31dd01dec98a9d7c7bd`  
		Last Modified: Fri, 12 Jan 2024 22:41:18 GMT  
		Size: 75.2 MB (75227445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
