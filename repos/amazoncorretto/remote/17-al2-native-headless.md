## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:a87aa99abdcd733e2177ece7c2dc2b9af5103865f574880a9182ecb3dec1f9c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cc0bb1b1df123ab1d7b86e976101d6a92bcf7653f3de8dcb32a3c729fbfbb8d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150561477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0944f777f773c96fc09be3b2b0b52bcf7107e700f9ce92620c1af482a2492639`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:08:44 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:08:44 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:08:44 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:08:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433bcd32a107e697c52c15a150b495771240a2d342d58d0689941f6706332787`  
		Last Modified: Fri, 03 Apr 2026 17:09:02 GMT  
		Size: 87.6 MB (87604967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:92aeca785cad3d23f5dec986fe72fb00b9b0bda705236babe82f32e335bad6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db13fceae2d656d16ac3ce3c7a52fabb34d1dbd08026004366533dd0a04eb64`

```dockerfile
```

-	Layers:
	-	`sha256:afccb916b62a0aadf0c8de2f1d3f91b8ae3bd82250d3f35cbfefb55ba13739ba`  
		Last Modified: Fri, 03 Apr 2026 17:09:00 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3e221d0e95faca0a5421c92341478203f864b359c8088653a48038ba9833408`  
		Last Modified: Fri, 03 Apr 2026 17:09:00 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3ee2aef8bef528a079a4ea1b53c44d9b6eb1c6783694c1547273f04f3ac62629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144635946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e903da2388d21f896931f7024e09a607f31e0d08fb094cbc06196cccf3a9c704`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:16:05 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:16:05 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:16:05 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:16:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425801707fdecbc3459546dbf12e7ec30b598c28acf021f86c044843a8e957eb`  
		Last Modified: Fri, 03 Apr 2026 17:16:22 GMT  
		Size: 79.8 MB (79832797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd2aff540e5413e551031a306649a775a58fb46a19698df7ba165aa9b16753e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2ddb8f3e5c25b161dab3cdfb2e57d15048f76fb8bb3f30d68328fe42c6bffb`

```dockerfile
```

-	Layers:
	-	`sha256:3cfb8cc85e3180924e34c078e6b66c0c5479771077f04e87d28667a118f36b52`  
		Last Modified: Fri, 03 Apr 2026 17:16:20 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1cc6e821b60f24ebc3db230779211751c765fb20a93ca3308e75f27fc9f29af`  
		Last Modified: Fri, 03 Apr 2026 17:16:19 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
