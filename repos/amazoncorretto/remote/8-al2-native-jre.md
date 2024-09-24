## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:a5a9c05519bb6d6548d894a5ed7336b2010279efb13089f6a3cc6cb23a1abf49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bdf05e38bffec3e903309e647fd4d69095462d07da97e342ab388186a4e70d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171781237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bc86afc19c8a6d5c23403b852af64c32c0992d9b1ddbcb64051b15f2c663b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e2c58384fe14ec994694cb5b302e97431919d48f3f67bb19233281569fa17b`  
		Last Modified: Tue, 24 Sep 2024 01:56:56 GMT  
		Size: 109.1 MB (109102703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:94642a3a241705158cf48fca5eda5d70fbf71a9aa357532687f11b452120695f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20335864fcecaa3d35081f764ab1407ec2a04325902228b8a65f87c6ef67f0c`

```dockerfile
```

-	Layers:
	-	`sha256:76c6927a4986b3ce808dd21216eb66af54737221c4376b3f2e7b976247381abf`  
		Last Modified: Tue, 24 Sep 2024 01:56:53 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5e5b87dc5a98dc85ed81af5b055614d669644a6e10e7d22ebc4ad6d64ad72415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f959422074b32a5c8ea61c98e912d10c6ab78d99d6f1edf5041bb2d6d7d18`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=1.8.0_422.b05-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acee8d181418cbe84434ca1b7928e3202e0c8ff13e5fe6d7d06137c35f3efcde`  
		Last Modified: Tue, 24 Sep 2024 02:28:03 GMT  
		Size: 52.9 MB (52935818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0eb62a91580066e4e128c4ac7138324ac4e3278677e93a78abd71851e7cc3d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74796a5e4a0ebff9cdbded9204cdd4503139c693eb37b94aad1b0a3f98ca49b`

```dockerfile
```

-	Layers:
	-	`sha256:6f758b9d1878e6bc3055b1027d17919383204ffc082effc77ebe74d8b362f53d`  
		Last Modified: Tue, 24 Sep 2024 02:28:02 GMT  
		Size: 5.6 MB (5613432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e56d45d6cd7e026e371a80bc861e8474aa1a67839b20ff8b531c11f8a2e4f4`  
		Last Modified: Tue, 24 Sep 2024 02:28:02 GMT  
		Size: 9.9 KB (9874 bytes)  
		MIME: application/vnd.in-toto+json
