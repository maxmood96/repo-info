## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:8e8ecbe7c184eb744d506590a3f2dffde6e70537b85a8f9c183904aba37003e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:193e43961aa8befea4e033817954f9210ed543fbe7bedd84e3c3eb657ecd969f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137782942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff878b84d8da5de76330b91c8e5de910c7a63a24888015d77cebe25f27df64f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:00 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:12:00 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:00 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:00 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b10a1fe4b10a8bb44f5dfcf530a0f2d716818498b40de636add12eec57713`  
		Last Modified: Tue, 09 Jun 2026 21:12:17 GMT  
		Size: 83.2 MB (83211786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:571b7e14f78d5b8bef9a0deaf67fe68502cbe126e8ec53e16716685e40b3b81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096fa4535d92a5582dbd70d5262f9a49f4687e2d15249393e194a6c740d710e5`

```dockerfile
```

-	Layers:
	-	`sha256:c4cec1b584e90c76be83dfd7509e0ea890fadd77268ae4355772c07725f5e46b`  
		Last Modified: Tue, 09 Jun 2026 21:12:15 GMT  
		Size: 5.2 MB (5215594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92de163cffabb59fd5b5492a907d6e9560e45c60fc4a02a1798552d034bf6b99`  
		Last Modified: Tue, 09 Jun 2026 21:12:14 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0a1d01859535ddd0d90bb7114477d375de301dbf1ec56b27a1be48b4c29fcf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136093007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85dce7393c9ec81a7c708b6d3cae7f5bbd460d54f6686d0aa45738a64bbb0b00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:42 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:11:42 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:11:42 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18886b7768dff6aa10cb5f0942c6e70e7d13b3862c034e5e88ea1d1231d7c72b`  
		Last Modified: Tue, 09 Jun 2026 21:12:00 GMT  
		Size: 82.6 MB (82635180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b30721d43120b8b26729c21d0f543b31f99b4e4e1ec8b7c70204e71b9b42b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0bf9d3fdedc6ed9890f89fa5181912ad67dc6a2208906228c51d1f31555359`

```dockerfile
```

-	Layers:
	-	`sha256:2f23a0a214eea8f9fb451b1976d009a180e736be09a33b0390ce9a49ecced0f8`  
		Last Modified: Tue, 09 Jun 2026 21:11:58 GMT  
		Size: 5.2 MB (5214386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bf08c3dc8599fa44ebd7f28fc49bf0c9f3f0925ca1b9b110e9b0f722372ddb0`  
		Last Modified: Tue, 09 Jun 2026 21:11:58 GMT  
		Size: 9.1 KB (9133 bytes)  
		MIME: application/vnd.in-toto+json
