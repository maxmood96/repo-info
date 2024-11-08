## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:3181d917d56fb286a828ba63bbaea6ff2d46e6f80ca3af1281786faee20e744a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be9d45a1de3a27bd910de8a4abef9bd926cc89596f38349b80b4771e4fe557cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145417344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c612f0475f9701bbf6f31d537cafd16a34830b1ad6757baaadbd252fe4126c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:5f3b500dc43eba4cfdf8e70913f712bd20874deac837800a822eb046b9b8bd01`  
		Last Modified: Wed, 06 Nov 2024 19:16:29 GMT  
		Size: 52.3 MB (52344739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51704b2c1e97c4ed4e25109cb10bd2a9b89142f0ed40daa9410061ef1f227cee`  
		Last Modified: Thu, 07 Nov 2024 21:48:01 GMT  
		Size: 93.1 MB (93072605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ce204a10180acefbf7d7232ae2eec30dabda621375c65f24cba00cd606f2d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67048fc66dd16c467c290a98c649aea4f9d0877c27baab2b77de9c1d9a6824c`

```dockerfile
```

-	Layers:
	-	`sha256:6540d4ed196d52f83486408708dfd4380d92fba5041cf7eff6baa689feb63f4e`  
		Last Modified: Thu, 07 Nov 2024 21:48:00 GMT  
		Size: 5.2 MB (5188973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c4ad5524dcb4136fede3a201e8a5ee7cdba41b3e847c97f7f2a088e8808fbc`  
		Last Modified: Thu, 07 Nov 2024 21:48:00 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9000070bf63f2d67cedb55c1e07818655eac86b9f245242ec5e9c18392d4e25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143470073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8483f865effb14e606639751700ff03a72900355c18d6b4f37eabbca1034b387`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203e8a4ccb0dbd60da6ce626c14a7d3f216dd4888d625cfc7621553cdb07c32f`  
		Last Modified: Thu, 07 Nov 2024 22:07:54 GMT  
		Size: 92.0 MB (92046072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:558c7e87d1161fbdf85c7d3a63792e980e320b126f153b152ebc82ba8762aaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:572230d58c8e0b0dec010851c7c42022c4720f89cb2053a6aeb61a10477f0f1b`

```dockerfile
```

-	Layers:
	-	`sha256:8976a183511704d49a57337deb6831753f1016dde93449734f041dcba4695599`  
		Last Modified: Thu, 07 Nov 2024 22:07:52 GMT  
		Size: 5.2 MB (5186959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc3217388ca7b45d8e527a6012177156bd714a23f85f4eb9b9643f2f9655f670`  
		Last Modified: Thu, 07 Nov 2024 22:07:51 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.in-toto+json
