## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e66a646f25205552e720b97624cc6cb9749b45653df8064f358ca2d08b4fc810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8a3e45c3b83dd18159e0683b5a2f4257469a20b948ed7a6b4daf5d25ec49abd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143586294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4100f4569d76e50960df917da5145e64783c48ce8fdcba8396739d7abfc0309b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8d10dc2cc1a90c5f8c3a0020fa2043587f8581c6213db6577c6b07544fea61`  
		Last Modified: Thu, 03 Jul 2025 23:08:27 GMT  
		Size: 89.7 MB (89746083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:31a5f7dec2f8a7ec67142bd1d42d066634570a6e28e1ac80d33909739f22f808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b7ba3fe080d0412c75675cd7f09a6b8e433d6438be5f5ec27232d285735151`

```dockerfile
```

-	Layers:
	-	`sha256:bd96d5b95904347209bef567efe265216106bd8041cf52e42ae9f358cfc3e88d`  
		Last Modified: Fri, 04 Jul 2025 00:48:57 GMT  
		Size: 5.2 MB (5210570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c24b0ec5b493308bc0cbb0ea9bfe68fc94c9024659e6f8785b5cb73eb9e249`  
		Last Modified: Fri, 04 Jul 2025 00:48:58 GMT  
		Size: 8.9 KB (8926 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75e32fe1df6f8d7d908ff89657420bc6cda21830faf3d43976f2481f7b5c99d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141369128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb96dddde2fc271a1be2f3b0b614320d07f105924e415032f7c043c71fb781d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d19ee85c94d6688aac198af35025327b137b28bd14f0692fa96a4172fb569f`  
		Last Modified: Sat, 14 Jun 2025 00:07:52 GMT  
		Size: 88.9 MB (88887436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:610b4eae75d8c45b65342f7d3b51c92937c4c025e01b48c5b1ff4af0478315bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bad48153a0bbdb16d56f7100a3438b34224e2c1f6ac0bac9c56bc5d628fef7e`

```dockerfile
```

-	Layers:
	-	`sha256:dbf1bed4ff7ecc28cc3f380bb112b279c4cee810c73a66b8d889fb7c73483b5c`  
		Last Modified: Fri, 13 Jun 2025 21:48:56 GMT  
		Size: 5.2 MB (5209357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b793c501bc565dcb68a73656a80c0ca0dc23a8cb76c56690f2f1704a9f20a874`  
		Last Modified: Fri, 13 Jun 2025 21:48:57 GMT  
		Size: 9.0 KB (9006 bytes)  
		MIME: application/vnd.in-toto+json
