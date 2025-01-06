## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:43b65c1d1c46e5e5c0f0fede6f2603e44da9ee478bd36e6aa4fad0122805e018
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f8f85c3b312b5db21d4326965dc000d1e51ae3b4110aff46844fb0af269c6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142116904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41912d4b83e530a7dd9e924ff1e385274b88d91fe67060ab8a809f304d9a8d10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed39a5f7e72a2e89c462ba11778025c996c95cb3acea512ecfb297dd61eb2db`  
		Last Modified: Fri, 20 Dec 2024 22:33:30 GMT  
		Size: 89.0 MB (88960591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ca122b97751e5476c0c193e6ad3fb6716acfafcd5830d782cf5ddd0570bcc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed512562632c92c344e9531b4870e0c1e7e04e539e970ea9bc9968bfd0e1637`

```dockerfile
```

-	Layers:
	-	`sha256:7783150b94d72767dc65d141f04f57fd812961e0bc0e3629e892c0054dd413d4`  
		Last Modified: Fri, 20 Dec 2024 22:33:27 GMT  
		Size: 5.2 MB (5181042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2ed438b8fc35448d8b0d1ff01520f2e4e39b88b6c950f5db71c0c6901c71a4`  
		Last Modified: Fri, 20 Dec 2024 22:33:27 GMT  
		Size: 8.7 KB (8749 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:645dfd7163b18c53d9a969ca43dd41b16e7974a3d46987d751920f127170de86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140348138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22c40a37036f89185d8e939186ba916e8621cc7de6e0261f34c5e4b7f74a09f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:98ab3ce9b55607064b358289eeb810db43f69e016067c07e7136a807475f6f27`  
		Last Modified: Tue, 17 Dec 2024 02:01:08 GMT  
		Size: 52.3 MB (52276382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cb3526abd650a1cc6590c84334132cf5a05c8a1e4f6a2eefbf96a929266b22`  
		Last Modified: Sat, 21 Dec 2024 01:51:09 GMT  
		Size: 88.1 MB (88071756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9f76bc8cafcebd496b0ae524c21cc7fce4b6aee8193eaffa93d7839ee209f04e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f1d8b39f0cf23555e20e2de552222b50ad58aa44cbb9af063829eab479603e`

```dockerfile
```

-	Layers:
	-	`sha256:b911d59fde20ce74bb41032f098dff23940b431d424528e68f485d7f0257a59b`  
		Last Modified: Sat, 21 Dec 2024 01:51:08 GMT  
		Size: 5.2 MB (5179832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f4d1c4dbb056fd92c9488d11e0c447b759dac56f44d7d4b022dde603ed9c80`  
		Size: 8.8 KB (8829 bytes)  
		MIME: application/vnd.in-toto+json
