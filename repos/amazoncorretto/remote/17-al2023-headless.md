## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:824c40de586807682a31396bafa81660537f602f244e06969057728833934271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:86d80c4344455298ff56586244ceb24a986b6879051298d071170394ef1c7792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137059714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b198d3a8848f7bc7ddb5a783543e71ac8f26a1972599eacf1c129f3ee1412b3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:56 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:56 GMT
ARG package_version=1
# Sat, 30 May 2026 01:11:56 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:56 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa304d12b26e5df0099aac2d8790c6cbbe9b756947aa1257caebb2b6ad50093`  
		Last Modified: Sat, 30 May 2026 01:12:12 GMT  
		Size: 82.5 MB (82488558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1e281ecfcf90bb91568270b929fda336614c6d7e99894d10135eaba99c83e737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb703aa8e38b2396041b56d7f94fa2bea6d4876c9b50230012796425df78791e`

```dockerfile
```

-	Layers:
	-	`sha256:24a70e8e13366bfeb74f54d2738df7265b23865e9c8bf64718db485ba5f29e72`  
		Last Modified: Sat, 30 May 2026 01:12:10 GMT  
		Size: 5.2 MB (5190163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78953d852a4ea1f16ded48e6fbe4ba94d976470eb75db050b46d84d035e6c1e7`  
		Last Modified: Sat, 30 May 2026 01:12:10 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:93f307aaf48639fdf97cb233eaf600f8e164d48bfb40d2042e0541698bdb8695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135356401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfb071efdae511cbbf4be0bb2dd905401d6d5c484b3ea43fe939650c04fe9f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:45 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:45 GMT
ARG package_version=1
# Sat, 30 May 2026 01:11:45 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:45 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86613385491dc81323dcbf052875e9797a1a1a8a3bc92256f085d9568fb23031`  
		Last Modified: Sat, 30 May 2026 01:12:03 GMT  
		Size: 81.9 MB (81898574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:751fe1b6f7bd477e37ce17d874e2e6adca4b140b2e98e0a91d1c5c9dd869891e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5197914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893f12ad5ae2cf2171f79b40121aa6b8e0b9a5c16bd3b0fb895820c69d7ed98e`

```dockerfile
```

-	Layers:
	-	`sha256:c605c02c9cf9672026fa20d43018658f98c4fc4d1e35df191cd451ad5c45ff4d`  
		Last Modified: Sat, 30 May 2026 01:12:01 GMT  
		Size: 5.2 MB (5188952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15320f9513c18184ae13c0184fb36d07ceeb12ec46acdc7c72e9193fc8bb233`  
		Last Modified: Sat, 30 May 2026 01:12:01 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
