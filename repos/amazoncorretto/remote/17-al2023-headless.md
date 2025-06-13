## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:82141513b9dd4d37504bf573b9ef9fa037d148b22de277d5408798786fed4e71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:df169e74d43eb65345ce1d051b91f597342d72c74d35e3b80ed2dcf27a85357f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135741258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaf4ed1b20a2f44cf20f5d5bf0cf81bf8559f11dfdd621000b2f67656b730a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da77413fc9943de2c4daf17ca14f779c7680b4777ea579b2092212c50263e05`  
		Last Modified: Fri, 13 Jun 2025 17:03:40 GMT  
		Size: 82.2 MB (82170898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:22dda964b8b45a6d3a84881d5b7d6b8ac52faf432b0f45e888789a1b592a340b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614ea1482ae8a750a35bfef8f9306ffc05f1aec12a0f09fd4b68df536083fd14`

```dockerfile
```

-	Layers:
	-	`sha256:74cea94b89cdbae3925e5ee49820fa0096735b878d98f03f706d6e35fd69dcd4`  
		Last Modified: Fri, 13 Jun 2025 18:48:24 GMT  
		Size: 5.2 MB (5183519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a7021126799e4d023f6779bffd2e50a993ced978f5eaccca10bdde0c534e773`  
		Last Modified: Fri, 13 Jun 2025 18:48:24 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:013dab6949f05773ae0a37a527e363d2e1b22ac04c39e06b7d7ded9ed2233418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134167062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfc3e86240b4beaf3610e03ec1b1879aadb42e337a119d99ef6c1ec4e2ba20e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cf8ba6d006cc99b5e32ea39883b8421bf640af1b3db67f2ddfd97097877091`  
		Last Modified: Mon, 19 May 2025 23:56:54 GMT  
		Size: 81.6 MB (81601325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f617a09615d487cfa5d04027568462f6c536dbae32d898be7731043f7f6e32ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b6b6a775515c92adcf134aaa6041ce1a0f7ddc05e8f02435c3b26a33b6c614`

```dockerfile
```

-	Layers:
	-	`sha256:862d230369707fae743b38fa8655b04f7df6fbdd7c8e4ca41a2aa8d88fb631b8`  
		Last Modified: Tue, 20 May 2025 00:48:55 GMT  
		Size: 5.2 MB (5179293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d76d73b1c1edc67689abfe2987ecabf27859dfc9b81c7a988018f7c00a211`  
		Last Modified: Tue, 20 May 2025 00:48:55 GMT  
		Size: 8.8 KB (8830 bytes)  
		MIME: application/vnd.in-toto+json
