## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:efbe3a114a2fceaf78c21bfdcbc36e672923f3092485a7a2402d3df8a2abc92a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:18046ac679aa588803c3a78e6e1f8cb3934119f64b44af7bfe8c29765221692c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137112477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e5986cdf2c77f556a69ee336ca20856145d51ff43a4f4f7a8fba3703b98cab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:18 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:18 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:14:18 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:14:18 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2f47d0d6d95382b350ab417132f8b849286c09e03d17071897c5ebc465e929`  
		Last Modified: Mon, 02 Mar 2026 23:14:34 GMT  
		Size: 83.1 MB (83079637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:82becfef8d1a63d2dc3ebcb45bc6f48d90233fcf6b1e64245946a1df02cdc4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5628a24ea0865254f3bb870fcf042fa8ca97dfef4f2cb6ad524472fde2e2c3a`

```dockerfile
```

-	Layers:
	-	`sha256:8bef9267de9de93a310b66f1df3bef03398473ca9a696af011b8c8835d6b5113`  
		Last Modified: Mon, 02 Mar 2026 23:14:32 GMT  
		Size: 5.2 MB (5208395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08529afafbf981b1f82d624a461e0acd017f2bacbbe15b6c30097da547dbd430`  
		Last Modified: Mon, 02 Mar 2026 23:14:32 GMT  
		Size: 8.9 KB (8891 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:445aabd0d7c24dd0f98977c397295eedeb89a5e8d0f694c57ec3461b9f71b0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135442410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6796d4b4e5710abdb839e5a57d5f340e7aef244f9590c57cce838324d8faba1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:31 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:31 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:14:31 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:14:31 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4f813ad42bdeb7234ed0d9e9aa3863a5d544590001a6e0c499b43a1218019e`  
		Last Modified: Mon, 02 Mar 2026 23:14:49 GMT  
		Size: 82.5 MB (82501091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:25d554122dde5989c5f5df8d2726fb2e8e572ac177bc5026f493aed3883f29b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cf0ecd9acb42cd27b9903364d091ed250c047e3ef4be985406f685cbe1d5cd`

```dockerfile
```

-	Layers:
	-	`sha256:a59dabc7c0b11d4fa1eac87015984bdee7f8a1952f8259a6d27cf1ae9fa71ffe`  
		Last Modified: Mon, 02 Mar 2026 23:14:47 GMT  
		Size: 5.2 MB (5207186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdca97fecc998af1ff61adc2e35f8638a23fab9c496c9aebae17c2a91ca93773`  
		Last Modified: Mon, 02 Mar 2026 23:14:47 GMT  
		Size: 9.0 KB (8971 bytes)  
		MIME: application/vnd.in-toto+json
