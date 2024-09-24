## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:b712d81616055eaf07f0b550c5c0d1a40dd513bf274601bfb8a95f746506e417
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:24bcfd34ce173329193de10541130773cc0ac7f141601eefa4800e883fb74d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150470784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c5f7dc8551caffac3259ae97d58f22eb0d49a5dbde0f5a233f325e7aaebbd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a2b3401fcd5c8e948a9cae5fc788a34c87caa686b6c3b1d652b79e90f2fac`  
		Last Modified: Tue, 24 Sep 2024 01:56:50 GMT  
		Size: 87.8 MB (87792250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:401b43b272fb0d082f01a15304a8d0838342e907fcd173705a5552cbf169901f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c622c0908ac208809ac2c1a744c0447d17d7b70fa9ed1f44dbe9618dcdac3db3`

```dockerfile
```

-	Layers:
	-	`sha256:4b3cfa95c58fbcb4798fb93d2489de669dd8853cb5805d2067ac893453e53ed8`  
		Last Modified: Tue, 24 Sep 2024 01:56:49 GMT  
		Size: 9.1 KB (9083 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e44961517edb5b1a38d171e02a40033e817b9bfd41cef1ca55dafb394adcebee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144662452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0173294391446f503d6b5810e678493e8adeefad8b6e75065aab3faba8cd192b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bf50bc2aa5d59e6c68304bfb76801051ba1895ed48faec4dfae117fcae421b`  
		Last Modified: Tue, 24 Sep 2024 02:39:36 GMT  
		Size: 80.1 MB (80075905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8e6ef1118af9401ef37c3a929c1b11c3d5fdacda329694231e52a8058db0bbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab0569cdd5b2a5df184b985ab62a44c699d20b48fd4b08c58b1f1188a3ea7d4`

```dockerfile
```

-	Layers:
	-	`sha256:0903b325fa2e72afb9493e2e556fd05962add6e7bbdcac1230ac80a4baebaf1f`  
		Last Modified: Tue, 24 Sep 2024 02:39:33 GMT  
		Size: 5.4 MB (5442053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0e8c9fdc836fea880d2bb71a01e0c16d84d92c40fcdb6bb9c6093c4f0df2ce`  
		Last Modified: Tue, 24 Sep 2024 02:39:33 GMT  
		Size: 9.7 KB (9662 bytes)  
		MIME: application/vnd.in-toto+json
