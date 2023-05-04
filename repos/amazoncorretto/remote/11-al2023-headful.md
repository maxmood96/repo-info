## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:aec466b104e546b10e14258eb4022eee695605b6c3bad8002784e40d18965663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5f5f8fa034f1cd358d423c2dbe6b5762edd9869fa07e33ddf22fcfcfb5a442a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268cf3d69983823ba0b346cfa2b4272ac57e4a353acc68fa043d00b4de150068`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 19:19:50 GMT
COPY dir:54e5777658be1a3cce5e4a60768f16ebadb522eb8101c0ae54ee1f769c3b164e in / 
# Thu, 04 May 2023 19:19:51 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:39:35 GMT
ARG version=11.0.19.7-1
# Thu, 04 May 2023 19:40:29 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 May 2023 19:40:30 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 19:40:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c863b89e86f3f74e3b816088bacc4f7e984643e02457c9de2f2a80f6f92b9c34`  
		Last Modified: Thu, 04 May 2023 03:04:23 GMT  
		Size: 52.3 MB (52264363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1679266ad66b5a97c385317abf4b69db1cf31cded625e2e1ab8f3fa7c15ea10c`  
		Last Modified: Thu, 04 May 2023 19:46:05 GMT  
		Size: 76.6 MB (76551132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:63dde7fe491b655b7ef10148d152d4121f9bd8481c994a87a589e141800800a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127018824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df50531aa89cd2c6f97ab28e5e72fe612ce5856c4de2e336bae42b2972685bcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 20:02:38 GMT
COPY dir:c3490ddfaf576048c53c1266c10c570c0c31d1ef25f639153f91097415fe319b in / 
# Thu, 04 May 2023 20:02:39 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 21:16:43 GMT
ARG version=11.0.19.7-1
# Thu, 04 May 2023 21:17:35 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 04 May 2023 21:17:36 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 21:17:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2356aaf73de639cb8d40c53e05e60b5aa503113b2f9cf79ee0c5fdf574f1a50f`  
		Last Modified: Thu, 04 May 2023 03:06:59 GMT  
		Size: 51.3 MB (51303115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8a8532b9c6d79073d282b982f930b46288ecccbed34e4363d8f44355652e53`  
		Last Modified: Thu, 04 May 2023 21:22:12 GMT  
		Size: 75.7 MB (75715709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
