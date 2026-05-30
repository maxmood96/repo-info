## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4c72e3c261f401a3d5f16d269a747e198b6c1c27f4d08340fc99e085a328fa07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9d634b17aba493ea9b7b4a36a594f785718b2f7ceb78309e1365e496977d7c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158292887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887855218dde018622310192cfa31e2d086556db532fc7fcf6d046428f8def00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:50 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:50 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:50 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:50 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c503cf364c5034b695052e9d1eed38adf3ae9b3f30a246f32df9ec9f347189`  
		Last Modified: Sat, 30 May 2026 01:13:11 GMT  
		Size: 103.7 MB (103721731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4f1015923e0547251c0276b378e3f97e1f66af5edc7adab646b5b4809cd61af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8aa33627f906a43ddc4d5e8f179efe2248e7a05cc3fce9a89de213fbcd47b1`

```dockerfile
```

-	Layers:
	-	`sha256:c6ed86d793d466459bb87fe2029e8774a85d2268b0120d4069d8dd2e321ff406`  
		Last Modified: Sat, 30 May 2026 01:13:08 GMT  
		Size: 5.2 MB (5202050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f42e35b6f6a8b714e0a19c6ab417efb15a5bf4d33e88b5303be62b10e4f26ac`  
		Last Modified: Sat, 30 May 2026 01:13:08 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:36afa1ddfe8c17c95c721c960e2b8fa49ca4373a632cb1497226d59c2f232297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156109547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0905494ac0172a21b6dc46b8094589fc9940137ce7dab1c9515eaef58422dc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:36 GMT
ARG version=25.0.3.9-1
# Sat, 30 May 2026 01:12:36 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:36 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:36 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14909b69121e268ebbff9b5552ae9c022be113a98e82c9d6beb97bbc107b4c40`  
		Last Modified: Sat, 30 May 2026 01:12:57 GMT  
		Size: 102.7 MB (102651720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ecd53bb8ef1b80f1a5e90abee2861c3fc8e2ee59b04f85e900d6cfa484bd017c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7aad1c8cddbe8eb5548509a0b5b7cbd20ced36380b21d3da8eb7e0a845c51ef`

```dockerfile
```

-	Layers:
	-	`sha256:da1b3af4b1e115ee15929750936779a414b82655e8dc039be63ad23686af8f79`  
		Last Modified: Sat, 30 May 2026 01:12:55 GMT  
		Size: 5.2 MB (5200862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4457eb8b79ade964e13e0e6b8d2a7c03fed827e4eb5a005f9a55944a99649f13`  
		Last Modified: Sat, 30 May 2026 01:12:55 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
