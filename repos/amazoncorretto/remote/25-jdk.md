## `amazoncorretto:25-jdk`

```console
$ docker pull amazoncorretto@sha256:6ba4f6ca82ac3f8bad2e514a1ba060e6314e8dff2d46b06c3bd6af063a7c2eb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7b3f4bc4d51326abc71c9606ea84621dddbba6eb241e4db7e1aeab9defd3c567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243159036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a088c9c4ebcc048b7eda77a6b764648c92e7e1096a90233b4a692da8b1617c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:13 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:13 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:13 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:13 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d88fe3c4b256f3e9e43b9cb5ec26a56a3f9a83b14d7daf8a3ab39250d61c86`  
		Last Modified: Thu, 15 Jan 2026 22:52:23 GMT  
		Size: 189.1 MB (189137832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e0df46f04b6008ba55c1ec2561c193292acba7d86b622ad477a8871cf93af09b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5340079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1d0ed9017566b9f53efae1a0f227c73b0822eff591ea3e51052839ae3a8280`

```dockerfile
```

-	Layers:
	-	`sha256:dbe22afbd304a7ee5698715430cf5a5b6f06570aeae49f7c03c438936799e7af`  
		Last Modified: Thu, 15 Jan 2026 22:10:32 GMT  
		Size: 5.3 MB (5329570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402b7efd6d6258654409c0aa9fe1262f22b2bde47b3b190e4c43c9cf4881cfc7`  
		Last Modified: Thu, 15 Jan 2026 22:10:32 GMT  
		Size: 10.5 KB (10509 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1f45ba4745f8c8c204ca858eb7b442fa2f0f7ca051ffbcf7ea799dd45e395cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239973790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73036706802e2b7267d5a0b035570c9f49aa15689479385f1768f0c44072b814`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:20 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:20 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:20 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:20 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506418744a0e688a95c939f508921fc21e961eb25ec4bf5c8550b47aee8f9d3e`  
		Last Modified: Thu, 15 Jan 2026 22:52:34 GMT  
		Size: 187.1 MB (187059433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7b10ccd10c9169f347e4facfb2cc7709f3d80c25711eb4b3640680a27e36e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a404a573e02c662053fce46762e2224d2ee34846c3fe0754913519e8d220f4d4`

```dockerfile
```

-	Layers:
	-	`sha256:f02e1d7690b4ec0f300f424ea7206e838d9673e1601b3c004bc5e9469c85dc0f`  
		Last Modified: Thu, 15 Jan 2026 22:51:38 GMT  
		Size: 5.3 MB (5328550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60ea3d8b62a0aa8e4b2d7ebc4b81fa9f9d2cfc5b6305040200ca5a0e04ea578`  
		Last Modified: Thu, 15 Jan 2026 22:51:41 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json
