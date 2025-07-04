## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:f19bfe4b315ee93b36cf074f6066c736c30664d09994754584daf81ec2e96068
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
$ docker pull amazoncorretto@sha256:4a5f6ebeb025646707f1d629ec7535b20da90f5006743b90fe041472b8429514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141606190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1b7d45d55280cb510ac5d77a25009d9a9fadc614200f00e54e52b4d78be8c1`
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
	-	`sha256:0e455f237a70326021a937388393d9d7ac6f9ae1616673300f248aeb280add13`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 52.7 MB (52717557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c24d0bd1bdf011205d90b3ef9d597f97246e2679b81b85500dd623e5d9e604`  
		Last Modified: Fri, 04 Jul 2025 03:02:16 GMT  
		Size: 88.9 MB (88888633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9710432a8b399f5ed5568adcb681f9cc8f6859d4eff4b88be48d64d0b386a64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d04c57527643ba4dada44a9135c77307278a10b438feb9abdafb85961ea16d`

```dockerfile
```

-	Layers:
	-	`sha256:0690daf23eecbeb509e178a36798d25bffb9ccb2d869fbf53008a954cc5d0e4c`  
		Last Modified: Fri, 04 Jul 2025 03:49:00 GMT  
		Size: 5.2 MB (5209363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3daf7513a29ae107a06badd5ec42720c44ddeb7d9076bb405d97fdec4d2e18`  
		Last Modified: Fri, 04 Jul 2025 03:49:01 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
