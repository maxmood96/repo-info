## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:046dafb1aef08c3eedf03d1e068de4e8ae95567b4c2c5d1c7961192d1766dc90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2694075a505be5652e9b98c2cd8396859eed3971930e81814578d38fda1dae3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143928449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c500816a9d3ddb99005ee45048c9ceca3f47294ac627ebb0e11f648ce0c13606`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:33 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:24:33 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:24:33 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:24:33 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0977964724baf3d9c5553685e7194f3f31ce2e0b6c9fb7b36a96ce317956e3f`  
		Last Modified: Wed, 03 Dec 2025 20:25:17 GMT  
		Size: 90.0 MB (89959428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:214d309dbb81a2dec26832f15b16e73d48a3c07a5014334ca4c33c218fb8e04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be1844c20b631dffa7e4b81c7c6e74c79d5ffc80e3ef78a1d2ef71ec8e4b7802`

```dockerfile
```

-	Layers:
	-	`sha256:7aecddea6f27800a12ade90f07c486f4eea942a9e97e57f41243f6ef94684268`  
		Last Modified: Wed, 03 Dec 2025 22:50:11 GMT  
		Size: 5.2 MB (5209943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a6b7b43072d8dabdbbd0eee53a31aa9917714d4f3e169b55e3817bba6de140b`  
		Last Modified: Wed, 03 Dec 2025 22:50:11 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:97bf219477995070be1e8a5b9aba6d390bf8ae34b55718c81acb98d9f9efaa5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141967550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b6656b219250845d3fcfcfc171975c2fa1e2c24031808f20952872564c784f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:38 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:38 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:27:38 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:27:38 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fa873b0071ab02bfa1e9278aee5ef2d6a913498c07c9ca65699f575614a0a9`  
		Last Modified: Wed, 03 Dec 2025 20:28:28 GMT  
		Size: 89.1 MB (89098129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f34efffa894dd7e96c5f7452e442ddcdf967835f5d96eb3bfcc1a113d38c6c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0acbd67175c6077484614dc65b18f2a7375f6cdb7dfbb50e8a5c02bcad65dca`

```dockerfile
```

-	Layers:
	-	`sha256:eb41dffbfd1c0de48e7e825c1c1b9c3479c7fd2a724b6ee04e6c0ef2a5b17267`  
		Last Modified: Wed, 03 Dec 2025 22:50:17 GMT  
		Size: 5.2 MB (5208736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e59f14b4cb2e25afacd4fc859ce53abce5c1e574a111aa84d2784f329f4242`  
		Last Modified: Wed, 03 Dec 2025 22:50:17 GMT  
		Size: 9.0 KB (8969 bytes)  
		MIME: application/vnd.in-toto+json
