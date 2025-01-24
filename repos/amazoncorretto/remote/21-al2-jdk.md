## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:a5171cfd8b79b985d521ea214c6a58d5c2e543bb8eccb0226bd440c6b6138c77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7e5f3f08110422abf9267fe1bf606f7d526e5420d779a77f318b89ca7233e28c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227381332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23955b090212047193b33920e646f0c512b4627541c8932f1f22f911d6866d8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:24 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f4f4804f0ba33928a2a9292016fccac18bd4ad4e1909ab89da3073c65759b`  
		Last Modified: Thu, 23 Jan 2025 18:27:33 GMT  
		Size: 164.7 MB (164745502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:334f95d3d388e258be8b9c870fd9adb8b874d01dda45cee55d6bf33259bce63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6523522315fbce18774738ec9f657202535b7057e0c5fb1ccc79f2b865f2335`

```dockerfile
```

-	Layers:
	-	`sha256:bcfc078df5092ebf036dc6b1513c3005fe88cea7f9cf0dc891ba4a2b85666806`  
		Last Modified: Thu, 23 Jan 2025 18:27:31 GMT  
		Size: 5.5 MB (5516997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cd46cbedb8a2fb6d97bb0120c7bbff022c74125f36a1e998c80da3f2c74857`  
		Last Modified: Thu, 23 Jan 2025 18:27:31 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:185876a48ca652b810db7f5ed041f90beab05566b0423094a1b6a6a5bc0246f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227469631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080731d354a73babccdf98c9792e7af6bf1e0bfcaaee624ecd3b7697771b1aaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfe734ed07854436c37e567b57bc647f777cba775ae3377bec6f255cc7fb706`  
		Last Modified: Thu, 23 Jan 2025 18:49:48 GMT  
		Size: 162.9 MB (162879326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd38e64adcc434e6d2aa738f9860b35ffe2d2c40b19e19a9b4d160465583002e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6f06f08f75e7a93bb296be345a39675186ea72dd12dcbcc0352de0011eafab`

```dockerfile
```

-	Layers:
	-	`sha256:2d968e8b97b5076aba5aee65605c606502d64cec10e972945856ae62f02160ee`  
		Last Modified: Thu, 23 Jan 2025 18:49:43 GMT  
		Size: 5.5 MB (5515686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2e61cddc63b0fe4a088bdfd7be8603e8443254a19d431bfd9ba5efd993fd2e`  
		Last Modified: Thu, 23 Jan 2025 18:49:43 GMT  
		Size: 11.4 KB (11399 bytes)  
		MIME: application/vnd.in-toto+json
