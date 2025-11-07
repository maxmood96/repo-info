## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:a0ef31e8fdbff1e7d244945defbae6192f8a8db6d8e377951582d37c886e97eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7bbc2b44358d3c5f0eaa078ba14b49569de2fe8aa1a82b40b3acb63964ed6d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158330953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bff67f88b6c7188f8735af92c197667d80e2f60ede1593523e6b28c91259ad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:48 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 23:12:48 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:48 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:48 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce9d6591e66a863a4541da6b74428442a855ffe69d839ec2691222802460e6a`  
		Last Modified: Thu, 06 Nov 2025 23:13:23 GMT  
		Size: 104.3 MB (104330450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba642c9446fdf9215920a481f378df0c253518d23af1846bc78700f74e5226ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4160e400e5fe257edd1148eec8ab994b9587746b787b89a064782ad2476029`

```dockerfile
```

-	Layers:
	-	`sha256:210ee328a8e9e8ecaf9c143befd675babd3979cc3a0e4ee1b067aa3086add9dd`  
		Last Modified: Fri, 07 Nov 2025 01:51:12 GMT  
		Size: 5.2 MB (5220208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3027dfcace50e5ce6d7eddc33afeff7f911bb4428aaff39bb55c0f430a13e18f`  
		Last Modified: Fri, 07 Nov 2025 01:51:13 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0815c9fba438a6ec1993afc9e050d19588657c735b557b044a581a08b5281d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156178338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2d1a355e0032a5447668dd8413d50b1601a66e4efb16955d3a7c9f07563fa0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:43 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 22:14:43 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:43 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:43 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac643f53b68b70e9ad80aff187d2523c4e0990841f5a01ee23eca67fcc9f2ed4`  
		Last Modified: Thu, 06 Nov 2025 22:15:21 GMT  
		Size: 103.3 MB (103276654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3526a1f31f577606c84276c81f5e5b8068be3c7e8bc6d68b1efabf3c3f7aeb47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58492044224d053f639fcb114d7baa5c9cf5a11f88f3020f7aee1f2d25d3e159`

```dockerfile
```

-	Layers:
	-	`sha256:96b5b190b4a99a4340528658d1dce20ac7e5035963527814eab4c9a83e7d92fd`  
		Last Modified: Fri, 07 Nov 2025 01:51:18 GMT  
		Size: 5.2 MB (5219022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:465fd5fd2a0fab3e68b2ca2c4db1a8542d4dcb5c8de0e52b0ce882aeac491dfd`  
		Last Modified: Fri, 07 Nov 2025 01:51:19 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json
