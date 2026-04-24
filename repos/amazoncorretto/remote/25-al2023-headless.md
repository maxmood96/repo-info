## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b74afe61ec1f0964352b10e2889502042455272f66eec437f23cbcadabd41fef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:30f0c46ee06292e3cc8d7478c058cd569901b10b18cdcdd22d881707e09066bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158290214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f868747eb6f15edcc60e7cfc778df21839a562927326c1cf9b53f690cab13633`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:11 GMT
ARG version=25.0.3.9-1
# Fri, 24 Apr 2026 00:13:11 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:11 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:11 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6343ff79c359a32ae1d3dec72f36e533e9a31774924a70a6c8c820ab647fa5c8`  
		Last Modified: Fri, 24 Apr 2026 00:13:32 GMT  
		Size: 103.7 MB (103720509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3724e9e56178c1ea252286b9ff6d09f76f4e89ccc9c6027475fdd65bd6c4c2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c91ad2aa4a534876003e1746868723ea4dec45b6054e2a4c35a6166d32e21c`

```dockerfile
```

-	Layers:
	-	`sha256:e79a7ed993fc38c30dacf4daa47ffa7607e84d2feddd56f57848806e2d7f86b9`  
		Last Modified: Fri, 24 Apr 2026 00:13:29 GMT  
		Size: 5.2 MB (5202050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713ecccd37b74eaaf34eb63fba80db1d7bacd4adcf062f06a8b7ae389fe2bf87`  
		Last Modified: Fri, 24 Apr 2026 00:13:28 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b8f622f4f25980dabfaa8030753ee082de42dd476bfb5c87ec9a1af5b5af57da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156103186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efee91c8e3e68fefdc2b652cf6f59723d74a5b82ded417876aaac62e14de3661`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:09 GMT
ARG version=25.0.3.9-1
# Fri, 24 Apr 2026 00:13:09 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:09 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:09 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb821275ba779d281a14a231a08b33c379d30d5824f1df6fff34265dbccd0cb`  
		Last Modified: Fri, 24 Apr 2026 00:13:29 GMT  
		Size: 102.7 MB (102650933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c1fe476d50e98f03281de5d54ca60d5d2acff00d66fe15fb48ff92fc3513e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bb98b7efa50d250b53cc9486bcb3970c8371629f55e8553c936bd52aa125c0`

```dockerfile
```

-	Layers:
	-	`sha256:fb14d83b2588f2587407ca9a4ac33c58a38e947aec84bfba34258d6d5303fea0`  
		Last Modified: Fri, 24 Apr 2026 00:13:27 GMT  
		Size: 5.2 MB (5200862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f52eeffc84eb6856982e1f1badcce2619533f15d986a3aa60d16f3d4d20635`  
		Last Modified: Fri, 24 Apr 2026 00:13:26 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
