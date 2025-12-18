## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:dbb8164b4e98cc6a4a48fabb13479d5e2dcc2d1366c70e101fc140af81f21d2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c61afa8480cd96facc80f7b67658892f1998df98faaf4cdfe34fea8c39ee5b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154221269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1b3287cf00cd92128d6698cdac35435bec2dd7db78b0a0d87e653b81f321f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:32 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:18:32 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:18:32 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a84d3899018127c0f4db767a5ccf8748a88fd6966c39cc6bed5ce3508071f8d`  
		Last Modified: Thu, 18 Dec 2025 01:19:09 GMT  
		Size: 91.3 MB (91280294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c5884927802db05d4e2165cb10caef6badf19f7c3682da16947d870d33353c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86d322a3d4e16209030821ea2d0d089c3b3d3adfe7dcf3c92c872a3964e7acb`

```dockerfile
```

-	Layers:
	-	`sha256:2ce46726c2b8ff25104101be72f3df9ea89a63f03447ae9470ebaa168628bf9a`  
		Last Modified: Thu, 18 Dec 2025 04:48:46 GMT  
		Size: 5.9 MB (5865824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a2ba29d33daaaaa31173290041aa49ebede2f4e1d292e6050547be9bc09fed`  
		Last Modified: Thu, 18 Dec 2025 04:48:47 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:17127eb51ec8fad81112cb203b6acb65679c43df9ebcb3861acf5efb6a7953d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146787188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c4263722360538db98e5cb2a5b54ed389a0c61d84c4cb3852ef2e2b18f9927`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:30 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:30 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:26:30 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea48fe487820379b35af7d7e47292eca4fdef92e37d197b6fd6352205b836fb`  
		Last Modified: Thu, 18 Dec 2025 01:27:00 GMT  
		Size: 82.0 MB (81991433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1f5822134b4e1bc7e4be079a88b4b973bf7d86cc53e124a982b7d60f9459526c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d20f3335615741906df101d71952e76cadb20fd06b94557f17a2937697eaf3`

```dockerfile
```

-	Layers:
	-	`sha256:7454ba44fb3ab8790c2c10d8f08afcad7767d3440537e15907dddbc0f62f16f3`  
		Last Modified: Thu, 18 Dec 2025 04:48:52 GMT  
		Size: 5.7 MB (5657567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43c9607eb5b7a33e45dd287b83cfa467c493d9ca0f0a0024737eccf51aa063e6`  
		Last Modified: Thu, 18 Dec 2025 04:48:53 GMT  
		Size: 9.5 KB (9509 bytes)  
		MIME: application/vnd.in-toto+json
