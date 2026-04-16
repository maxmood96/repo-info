## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:4f61c2fea283b4b39a8339a1d8af1066b6706400d4c33903c2a3496957f6957d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2f0b17bd01e200123fc419ef4fc26ffbf042e98fd936623b148ca5f7cfdd3f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158903560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f6ee025cc66bbc4fbd4de07a86b3bc82601de6523312042d4cf9292f128c335`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:45 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:26:45 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:45 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:45 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e0824b1c5518056af9ea3389d2615b54556beef5a0c45c7a01b12618fdca6`  
		Last Modified: Wed, 15 Apr 2026 21:27:06 GMT  
		Size: 104.3 MB (104332306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:feebe91968e3eb9443be12a22767f0fbd1ab73852dbc261763b22f1a852d76e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244b8e740d72a8b2289813971d3ad2c7d1a782bda76b11d3b82cc5704ef45a6b`

```dockerfile
```

-	Layers:
	-	`sha256:f22f3492cb9529a4fbd63a8d6ead5ac0dd356438b21c3fc7fd6fdb2e9eb257b4`  
		Last Modified: Wed, 15 Apr 2026 21:27:03 GMT  
		Size: 5.2 MB (5226662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1288746f3d77781a82d977b0623aaa5b9b05f872efb5173c7cd7abbb7b0bba3a`  
		Last Modified: Wed, 15 Apr 2026 21:27:03 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1222c851a77069bc7b98fb05365efd089c7e8805ac10975456a3bd8a10ac4d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156704637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7953c8fc0a28c2b0ac8e513bb1396ff94321e4a7ae0668c57a87a2ec9089cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:53 GMT
ARG version=25.0.2.10-1
# Wed, 15 Apr 2026 21:39:53 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:53 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be94cc5120b4ceeda1591a3def47af47fb67f991cecca8d6c6da0eca1a20d4e7`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 103.3 MB (103261898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:37255176dec607c6c5ec6c79341a396f32d837a5ce8d8bf0090b5002bf577efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac3e83306a2f7541c074d3e6baa5b3dc7c829c996a3cd9a919fe98a9e6d7622`

```dockerfile
```

-	Layers:
	-	`sha256:50707b796a835c1273ea70171e05113d9f8deb9b7f1e63408af12c851c21df5b`  
		Last Modified: Wed, 15 Apr 2026 21:40:11 GMT  
		Size: 5.2 MB (5225476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1de9080f107dbe719c55aaabc578a829001ba47bdb855c30f8b3b9a1fe28127`  
		Last Modified: Wed, 15 Apr 2026 21:40:11 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
