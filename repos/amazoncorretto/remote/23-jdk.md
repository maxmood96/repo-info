## `amazoncorretto:23-jdk`

```console
$ docker pull amazoncorretto@sha256:16a517892e536f9f2823fa90169ff3f9f3009f26d701246cee44b4e332c6790c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:95c594382b5e5d45f52f9e0bb4d6c51d800f3c13241f815e8accef641caaf5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229858521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c06fc818f7bc826a719952751469eb658298dfcb4cb283b9d5d153ed957e734`
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
	-	`sha256:5f3b500dc43eba4cfdf8e70913f712bd20874deac837800a822eb046b9b8bd01`  
		Last Modified: Wed, 06 Nov 2024 19:16:29 GMT  
		Size: 52.3 MB (52344739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536ce284584145070875377e7e438426546f0db21fb3685e4bb60d88842caeb2`  
		Last Modified: Thu, 07 Nov 2024 21:48:14 GMT  
		Size: 177.5 MB (177513782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e3d9a620cfe1d754d78b20c8b45867edfd394ea7096398b2201bcc13bf0ec084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf4d3d232f5eca4b14cd91dcb71f25d966932d508c01101555cc5498a639f72`

```dockerfile
```

-	Layers:
	-	`sha256:d28936131b611b962eedc84a6e37b30ba6c4fc22a735c6362da4dcf88dcfa366`  
		Last Modified: Thu, 07 Nov 2024 21:48:11 GMT  
		Size: 5.3 MB (5321745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f0948a0803be49bb3e1d42b0ad5e8628add23246ba74a096ecf82bb307d35e`  
		Last Modified: Thu, 07 Nov 2024 21:48:11 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:108d8f3260ab6a5deffe5a8a87958ebfd9a8eeb50a6d69a6098dfbf72468c2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226914150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e7d5dd4f963ab31fee7c00063bfc7d0f2ac8591c4ac43c23a17fc252731e84`
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
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288748a89ba6dbce774bc02546a24964a04fcab71a69df0fc426e9ef4c1ff257`  
		Last Modified: Thu, 07 Nov 2024 22:07:04 GMT  
		Size: 175.5 MB (175490149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:96da9862d6de4ac4a4b41bf003641500d70723b8c2ccd9bd1d342cd5d7ca5426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f75bf55a9c06bb26df46d3aea4344ffbeba97f705eb83820dc4ae74d618a117`

```dockerfile
```

-	Layers:
	-	`sha256:9157db86824ec9bb6531ae7ecbb01870fe141202b3ef6224d15df0c71a965147`  
		Last Modified: Thu, 07 Nov 2024 22:07:00 GMT  
		Size: 5.3 MB (5319886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5abbcbed9d7a6868fd2db2eaabd2ebb447608a4ba881f33ec34d82197bce09f9`  
		Last Modified: Thu, 07 Nov 2024 22:07:00 GMT  
		Size: 10.4 KB (10354 bytes)  
		MIME: application/vnd.in-toto+json
