## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:73f73b2375e89a87b4be0180dffba047fd58e85fb1eff94af3fcf0d0969728ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e509fd42b637d158538cda6d07eff1cbd88f674e1cd33e1ce438c345075163ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.0 MB (224989668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa69971ebd584a4b797099176785dcccab5d55b96b337feb8f878855cbdefa85`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Thu, 15 May 2025 19:23:52 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404fa59dc7b28731b6c1fc34774e41fd28ff9cb064c3fe51e70127d18080badf`  
		Last Modified: Tue, 20 May 2025 07:01:11 GMT  
		Size: 162.2 MB (162229683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef1685215e3b97e6f0eb8005826c7dcb4629f6c252aebefb143a2a24fa8c46fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6000084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80dcde981aa492260cda7ad7d69092fb280647440cfaa7ef3ee6223074888bea`

```dockerfile
```

-	Layers:
	-	`sha256:b4f288554d1c3d90fc62363020a3562cd620eb37cce886f283264496eebf3b9c`  
		Last Modified: Tue, 20 May 2025 00:47:35 GMT  
		Size: 6.0 MB (5990644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9201a140f879677cd9a90039bd5d5e6b344dcbdcb2977ad897819770691280c`  
		Last Modified: Tue, 20 May 2025 00:47:35 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8bbbfaac8f9962d1842576fee3815f1ee2a95cc7ed672f7a3c33c2e88fbb2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216974096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9154525a3b3bd61d6f2d1eb6e69c6cb0ea45ba6d2fe13497f7f7cc497aec72f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Thu, 15 May 2025 19:24:15 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88ebcaf0723670a08084957365754e861b2ef98852d7113ea661695330b55de`  
		Last Modified: Mon, 19 May 2025 23:54:01 GMT  
		Size: 152.4 MB (152366615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd9f41f98076929b925d9d3dbe764a4ae0c1359a61223f776723ddc12503f09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcebfd410bae3e8a163a177ca8d1722f1d98a62eb4c6e3eec7253c28a35d0992`

```dockerfile
```

-	Layers:
	-	`sha256:0515bf2daf5a3f4a2d2fb8029b2bfe5532d7f262f5b3ad9449525903e089ac0d`  
		Last Modified: Tue, 20 May 2025 00:47:39 GMT  
		Size: 5.8 MB (5783358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa2a1f985736ce636cd4e663cbfeedf82d87be86e803b8ef107332550e030d4`  
		Last Modified: Tue, 20 May 2025 00:47:39 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
