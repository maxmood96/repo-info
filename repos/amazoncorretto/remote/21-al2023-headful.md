## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:310626a623a5af565d76a89d79acd33d8e507154a7d73d2939607e3d62f2c2da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a1328756d989528ccf253dbb66361d8f8ab4e475919b857311f5ebc1ed9f1b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142576295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fc09dc096b57126ddf28fd11f9c1159fadd1c59038b45e74cfb0775bc47f44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:8edd892881e79c0c11996c1a60e2c04d066537e06bdf88e1def994a6148ea23c in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
ARG package_version=1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ee5ee70789863a32f444d11d47a2849acfc6089e3e8c78d196f63475ee994293`  
		Last Modified: Thu, 11 Jul 2024 21:19:58 GMT  
		Size: 52.3 MB (52313695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6c239de70fa48c4e661a4c4818dfb8f4fe942fc1b79e5aaedf15789d595aef`  
		Last Modified: Thu, 11 Jul 2024 21:49:12 GMT  
		Size: 90.3 MB (90262600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9cc63eec1db0546bdc252b864c3b4e3e71f63a3b1091342349fbef501b4eedfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347a76afa98925a1fbfe135fca1e14664bb82cbf20f6602c71fd54608a4496ef`

```dockerfile
```

-	Layers:
	-	`sha256:be32299ede13f48bf9086ff5104d4c5357e4564a80345cf9e264cdd0b8353fb9`  
		Last Modified: Thu, 11 Jul 2024 21:49:09 GMT  
		Size: 5.2 MB (5183141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2013f674425330b401351c9505288769489947fab2f5be135fb6aa705879abd`  
		Last Modified: Thu, 11 Jul 2024 21:49:09 GMT  
		Size: 8.7 KB (8696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3a60e0e848a9ccc3d3bfe3d57fc179c897fe5116f07d84c4a00ac7f132f9586c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140707641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6899fb9198be352530a327bbab1cda76b295eb366b76954457e7fc115e60889`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
ARG package_version=1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db239cd3fa97e52e5b0c725151440690e4b2fab87be8d14a90d71132ab5a7fa`  
		Last Modified: Thu, 11 Jul 2024 22:56:40 GMT  
		Size: 89.3 MB (89306503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6f710782d62f38426904d5010bfb33a1cca7029251dfd2677c430515c459e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4372b442697137778a8f7cac956129ed25b9da857feed99090a685637d2fa766`

```dockerfile
```

-	Layers:
	-	`sha256:b200dbd05fb64120baae266ae4a20d97a4c3d77c5e7f25ab4f4c98045b08a485`  
		Last Modified: Thu, 11 Jul 2024 22:56:38 GMT  
		Size: 5.2 MB (5181931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912e67ec67587b7cd4858934f9b79f04942e4b8e00557ebac74f8a5767006e56`  
		Last Modified: Thu, 11 Jul 2024 22:56:37 GMT  
		Size: 9.0 KB (8978 bytes)  
		MIME: application/vnd.in-toto+json
