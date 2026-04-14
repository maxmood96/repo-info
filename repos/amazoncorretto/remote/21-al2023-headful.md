## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:d8ed93ae1678c995751cc45e6c5434a645b1dff31cc97ff9b8d319ce49eb2fe2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0d1d8aee0d8a4ca6414c7440318bea1967e909f3f927fe1c1c423d8af30bbf12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144542979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb59e93e509d46a2725c4a3df737e1a103c01340e459bd53ceca50fb694036`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:26 GMT
ARG version=21.0.10.7-1
# Mon, 13 Apr 2026 22:49:26 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:49:26 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:49:26 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e7a42e83dd5c0764150e2d279f750c5824bbdfcdc181175d5839baa0ce0a0a`  
		Last Modified: Mon, 13 Apr 2026 22:49:44 GMT  
		Size: 90.0 MB (89971725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2a4672fd1ecbee6b1bceafa14d39478d25654877368bd49e2e7043e59ed05fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac2c8cbb6c9d8aa98ff6aab4e4d667174c14be43ad0eea91b94f8d9f25b1c20`

```dockerfile
```

-	Layers:
	-	`sha256:0dc0dd816c298270430d480c894a40f7228409c69e58ac4ec58860be2c765a14`  
		Last Modified: Mon, 13 Apr 2026 22:49:42 GMT  
		Size: 5.2 MB (5216395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a45f99ac0e8094e964e428927dcb58a12da4f7b1cabd49c9a2c699aca21f83b`  
		Last Modified: Mon, 13 Apr 2026 22:49:42 GMT  
		Size: 9.0 KB (9048 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ca30c6888a365955e71f885e58ed09d15d25a31509563f1ade35cd7bd2d2c7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142555919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935a72e309a1e270d393d6814ea14ba844092f6556e618889596f1aa6fadb1eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:12:12 GMT
ARG version=21.0.10.7-1
# Mon, 13 Apr 2026 23:12:12 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:12:12 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:12:12 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:12:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66376ca057287745e98c0e4c2b9f722642c5d7370da5e169e4e5e3e95cb1ec0`  
		Last Modified: Mon, 13 Apr 2026 23:12:31 GMT  
		Size: 89.1 MB (89113180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4fed7b2a84721bd10ca127750fa89cc188855ae0482890d5fa5db00309cb48e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7d35a7460fe0edd4c614381daf781734f3ec4c8dbfad9fba9cc4f921bfdecb`

```dockerfile
```

-	Layers:
	-	`sha256:5c70e9254aba3d7fbc9e88f9e776f158c99e3e2ee5d8312290ffb72577b139fb`  
		Last Modified: Mon, 13 Apr 2026 23:12:29 GMT  
		Size: 5.2 MB (5215188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cab6b43510add72fb9968d364a050ac9e8049cdfc5952f9ccf6cf78e68190c22`  
		Last Modified: Mon, 13 Apr 2026 23:12:29 GMT  
		Size: 9.1 KB (9126 bytes)  
		MIME: application/vnd.in-toto+json
