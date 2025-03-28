## `amazoncorretto:23-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:67db2af7da4c83f89310e3d4aa63e8f5f6282247caae42a7a5af1e7972a7034a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:26a950b84ae47b03bf3416c936cf890b2cedcc63661e0348812953a6aee2aa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146257448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e63b16853654ed8f1830b3fbb1f6af14075dffe01fa11190cb553dd9f7ed90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a3997625fdfa5907bca53f4f3f5dda1fb87e6cbfe41b47c4abaf94b08dbee3`  
		Last Modified: Thu, 27 Mar 2025 23:58:55 GMT  
		Size: 93.1 MB (93134159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:68134e5439f065da913d10f55b7ff6c29709edc0e33d23f8a62eb3abc7ec3d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c798bee5e3f1dbd3ba937ce391a83d312afd751f56f6b615f5917e72bb529348`

```dockerfile
```

-	Layers:
	-	`sha256:95942b6d311ef6c7b53677c8b53e4624817fa55116b3e95ac192223d8e3a8394`  
		Last Modified: Thu, 27 Mar 2025 23:58:53 GMT  
		Size: 5.2 MB (5164154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0658198f55ea49741fa801cb6ecee37450b152f25a704594b76d399b7cb2f7dc`  
		Last Modified: Thu, 27 Mar 2025 23:58:52 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1115a00954b9a2142a652818c9bdcf82302d5ad67c73e4c8cc746c76fa75a4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144391892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d506275beeb9555a6d456e11b717838db78f94dcb54cdea9cdb3a301833e0f6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733785b4ebc8e9220908ae3ad86833e51866c8f1c3d840a86f58e25a6ca5d087`  
		Last Modified: Fri, 14 Mar 2025 00:32:31 GMT  
		Size: 92.1 MB (92145914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4008328333e6891fa636ae7cb1332d21ecb16c24069f27f46b5e5c663513d293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d8a81fb8136d546f1c3e35db225245d5a1186b9dbf378ed819ce72057c0024`

```dockerfile
```

-	Layers:
	-	`sha256:449b4c393bfea08315ca2f2d18e57796e61314523389290a414f9b63ce8917c3`  
		Last Modified: Fri, 14 Mar 2025 00:32:29 GMT  
		Size: 5.2 MB (5162143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1e80813546a456840d4fda28f0682016c70bb4b049214794ecabf3e06adb58`  
		Last Modified: Fri, 14 Mar 2025 00:32:28 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.in-toto+json
