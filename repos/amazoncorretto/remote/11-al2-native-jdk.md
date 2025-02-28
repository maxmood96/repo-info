## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:3a0ad8f1bb80bf0e53e696b75b6a558ef8542fd58749ab110bdb0f86e98bd5de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f8a17d531f4a3e84c8a3ec7ba79b1f3c162564f498148872bc7136792bf3c130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (225029392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586b1f9e17e647989d4b3bcb74c56aea5918660d4dca56b36eae68a703902be`
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
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5779e199522d2a95edae9f9d6dc336162a143f4fe1c85f11616b696eb1d998a6`  
		Last Modified: Thu, 27 Feb 2025 21:08:37 GMT  
		Size: 162.2 MB (162227350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28cabacf9db7adce0e1ea9ab3d4d67c5b49b640e3f56f2b5fb817d13d7e95a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de30d928e644b2c45b7ab055106138e52aedc2a36d83d5981032913ea41708c1`

```dockerfile
```

-	Layers:
	-	`sha256:abf45fef5645f52150ae510f856aefe649461b2cf217c3d47d854a167e6a1f52`  
		Last Modified: Thu, 27 Feb 2025 21:08:35 GMT  
		Size: 6.0 MB (5978820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc136a3ad29440ecb703459e76d5161cd68ed178e3c27d53ac2b888d1b58071`  
		Last Modified: Thu, 27 Feb 2025 21:08:35 GMT  
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
