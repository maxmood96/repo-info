## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:34d5ae34bd5f1625dfa99ac2a3f4118abdf57097008d26409742faf047b1486e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9d9c5d562d95ac35071900a8d341f198bd6fa187da6766fc0ef72f5f45104e2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129004941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafaf8ad92ba809d91310cda53635cebd719bfb39b72ba89ea1288fd50b902db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:41:37 GMT
COPY dir:8f7245a97c061726fd1f5e8ec557a254660d588f51008b0475bdcdcce3a48bba in / 
# Sat, 20 Jan 2024 03:41:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 03:46:24 GMT
ARG version=11.0.22.7-1
# Sat, 20 Jan 2024 03:47:24 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 03:47:25 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 03:47:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:cd4602cb0e84e00e8b7d38510ab92c4d091288133108bb74e581c22d31377e8b`  
		Last Modified: Fri, 19 Jan 2024 19:08:42 GMT  
		Size: 52.2 MB (52244936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a97ccd6f3a508fd139a18b671e00c37173fc988bda956e6d9320d46927e6e34`  
		Last Modified: Sat, 20 Jan 2024 03:57:37 GMT  
		Size: 76.8 MB (76760005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a677d6a892c32b906424c00706f89a91e03b00f5e4a2e7805e85374076fde276
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127237513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b12ac118cb317bc2fad33b9c93263e79ce94dca44ccbd1fa94a015403da2973`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 Jan 2024 03:48:00 GMT
COPY dir:bf3fca734fa6b784c9516c9f20cd0ad6226e1fba4faa2ef00cc5ba4e2d3631a7 in / 
# Sat, 20 Jan 2024 03:48:02 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 04:28:16 GMT
ARG version=11.0.22.7-1
# Sat, 20 Jan 2024 04:29:09 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 04:29:10 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 04:29:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2cc150e431896856b2c36c9075baaf386855a496fe588adc23ed44af495843dc`  
		Last Modified: Fri, 19 Jan 2024 19:08:39 GMT  
		Size: 51.3 MB (51309289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f73347b2b45f7f22cc24de9d8efa751dfc33598669ef544ef38d0bc454b893f`  
		Last Modified: Sat, 20 Jan 2024 04:34:02 GMT  
		Size: 75.9 MB (75928224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
