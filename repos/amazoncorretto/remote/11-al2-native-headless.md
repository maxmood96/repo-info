## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:7de38ca488818e81116812c0fc77fbbccf69b7648bd02c776b425fdc71246c95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e4e6eac4686fe83a131d0575f0da7078f473ab65b5b2d84fae39aa7cb7ce498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218017441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79ee52240f9a044e7175fc5b70a265b7b7517d4558b52966088918f1d16705f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f21a9c156d2ab29af4b5e451610a197ca56345598aa7ad950a22561b52bd146d`  
		Last Modified: Fri, 22 Aug 2025 17:34:29 GMT  
		Size: 63.0 MB (62978125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72aeed506f7ad581538b16771f238dadf6a5410c7566b77eec2c5509ad72bd80`  
		Last Modified: Mon, 25 Aug 2025 20:18:22 GMT  
		Size: 155.0 MB (155039316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c1f87d60a2499c52a54dc43d9a90b59f3d5b8729aae3b8076482105d4b8700f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7146d7b4024033580d79cf4f6e6c6d6b4d2da9cba1e754e1f89f640a91ced2`

```dockerfile
```

-	Layers:
	-	`sha256:f9b66929a07161f8596ac7319f668165c3ff78e824db6f6e49c1e8d7c78a43c4`  
		Last Modified: Mon, 25 Aug 2025 21:47:25 GMT  
		Size: 5.7 MB (5683301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:316a32765a4e78e45525cd5a93af0e551b90952746fb2b933df04b25015f2980`  
		Last Modified: Mon, 25 Aug 2025 21:47:26 GMT  
		Size: 9.3 KB (9330 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:62647035969b135d3980504d21a038f69f0294d7d82cdf7ac59d28f5f9a0e415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212140958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ba48e927714e420712a9b8e7116c3e1cfeb494090ecf746488b1143b5e9359`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=11.0.28.6-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a3bec375112fa06818025bf7b6ee4b903edf4e301e27d2464f104b8aabf964f3`  
		Last Modified: Fri, 22 Aug 2025 17:35:51 GMT  
		Size: 64.8 MB (64801350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e948141f26ee73d6bb234f9d90ee78b8fa8dd6efe52385e22d6b6d76dc20ca4e`  
		Last Modified: Mon, 25 Aug 2025 22:14:01 GMT  
		Size: 147.3 MB (147339608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f1ec5d547cf46c80d1c4379daa1c8bb64c8489aa39663838f8d197a565704666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727be63b5b7d70b91611f24f3c2e3ce747b3165761dc65783777cd0731faf6d6`

```dockerfile
```

-	Layers:
	-	`sha256:4596bd95b75a1feb48d58c92b3a4d089f7cfcd36979668741dbca427dda13b8c`  
		Last Modified: Tue, 26 Aug 2025 00:47:30 GMT  
		Size: 5.5 MB (5501769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb04b0309e9dd25f186ce1cc6e2c77bc049d7b01af81f8621385e2e8f89c809`  
		Last Modified: Tue, 26 Aug 2025 00:47:30 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
