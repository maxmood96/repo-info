## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:57414ee69c0b852661946f3d14e0bb9289b5bec8d1bc6447e0ed43fc53971de0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6be2c3df2992fdbead969ceb47868b507b01d405aefcc7c97a097715114e434e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154248900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2109bf968f3cf05cef223688068dfcbc98610084ef3d2481dcd7720ff4a32d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6923f12e68f5f5a04356391ba9fab022af9224f764b90c89e6d6d26ea5477337`  
		Last Modified: Fri, 12 Sep 2025 01:10:23 GMT  
		Size: 91.3 MB (91265612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1574aa0cf102e7822dace794aa60cc65bb25df70776d2b39c602f1df2430a1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5875285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3ecd4c9e548ed256553c5e065382a1672a20d6b6822cc2791c8b413cc74032`

```dockerfile
```

-	Layers:
	-	`sha256:fefebc386760029286c9bc57b06d78db6db07d698e17a2a6805b45ebb119fc77`  
		Last Modified: Fri, 12 Sep 2025 03:48:48 GMT  
		Size: 5.9 MB (5865814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58fd3ee305a18d7f59988fa0b718434916d7e36f370dfd86c2548dcd7d33845e`  
		Last Modified: Fri, 12 Sep 2025 03:48:48 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:37a0acf4ccd77130d99831b758166c60f48ffdd41e4d1f13dadca6e6259df33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146729256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c6219e4279df51f492cfc84a4b3e6f7248d8b9c5c9f54e4feb8a8207767492`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d07f287108e893f5ae3220762de4e391060546d85524749f491903c5829aa41`  
		Last Modified: Fri, 12 Sep 2025 01:12:31 GMT  
		Size: 81.9 MB (81937533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f05085dc2ed319dfefc7705373cf89fcf1945b781b22cb460852b4d60a4b3224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5667107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0dcfb206a9ea6fd4a618ee35e3018baba6b9591634875aeb49cffefaa09cc86`

```dockerfile
```

-	Layers:
	-	`sha256:bd9cfddfa8526b3173858c630bac90ebf20381756d3228efd78fca2a584534b8`  
		Last Modified: Fri, 12 Sep 2025 03:48:53 GMT  
		Size: 5.7 MB (5657557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75e2ab18cf7ab3a692a7b893c106415a40b201def833c7d66561b4b0361c027`  
		Last Modified: Fri, 12 Sep 2025 03:48:54 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json
