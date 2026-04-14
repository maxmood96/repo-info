## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:dd5cbe6fbcbd6634e477600e55ef19e4d1dc1d4fee6027bdd2c7ffc80bc1b6de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:555c46fa993d04686d9a0ca266c2feed48def558384533d46d7e02b259962aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217294732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52710974cc5a4b1e836b16c36074576b88a67795297bf55cfb1a360ae89776e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:57 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:35 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 22:48:35 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 22:48:35 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c95082186a1ec9f46782dd4f3132a1e83cbb7cb233111aafcf507bbc1acf53`  
		Last Modified: Mon, 13 Apr 2026 22:48:57 GMT  
		Size: 154.3 MB (154339466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3519ee25846c427b884d46d0a5283309215e68ebe0de59b6d30919d3c9177d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6569794b1e64729fefb97c9bd3ee6da1343a87d0aafb031669ad4b1d31c007c0`

```dockerfile
```

-	Layers:
	-	`sha256:1020ba44246bc8cdaca6f8cfbc6914d4a4558aba03bbdf23d7ce53e659a95a1f`  
		Last Modified: Mon, 13 Apr 2026 22:48:53 GMT  
		Size: 5.7 MB (5683402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beb19b0dd763a9cf46f9f5fb332046345e9187e1bd15647ff25c18d7ede1b2ff`  
		Last Modified: Mon, 13 Apr 2026 22:48:53 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3abc517b14b4f4f8064141e8ac172d730badf7341080338e4b35408e1bdb1843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211406455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3354d833fbaf07a629955939f7d3dd0cf5e8d423f70e903f87091da7951f2870`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:22:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:22:09 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:10:43 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 23:10:43 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 23:10:43 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:10:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890f38542dc5391f12c4f9da65e67271b5e4f6f03c6719d3937caa591ddb207a`  
		Last Modified: Mon, 13 Apr 2026 23:11:04 GMT  
		Size: 146.6 MB (146603480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b897172c2b0d9a681bb777e0655ddaef6ac7ff9132020c591763fc3e551b7691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8a1fd66969081d55050ec485147816e15c192485c6c3846abc6270833d51ef`

```dockerfile
```

-	Layers:
	-	`sha256:616046c36e0b176a47dd6f79b87e00d44d20b71352f950f0363b7138b9ff83a3`  
		Last Modified: Mon, 13 Apr 2026 23:11:00 GMT  
		Size: 5.5 MB (5501870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee6665a4b57c5f5c8101b4dbee3eae360f999528dd1ec53c236211073d27fa2f`  
		Last Modified: Mon, 13 Apr 2026 23:11:00 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.in-toto+json
