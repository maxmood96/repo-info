## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:eb2496d6f3cb1b8087bfa2d850497f9cab3e4744b67cbc7b3c0f5099791e2fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd8daf210b5daafcf50792b77fc31dab3a54c0d5f7563d6188904f668c81a7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158276755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aedc13d35651f988e6d2fc8f3adb54c194825a4a794ea8775273b792f6d4e468`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7488ff503073695e13c4374e385219f427cc05f6d2805550b59220296eee1d`  
		Last Modified: Wed, 02 Apr 2025 00:01:45 GMT  
		Size: 102.4 MB (102369702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:123192cf9c67e24c3bce7b58921f2221f3e6d4781410c4dc9b0a5eefa4a3bfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4300808eb6393db69dbb9fd94492e28e808d78c48d0fe8761a041aa029b7fff0`

```dockerfile
```

-	Layers:
	-	`sha256:74933a6c2580ebf17c669c33c68b5dee72a9312a06551603d5263f714fae9891`  
		Last Modified: Wed, 02 Apr 2025 00:01:42 GMT  
		Size: 5.4 MB (5437653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8571af5dc4afa8a0838186b14ecfd8d8feb85903c6ecc6a2df2bdd2df6fde6a5`  
		Last Modified: Wed, 02 Apr 2025 00:01:42 GMT  
		Size: 9.1 KB (9073 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9fcdb53c5ae5daa85235b4067cb1305e71ed15384d69663b2015d2b38d7ad0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153506910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d5b1b37b6b16e2781a33f4d26f9690e206abf71f1c9057603ced091d49689d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c667e213f0556b724833a064eb4736e28d8c15fdbaa3ffb0c2621ca97f6039bf`  
		Last Modified: Fri, 28 Mar 2025 00:26:40 GMT  
		Size: 101.3 MB (101258920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:779b35f1255c60a23f52857106bb6edc22e5be18443e6b638a3c04c8453c0ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02edd318aec8725837faa559ddb59d24900a3a050fbba5e63768f65ecdb8f625`

```dockerfile
```

-	Layers:
	-	`sha256:19f8190e070b42f0fa200946fd73a21176db3d4953dd1b476897c1ef6de8f108`  
		Last Modified: Fri, 28 Mar 2025 00:26:37 GMT  
		Size: 5.2 MB (5170400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5394faf2b250a10ae850b944e8fada7a0028a40b20461ce0a79861c3069564be`  
		Last Modified: Fri, 28 Mar 2025 00:26:36 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
