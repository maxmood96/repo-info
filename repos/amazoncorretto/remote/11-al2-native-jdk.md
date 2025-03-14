## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:48979063cdab3a2ccb8dffececf788563c7b1624d78aa7e40ea283bfc2175ce6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:76fae5ddd18e80a520247ab9fce67494b86c4928d265e8b51b36ab5623f4c2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224980493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eac6c07bed22f8740789daaeaad5469c11882be9689dbfcc4e437d29bfe2cad`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed40236ffac03e8c6f8c4495c0e676717b98623c1fdcc37668167fca722ce368`  
		Last Modified: Thu, 13 Mar 2025 22:53:28 GMT  
		Size: 162.2 MB (162207655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b8506c4a71761b3143c2599859f83017787f7726ce2bdb463a631e24e94daca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9735e26b57a51f9d9cff56e42fb81f474c5da7ede9dab8521b1d5d08086806`

```dockerfile
```

-	Layers:
	-	`sha256:88c2f9bb038741e4299ea09acc6b6d1026617cce884e4aace539e0043d36072f`  
		Last Modified: Thu, 13 Mar 2025 22:53:25 GMT  
		Size: 6.0 MB (5978820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a6019a6f06338ceb54e8d0b493efac722cdd2ff91fed7c3b6161b05ac5d0453`  
		Last Modified: Thu, 13 Mar 2025 22:53:24 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1a0d2560dcb2f2f913743fc5e1f8115d47d1d7d513f8c052573fff7135922157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216807121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a474a650c65cc045b5dc6b494f6bfb54e688eae4633b9b45f91190552fbdf6b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed5a64108dbb4e8d23f51f4f5e0cde9dc36a1ebd1fc6e1311f5abd39a17189f`  
		Last Modified: Thu, 27 Feb 2025 21:14:58 GMT  
		Size: 152.3 MB (152285913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:66262b2fa84e814291f9ca6082e0cb8f8c265261921a39ba12ecc19c1011a959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5df4f50c72ff0e52c331214274e1b8bf8dea70ba5dc0c6b659b57f6648b7a37`

```dockerfile
```

-	Layers:
	-	`sha256:b5acf2d08e2e7d7e2d293eebfffb0740f982ba2c075389a958528a219afbd9bc`  
		Last Modified: Thu, 27 Feb 2025 21:14:54 GMT  
		Size: 5.8 MB (5771534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9692a97d13411516e75e447ebf6ba2236a34dbadfd5a5d5233ea34c7916761`  
		Last Modified: Thu, 27 Feb 2025 21:14:54 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
