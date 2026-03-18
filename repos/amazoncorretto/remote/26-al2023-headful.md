## `amazoncorretto:26-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:12dff7d0d17c6f8da5a1c55ceac70057545d88d7c596c83c9509b847cad476e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4d79f78d76fe616616fe961fc4a4a7ad51d76eb1542baafd6f570a6d5de18907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160572947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3663a5b8feed6a4e999fe97ae342d045fd1d752c2d115f2ea25e11e2d350b544`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 22:59:56 GMT
ARG version=26.0.0.35-2
# Tue, 17 Mar 2026 22:59:56 GMT
ARG package_version=1
# Tue, 17 Mar 2026 22:59:56 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 17 Mar 2026 22:59:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1d09fa4c5c0248a2372d743138f2b20ca80d9a78db81683babb8cef24092cc`  
		Last Modified: Tue, 17 Mar 2026 23:00:17 GMT  
		Size: 106.5 MB (106539857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:167ba41283c0c1ec729a5735c6ef441e347d64d94b71f17b994fc1c73e6cf649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c68b84a6b5e8315830077fd0bb9c63db9737b3d7bd4bd0684ec163cbfd37c8`

```dockerfile
```

-	Layers:
	-	`sha256:d945b4e3350552ea2de6d66007fc265170f1e5e1833837aec76d5e298d5e20c9`  
		Last Modified: Tue, 17 Mar 2026 23:00:17 GMT  
		Size: 5.2 MB (5219457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eba66894b4b23cdb363ec900393ae88b9eea43940d17b735d7574974ee6f75af`  
		Last Modified: Tue, 17 Mar 2026 23:00:15 GMT  
		Size: 9.2 KB (9212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d75f1fddfd3e1aeadd771e08403f061917b273ea4ed9ec57e500e4d0606776d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158374993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7c484c2d857a3d6187423b0e209f7206a4fd840f76f544c1ef420dadcfd49c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 22:59:56 GMT
ARG version=26.0.0.35-2
# Tue, 17 Mar 2026 22:59:56 GMT
ARG package_version=1
# Tue, 17 Mar 2026 22:59:56 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 17 Mar 2026 22:59:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f199b47f35075e115c07bf44dd661a09872375cdf95581f143cb31ebfd72df2`  
		Last Modified: Tue, 17 Mar 2026 23:00:19 GMT  
		Size: 105.4 MB (105433618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61c34cde840b628e2288d630ebee08ac78e5d43cc6cea11f527430a475f1951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c40bcc7bf9c61d58a912773c8c1066478d0b52143fcf3280fd615648f2f3768`

```dockerfile
```

-	Layers:
	-	`sha256:52a9fc1502d5099fe6750c786f3d814353c5483597978c1fdd4650f874ecb59a`  
		Last Modified: Tue, 17 Mar 2026 23:00:16 GMT  
		Size: 5.2 MB (5218270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e0f4e4231ec82d550e9179f60b028e910303cd5514791525308b560a3dcfb1`  
		Last Modified: Tue, 17 Mar 2026 23:00:15 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json
