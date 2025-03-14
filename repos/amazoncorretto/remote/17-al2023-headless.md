## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b4467df5aec85685e4c231aa0ed15eecf3ecf796d0b8e5619d9ac14cd5ff9fa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5f02710c162b4d87d768b71eddc99ecc425405c11f37ff19f52a87be7af420d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135257653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56aa8fcc630bfa0b231c299d5e953b33399ad6201c9add45074c4620a2c5c3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aa32d86bbea14d2ee7e74d7af03079c26c97bac200f8759fcd717bac8f6418`  
		Last Modified: Thu, 13 Mar 2025 22:53:00 GMT  
		Size: 82.1 MB (82130777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9243f914f4add160e4c834c92433ecad8326b4c802c581c26f10d6ffad09235a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daac149af5afba920e9676c6ce72f4f235440ace1b01ec349a33a9b367e5d4bd`

```dockerfile
```

-	Layers:
	-	`sha256:b5cbd4498d2e481c569d45a01668bcaf133dad75fb8bb6c926c793190f5fd43f`  
		Last Modified: Thu, 13 Mar 2025 22:52:59 GMT  
		Size: 5.2 MB (5159712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a4d088338e381d27d9dea645b6f9b816e9f065d7d82975da8759e5050e6084`  
		Last Modified: Thu, 13 Mar 2025 22:52:59 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a3bbe15eca1efba6c5ca888b518278d4af87533ce8f7a9eda90fb1db1ed64f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133811242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d5432b8f8cd213099fb8554aa81ee00796343a6447702efe0044f2c2863452`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9494e20c1d9bbe9df9f7d695fc8a77124fac15af29be88561c01d1ec4b66e7c7`  
		Last Modified: Fri, 14 Mar 2025 01:14:29 GMT  
		Size: 81.6 MB (81565264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:87dd538c5c9aa8ecb0e6c63dfa359877106d98f3f6a033fc034c82dc6675ea04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922fe8fcd8b068a8ee2a918de0a540f133c788e2e7180749318cd885b040b2e7`

```dockerfile
```

-	Layers:
	-	`sha256:83a3136cd00ef32241eb0a1a285cb543d520c0334e18b26347da0bc192ed3511`  
		Last Modified: Fri, 14 Mar 2025 01:14:28 GMT  
		Size: 5.2 MB (5158500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f9b8ddbc3d2cee84b8c5b255944620bc50d94977435543346ba117353c5157`  
		Last Modified: Fri, 14 Mar 2025 01:14:26 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
