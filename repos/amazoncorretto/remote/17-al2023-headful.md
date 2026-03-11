## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:43629799b55bc181898d15d2c4b4bc7b42cc500357488e62ff88e21e1d6e65c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5d31db50e99b94bc91b863352467543583131943a6086c0a0351215536e5fa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137113173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066ef1c6abc9aab3cb1e31b8ad1c0e0716b616da7894d82ad76b177e517084a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:39 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:33:39 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:39 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:39 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707662ac45bb40f060abe699899893f0a8a446f55d4827ecb7eaa8213be55ca`  
		Last Modified: Wed, 11 Mar 2026 18:33:57 GMT  
		Size: 83.1 MB (83080083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d219dd8633619d9f7886fab4ea1c25d851259460e9674e11324f93124430b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afa2dfe1f3af7e5074f610ba18c553c9d13448e359ee2da5caebdb80c69cb63`

```dockerfile
```

-	Layers:
	-	`sha256:1ed09536fefa715943751a62fff8acbfde78cf0a0a17749fbdab2388414595de`  
		Last Modified: Wed, 11 Mar 2026 18:33:54 GMT  
		Size: 5.2 MB (5208395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854b84ad993da7eea6f0d8e3f0fbab15825698163f1961c6ac2e9e61f2f94276`  
		Last Modified: Wed, 11 Mar 2026 18:33:54 GMT  
		Size: 8.9 KB (8891 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b5643776b713cd582379740b33266e25c84584878cfe9faa78a30117b011fe02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135442761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ee3da0543650d780f6f07967b1562f21886f5cffc733e4fce06f90d56e69a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:18 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:33:18 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:18 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:18 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3650f625f59fba6407645d9a23694fa373bbf873fab8d21235e35ad73612e8d6`  
		Last Modified: Wed, 11 Mar 2026 18:33:37 GMT  
		Size: 82.5 MB (82501386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aeb638ada1f8eb1e3699a19f156d7ef82bc634369289068ddaad52942d0f5e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c5f0e9ec159abb3bce599eed7ee87978fff06a40725dbaf594d1b9ff239942`

```dockerfile
```

-	Layers:
	-	`sha256:68196cf58792bb12ddfca5f268184ebcd9497ba7fca37129b2bc3829f3576aac`  
		Last Modified: Wed, 11 Mar 2026 18:33:35 GMT  
		Size: 5.2 MB (5207186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71015921a9a81f07dd3990d3c55d26888047c366a85a006cfa89c0de6d555e46`  
		Last Modified: Wed, 11 Mar 2026 18:33:35 GMT  
		Size: 9.0 KB (8971 bytes)  
		MIME: application/vnd.in-toto+json
