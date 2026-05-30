## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2c516afc18583390c3160e2eabaa4d6bb147f0a83166ed928580b009bf2fcca3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34bb6b78543286fc414d336cb7b7b7a2e533c817c5dfdb69f5ad4814f312face
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130629652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a138a7c2dcb0204517a8bfa6d4ecb9f0f4283740160c89f0b9143cbb87b19e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:25 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:25 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:25 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084b3cf6d03d3f8404a7b4a854c27899d3b6d37edf0953e84e11a5c981c1f108`  
		Last Modified: Sat, 30 May 2026 01:11:42 GMT  
		Size: 76.1 MB (76058496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:57b0f8cecd07972be893313d878f50ba913dd48b32b6b3cae746e332a9d6be88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b82080a4355521d0a7088cafd62c1b17614856735a78d0b94b862cab0862ab`

```dockerfile
```

-	Layers:
	-	`sha256:80b85d8f1c55ddba63d066d6c1c7483d2165ff424757189634bed371c373c4dc`  
		Last Modified: Sat, 30 May 2026 01:11:40 GMT  
		Size: 5.2 MB (5203271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb57dc1b9e94a114e8733fba3fb512dabaa5a13e13306fc54b1b33d74596c5b`  
		Last Modified: Sat, 30 May 2026 01:11:40 GMT  
		Size: 8.8 KB (8783 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:112ee37e9e6d8126bccc850dc588cb6d0439f203a80f11638dc6bcaa08565961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128762596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f643f3d5d909e337b666e4c4b8c1c78f1bdf585b58de0bbcb872e0a8ce3969b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:29 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:29 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dab700d5f9e8b13c5f2518c09b7114cc87849e1f68614407b7c0b22a1b196b`  
		Last Modified: Sat, 30 May 2026 01:11:46 GMT  
		Size: 75.3 MB (75304769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ce67b16bf7e9f92cd1cfd9ffc2ba930dc22abf7fb642fed6901d12df427c17ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2034d9b8078364654fb89ef45d4c65bedc4e7393e8b2306c8953409efa6d2b92`

```dockerfile
```

-	Layers:
	-	`sha256:2dd36d3ba0d958000bad347d592d18432f50429ba6991125263a3feeb7073296`  
		Last Modified: Sat, 30 May 2026 01:11:45 GMT  
		Size: 5.2 MB (5202889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d478b929a6a73c20d55afe8378d4685820fd1afc3cb8c64d03fea04316475f0`  
		Last Modified: Sat, 30 May 2026 01:11:44 GMT  
		Size: 8.9 KB (8863 bytes)  
		MIME: application/vnd.in-toto+json
