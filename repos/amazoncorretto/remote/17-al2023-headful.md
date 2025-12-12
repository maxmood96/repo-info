## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:aca99befbdd4a8fb7007206a51065c1987e345ec43a79775c9f349549163c8f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a43b0786c4eb21b31a5bc11886ff4282f2c0001933a96056bdbf2855341dfd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137076507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a49a75b2938d9573634297140cb4a225c8fe4424e5e98f9b1c87d5f4ca2f43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:48 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:48 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:12:48 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:12:48 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679413605ddb2aa7ad970f50253da9aceee5d3f5647ca53f2fe2beac0201d48a`  
		Last Modified: Thu, 11 Dec 2025 22:13:20 GMT  
		Size: 83.1 MB (83088047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:69a6c2285de4580b092490d175bd35fc7ef754c096fc39e82b21acd1ed828cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c033c07110c4a3776ee2da2a889d3b643063aff49c93c2c91d93dcb1d3d5ef`

```dockerfile
```

-	Layers:
	-	`sha256:6198b0afbe5ab52cb65069bb2e361e7c1522263cfe42496b6c0d6e5feb3e27ff`  
		Last Modified: Thu, 11 Dec 2025 22:49:10 GMT  
		Size: 5.2 MB (5208327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eebb0eaed09f210cbea8e40c8feaaf42e0798069b575918e22339e6f9098538`  
		Last Modified: Thu, 11 Dec 2025 22:49:11 GMT  
		Size: 8.9 KB (8892 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:eb37af6d7123211cc60c14a147793c21f1b61bab197861804c361a76b6189410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135374745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e61dcd94716bae32519f4986410a2f11a478b5f6b3d3184ab87231e568c952`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:16 GMT
ARG version=17.0.17.10-1
# Thu, 11 Dec 2025 22:12:16 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:12:16 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:12:16 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c313d1cdef642f82e1515f2196c5bfd600d17d3698d3d28d73e32f46c1e0ce`  
		Last Modified: Thu, 11 Dec 2025 22:12:48 GMT  
		Size: 82.5 MB (82501295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:caea23aefbfd880cdbbc9baa65d3eb740fab22d7b3998678d5618257c8eebc2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5b9697c04a2e2e0fa1262cc4365a98b3038dd04f2d2677100c37198fba168f`

```dockerfile
```

-	Layers:
	-	`sha256:a83c7aa00b2384c51bdaec647102b9dad843695aa6a089add4e1f19d805af4d7`  
		Last Modified: Thu, 11 Dec 2025 22:49:18 GMT  
		Size: 5.2 MB (5207118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e2a9d49e16bc3979ced20c4316a7d823136682a447334f1fd86b6f060b0e7c8`  
		Last Modified: Thu, 11 Dec 2025 22:49:19 GMT  
		Size: 9.0 KB (8972 bytes)  
		MIME: application/vnd.in-toto+json
