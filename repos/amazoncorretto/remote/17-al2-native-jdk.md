## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:889b8d524bc68acd6ae218b205aef759b41e18e364ea23ddc593dd37a4e69795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3b3277dc6625de3feb6d7b7a6031ea3e131c90eee0ad4df72fa72e441f4cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228041139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6fc8f31c865e057876ab681c5212d39c9c2ddf56057bfd0fbac4f38415fd0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:39 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:39 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2ddc0aa2636ed19b988b4176374929a92f5862f6c6e88ea255d352140af781e6`  
		Last Modified: Fri, 17 Jan 2025 20:13:56 GMT  
		Size: 62.6 MB (62648554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834b52c04d035fce40333b90fddc2a78db69f42afe14058abf5a231fd43d0e6b`  
		Last Modified: Thu, 23 Jan 2025 23:08:40 GMT  
		Size: 165.4 MB (165392585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d531e5d8dc4053002cf78fab1903d281cc42068ea8dcc4c5df6f4cd5a42b8501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063bf213d01edae9e3f59b127effe2260687f2af2af22c9a6a7dd5d8f5fc3f1b`

```dockerfile
```

-	Layers:
	-	`sha256:0934bc8f900ba6b43ea19f91dc667948dd689f02ffb2ab226b7a0f5383244f3d`  
		Last Modified: Thu, 23 Jan 2025 23:08:36 GMT  
		Size: 6.0 MB (5955190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8cd64640c75cde4c3a85419dfa8b3ac31aa3655970730b45a344cc9a426f38`  
		Last Modified: Thu, 23 Jan 2025 23:08:35 GMT  
		Size: 10.0 KB (9957 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e26c6660d4232e30873aa7e61b9b9ab01ad46150a5040e7064afc57d871590a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220574242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df78a005823297140249fdc18c14956da7be4c66520f40ef97ac4aa0ad0ef16e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:43 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:dc3d403853487343f06bffefe21e65d842f88da2d7a1073ba2820fdb1b7ece72`  
		Last Modified: Fri, 17 Jan 2025 20:14:11 GMT  
		Size: 64.6 MB (64590432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0c76c5cddb4c3397cc0d2343f44e5cbc86b1ac22749d4e2fdf50d494f57ef0`  
		Last Modified: Thu, 23 Jan 2025 23:21:49 GMT  
		Size: 156.0 MB (155983810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6b7abe078be23596d69025e255d9ed2261cfc6d39876555dd5925a13bd274af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5757096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c01e58dea6c0ca3ce6c7e91817821a165d96b9990f96d3357156314931a2a19`

```dockerfile
```

-	Layers:
	-	`sha256:b20162588cf488c717ad66ce97554d5ea580c02a5942058721d77d41f65396b5`  
		Last Modified: Thu, 23 Jan 2025 23:21:45 GMT  
		Size: 5.7 MB (5747060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a889c29d34c431ee5eccc80f868b910f3bc2b167cf3ee54082f4a9c20b262859`  
		Last Modified: Thu, 23 Jan 2025 23:21:44 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.in-toto+json
