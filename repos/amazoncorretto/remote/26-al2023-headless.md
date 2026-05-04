## `amazoncorretto:26-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:d85c72eaf0fa5ae70d5622ad354fefc8d0607ea8436b5124344e03599a299cd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c5e539cebacfd0f6d729f3bf1874e5427fce207ea80d55a2ad8f03f19c2c4a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160400374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64df153ecdaf62743bea5771867df9bf269859382fcefa03badf4234ee1e1095`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:19 GMT
ARG version=26.0.1.8-1
# Mon, 04 May 2026 20:13:19 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:19 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:19 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d2dbdbdc638ec2d870dea4539b7afcbce76dc8c3a99ce40febb8f3654fb42e`  
		Last Modified: Mon, 04 May 2026 20:13:37 GMT  
		Size: 105.8 MB (105823621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0aaf6481e8f930f312ec1fcc9441301053e4e55b51a32d0e10dfdfae47e6d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4425f0c6d06340cd434125fdc842c0ceb8779ae781432d54f0435daba07b29`

```dockerfile
```

-	Layers:
	-	`sha256:c026bca0c3ddca10acbc8eb197d880981d9036ee37dd9e030d39eae760214e90`  
		Last Modified: Mon, 04 May 2026 20:13:35 GMT  
		Size: 5.2 MB (5200408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e2a8044161d29aa3d945caeba50e9f71f591f8284b9b7ea8c2005c82f595ecc`  
		Last Modified: Mon, 04 May 2026 20:13:35 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:692d57c27ed1bc40f1a8b9973a6b7fa1b0a8ddf808030bf8a04d3b56c5601293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158164771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2925422deb6a683089cff172b27e97434b2f439367194edc4f2e40fb338a55f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:11 GMT
ARG version=26.0.1.8-1
# Mon, 04 May 2026 20:13:11 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:11 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ec731953f04bc6818e3860b013a647cbb2d525b3176d513ff14232380bfd2`  
		Last Modified: Mon, 04 May 2026 20:13:33 GMT  
		Size: 104.7 MB (104708001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d819a9d95566855cdaf50afcf8850f9ee06be13dc9a487d2f204681ec7f15b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454625585b2b3e184c94038aa0fe05ac0ad1b7c264ed5b00d8e1cb139a636fb`

```dockerfile
```

-	Layers:
	-	`sha256:f78c44e54a700943a25ea6e761ab46fa92a4392a4c0270a84f0b20e4226d37c9`  
		Last Modified: Mon, 04 May 2026 20:13:30 GMT  
		Size: 5.2 MB (5199218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93d19905746e160da2c551a24e01ec43af02948ee84a8a023994ff7a087f8fc4`  
		Last Modified: Mon, 04 May 2026 20:13:30 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
