## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c724ce8c137890d6c4efe94a84e5e80bb381e80997b2c915e7bd8c462ef0b3e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e3742c3735ee3be9752d1be6bc2ccc3aea8b0a506bae0a00f152f3c747d98258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130833115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac75d81d44a6be304b99286583f3e59fa7eb92c506b56b2189c6a742deb28c87`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1c3112c87ab2d6209030c22629180b5d1958fca3765b3cbcfbc9bcfa1ee6e425`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 53.9 MB (53880920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1192a1c432917271246548b5fe89cdc0eafe095561ff84a74827c0fa4ecbdf3`  
		Last Modified: Thu, 01 May 2025 21:08:16 GMT  
		Size: 77.0 MB (76952195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fe8b7476966e592838e2267d93f9f68951e7858377774670e0f7aa3fd072ec7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb960394ca6d6de372a834c2225c972e6ab35ff2f52c8dabb0b056f18d052a4`

```dockerfile
```

-	Layers:
	-	`sha256:a336cf1661a4755361353e97889bf63ccfabf99055fa5ea91c1166532dc117d5`  
		Last Modified: Thu, 01 May 2025 21:08:14 GMT  
		Size: 5.2 MB (5207440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71eb2fa6410bb3592e2bf9dca7714495c72a50e9934e1244c0c463083988b67e`  
		Last Modified: Thu, 01 May 2025 21:08:13 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f93dbb481397867c5f105b8b1f906db2a990ac5b8d947a0841afdb20c1071c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128985327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a29bd94942d9330f71eab0c90dd33cd5c6d4af6133c7057f9babfd1b8ab6849`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5804bd91a568b15c202af6e01f57d869865af0d532f8773d8faefb503ef0bbfe`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 52.8 MB (52811047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096425a8ca700c930931ee921f622231a62e02488a9cf3a006cdced8cf85988b`  
		Last Modified: Thu, 01 May 2025 21:13:06 GMT  
		Size: 76.2 MB (76174280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:91190a9f1c0ca7c7b41c1f33c5ba3301726ecea911c1df548b37e881b6db3036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9224b8ab5bc980f872b46ba9652acfab8bc0556b40b91c483345309bf79c4136`

```dockerfile
```

-	Layers:
	-	`sha256:5cabfdc800348eb555e3e69ea47231c4ae9fad069070e3532e084d531548baa9`  
		Last Modified: Thu, 01 May 2025 21:13:04 GMT  
		Size: 5.2 MB (5207061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566a2f2abf8fb77f454ea97f7040eaa3811ca34ab5b2320c8153691a74259d57`  
		Last Modified: Thu, 01 May 2025 21:13:04 GMT  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json
