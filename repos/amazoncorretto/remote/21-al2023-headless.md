## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:7559ce76db44c0af892dbe400477f0c9528ff5fc7ffb758f6b091350feeba012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ee930e7f36094c3617f527ca82a66d6b584f3466e3f5259fb0af3a72c05bf4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143934477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e56cda2699b4b06ceeb53ed7fa775b8f2af8f293fa7eaa77c231ead87aa3ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:02 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:13:02 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:02 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:02 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f4bb68c2a18967fac31f0b85e6e4b4fb280ddd884c4fc37fbe20800be4cb05`  
		Last Modified: Mon, 04 May 2026 20:13:22 GMT  
		Size: 89.4 MB (89357724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40b9fefab6b3176c244ee3a27c4f7ea5ff74c840d1e08064eba41aef123f64a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872fa9c8020371e695157fd76823fe74286995983af4b0c7019ee21adc8fae38`

```dockerfile
```

-	Layers:
	-	`sha256:c7c9e1075ac7e64429eef0d2c9cfc7b283b627d8e1ac05af6491a390cc2670e0`  
		Last Modified: Mon, 04 May 2026 20:13:19 GMT  
		Size: 5.2 MB (5191789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5b2ec0e40297ec7b763f6761aafb83aba0610e9118c11cc2f09d4bb3e5ef3a`  
		Last Modified: Mon, 04 May 2026 20:13:19 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6405b24aba1f8303554cb7b467e09e69f5bc3e44958435813f3eb2b4d729ec2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141948339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e0956e5d23eede44c626d03a4d3e0809f18889bf36d6fa122fdb043caded25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:22 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:22 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:22 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:22 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f959aa038750cf57fcba2ebcecbe9789d36f81d4908d8a89095a5ad14c2ff7ca`  
		Last Modified: Mon, 04 May 2026 20:12:41 GMT  
		Size: 88.5 MB (88491569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:581fa9e3be8fb8ae2fc1683e2c2d0e90a0598b85c6aed05b9d5c9deb04d077b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd3cc62123f2bb42e5d10b18df9fcc4d6a71a92853572c4f9b49a50b78fc1fe`

```dockerfile
```

-	Layers:
	-	`sha256:5913800efd5ba82c14818436046b993c642f4ec15a973f048d658d2be84c4663`  
		Last Modified: Mon, 04 May 2026 20:12:39 GMT  
		Size: 5.2 MB (5190580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9854458da9b4a3177c5707a3420db4f658c8b102ecc2f2f421479aea6c3d5`  
		Last Modified: Mon, 04 May 2026 20:12:38 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
