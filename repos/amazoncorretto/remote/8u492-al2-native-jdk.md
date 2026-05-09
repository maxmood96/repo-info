## `amazoncorretto:8u492-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:fb47203d5d5e055d15dda9fdc306ef932176f28205fcbda20e6320cfacbc880e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eabf49365b87045f107a88887bf3b0d572aa477455a35c11764c8163d56ad594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188218391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd78a46489f0d576d394d6a8ebbdddbddc22e2f9ac13b6407d053d52c6023ec2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:56:20 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:56:20 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:17:25 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:17:25 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 09 May 2026 00:17:25 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:17:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:3f708fc5705625846e206621966842bfead7ee5b8e4fc20aab0c77c563600126`  
		Last Modified: Wed, 06 May 2026 07:46:46 GMT  
		Size: 62.9 MB (62859738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25237c0ecaa349def96a1c7811f488129a754703ae446ed4dd5749bf65226e5`  
		Last Modified: Sat, 09 May 2026 00:17:48 GMT  
		Size: 125.4 MB (125358653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44a475f04727423a423dbb2fd2b51d3e13d89c1f142f3e239c1d28868f39aee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7441749d3f295f08baa9037e0e2a38791bff8f98d423072bfb97102afb79b72`

```dockerfile
```

-	Layers:
	-	`sha256:15372061277723dfd91fe33ceee0fa833bc81147ef14a64ace6dd97d4e72ca3c`  
		Last Modified: Sat, 09 May 2026 00:17:46 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c5f69e82c38544fe8416d0fc4662d47e60f690eb104147e2cf37ad26ea56447`  
		Last Modified: Sat, 09 May 2026 00:17:46 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dada5a3b29bd7611b6f3ee36151896602f90818f2bf6f38a43257c3675bf5c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132506593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e046b3ac5df27f6b878bc1a8ac9eeeb468fca8fa6f87f9739b6514b076ce81e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:14 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:15:15 GMT
ARG version=1.8.0_492.b09-2
# Sat, 09 May 2026 00:15:15 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 09 May 2026 00:15:15 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:15:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:835dd3779a793c24eeba54a176badcbf0ecf82042603b5459dd57e14ad679d47`  
		Last Modified: Wed, 06 May 2026 07:46:52 GMT  
		Size: 64.8 MB (64808915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91116cb4d5322d3d2d5c171e4a0b141a5c676f0f426e0a948c8b85eb9a973d1`  
		Last Modified: Sat, 09 May 2026 00:15:31 GMT  
		Size: 67.7 MB (67697678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8495590f94706caf507db684570632f9d60ee4b23cf43005ba12700710be343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be0d69fefd9b3bbda7620401c75da47f12ff957e9e0deab82a442ebf941a847`

```dockerfile
```

-	Layers:
	-	`sha256:446ab91f2e98a83c0117ebe32389965ca2268aea0627a361d29cf708938c339d`  
		Last Modified: Sat, 09 May 2026 00:15:30 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857c9746a16ad31aa6ab0ab993275726cb2ef77cbc36dcd7047ed40d9f77f52b`  
		Last Modified: Sat, 09 May 2026 00:15:30 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
