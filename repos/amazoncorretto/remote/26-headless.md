## `amazoncorretto:26-headless`

```console
$ docker pull amazoncorretto@sha256:67d1d693b1bd307eff836119a3887c75ff2242752b48b077e8191b0b28aa6d5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:02267255abf6074c12b91814d7302d6af8b39aa0016a3252288eed7710f295ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160393408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bbcde5106e5b422a83d6f9b25bbfed91e4995157d48b144372a2c71fa2d11c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:13:01 GMT
ARG version=26.0.1.8-1
# Sat, 30 May 2026 01:13:01 GMT
ARG package_version=1
# Sat, 30 May 2026 01:13:01 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:13:01 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:13:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5b77a04e24c91b119e9578d4d5cc95fcb0a8fcc060414eb0a2e423154cd690`  
		Last Modified: Sat, 30 May 2026 01:13:20 GMT  
		Size: 105.8 MB (105822252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9554747f4fbf56beed090789edac30ab6039bbe7a0d109936edb7ced23af8379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe47cac534dbe80b39d609e1090faf6ad35c9d5cfd0160631f5d8928bce1d96d`

```dockerfile
```

-	Layers:
	-	`sha256:479fd0caa69dc3f109337c1dcd60fc359d5790d19e831f0d905f75d3d71f9373`  
		Last Modified: Sat, 30 May 2026 01:13:17 GMT  
		Size: 5.2 MB (5200408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e9866deaf76e563f14befeaab084c981e0e29e99b5ff1e4b4ec62e97dc42d8`  
		Last Modified: Sat, 30 May 2026 01:13:17 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e9097008fd1166dea57c8bbd56998bac9c3778380a55aa03167a3e177611edd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158165865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6344a9050b7e68ee76e379ff76553ae6fda0245ca028af0261c9a1550e4f4e3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:52 GMT
ARG version=26.0.1.8-1
# Sat, 30 May 2026 01:12:52 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:52 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:52 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83af6547ffcf56b5007dfe7564fc037cfad2f0eac4aeba336681206073dcfb43`  
		Last Modified: Sat, 30 May 2026 01:13:14 GMT  
		Size: 104.7 MB (104708038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:62a4c2691eb62b8dd23422485d79a3e47e4e0b6816522ae72acfbca2b6cbdf70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce6661de9bddd700b908d6a8eaf7e6c79c00fa0c9b3ba63f0d99c5dad7fb95a`

```dockerfile
```

-	Layers:
	-	`sha256:87c0cd23c939b8841d44aa9e8e6db93bef1a93a6878c20ae72fae9f878b2d3b3`  
		Last Modified: Sat, 30 May 2026 01:13:12 GMT  
		Size: 5.2 MB (5199218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339545750bac518b8feede6b3fba7143bb98b905d5a5bfdebdd7c2d4d60af01f`  
		Last Modified: Sat, 30 May 2026 01:13:11 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json
