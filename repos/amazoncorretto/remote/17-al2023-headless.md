## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:6d9995b388c19d09e2d1ece55ae61a0814b39efa9e7ac5642a5373db415810e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e7785b4c603efb39cf32f08c6240d20b474caebdf766f473cf3012f698000f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138130676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfb2c1d8632e62aa3a141b9a10194a222c6f23b3d69265cddd66554943cd51b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bd6bf3c48550c355ceb2760e35c366cc8e9cf9f54937d08d834713eb0d770b`  
		Last Modified: Wed, 02 Apr 2025 00:00:20 GMT  
		Size: 82.2 MB (82223623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:74f476d70ca48009f57bea74978b4ea6b629e9332392f488ece93ab8f0236ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbaf754204aed7dcbdf8f5c5938fcea5bd2b91aa30b2b1fabe49dcce7ce1961`

```dockerfile
```

-	Layers:
	-	`sha256:abc19a5b828d148fa3e5269ad24bfa258a8328b9847582ea18610d3fbcf38eed`  
		Last Modified: Wed, 02 Apr 2025 00:00:19 GMT  
		Size: 5.4 MB (5425776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4071aaa9f1e421b5c224e28734113311e94be8c762c79b73075324df3e7664`  
		Last Modified: Wed, 02 Apr 2025 00:00:19 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e3235e0c2334111a46b2728123bfcf901bcab20690a6fe753a74cfb4daa7f6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136621508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579d7275a82e010841e8e397637fe0ea37e211ed5eda4d54649b6ef645bd1e10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638e747f4c8299f2e21f66ffe1d5523e32ae50102c734e89003da005bf74da76`  
		Last Modified: Wed, 02 Apr 2025 00:31:34 GMT  
		Size: 81.7 MB (81660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8be59e15661111f5a12a725f5921eea70fbe3a29bfa8d6f551cf8920591d84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5433395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a46d9c7ac27686edc7a9630cf4ffdcbea0f00be8e9150fb4ef3c6d152b1fb1`

```dockerfile
```

-	Layers:
	-	`sha256:a95580616e9bbd72b412ec5132f6e8a743d08f92f69af1416795c0b0f8fe4ec5`  
		Last Modified: Wed, 02 Apr 2025 00:31:32 GMT  
		Size: 5.4 MB (5424564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00942200b289fe3bbc5cd88acdddf2717ce9aeae7f4cd0efbba073cadd0256f`  
		Last Modified: Wed, 02 Apr 2025 00:31:31 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
