## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:f3ae165414843dacf4db28adcc7bb9bac08e27409cc99fe18a3b86dbab1ee802
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b843a0c7041f4bda00574aa4ead77d2b3379c38b76bd1bbdd3533930a9413805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150556408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583250dfb430265c0c4d220ee08d723aeda30f21caa93e93fccb35b6f3bdd92c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:28 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:28 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 19:00:28 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6f657cdee96f04a9acf8909a4e096ae3311a9dfcd7a3f3621b334c0ba16403`  
		Last Modified: Wed, 21 Jan 2026 19:00:46 GMT  
		Size: 87.6 MB (87616252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:339a5d6cb58dd0eb3fab89ccab13d4fc64d9b57d262e871a6cea079f4c10ad59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c37e02695e89210317a84b1262953909322cc86034e1c547ea06ed0b0db06bd`

```dockerfile
```

-	Layers:
	-	`sha256:23c07ab9eb543530455b89d3c4964a85617cc5a8209c94e26d48e94eb18114c8`  
		Last Modified: Wed, 21 Jan 2026 19:00:45 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031d49e92414f37e7f3cd80af5542e2d7e529ac97c8238d15b6429d40b971844`  
		Last Modified: Wed, 21 Jan 2026 19:49:44 GMT  
		Size: 9.3 KB (9293 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0e659036aadc7b3fd94383ac1f6b4b07085e1a8c74efb1787c2adbbba8cdae07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144612062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c072d361b09368d5f646b901774cbd4e930470fa7db798f65e9497ac27988d76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:41 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:41 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 21 Jan 2026 19:00:41 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf9b158c033573be250213b8a181506daff7831a839c1a7055e9d3c966c768`  
		Last Modified: Wed, 21 Jan 2026 19:01:29 GMT  
		Size: 79.8 MB (79841628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:16bdb6d2df46ea2821f55b1cc6fae7dd605f0de29a11cafc150b36108c7ace09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebbaec43612cc01cf820525302a434a70e107b0f361f6b69bc9269cba656ecc`

```dockerfile
```

-	Layers:
	-	`sha256:67fd06dfd2f7abc3cadaadbeb8b26e322a118ea2833855f09479bdf0d702a14a`  
		Last Modified: Wed, 21 Jan 2026 19:49:48 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57dc213d6c29978dcb37411642c7122cb4d4877d2fcc5acfdc7f88988db5c7d5`  
		Last Modified: Wed, 21 Jan 2026 19:49:51 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json
