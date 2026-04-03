## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:44afdb5bfc58f48460a14a97904f72a131cc5f1407998526ce1a4392380fc47c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c3d31c177cdd041c84d58465fae6690b5ed60a25e0265763ebd3edca4f39b4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158365292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79199b0f1182daaf1e13fc4e787a9cc287f7a2cad91f0591c1f088131f92e40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:10:34 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 17:10:34 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:10:34 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:10:34 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:10:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc85f7b9902f126dd6f853600870778222a058e8520a330756b9bff6ffc8af2`  
		Last Modified: Fri, 03 Apr 2026 17:10:53 GMT  
		Size: 104.3 MB (104332202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a24868a97902100bb88df518db2982e38146e7b353177f8fc164bbbdb585afe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593fb19cce1520433cb149b21ce0a78cca9b98ac4231bc36b88782f3844faa7a`

```dockerfile
```

-	Layers:
	-	`sha256:554378f80d3fbd5115432965b8a614a948bc1dfa41765790eaad8df36cab8247`  
		Last Modified: Fri, 03 Apr 2026 17:10:51 GMT  
		Size: 5.2 MB (5220288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8068516bdbbd8955fa0cc1341d8e6cedc93c547ac469b4a02eb5f6be650f6aba`  
		Last Modified: Fri, 03 Apr 2026 17:10:50 GMT  
		Size: 9.4 KB (9367 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0280f2e5c02a6b3e4f22745d1e78bbb92da704e7fd803f50c357347515c8a9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156201848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed6dc5322ff2d7b174a944672b6467677def456b995c17f54f5ce6d54ca3a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:18:24 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 17:18:24 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:18:24 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:18:24 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:18:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b134471256f80f390e73adabcbcc9ede6a969ff8c046e794fe85d8e3ef9cba`  
		Last Modified: Fri, 03 Apr 2026 17:18:45 GMT  
		Size: 103.3 MB (103260473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:53e7c2d173547e76aca2daa06c1f15c9a68adfc4cb7c77e86e34abb5b9f39c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f304f549374e80a4ab751f7f9b283400ae8acb78362dd48df638d5be58c0df`

```dockerfile
```

-	Layers:
	-	`sha256:6bc2ca1596550ccd9ca25633f1d7f2b812ec85079870a4ebb10607e74a026cb3`  
		Last Modified: Fri, 03 Apr 2026 17:18:42 GMT  
		Size: 5.2 MB (5219102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd739163b8a0d8ee2654c560fd6fd569dea47dcfc0ad32752867e36104e0105b`  
		Last Modified: Fri, 03 Apr 2026 17:18:41 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
