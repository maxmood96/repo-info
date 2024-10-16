## `amazoncorretto:23-jdk`

```console
$ docker pull amazoncorretto@sha256:e4679465cb5ba8c9389fbe2876be83be924ae9959c7f35c82de22c350cc96868
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:03f0a4c4e751a5bef547a910fe3c4880db1f9128333a1495cf50c610ef69d856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229815575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf27644aa4a151953158892a3ab316ba53d7d280be66796e29ee0da10d5089d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
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
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6329d9b869213ee0e8efcad26136d8b77d4824e5d21994c397d8eafec4726030`  
		Last Modified: Wed, 16 Oct 2024 17:57:54 GMT  
		Size: 177.5 MB (177490270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bf4f682f3e0fb523ebada97cff41b8854509e62032f28e0f37c67b3492ba0dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9295506b791df62dfb42f88d73665937279b3ea0fdee3de574118ddfef588f4`

```dockerfile
```

-	Layers:
	-	`sha256:bb4d80cbe3ac747938117e06c741089bf2de6e552dec256354785d7e94e22f74`  
		Last Modified: Wed, 16 Oct 2024 17:57:50 GMT  
		Size: 5.3 MB (5321575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688b50fa1f97f438801d363c76a75e87d4f1f39a26e2873798ffb0a4479ca055`  
		Last Modified: Wed, 16 Oct 2024 17:57:50 GMT  
		Size: 10.2 KB (10242 bytes)  
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
