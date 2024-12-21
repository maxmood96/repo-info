## `amazoncorretto:23-jdk`

```console
$ docker pull amazoncorretto@sha256:728fe3db51e8d43abc74101cf4487ec0feb4aa9531060726ddce80dded077d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be474ddad2721047ec1575f04b32bf032e5ab9bb7704df7755f5d8b24ca68bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230725748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4eb0b7043c84e869374c10e750a8bcbc5ec06cfa12275343d34aa27502d2058`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e3ad49c8506e0d302aebee4fb134ecf63af597150b3973092be755c3ef985d`  
		Last Modified: Fri, 20 Dec 2024 22:33:35 GMT  
		Size: 177.6 MB (177569435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:05c47f376b75b5060a768dc228d22e8cfd7584f3d50d7228951792a6e135b8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5326401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8009c5dab40c95e5dba4a27c74aa48eced4d7ff7230ad413797408a2373f977c`

```dockerfile
```

-	Layers:
	-	`sha256:d4517c3efad33cde9ef9c8364bf6c9d5e007d883b81a63d41dc6c4f6b5c255d4`  
		Last Modified: Fri, 20 Dec 2024 22:33:32 GMT  
		Size: 5.3 MB (5316163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69dd9c10f7d32af2aac6fae61ec456bf53e795352da9fc9066b3ecf31b39dd91`  
		Last Modified: Fri, 20 Dec 2024 22:33:32 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4309d765598f57cfa0cedb864783f92eabe9e9e5caeb1195a440b7fc23e75879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226955735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8f235f0350209046913e5e1539a78052e4ff2f555f8f57baf390fdeaeba200`
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
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1a30d671c2eefa174e9ed9df10f3183c4fc537c6c954702f75aa306d4113b`  
		Last Modified: Mon, 02 Dec 2024 23:31:16 GMT  
		Size: 175.5 MB (175499891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2d4963a268f54ab7f7f547db4b562938e5a0a2a8c65052649972227fd8ac2b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb681bd77d1e94a73f079642789bc5f09ec04885d68b3f7207cadced0b7b3ff`

```dockerfile
```

-	Layers:
	-	`sha256:9d2f01f7c23fc55395c5a95afa9254614d683c595e38a3b13d74b51fec90e81a`  
		Last Modified: Mon, 02 Dec 2024 23:31:12 GMT  
		Size: 5.3 MB (5319885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573ee96608d347c0062549cdc171d2dbb32a4918bfdd8770c9397dfa19fc82c`  
		Last Modified: Mon, 02 Dec 2024 23:31:12 GMT  
		Size: 10.4 KB (10354 bytes)  
		MIME: application/vnd.in-toto+json
