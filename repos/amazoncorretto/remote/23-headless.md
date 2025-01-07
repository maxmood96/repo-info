## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:e05f5710cee63cfa78dfa8e52b6732f0a9ae523fbc950266bb7eb6ab8ae0d4ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c0a30542b5b093a7e134a4474db1f1bef02dd159b3ee813946f98fc6c6667d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146283506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba7570d22f56c1a50dac4436ccddc8d4710c29c4c8b1f17dd350c4261f36eb4`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:99232b3fa37edda1a2ec9bd4deed4d5d1e98e718ea5c97023d0346c9420a06c2`  
		Size: 93.1 MB (93127193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:46d4943d34ef1d74389e8f6a4202274a7db8d9c83ebd028ceae27e6852a4c654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcde5e90b3690544b424a08708b5bf2735c3f74afd44676920e7008f777b622`

```dockerfile
```

-	Layers:
	-	`sha256:ca9ed1eea6e2386feadf49fe5c74903fce6a491a40f33e24821933040b6561ec`  
		Last Modified: Fri, 20 Dec 2024 22:33:34 GMT  
		Size: 5.2 MB (5183862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8c46507883be69b78d498dd190791b15824285b982b96661408a254254fde1`  
		Last Modified: Fri, 20 Dec 2024 22:33:34 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9c726ab52c71eedc621135da11c9de6fdf5fad1e5e3c16e7eebee9b1d3e06dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144373535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cd19dec62f622d1528dbcf3ff8c71b6e6d46d4a5b93a6500bf02c5158d91341`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:98ab3ce9b55607064b358289eeb810db43f69e016067c07e7136a807475f6f27`  
		Size: 52.3 MB (52276382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5589753fdd1f3b3fc6a74b7f95738694f38b562b37b5328992b07691fbb92f32`  
		Last Modified: Sat, 21 Dec 2024 01:53:46 GMT  
		Size: 92.1 MB (92097153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ce29a5e8a9b176488a229ca728cd5805578c8a78429997145bd273b92ffdf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a4c16c3a4e1295d4c5cbc56ce44d926d19c0dd9569dda0f50d0e8e61f95940`

```dockerfile
```

-	Layers:
	-	`sha256:53c468764e613c9ec0a5eb7a40c4bf03121462968940a42cf5e6241980f3b2de`  
		Last Modified: Sat, 21 Dec 2024 01:53:44 GMT  
		Size: 5.2 MB (5181851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:289b91832520522f698d3b4d032940953086c7785391dba9155dec4ffc4dc970`  
		Last Modified: Sat, 21 Dec 2024 01:53:43 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json
