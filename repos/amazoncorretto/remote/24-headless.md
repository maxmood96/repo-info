## `amazoncorretto:24-headless`

```console
$ docker pull amazoncorretto@sha256:40bac72439fe60d92fac11fc3a82f8bebe0169233129ffcb4fe7f24a971298da
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
$ docker pull amazoncorretto@sha256:09a7baa9968d84b5d8cda1d8b320c6c995d446347f024ad33d35eca06f06cb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153835861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db54b2e9d5c71bd9a39cea09fefd6719103c8a1f7dcbf29c78671680cb39949`
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
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f270d4b29a7eeeb2b790617e182170135d4661a5e00a544bb1c992da8525c`  
		Last Modified: Tue, 20 May 2025 06:09:13 GMT  
		Size: 101.3 MB (101270124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a1b958201b1274058ec02beb6a4eca541a648f47a813a46ccb46662f9a56e669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d46e51d05f9272d949a6ed363730c80dd665809b69b726ac4aa2309706dcd2`

```dockerfile
```

-	Layers:
	-	`sha256:bf42fe3ce77b46b6304a572649180282812634ba136a56e78b582d14e4cb0b1a`  
		Last Modified: Tue, 20 May 2025 00:50:15 GMT  
		Size: 5.2 MB (5191197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a1691cc87212399c48be51d6732c6daaaea8e392ce14f5a49f88016d479822`  
		Last Modified: Tue, 20 May 2025 00:50:16 GMT  
		Size: 9.2 KB (9165 bytes)  
		MIME: application/vnd.in-toto+json
