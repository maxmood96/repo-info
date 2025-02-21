## `amazoncorretto:23-jdk`

```console
$ docker pull amazoncorretto@sha256:7de95a59755f5a0e9160abb7f5e44c83ee19dfa5af3349ce968d404fd45126bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d905bc40a44d0261f32bc65efea929ef69de79898d9bb71240a96ef0548cb3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230727565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2c8bcac80eb2268f44218ebd7da1aa49a380ad1c6be5ff45025b6ebfda73df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073932606b83d7e36d356d36cf30841afac184f1873b5cf0eb2460f423146c8`  
		Last Modified: Mon, 10 Feb 2025 20:08:51 GMT  
		Size: 177.6 MB (177576982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ec2e3d8e1af02669ab39e68abd094496fc82ab5c2af20816c5e93286e6e6637f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627247b654745b0962b58f6dd1dd1fb6ee869d7ba47431eb192d0a5ae2e39c27`

```dockerfile
```

-	Layers:
	-	`sha256:32ae79ff229d58492e30a241d8d55cd3c3348bf3839d163aee6d48fce40bb07e`  
		Last Modified: Mon, 10 Feb 2025 20:08:48 GMT  
		Size: 5.3 MB (5296455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0deae4d5adcd255ccb86543ffdd30d3ca5cd799b1248454e066b1a40c105449b`  
		Last Modified: Mon, 10 Feb 2025 20:08:48 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5bbc61913a51d7757fedd4c7361aeb6fa3a307fefecc058b4340913a7e4e31a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227879407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0abb560561d33181d7ff056984fdda25be54848263839cfa63179c6e8f54727`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc3f95e28e80d0726f0a42fc5782fe710190034937206e3e830873d8e426ba4`  
		Last Modified: Mon, 10 Feb 2025 20:29:43 GMT  
		Size: 175.6 MB (175608456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a0e85918bf2263027dda21d4a6c0d997fbe71c9e711a4e10732b232d69224ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d15b11bb565437aacb8b2baaf39ddc6ec29dec0c397dde2da85cee6d35f815`

```dockerfile
```

-	Layers:
	-	`sha256:45555a6b8892c9effe8da58ba19bef7419e2613d32981c7294c9b67758918c22`  
		Last Modified: Mon, 10 Feb 2025 20:29:37 GMT  
		Size: 5.3 MB (5294599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3273ce21626d7dba6e915e7b10e75319b052bb2244ba09d8ff21f1247b1dca`  
		Last Modified: Mon, 10 Feb 2025 20:29:37 GMT  
		Size: 10.4 KB (10353 bytes)  
		MIME: application/vnd.in-toto+json
