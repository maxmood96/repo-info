## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4e0285a1d225150d91ee7acab3dce55f780fa12b268c3b4a045176496a583535
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8bbbdfc8b453b64ac5e05cd6c99f58bb03d0edeaf28fbe81e8661df95b407cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128478155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb2a21ca0066cded22d10570b35287d85c54aba7808da7dc6ba6121976773c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a866fa19846ed08f159788df1dd3eb21fa0b355d5d1c3ec5a2d19641796ef0`  
		Last Modified: Thu, 25 Jul 2024 21:02:18 GMT  
		Size: 76.2 MB (76163976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dcd0f0760c7c702dc17cf981cf446315f3e8d83c1a3380dc0691c2059b9f01f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c1ee955f4b80e29c8b4823926a1d83eb8193799cb8ceec604d0f71fe71e2c7`

```dockerfile
```

-	Layers:
	-	`sha256:64b59838f162f8da2d7ebb0a7665e06b15ba1c6234f58aa379b5864bf2b2fe86`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 5.2 MB (5197285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721796611f34d7abd5eb2229f8b065474ed98a43b3373bbfe7f8492ce78efa52`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 8.6 KB (8618 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e0408755d7302df3cbd51fe8602e38db1fd0609d85867a5b57a86c61f6559f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126703412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c90b75798618ee4f6860444cd871f82a75525281185f9566b72978337cb2dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:69f1520adb0e35dcf91717c80b7867ab26fcf8ef8506b9831fcca72a1b38b618`  
		Last Modified: Tue, 23 Jul 2024 01:08:54 GMT  
		Size: 51.4 MB (51402016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473c8c54f3f04f39052acec854f134c55dd9bf01b07aa120d270c90d2f5b9350`  
		Last Modified: Fri, 26 Jul 2024 01:51:24 GMT  
		Size: 75.3 MB (75301396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bb5e601c0b82fdf74de51e2f9aa3ca7b36dd7b39b2d359595a21057b32e7a7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21c6c99a28988a35e876a88d48423643d769495a6dff00341f63baf41ae3f90`

```dockerfile
```

-	Layers:
	-	`sha256:268f852b7ba0eb73246d9a6b11d056398639a9b8d0d7064a7152fe2af72799c3`  
		Last Modified: Fri, 26 Jul 2024 01:51:23 GMT  
		Size: 5.2 MB (5196902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f0a756ad7b3ac6f40ae7929dc704c1ab3471c02419d2c2028616af52cc815d`  
		Last Modified: Fri, 26 Jul 2024 01:51:22 GMT  
		Size: 9.0 KB (8978 bytes)  
		MIME: application/vnd.in-toto+json
