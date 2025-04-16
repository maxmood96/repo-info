## `amazoncorretto:11-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:ea97bcea6dfba7b1e5ba2df4892cbc5376670458377a7c0c0798f897cfc8d404
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c9c112691dac13988a29c718cdb170d35678dc5aa121dffaf767fe4e623772ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.0 MB (211042428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91965d8be303cb9b06ea81e2d389b23e5da8f9e057564c8acaefad86e16265c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe545608f09f13a373878770c982b3170240cf89fec38751899698424970c47`  
		Last Modified: Tue, 15 Apr 2025 23:55:54 GMT  
		Size: 148.3 MB (148289539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e5378777877907817df537ae2c9f91fa7c6cc6389ed8babf7c3de4cb5a7cf6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe6a1dd703a54f47abd2feaa71d6d35c190024578417a04b04384279eb81297`

```dockerfile
```

-	Layers:
	-	`sha256:ed8efc4d937fe5d153c3a5eedded110de896a26fa34a2f1012b4be84afe27885`  
		Last Modified: Tue, 15 Apr 2025 23:55:50 GMT  
		Size: 5.5 MB (5524439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4daedd906dd002aae3bc4c16608f47cbcdb0c8ae290bf54ca4fb3c044a1d40`  
		Last Modified: Tue, 15 Apr 2025 23:55:50 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bbcaa7eeaef553bee34322a2e439ff7be418bf8cc547b8fb12040ba02d1439a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209892082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0febf4c7fe8740b2fdc1a689c32ef0f41b0fb943a6c03f231bf1a7808874d25f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ccb924d5aea1ecd0b7aa6ee9015b77d1eda6fbff9ebbc620dd2766d808ea14`  
		Last Modified: Wed, 16 Apr 2025 00:01:17 GMT  
		Size: 145.3 MB (145326260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7c99ac66989cbf4a3aa121079172f668b99e3e518126ba743f85be7e5a491e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ce5a89f63b792309a8e0f610c7f107036375be9c6fe1a0313218d2c64c7322`

```dockerfile
```

-	Layers:
	-	`sha256:3108a2cf731b2184959ee7209b17ff65b7d26772dfaf2829f76d317e4797c88b`  
		Last Modified: Wed, 16 Apr 2025 00:01:14 GMT  
		Size: 5.5 MB (5523933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a49d36d452a67dee2243ea6daf15c7c79fe32b5a61cdef52741ac6032a953f6`  
		Last Modified: Wed, 16 Apr 2025 00:01:13 GMT  
		Size: 11.4 KB (11406 bytes)  
		MIME: application/vnd.in-toto+json
