## `amazoncorretto:23-headful`

```console
$ docker pull amazoncorretto@sha256:0e3263c16a1d4c868a6f239c18c982104591a533e33da14f4b86c061dc189621
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e0ad59274b720b0f561173df1c73310524ec1bc2ea8697838babf0034ffa44e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147004335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59662b4429ac481b68a2ba8bf29c783d422e5f7d6d9bc2055bdcb370cffbe7b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b09b6206031475228f5ccb0baa337f5a7881ee2a256822a59587f7f20a92b22`  
		Last Modified: Thu, 23 Jan 2025 23:08:22 GMT  
		Size: 93.9 MB (93851800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5758acf49a9a2c0e22e0dba0f7dc1a19514494e33577957b5ad71a7178e06023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0503f5c1f39634d8e7c9552674e2418051b6abf918cb3bb38fb7516ad9dab8`

```dockerfile
```

-	Layers:
	-	`sha256:58c306d5c7f931011df70d206f3b884c3a8c9e7f0c1ff0a584e2f73bd72ff708`  
		Last Modified: Thu, 23 Jan 2025 23:08:20 GMT  
		Size: 5.2 MB (5209108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d206d2d11a65040cd3f9428f111baac216226a8488cdbd3576f26237b20c93`  
		Last Modified: Thu, 23 Jan 2025 23:08:19 GMT  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bd370c63b18e5898dddbe8a7031347d97aa86163a0ff1b5cadfdcdcc0125c6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145138188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb441dca2388337aab4599dc1f840070b82f9bc3bb50bdcc298723fea9f88541`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654732b1a46ca449a335f7b4ede7615441905657950a39f8b040826617757ebd`  
		Last Modified: Thu, 23 Jan 2025 23:28:09 GMT  
		Size: 92.9 MB (92867989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bce5af687cb0dbac1f5ecc8b4bdbacaf28980eef1dbb84edbda0522297dce6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e8bf8a72452c905c34063291c6d71af376a2c2e174c851e4aca88b2f77f917`

```dockerfile
```

-	Layers:
	-	`sha256:655b1d2116ee8c94908fa822fb3275bbc53bd4e00d984ff045212a2d7263e059`  
		Last Modified: Thu, 23 Jan 2025 23:28:06 GMT  
		Size: 5.2 MB (5207100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16247432d5a51b3913f00ece11f3969734c594d24c434f8f566980ef31f46608`  
		Last Modified: Thu, 23 Jan 2025 23:28:06 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
