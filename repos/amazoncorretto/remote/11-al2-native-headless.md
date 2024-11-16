## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:acaba24715203fb2403f4400a151749fdf0be96d5e05bf182a52ea7b379cca9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:011916335fdf35f12e6befc83772132f9fea3a68ce63fc770645508b34e1d61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217571760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe7a2ef866df410aedea415f4dd24f8cc545cd466f6b6f8a36b9880e67e1864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d4c94754ff4308d4d81a801e82c6a22c2f3c7988231fb781dbfa4f15f30330`  
		Last Modified: Sat, 16 Nov 2024 00:48:17 GMT  
		Size: 154.9 MB (154894321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4346f069701f67b3d15ebe9c23cc05d1c437402ebee290c8391f1607a88d341d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5688088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f357dc64ffe76d83e643a050f969b4d2f2ff08d0e8ff66e47b1ceb4f9c124101`

```dockerfile
```

-	Layers:
	-	`sha256:02323bd63f8726dd313ddd622593e372e7ab23915546a2ea7bafc6b7921dc267`  
		Last Modified: Sat, 16 Nov 2024 00:48:14 GMT  
		Size: 5.7 MB (5678758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8baee16f7708bbb872cf61fe6f9bf58c4146a3eb95dca01845c71dc96fa7540`  
		Last Modified: Sat, 16 Nov 2024 00:48:14 GMT  
		Size: 9.3 KB (9330 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:60cd8f5b6489536f5cc03a2af98772780472f813a4c22785a6e35e8c4e99ddd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da181c2cd2c20b856793a74fb7f68e30123698fbce69a90d8b46d6ecd577d799`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08ae8c0826952c26abec06247bbecef1770c71716ec0c4782e02e04f364e709`  
		Last Modified: Sat, 16 Nov 2024 00:56:07 GMT  
		Size: 147.2 MB (147225958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b53ed2c0453dfd5da4581e21e4987ea04f43230c40284c5b2bd2195c40ca44cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5506340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78f79a08ac91a075617dbfe441f3cffa40d024a2792fe10cc2148c9c10cb385`

```dockerfile
```

-	Layers:
	-	`sha256:a4409551b21109cb063a82caabc43655705b263eb593a1cfcc9c1d58454b82b8`  
		Last Modified: Sat, 16 Nov 2024 00:56:04 GMT  
		Size: 5.5 MB (5496929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39646f4a3de0086f059321f4e0bcd7b157faf9478e27631dadab0a07e5751e4b`  
		Last Modified: Sat, 16 Nov 2024 00:56:03 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
