## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4fae1a87b0b96332c79cce4900e83970ab1e85f1094526bc0def6e63f9f94bc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9b74e227b7ee6c1f7e06ef4f4aa172300e56e63be6d0f58636e2af3c5ac6dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141901061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f790733db81cf4bb8da1c3ee11528a8aa3d73a2a982fbbb42dfbbc189c1900d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2888bb54d8028843ebdf448070a3e12bbfad0ee68b12082ab4c2552fbc1dc016`  
		Last Modified: Fri, 09 Aug 2024 20:49:31 GMT  
		Size: 89.6 MB (89583158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cd2082de072b98997e82b0ff493d77bf8ce63004c31e68a04e24ac6353ec7e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7159157080c17425b1d8fe053a3c1cc4d97041390e0f571842fcb5d72f1e0f14`

```dockerfile
```

-	Layers:
	-	`sha256:9ee331adf05d3aa0f7b07b82a50cdbe2bc063ce36199663e72d827388c520bd0`  
		Last Modified: Fri, 09 Aug 2024 20:49:30 GMT  
		Size: 5.2 MB (5186087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f629ece030d6b8b1840f104d62754ff7a5c99b181321344e1596abb0a0f5b64f`  
		Last Modified: Fri, 09 Aug 2024 20:49:30 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c616b229c1fbbee552c0d2b9f420501fc298d0bf57eec1c2e1a68b7d55c66ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140020512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6e19e2cd6131d7d39b360c1b35054331011f3f00443cb98879e10de894dc5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:6dc418e3f016a388470ba66be212f100f862b0633543844e880b17590526cce0`  
		Last Modified: Wed, 07 Aug 2024 03:04:12 GMT  
		Size: 51.4 MB (51409634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5767465f7bd8199f41ee7fc9b33365753f84e80ab2a7038d7825a9e7b938962`  
		Last Modified: Fri, 09 Aug 2024 20:56:19 GMT  
		Size: 88.6 MB (88610878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7a25f1de80624ea66ffcc59e8b29b28ddce9456e795902941a4c10ca3c4053e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255c565093d3034c7bcbc9cd111a78e14a7aff7c3d81c075fb2d6ad754861e7e`

```dockerfile
```

-	Layers:
	-	`sha256:842de4fe749bccb44b8bc67fa79cefb3e115b163c4673ae1df834bf900993221`  
		Last Modified: Fri, 09 Aug 2024 20:56:16 GMT  
		Size: 5.2 MB (5184875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b843f0d86f70ce36daae9e29825f5e9fb91c83a73718e0451ff6acc3d79bdef4`  
		Last Modified: Fri, 09 Aug 2024 20:56:16 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.in-toto+json
