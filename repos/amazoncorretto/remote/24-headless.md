## `amazoncorretto:24-headless`

```console
$ docker pull amazoncorretto@sha256:b0d76cfd5aeec5fa7dde2b21bf9d7d3549846e68d9aae70589dc9ff282b005e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fc7c010d2ff43954b79115817324dbd601aecd17258d92814bc76c244743ee75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155845682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc666b36a9fd8f500c1e62ce828b66340e1004fd604f94d048a37cd798fd4dd`
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
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbfc86ce8d3263a219495b9f3c56694ae47ea6b390935a9a6efa75c537697f3`  
		Last Modified: Fri, 13 Jun 2025 17:03:32 GMT  
		Size: 102.3 MB (102275322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f333a68f7cf303340ce3b72a9795e0ee9a52e6ade55a2f39f1df084315c5dcfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff4fb1ae6d19b543083d51f1cf2feff9bdfcb5f2da1847350fb5e058329928e`

```dockerfile
```

-	Layers:
	-	`sha256:85e1a0f8ed5bc33a8a3edaae0188f5b1bf1ec6d9a9e0b1e761bf01a699180d52`  
		Last Modified: Fri, 13 Jun 2025 18:49:27 GMT  
		Size: 5.2 MB (5195400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d591e44ebaaa93d7e095995001e5a6e857d80e1d0b2a2904ce712289f469341`  
		Last Modified: Fri, 13 Jun 2025 18:49:29 GMT  
		Size: 9.1 KB (9073 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headless` - linux; arm64 variant v8

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

### `amazoncorretto:24-headless` - unknown; unknown

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
