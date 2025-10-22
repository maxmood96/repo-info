## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:d0a7fe9ac0e5ff70cd04285cb36789a276527c240d4a9feced6db1c0d5134c5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:78d58873a5e06ab3af40c133d9ebc26475a55ad855bffcfb4ae5ebf8ac2a17dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130720429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dba71fbe47e10225d1e5b8e25afc3cd0927c1cc8a9342acdeff52fc2c2c21bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:56 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:56 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695d80786fab015a5a1f12f215ec40f0f99612c3908a9dd4e175c15adbf0cdb`  
		Last Modified: Tue, 21 Oct 2025 23:26:57 GMT  
		Size: 76.7 MB (76715298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c55cf2dfeeb3365c96f3b27ff2b30916ea8c46428a6d2c2da5e4e79a94e53933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d23b920ce2610f326c58e2c818da4913a44d577de5882540472f996c7824064`

```dockerfile
```

-	Layers:
	-	`sha256:9735a122e4ea210738906fdfaea23b7bba1e7f2dddf6354ab3cb0d02a6f7992d`  
		Last Modified: Wed, 22 Oct 2025 00:47:51 GMT  
		Size: 5.2 MB (5222168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced561d071e9f40046b2f8b5d2dfb178ab6b2e6f01ea302e1fbb8741e3eeabad`  
		Last Modified: Wed, 22 Oct 2025 00:47:52 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:366d8f06c3389af9fbfef6676c6ca3c3e719eba8a6b604e84d88c0a1598fcbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128847682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b48f295dbf2f50574829bb52ce8efee0f8f6101138edef6382d9b52e71d2f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:59 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161033820a15337a17d8364d5c2877d46231f820fb814344f644fa350296baff`  
		Last Modified: Tue, 21 Oct 2025 21:49:56 GMT  
		Size: 76.0 MB (75956479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b2baa6c1928ffa5f545840cb7cedbff15dcaf6e2c8f1de5a2a2ffd3ba062a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7d737f07ea050bb0899b826c6d1bcea8fca8c0184967d876d862e569332714`

```dockerfile
```

-	Layers:
	-	`sha256:784c88fa0fac2791d5f5bec523342b9058c458b25d847e9571ce22ffbb5c9f22`  
		Last Modified: Wed, 22 Oct 2025 00:47:56 GMT  
		Size: 5.2 MB (5221789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729f0794db071d5723261dbcc2c30abfdd4f4186822724ba92e3d4c44b6207c4`  
		Last Modified: Wed, 22 Oct 2025 00:47:57 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
