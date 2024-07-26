## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:28d261748f6a7fb2a74f3af0f7ba725504c4eeea8065b6e92cc26d5ab1fa6e4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7dad09d4a0ae7bb993728d4f61a9e128e03fb9b1dddf34b3b8a2eca8c3e70692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214926805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f956a2e5784aade095b7ef04fa76592e9f3635957eefd61b82dc988be74b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16d1356ff865ed2ae4a8317d0fc95d8da710d367d04ec8a934e449d8ff736a1`  
		Last Modified: Thu, 25 Jul 2024 21:02:15 GMT  
		Size: 152.2 MB (152247639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:89910eb62d56f5fb7d142499ee2bc2ed3b0afc6ad97f328a5a8cf8fec106ce05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef9687d9af85339ed1e153f4ccfb51f8e01dca9792c0c73c30cb83d86343f61`

```dockerfile
```

-	Layers:
	-	`sha256:5cd84c8842b122bce4a1680e30fab57be7b36246aa6a8f043518f826aea85dec`  
		Last Modified: Thu, 25 Jul 2024 21:02:12 GMT  
		Size: 5.5 MB (5526938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a7d06af902b9998d9671ee415af8ea111b4eb627701696dbfd4f64283347f2`  
		Last Modified: Thu, 25 Jul 2024 21:02:12 GMT  
		Size: 11.2 KB (11218 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:78829d7ce0df487158dbdfaba50caa0494c3dcb3a7f38a9c14ae4dafd94f1c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215441843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0d17a5dd5ede45b0c050a01f54d90d759a94d883ff3d7720fc188c4e6313d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7670e0f13dba13cacf8a72508b2840f1c1d5b318edb811accb584aab4d61a118`  
		Last Modified: Thu, 18 Jul 2024 22:55:17 GMT  
		Size: 150.9 MB (150866532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:589bc0c33fe26ebac359a44136bb364b3fde9bb030327aeb6a67a38e4214653f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b922df30415df794d2e8e8bc576bdeb51ffa5d1f374792a64a98d079f87316`

```dockerfile
```

-	Layers:
	-	`sha256:590027cf6c50382cd442fd2fce7b4ac2a48ed7aaa7f040c5e35b650edd50db19`  
		Last Modified: Thu, 18 Jul 2024 22:55:14 GMT  
		Size: 5.5 MB (5525625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3f7ff7d75762da91b75e8b9c3255450a7ccfa3402c69ed673c182e47fdeff9`  
		Last Modified: Thu, 18 Jul 2024 22:55:14 GMT  
		Size: 11.4 KB (11366 bytes)  
		MIME: application/vnd.in-toto+json
