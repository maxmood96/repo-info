## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:55c817d4fd893ffd6732b78d68c7146391bde80c8cc78ebb6055bc63f65f0ec0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fdf66673bfa5b9539a948bc5ac277ca78f5132a986e92f727f56aaa8c80a2a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228483144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d3da50ed64934720776f206100ca46cac1ad1de8d3135a781abf008e21587a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e141968a6df4e40ff9a246120dba6a9e279f250efe865ccdb1e999bcb2a4d89`  
		Last Modified: Thu, 25 Jul 2024 21:02:23 GMT  
		Size: 165.8 MB (165803978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6bff1bae1e0037f98a916a445fa484817ef95821e0765aeaf900f9b4dd4a8080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f110fef0fbc7c601208b3f6a6ce08485f76bf77cfecedd25fe28766874e5d546`

```dockerfile
```

-	Layers:
	-	`sha256:28042736744a0795e79244dd2f34876d153aed964aa168b6fffa08b335999e9c`  
		Last Modified: Thu, 25 Jul 2024 21:02:20 GMT  
		Size: 5.5 MB (5527650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaf543ca0aeeedb5892a1b6a0e9917b92a2fd8e5343760ccd81c35b3bb7b083c`  
		Last Modified: Thu, 25 Jul 2024 21:02:20 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:621cc16ef07e654c25ca38246f377a511cf7d1042e7eb363b6b3c4ab83c8c7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228401651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f428b4d515e8e61a74910e0be51ae90a1f9378efd255252520e57b7db9a2cd10`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1609bd2184809b739da413e633f5601c72bc3556d78906f97f51ea40ece2c5`  
		Last Modified: Thu, 18 Jul 2024 22:59:14 GMT  
		Size: 163.8 MB (163826340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:89ad1e22d5449f63c9524374dafc519c67c3e077eb5e57a985af1eaa59bb064c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3809e9f3b780ada370e9775240e8b536caf5afbfd67b3c2cb07b4a7d40ac0ed2`

```dockerfile
```

-	Layers:
	-	`sha256:86f0c0d87a6a40892f5e43f792ae7b7a61b091edf4d48937f726ea5d9275708c`  
		Last Modified: Thu, 18 Jul 2024 22:59:11 GMT  
		Size: 5.5 MB (5526337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6adc780e35803835131488059336963df3cea32081ebdd314eda1e6144be670`  
		Last Modified: Thu, 18 Jul 2024 22:59:10 GMT  
		Size: 11.4 KB (11359 bytes)  
		MIME: application/vnd.in-toto+json
