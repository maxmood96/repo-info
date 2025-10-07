## `amazoncorretto:24-jdk`

```console
$ docker pull amazoncorretto@sha256:4392325b718f643e2350800f9b1cbfcb6701d4cee11dd55c57acc01051f2c5b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:65ee7c282e746b9c45f6c3cbd5fc337f44831fe3e2f180a55cd5cb8d7e724e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.4 MB (241399833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f580e998aee9a071240b3f8b1efa5a96191c6b0f5b4a153afa81a9d3b6fede70`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b659529362324a4924ebe72940d12aa052ab5c84a979e7141ba538d8f4cbf4`  
		Last Modified: Mon, 06 Oct 2025 22:59:30 GMT  
		Size: 187.4 MB (187394702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73ac794d239b1d976441848482d1bdf7f701910921f12c11bf76bfcca35e6929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7791c872f84b99830895d833226bec892833445ecd1141e63713f76cecda4418`

```dockerfile
```

-	Layers:
	-	`sha256:2cce1fd447a5984315d05c80616be12e1007c7d697e9f6f526fac0385958992a`  
		Last Modified: Tue, 07 Oct 2025 00:50:51 GMT  
		Size: 5.3 MB (5329176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5249512d6a844e89fefcf9cd39d3323d7b6d2c8839f759b8781187e9add04530`  
		Last Modified: Tue, 07 Oct 2025 00:50:52 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7448022613fd6b4662c3e5c0c81806dc9dbe8fb26de44da249a4237ebcf30448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.3 MB (238330537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f284a844c8b8753b1b790df4f1eed074193c6c6311df2233deaff7c9dc53ae2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f92cd41b876f74ccba948207ca3ad51dc368e3be89f4da98af7d370eadeff0`  
		Last Modified: Mon, 06 Oct 2025 22:11:46 GMT  
		Size: 185.4 MB (185439334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:64cb8feb342a24fd4df2011d1b8f144456da3b49b9b797a295cd323b9ff9d74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b53965c85b594dd7a0a32696d958d649c8bb5125ae8d28174884ed97c1f4f99`

```dockerfile
```

-	Layers:
	-	`sha256:ed1aaa1c6d28dc0d5003da1be1cd6cd2fb349f88b7814a649837565debb051de`  
		Last Modified: Mon, 06 Oct 2025 23:19:16 GMT  
		Size: 5.3 MB (5328144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c17991382d6b98c5afdde8f5a9e8eaae71010cf5ec74e159bce66651f02af23d`  
		Last Modified: Mon, 06 Oct 2025 23:19:16 GMT  
		Size: 10.4 KB (10355 bytes)  
		MIME: application/vnd.in-toto+json
