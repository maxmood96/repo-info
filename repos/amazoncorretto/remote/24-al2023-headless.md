## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b0cbb902660f599a7eb4975da51e210b240bfc120612fb23e63a4f0f0596d09e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:814d741bcf4053164e9664bb48b94c7d9d9910d2ebc548977ae2973c88c38e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156119426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9169be76878510371cb7c924bb786c21ddb3d8d86cf0989eed2bf73ddb77d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaa1dc7b41dd6c4142e19c4c806f9d33d31ecac2976dad71133452ad8b2b975`  
		Last Modified: Thu, 03 Jul 2025 23:08:41 GMT  
		Size: 102.3 MB (102279215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6b174484b4cbfa1f7d668ab5a4a78f12859ad35f290f641ecf3c86503b4a4362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0adaca01adb6ce46f846d05916f11732767d0efda9d853bcd07fc44c3424c32d`

```dockerfile
```

-	Layers:
	-	`sha256:ce4e8b2df37d75615fefa962bd6b3eafc11985a584b48efc47da5cb2e202e465`  
		Last Modified: Fri, 04 Jul 2025 00:49:29 GMT  
		Size: 5.2 MB (5195406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f01e94a78bf84e8f3e9a0904fb79f52202491c51ba71740adcf750f746a0b6`  
		Last Modified: Fri, 04 Jul 2025 00:49:30 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:51f38e6653e8ed835584d7fa40c1b7640efd0a140e0b7f057b681c2ff329b9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153757279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de70ba43a16962c9bb1faf5eb53396e4dd27a90fa7f42355c122a4d429f86d56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5169fd7accce154a44567ff93aab40dd61ca59077916cdc872ea57a4f584d7`  
		Last Modified: Fri, 13 Jun 2025 22:54:54 GMT  
		Size: 101.3 MB (101275587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:43480943a329036519ff0a80cdafc7273cab3f5c840c8c77a15930e619a758b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd549df9e7dfd2397fcb7bc21a3f175ff6305fb8aeec336a986c319599253e96`

```dockerfile
```

-	Layers:
	-	`sha256:6d0a585e64a024451d7d86a661f897890ce717e148e768b120c4eaa4c67921df`  
		Last Modified: Fri, 13 Jun 2025 21:49:24 GMT  
		Size: 5.2 MB (5194211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4ec365109751784d75346c03dab9a279e193433c4507fb8cb763c6113da430`  
		Last Modified: Fri, 13 Jun 2025 21:49:25 GMT  
		Size: 9.2 KB (9165 bytes)  
		MIME: application/vnd.in-toto+json
