## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:8857f6e2592f54a5211db76ea82523aa16a9c6d8f27ae18417e9c5fd871783c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b894876095990ba7e9359b35324675a909e9117c83420bad5d952190f9708219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138152651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6081576612bfb0a55c7cea11fac05f902641c07f8d79682123162ecd1d02396d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89256601defa1190e8ec34d845d2529c95b5f8c9e023ddb065ccef37186e919`  
		Last Modified: Tue, 15 Apr 2025 23:55:53 GMT  
		Size: 82.2 MB (82245598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d7dcfaf2e780d786ce2cdf0cbbaf2a80744f8b5cdf76cd9b3f93b983e067bcf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f28d6332aa68404991f0bfca4313caa49d6bb297a5915831854b4e4ffec11b9`

```dockerfile
```

-	Layers:
	-	`sha256:c587ed86182583b09df085a3af91db5de667e62900bf797a147f75fc9e0a747e`  
		Last Modified: Tue, 15 Apr 2025 23:55:51 GMT  
		Size: 5.4 MB (5425776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcaec1b07da2e77ff7303bd64f2089cdd6e02e646f7dd0c61bd69b98732baa3b`  
		Last Modified: Tue, 15 Apr 2025 23:55:51 GMT  
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
