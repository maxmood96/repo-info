## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:d7c744a40199dc18bbe08619ad41295f7dcf34ef1477233026f5cbdc95bf6a2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b9dc0be2f27be8fac021136f0d82b0ff26aa2fe421ebd00823b41f2cadcc657b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130629701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c1f6f3e93a33114d61c74a8cea6b34c0f2ee51e07ad14078a61b6ae54eb551`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:14:49 GMT
ARG version=11.0.31.11-1
# Tue, 16 Jun 2026 01:14:49 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:14:49 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:14:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818aafc8133016bea8082c9287b301711097ef6b6e3fdeac1d7afdd716cc5eff`  
		Last Modified: Tue, 16 Jun 2026 01:15:06 GMT  
		Size: 76.1 MB (76058545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:736318ed960c6aaf7803b0cb5277ae15ff1fd83be94227caa7e504768308701e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b437735e8c3ec8c37211c96dfc88787bbe6a86900000b80c711cc5a7afdc7ef`

```dockerfile
```

-	Layers:
	-	`sha256:d5cb723a30d299cdcd251138e1bb517d4e06c0522beb0a761afd0ba40deea17f`  
		Last Modified: Tue, 16 Jun 2026 01:15:04 GMT  
		Size: 5.2 MB (5203271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93adce8979b846f0aae8ab9c5f9421122d89bd559c0f13b00baf02f86339ff0f`  
		Last Modified: Tue, 16 Jun 2026 01:15:04 GMT  
		Size: 8.8 KB (8783 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:863c68e14a3340fcc3c5aab4add23378972ad08230fc2627c1bb6f90e2406722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128762622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8804134f63b3652718efb1f86154eab838bd3a8a5fb9db655cc6592c057e37fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:00 GMT
ARG version=11.0.31.11-1
# Tue, 16 Jun 2026 01:16:00 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:00 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0d579dfa1ca8dd9f6dee097b22703459e204b645d95487525e9f5bab106f5`  
		Last Modified: Tue, 16 Jun 2026 01:16:18 GMT  
		Size: 75.3 MB (75304795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:423901a4c08e68843bbb23c8455f4490f855bd291dad5340327f2074d132060e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331b31770822957bd6947e65d5bd4654d1839cfbe2dbc8ab1361d4f9e73a523a`

```dockerfile
```

-	Layers:
	-	`sha256:9f42db405336438eac27fd1ef4517795a12064885a17638a700ec0b0754a42e1`  
		Last Modified: Tue, 16 Jun 2026 01:16:16 GMT  
		Size: 5.2 MB (5202889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90783ca014a73e3783ae7a8ebf924efc9204e86f6e6ce606cc12fc216464bcbb`  
		Last Modified: Tue, 16 Jun 2026 01:16:15 GMT  
		Size: 8.9 KB (8863 bytes)  
		MIME: application/vnd.in-toto+json
