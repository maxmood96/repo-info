## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:4209799bdb0de1a3eaab963e8ce1110fcc2ad6ac3eaa98c933bb597ce12ea3e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:50d2842f2265535092400976a1b04863bbcecf4ea2f644b47d1ab9d18ba13c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150553031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2703830651cc14f9caa941440d94a6f95e4e24cc3ba23c952d25890e8017176f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:00:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:00:43 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:35 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:35 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:14:35 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5e0c2ef2594e62ec562f5df2ec3efec8dcb41bc052b756c68995456ef5a13ec6`  
		Last Modified: Thu, 02 Apr 2026 08:04:33 GMT  
		Size: 63.0 MB (62955301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd89fd9756f7e4a057f36fd94aa47265a178d244782a3e6d3ac1a438b458569e`  
		Last Modified: Fri, 03 Apr 2026 22:14:54 GMT  
		Size: 87.6 MB (87597730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ec1a74c9f0c3f9495e992b859fd494a2559a071b0ed663b254b5cf4fbc14437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7def73bbc12437650d0d6acd0da38c6d6ad820553fd3b7386d862c61aa4c9b`

```dockerfile
```

-	Layers:
	-	`sha256:96f8b9d15035700dd27d2db6398152733b3ef3bf85fd5979e333fbf4c8aaf1d3`  
		Last Modified: Fri, 03 Apr 2026 22:14:51 GMT  
		Size: 5.6 MB (5631856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66f9ed0600f3a8110d9ee0470abd5cf6cc04830c26a5d906d6da566b9214854e`  
		Last Modified: Fri, 03 Apr 2026 22:14:51 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8ed458e3debc5a8ddd21442262e7c55cff10aca95169064d9a1fcd2ed3d037fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144635935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b763a9a907153fbc007b1e03d6683994a1e08658da7082688c11e5e52b18b0eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:12 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:43 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:13:43 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 22:13:43 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2f277ffe2904df7c0598e4c64e34d0fbf604645e12c7f6d64d32c23097854f29`  
		Last Modified: Thu, 02 Apr 2026 08:04:39 GMT  
		Size: 64.8 MB (64802839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b444e1b73cf12712ba9d2af21e1179bcae12b8f6d7baf95cd15718c63247ff73`  
		Last Modified: Fri, 03 Apr 2026 22:14:01 GMT  
		Size: 79.8 MB (79833096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a8a09ccee046ffdec81b6f467248d2f472a1928e1ac0c28d8966e8f7a28683b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614a32233db4c4389c9ae2daafe93f0e600e6c09e0fd62af65b3a1db8e6ff462`

```dockerfile
```

-	Layers:
	-	`sha256:317349b017cfe5904c368911ec61c0df0197a5f397b60ee613ad035b1a5cbe82`  
		Last Modified: Fri, 03 Apr 2026 22:14:00 GMT  
		Size: 5.4 MB (5448132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8a3eee561cd7ca377fc8dcf5a60e8fc5508df49fc6cb1afe0f6f6e10463f63`  
		Last Modified: Fri, 03 Apr 2026 22:13:59 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
