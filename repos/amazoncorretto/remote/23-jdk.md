## `amazoncorretto:23-jdk`

```console
$ docker pull amazoncorretto@sha256:55235ff00f9c09f6ef9d044909c894723205c18511bb788c2ed49edf02fdbfaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:970f6d9f380db99a324d468af7d15e25994d79f1fb2ae5ecfab8179215affed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229858193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad094129c450a5160f7f57432ad351849072205a419ad7c1566a1bd76011d90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63432d46f0bf9dcc129c24c901e228dcb4238fd6c3d3049c5cdb5418c717d991`  
		Last Modified: Mon, 21 Oct 2024 18:57:31 GMT  
		Size: 177.5 MB (177514361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b8b2e3f99f066887f2346b00baa3c8d37fbf2ca2fc2f7d5627114ce00441774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff6bf2484a6732df79827863785277a9696ac8da24fbec209fb8b3a0b0a9e4c`

```dockerfile
```

-	Layers:
	-	`sha256:4f240d9e408167adcaa376183c9d3a198d16b9b2125c74f4b464556f4a974788`  
		Last Modified: Mon, 21 Oct 2024 18:57:26 GMT  
		Size: 5.3 MB (5321745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8b4bdd6e051b62e7c85ed8b447b3daef29827a04d006b2d78f56d269228dfa`  
		Last Modified: Mon, 21 Oct 2024 18:57:26 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:830c28d76cde27c5e29046c9a474803635163d50827cd8ad2cabbd5c6e272160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226845916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dabf08ac3ca5316f91129bf543a0ededdeb4322fa5850fe31114a80e5f1e7a49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39012886f509ba8d8b15f9a9fae7324e1b87b7f6f5344cc22388dca51a546f`  
		Last Modified: Wed, 16 Oct 2024 18:39:50 GMT  
		Size: 175.4 MB (175419552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2a29ca9fd43eaebf0410114fff19e1397548df81e41ec61f77255a8b1e28df03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3280b9bc963b994f07596669f8fb48b6dbd995c1875e1a7c68d10c8fdeacdfc8`

```dockerfile
```

-	Layers:
	-	`sha256:e2f63eb132f01357b066ab20c5d287d4971a3646c7a2f61b63a51d9c4d324d8c`  
		Last Modified: Wed, 16 Oct 2024 18:39:46 GMT  
		Size: 5.3 MB (5319716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef272c750eadbced04a9457fdb6376da72d2c9e1882a6aa5cbf0af7db78351b6`  
		Last Modified: Wed, 16 Oct 2024 18:39:46 GMT  
		Size: 10.4 KB (10358 bytes)  
		MIME: application/vnd.in-toto+json
