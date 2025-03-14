## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:50f674a5a6e40d10ca5c7a5005b2b9168d1f5479b5eb51cad0571fcbbdfefda1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ae078fdec7ed37db60b4a749e681bd40d67ce800eb08aa9af528dab5362ace9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146266622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77e3b5f3b6abc5afa0fc13dda0914167831cef35a9e5b34f2147e5105e45b2f`
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
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990892632b29d2bdc025aa0dd71a6801906843d6914cd0d0907e1c737f6957c`  
		Last Modified: Thu, 13 Mar 2025 22:53:10 GMT  
		Size: 93.1 MB (93139746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ca1297bfc64714c7f1dfaa7ba7ccf602ea3783bef17f3f1c9a061043ebecef12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5173226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a284ebfdfd047a8a9e9de3ad879edc6e3e894fc5a10aa197582e2a3be242176`

```dockerfile
```

-	Layers:
	-	`sha256:b5e8c929d2537e56c0650d7c55bcc640c2114321922776c517cf9f220beed70e`  
		Last Modified: Thu, 13 Mar 2025 22:53:09 GMT  
		Size: 5.2 MB (5164154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a94f86c8e07f10a929669a5025bd565ce80cf2a136f545139128bb991a79075`  
		Last Modified: Thu, 13 Mar 2025 22:53:08 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

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

### `amazoncorretto:23-headless` - unknown; unknown

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
