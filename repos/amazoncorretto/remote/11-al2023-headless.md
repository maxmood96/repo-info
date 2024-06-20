## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:c9580376fa7945e6cab529a7ff5563b311946f2be2bd45e1aa4e61a5a5e6443d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2f04b11b19f217d0d37aca9f1c7e9134caa089b4fbd52416fa54fd5c87af0626
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128471080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3d9700be888b87b829d0c723ed61072f838b4ae640836ea26bc086f6392427`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:08 GMT
COPY dir:1a64694c076f4e5a1aad0a3ea24080e6520840f532ade5fd6b4f5f6a7cd949b9 in / 
# Thu, 20 Jun 2024 17:20:09 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:44:32 GMT
ARG version=11.0.23.9-1
# Thu, 20 Jun 2024 17:45:17 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 17:45:17 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:45:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c998fa545dbe1c4b0b2d3ed9e2926d49f0c8c74ef41e9b93e4b933c5caf335`  
		Last Modified: Thu, 20 Jun 2024 18:19:50 GMT  
		Size: 76.2 MB (76151567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a207ac86ec5e85dbfb4f5220304d2bc0d2bf0fa45ab6b52cbbe842c27a371723
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126712794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef367958b2d8611d429e753f4459638b221ea2a3ad13456003aabc423904c4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:29 GMT
COPY dir:0c9326c957c0b22895e223bbba2686fb8615da2af32396db3026daf720546255 in / 
# Thu, 20 Jun 2024 17:39:30 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:20:56 GMT
ARG version=11.0.23.9-1
# Thu, 20 Jun 2024 18:21:33 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 18:21:34 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 18:21:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:15e2a4581bb8a27d0865d7375063b10dc543dbcfa6a288911a297aaf754984d9`  
		Last Modified: Tue, 11 Jun 2024 02:05:34 GMT  
		Size: 51.4 MB (51406731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4fcbf977a097128a36e0478957e12675d48968f49ec7965e8b4c03448c381f`  
		Last Modified: Thu, 20 Jun 2024 18:36:10 GMT  
		Size: 75.3 MB (75306063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
