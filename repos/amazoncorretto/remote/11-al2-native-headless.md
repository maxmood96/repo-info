## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:297c9bd4dbf770b6cefc14b11c95ef355371da8bd1c0b4fd6c67d8b543b5c910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:54571eaca24daa5445c6a7da40677751b597d802f262e2a4281c7d5487f728ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217551159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf800fe1975bdaa87b762023f5b6b9176db0099c58701823b2304b46fb1c781`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2eaf13f87a267bfe94d24626ba68967d829ad848f1fc18909743592d089657`  
		Last Modified: Tue, 24 Sep 2024 01:57:03 GMT  
		Size: 154.9 MB (154872625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:189f67d15731e024526adae6663addd8d4e3ecfb20cdb96b1533f318a0f7a516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc835367b9a5d050cbfaad362adb4c9389d800e0f6db7045ecc29cc4b5af9208`

```dockerfile
```

-	Layers:
	-	`sha256:49ece0d86e18f687d456df988c8f369c96be33a31e43faa3dfeac130dc96c2bd`  
		Last Modified: Tue, 24 Sep 2024 01:56:58 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ab591f31ff8db3602de0a9373e3a025ba90c7a5f1f9bbf1feaa99a714acc726c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211776572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c4a73dcf6124af432934c077b9a636f086ada4825246c5a6d9b495170a4d20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6ecc46824e918850a8a13ecba98d65fb2c5d7aad2c974b13131b691414286`  
		Last Modified: Tue, 24 Sep 2024 02:33:58 GMT  
		Size: 147.2 MB (147190025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e129a2890ccab9ea4851d59797bb2d0ebf3f5ca9444af1f1a29fa7ab2ed2232e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5506585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ce85de0c5ff254cb88f31a94f7c0df4184b8514f36a13ccdec390a90535a08`

```dockerfile
```

-	Layers:
	-	`sha256:c94ddf3422856b8c81e5c4d40535eaa25af7a29b086c54d0c4acfe1f245827c3`  
		Last Modified: Tue, 24 Sep 2024 02:33:53 GMT  
		Size: 5.5 MB (5496929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d242a4ae13d11b3530223396422af2b0c4d23ac50bb8dd03bdf8f307bbaa098`  
		Last Modified: Tue, 24 Sep 2024 02:33:52 GMT  
		Size: 9.7 KB (9656 bytes)  
		MIME: application/vnd.in-toto+json
