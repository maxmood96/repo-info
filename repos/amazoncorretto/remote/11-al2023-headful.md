## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:431556e9bf12c356f3d65be5267af25bb40eed20138ef77364688716276e6cc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:70b997d04e5453e4b40fabcc1187df6c388ced539cf04c542d9411383f14967e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130086533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2be71e0683b530d48309411994fdaaedb3035e7ccfbb8dbfce99834db14191`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b769c4b256c836ede846af8cb7dd3106b3989a4769b154cbc6ff8149eb209217`  
		Last Modified: Fri, 20 Dec 2024 22:32:17 GMT  
		Size: 76.9 MB (76930220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6c754598edbd67b9a70b4b2cb15be50a85e42f45f3d40cd08a459f00dccd36e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d342ad78c7bf447107ac135f6a11323b8fd28e3a020276a8612aeeb0132525`

```dockerfile
```

-	Layers:
	-	`sha256:93e70b0843b93a9b268bfeb3f9ccba4c7c36e8acfc931cf24067ad85e4dc4212`  
		Last Modified: Fri, 20 Dec 2024 22:32:16 GMT  
		Size: 5.2 MB (5218593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970ac2b7936dca7a7d8635c53c6852cddf00a048ffedea6a0a71186ed1636169`  
		Last Modified: Fri, 20 Dec 2024 22:32:16 GMT  
		Size: 8.8 KB (8787 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:306d7dfe1285d8de2187396d1b10ed1d37bcbce10ec5cfb9547f0ca591262b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128409163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f7535e0ac40a5f3b9ca6780d0118ddd85e05d003ca29cbc03a7a4626d9e21c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:98ab3ce9b55607064b358289eeb810db43f69e016067c07e7136a807475f6f27`  
		Last Modified: Tue, 17 Dec 2024 02:01:08 GMT  
		Size: 52.3 MB (52276382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc0c4ef63bbfa337eb1dcfc22b615fd0780038e286cf2b438f3802737ab6828`  
		Last Modified: Wed, 08 Jan 2025 06:27:27 GMT  
		Size: 76.1 MB (76132781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:264eab670e4fca9fb9d302b96c867c764a2f99a06b4847a17a7a6185f699d1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff7d0f8e66c961b80c1f997cc0e1c94f9a23fa2ae5c17980d2847a3e6dd8375`

```dockerfile
```

-	Layers:
	-	`sha256:f71b6f93222f3de859344d607d9eb826a561a165d0961710994025ffd9d84fc4`  
		Last Modified: Sat, 21 Dec 2024 01:40:31 GMT  
		Size: 5.2 MB (5218214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b8208307eca985599b108e14521300607fe8c864a35d58ea7b9b45cb79dee29`  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json
