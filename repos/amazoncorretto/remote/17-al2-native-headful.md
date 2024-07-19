## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:bbb5e3b319c159f252d192a8e7d5b141aaca44aa956cb26d809abfcc82f4ac5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2d2c15dc4d1cc2ba2c591ed806e3246ded6edf24589f70522f902083c1813051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154061480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1963db2f2d362f9af73aa66a8516ff85bf8b3c72d3177f96225d9fd9d71a83f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d433206fc8c138c1429e55759439baf414f24f7a31c23ec9af1494609c81343`  
		Last Modified: Thu, 18 Jul 2024 21:49:34 GMT  
		Size: 91.4 MB (91413554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:35e7fe1eff1f34713e6347f1f4228f52338bff7f61a30fd5f6d6c3d4723928fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6886260229a49c9539099426e583808880277b4cc7c203077dbdbafd70371370`

```dockerfile
```

-	Layers:
	-	`sha256:9ed283a43c3393757c8cc977832a52ddd75d134a15dc10142bc1105016a2ef3b`  
		Last Modified: Thu, 18 Jul 2024 21:49:32 GMT  
		Size: 5.9 MB (5860059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d941115e187563c14d9c15daa3f24908027bc03817018341a3ee61c8bf4b86a`  
		Last Modified: Thu, 18 Jul 2024 21:49:32 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a41575aa4ad6b6be3ea92f17501b9bb8c64521e1351c9128cf72f31cf8424293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146779850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bd252c31c577d7eeb5a7fcef406104133b1a3054a504b799dc6cc51c2e9d8b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1411920c9cbcaed23d0e1ce2311288c8ba3ba769ab1879a1b3ec6328d2341f85`  
		Last Modified: Thu, 18 Jul 2024 22:57:07 GMT  
		Size: 82.2 MB (82204539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1f738f738d68e61f9e3e31c8e2f60c428c474113dd7d00f0478fa5a273ef25f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5660970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d28f34406eeb0a7d52a3b446eaa2af0aec0b28a92fce4af6b42eae7560ed578`

```dockerfile
```

-	Layers:
	-	`sha256:8784d933e8ad3de669fe566a77db09d14b881734a630459db3e6fbacb51f43ec`  
		Last Modified: Thu, 18 Jul 2024 22:57:06 GMT  
		Size: 5.7 MB (5651461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e63c805f8ac93171cc14c614677137f26897896e7831d1b071900cc482cab85`  
		Last Modified: Thu, 18 Jul 2024 22:57:05 GMT  
		Size: 9.5 KB (9509 bytes)  
		MIME: application/vnd.in-toto+json
