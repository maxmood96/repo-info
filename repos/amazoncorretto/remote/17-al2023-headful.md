## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:be866107fb1b5b3557b95d1250a63cd3e0ab779958e5c37230316574600d927c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:184d5ae03a50ee07bc4c8b78e02f9811df8a8e262a82fb2341f0941383f5bf6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138856428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ef7164fe2a43a1ae48836568a571cfd0f881bb46070ff2f2f41451108139d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c4136f829226f1ef734b6a7901fdc2969a69ff47073f849729f367a233aebd`  
		Last Modified: Wed, 02 Apr 2025 00:00:21 GMT  
		Size: 82.9 MB (82949375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44cfae70ebf26398d8020a87568f58d5b41da1aa9f295a79eba54390e4e486ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862a0c9335d4d7f876ce7ebaf690a2f00214864ddcecff0580ae72603dfb1f10`

```dockerfile
```

-	Layers:
	-	`sha256:3ce40053f2d813fa7993dfbd0ba5aa0511fc8aaef89c47c6cb1dfb390713bd3f`  
		Last Modified: Wed, 02 Apr 2025 00:00:20 GMT  
		Size: 5.5 MB (5451028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49ff1d9497253d4813182d62e3b8e056d118c69bad59ca683864c59c66cbbdd`  
		Last Modified: Wed, 02 Apr 2025 00:00:20 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ae34968828e1e7c1d3a2ecf17d8e4d224ed505e5d2fd9b91d9d726000fa70341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134541618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875698245949eaecaf85201ac9fc5efe1ee906c16173759ba141fbf0ef4750ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0e1409da158a554a86a9884a4a3806c1401c6bc03aa0de69f96594b0801fc`  
		Last Modified: Fri, 28 Mar 2025 00:15:54 GMT  
		Size: 82.3 MB (82293628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aaf4007030c9603d6820f017a5755f4c3bbb781bd7b41b65d3c276fb71a7606e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dbe358676468eaf1589b666a598f9c4e8dd517b8d37a99d9a28371ac411c549`

```dockerfile
```

-	Layers:
	-	`sha256:232f3047bc42bfb76039bb6eb1c0e963f87d92fb1350983db12820fc25f2863a`  
		Last Modified: Fri, 28 Mar 2025 00:15:52 GMT  
		Size: 5.2 MB (5183753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c2f22879a9476c6f78497197bdb4de200522cdcd77139ebb202fcc9eff4596`  
		Last Modified: Fri, 28 Mar 2025 00:15:52 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.in-toto+json
