## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:128b1d76fe24e6af83ef44d1daa131e52eb8a68216344867de2e91155ac0afe5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:df169e74d43eb65345ce1d051b91f597342d72c74d35e3b80ed2dcf27a85357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135741258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaf4ed1b20a2f44cf20f5d5bf0cf81bf8559f11dfdd621000b2f67656b730a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da77413fc9943de2c4daf17ca14f779c7680b4777ea579b2092212c50263e05`  
		Last Modified: Fri, 13 Jun 2025 17:03:40 GMT  
		Size: 82.2 MB (82170898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:22dda964b8b45a6d3a84881d5b7d6b8ac52faf432b0f45e888789a1b592a340b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614ea1482ae8a750a35bfef8f9306ffc05f1aec12a0f09fd4b68df536083fd14`

```dockerfile
```

-	Layers:
	-	`sha256:74cea94b89cdbae3925e5ee49820fa0096735b878d98f03f706d6e35fd69dcd4`  
		Last Modified: Fri, 13 Jun 2025 18:48:24 GMT  
		Size: 5.2 MB (5183519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a7021126799e4d023f6779bffd2e50a993ced978f5eaccca10bdde0c534e773`  
		Last Modified: Fri, 13 Jun 2025 18:48:24 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a73664da9934f13ced6bdde8164f58131a8dfeee64be73f7d7b52bcdf7af3de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134088315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afc9076906e172d7e227e767c02782333982a826bea56b233550f1394b8a9ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f2d7ed50f9546843ccfc351551d6f453fa6a9205edf6dd60335a39ec10243b`  
		Last Modified: Fri, 13 Jun 2025 19:59:51 GMT  
		Size: 81.6 MB (81606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7eee4720ed5cdf4298c610537c5b0a2c558c239515194c5a55155ec36c5b0c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aff2beba49ffe7b0dc1a5a9d7127969376a40c2d38c9e1a506af2d5642d262e`

```dockerfile
```

-	Layers:
	-	`sha256:8003319a5f4c19e279a56d3e941873d4f3a0d50cc26fc7b05cda28249f0c47a6`  
		Last Modified: Fri, 13 Jun 2025 21:48:24 GMT  
		Size: 5.2 MB (5182307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9937017a639d29bb377e6468336fb6f050d17efccffdb04bba29cc8a598e3d`  
		Last Modified: Fri, 13 Jun 2025 21:48:24 GMT  
		Size: 8.8 KB (8830 bytes)  
		MIME: application/vnd.in-toto+json
