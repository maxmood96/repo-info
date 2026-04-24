## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:6fa549f5e05bcddce588ed5ecbb7b68d2f3b3c9e645d51e4b8499f80935c55c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b4f5d72397431298ad418e85c7ef5e08fa984a2f618c04596eb240e6c3b8b369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154357665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46efd026e1575b8a618777773dd1274c06066cd3c37e1e7a665066fec021d0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:41 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:13:41 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Apr 2026 00:13:41 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab898701db3eff7b31c7411fa231b89256a3a279dca1dc9bf5cd927fb5c1b42`  
		Last Modified: Fri, 24 Apr 2026 00:14:02 GMT  
		Size: 91.4 MB (91405482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4344f121fcb0f2caec67aac51f386077e36a7f5fb2da078427f148569b88c6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5876330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a321a8b992ae6724412ba1be71c684866f09f3f419e369eb8843c29db8817741`

```dockerfile
```

-	Layers:
	-	`sha256:879633802a571fb99ffd3c5eda01250c78b78cf5e3fbc16d1eeae8fb4b96c8d5`  
		Last Modified: Fri, 24 Apr 2026 00:13:59 GMT  
		Size: 5.9 MB (5866740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c6cb09099b06bfa8ab9e534f3b82a2c7f2b02d136a83b235ab91080a2687f2`  
		Last Modified: Fri, 24 Apr 2026 00:13:59 GMT  
		Size: 9.6 KB (9590 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:36f18e7435c8e85db81159dd781fd9acc46c7d25cd458e24d81db02ed68eb4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146912920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45aa75b5fd1f5ca5b9ec238ec4e2f034d17e12876b36e6361780613a39804684`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:36 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:13:36 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Apr 2026 00:13:36 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30c043ca4f3bafe35e30bf64bac9a8549241cc9d04c32357557b39ac0e16c80`  
		Last Modified: Fri, 24 Apr 2026 00:13:56 GMT  
		Size: 82.1 MB (82114137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5ae6ef76d5b81354dfd3cd6cf1bb1711606385bbfb7ab00c02c9414b40e4071c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5668154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dd47113e0c94364bb9b4a5ecf3d30fe848e960303e885d17f474576d9e1447`

```dockerfile
```

-	Layers:
	-	`sha256:fac510edaa264bae7a3c38b346cc097ecca432e6f875ec8dd1be4553a2b984da`  
		Last Modified: Fri, 24 Apr 2026 00:13:53 GMT  
		Size: 5.7 MB (5658484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c2a59d1b12ad5f5737670a22207c94ad657046ca936b9c0bb9d1a4e460e8cc2`  
		Last Modified: Fri, 24 Apr 2026 00:13:53 GMT  
		Size: 9.7 KB (9670 bytes)  
		MIME: application/vnd.in-toto+json
