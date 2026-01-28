## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c217e1b5482e64fbb2e332a79d6ba8943628b93bfc6b791880f51e945156801d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:aedbbd585bc9049af9b18cdbf260be9c36eeae29b8022f45a8ac215c1e0488fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137106193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce9715e9bf62c534c64ab267f9e147c3feab71e380ec162cb6ac9434476ee70`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:08:00 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:08:00 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:08:00 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:08:00 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:08:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba08f6c7085c1194d3120fd975634a5e55f94516193357d19a4b00f03a1a760`  
		Last Modified: Wed, 28 Jan 2026 04:08:17 GMT  
		Size: 83.1 MB (83082357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a5349a76a4214bcb0f2698f3d4252b3f16739c8b9f46398665655722618c559e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30558b248aa11983b4a6388ce0b3e0ce7f512b15b2e60d7b0803a51beaffd028`

```dockerfile
```

-	Layers:
	-	`sha256:293119e81682e84e0227abf538f170b50ba554145e5ff940321a173dc1c9a833`  
		Last Modified: Wed, 28 Jan 2026 04:08:15 GMT  
		Size: 5.2 MB (5208325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73d886bd1d0f982834df131788e063048093c6099fb04651baba23498016e98f`  
		Last Modified: Wed, 28 Jan 2026 04:08:15 GMT  
		Size: 8.9 KB (8891 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:34b0bf507c16c2d4d2a42010920494b07fe706fb5839182571db42bc0155c798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135416599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5396ae65532bd34b0956bfb0e7512dc79b3fc165c0e2584c0fdd7241e5a27c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:29:02 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:29:02 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:29:02 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:29:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:29:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a161f65eb73babb227183c165745698756c51eaf9662c934d3b20e96a2c6ddb6`  
		Last Modified: Wed, 28 Jan 2026 04:29:22 GMT  
		Size: 82.5 MB (82499961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a79759a28d4a1f33c64c765f1f6f4fc2a9f83802216ccedaed4704b0ff47039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feea816c904997a6b9f916867389ea592c57a27eb672bc4b00b47907304cf5a4`

```dockerfile
```

-	Layers:
	-	`sha256:50bcb7f93e252c2294d98f0774d2cfad8c08fb9d89eec0d09f1666527131b6e0`  
		Last Modified: Wed, 28 Jan 2026 04:29:19 GMT  
		Size: 5.2 MB (5207116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23dd74b90504e2b402b54c016550dae79bb84f5d80edd242beacd5faae8ad03`  
		Last Modified: Wed, 28 Jan 2026 04:29:19 GMT  
		Size: 9.0 KB (8971 bytes)  
		MIME: application/vnd.in-toto+json
