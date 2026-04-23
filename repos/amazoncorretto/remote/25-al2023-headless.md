## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:bc1cc4aabc8ff94f45e4d577192e6fc91952f1775a1908ee4452be6093addf74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d4f65ac9fc1722f6441a2198e190f1e53426dfa180075cf634aedfee0e1047ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158292373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3125c93dd310cc5a940d6a0403359982c947cf784df44e149addf7b86c3d6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:31 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:31 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:31 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:31 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc2c5e2a63d75125dbfcc3fd766ced159a8fd43d1707d4ce3fc35065622a1d5`  
		Last Modified: Wed, 22 Apr 2026 21:35:52 GMT  
		Size: 103.7 MB (103721119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de85293e3c3549e2f044572476725ef353c0db0ccc2f3e6f37464455edc1cde4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3da375e3666b91253a35e8625cc7b69cb9baaab91167b71ea716fd71f5ac679`

```dockerfile
```

-	Layers:
	-	`sha256:e4311c31ea0712f453c97729e0d7a4089d58d8f99d3e3b46d0c41c6457c13041`  
		Last Modified: Wed, 22 Apr 2026 21:35:49 GMT  
		Size: 5.2 MB (5202050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7cb9d141f09f55533b983ea4d2a0522e7eab9979458b913bce944759521f363`  
		Last Modified: Wed, 22 Apr 2026 21:35:49 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c8fc5beb362208a63f6bf83969a911b1980849ff2895759a0e2ef6226149f5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156096000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b1ed7733b2b1a2a00eafa0086bd68a43a1164cb2076c7afe5ba9258864b2eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:21 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:21 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:21 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:21 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19273025c8b03d035c7d2daa8c0704568633b1c4320b5982f50208586b7b498b`  
		Last Modified: Wed, 22 Apr 2026 21:35:42 GMT  
		Size: 102.7 MB (102653261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:03c0cde01f5ec5963f62b38f35d2f5acd2459db4b12937f9072be59db18f0403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6df7d471c5d41ca80de5b33018accffd54cf86747d60ac6d50c2a278b4178a`

```dockerfile
```

-	Layers:
	-	`sha256:4cb78f7756d82b72dbfc0eea18d41a693b7076f324ebac931e65c82e5acce711`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 5.2 MB (5200862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f3bdc59783a5c1c1bef9ee8f0dd489f1fa1a233dc1db344951fd927a7e660c`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
