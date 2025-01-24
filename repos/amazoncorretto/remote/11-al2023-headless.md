## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:e1c933bcc907f322754cd3a8f08eb26262b0439ee5ad3a51cdbff0f844f06287
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e404fa2ab7e3a0970ac33434b4d0ebc9a80a4037fc87c7478c267d02ae1d094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129373935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699adc29ee98aa22e814d87707505c66be7bfd79439ef9224da80dadff5661ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6ad17033055a0c024e14fe7c9700e1885c3874bf95cc7acdc5f5649c043a02`  
		Last Modified: Thu, 23 Jan 2025 23:08:00 GMT  
		Size: 76.2 MB (76221400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20a20b8ae98e9cd7fae8e72d48db199dda30c8db9ed9d2381db973ea4dcf3cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb608fde69e33027d971af4d8155a045e50c6b1a6942b79d07d78c2b4d7be30`

```dockerfile
```

-	Layers:
	-	`sha256:440f0f079b6349c4a335fdc804113e9115094251bda36ab985e0f0a3d8dff9da`  
		Last Modified: Thu, 23 Jan 2025 23:07:59 GMT  
		Size: 5.2 MB (5193347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5dac8e7ccfc21e3d1bd1d4066aeed5b97a2a2de0d74c27409ecab959ae780d`  
		Last Modified: Thu, 23 Jan 2025 23:07:59 GMT  
		Size: 8.7 KB (8651 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9671a32798c9a70b6bb392664187acfc51416811fcff9a4424e28a2db69a177d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127682219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89ceeea274055e598d97ebb95cdbe42f1691f1d59d28052d70997b0bdb1fd84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0729545c98eca517bd113dc698fd62382ff5033ea59b1b2748081e3490a14f`  
		Last Modified: Thu, 23 Jan 2025 23:12:45 GMT  
		Size: 75.4 MB (75412020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:409e8f089e4660240b993f5a59ea0e01c98ce34a67e181cddb86a2305ba3caa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdbec96d4cfae32658b81c9e1a1ead3e074baf2adc35d73d011c5ffbb93bce6`

```dockerfile
```

-	Layers:
	-	`sha256:8baf526e226eadc32abd038e39b56e2f4ad72ccc48721711e060d890e903e3b0`  
		Last Modified: Thu, 23 Jan 2025 23:12:42 GMT  
		Size: 5.2 MB (5192965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a6e39d7d98f067b19d0c05adfb652a8011fbd3db5488ff8f8ce8e0529604e5`  
		Last Modified: Thu, 23 Jan 2025 23:12:42 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
