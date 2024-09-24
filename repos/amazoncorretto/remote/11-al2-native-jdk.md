## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:9d101bdbead406c129833643ebc2d2543352e49dadb51bb1a907229778d0e119
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1771c2c7a87a4279631b01c616bce4ad1fdeb029c63cfa2cbc14e869929e567c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224811433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a09c171f08960a0ae098a4a191c425f2b32e7ffb8ea2da0174514ad45442c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:19 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:19 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:69e49d0477d7418fa8148e4dd5ab6e7b541cf2bdf558ddd0198722553d8ecfb8`  
		Last Modified: Thu, 19 Sep 2024 19:08:50 GMT  
		Size: 62.7 MB (62678534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81099e9d2b9669acb4763c6b1c56d8e33260c82a8a9ef6ed2bab1912aeaa799c`  
		Last Modified: Tue, 24 Sep 2024 01:57:02 GMT  
		Size: 162.1 MB (162132899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8ddd3353e3e4ba2b615131510c650d95d401e2feb3e2468957d5e768f665634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cab6d8a3133b6c01b95b450b88c9075191171c648404c5a76bf0cdd131db0c`

```dockerfile
```

-	Layers:
	-	`sha256:90d5f85ba0df1c510bad4334018b11ce9c3e555acc30868cd6255feda95b9de9`  
		Last Modified: Tue, 24 Sep 2024 01:57:00 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c1b6c5a240c36b88c7d6d6a84fce3f158a62324ada5a049bc83d26fd7395d718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216869265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efefba5750a5a86c29e3c27cdac59f9c8f88b29a53d7ebcadfeaf6b5704dd9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 17:24:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 17:24:23 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f8111d5d1a15a517300f742a82fff488242d02ac685b3d2f019de97e880b603`  
		Last Modified: Thu, 19 Sep 2024 19:09:03 GMT  
		Size: 64.6 MB (64586547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e14c68da975d29500d18e8139f7fc30310a3326c76afeb5b3a6631e208fea4e`  
		Last Modified: Tue, 24 Sep 2024 02:35:06 GMT  
		Size: 152.3 MB (152282718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c167f65cc4267eb41b2a8e5b11a2941ee4b840d15cd468714979466ea60266e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbd468ef873783bad224379f4f0d0bfcc9e4b9117c119cfd4a606451bbc9da5`

```dockerfile
```

-	Layers:
	-	`sha256:0fc808759f13dc06522bf12871d50e3ffcbd190aed7b3798d8e56d4921d6bba6`  
		Last Modified: Tue, 24 Sep 2024 02:35:03 GMT  
		Size: 5.8 MB (5782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a317f992f38ae90d17721ad331c46272af38dd0d0ceb889895b3c76f544e2830`  
		Last Modified: Tue, 24 Sep 2024 02:35:03 GMT  
		Size: 9.8 KB (9766 bytes)  
		MIME: application/vnd.in-toto+json
