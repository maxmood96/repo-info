## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:978494e9413a82084bff2a509e914343811b7f4a8f1ffda7aeca018e6da2637c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:324eedc32b182fa78b37d8b61946eb7be04d5814837923923e93adcbd393eae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135780305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee30cc23743be33d756b5314d16945a60ce83b8b7f3b9b9d031443027601c888`
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
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8043c8635c6bb52160e9ba2d4cbcc014d4521787ea7593e6a750559860c88c74`  
		Last Modified: Mon, 19 May 2025 23:37:42 GMT  
		Size: 82.2 MB (82165603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:37c09288a145855e50861adc137dc562f9e13297c72201bc527b6bb768771636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b06bcf78f6099fc76a6c340be4c8b5c9a79dbc3b12e26a1cee7caf2264c6209`

```dockerfile
```

-	Layers:
	-	`sha256:7340260a4f626f675841210630f74469cdf48d1b410e96113e3e7b89114378e8`  
		Last Modified: Tue, 20 May 2025 00:48:51 GMT  
		Size: 5.2 MB (5180505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82bfa083b3dacf95b60316df7f636b46feb469ac08f08aa9a778979e8b3274cd`  
		Last Modified: Tue, 20 May 2025 00:48:51 GMT  
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
