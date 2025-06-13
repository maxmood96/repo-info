## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:722267dea6e71f73a2897c3cb1936e713764471874e5b2de7660c96b9998a225
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:09a94429527e9206fb57804b6911052eb2334729b3c34c685e13a096c1cd7ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227817491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84050a6778306c4eab0e75783e72d15c923e0e0f6ed4a6e110abeec33b52e376`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:c93eb42fc1cb8cbc6518e0c84a8b5166a23b8e065c2ea156492279ccf234ec25`  
		Last Modified: Fri, 13 Jun 2025 16:58:44 GMT  
		Size: 63.0 MB (62962939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f9e34af8ecbd84622c0fbc24a367b13e7e66d52134ec026aeb549f49fd8dbc`  
		Last Modified: Fri, 13 Jun 2025 17:15:21 GMT  
		Size: 164.9 MB (164854552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a1871899df3ba00c24ed993cce9d1012603ae85a6db4a3abb5f0abd7c7963d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5543612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ef5647b5f79ff41791332bf9015bbd148214730057af6239e83a178602d3fc`

```dockerfile
```

-	Layers:
	-	`sha256:dd376548f9d07df0b8e24d1fc09242cce6437e07adb3efb81011e555bcafb4ec`  
		Last Modified: Fri, 13 Jun 2025 18:48:44 GMT  
		Size: 5.5 MB (5532364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cd2aa85f1810d2fc9b415f4f5431b1a8c49453fc4fa1d8eb1ba04f392989278`  
		Last Modified: Fri, 13 Jun 2025 18:48:45 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:abee581ed2ce7769051164d1a93aa28759274f2cf1fc24e04d76f4cdb3f9a195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227713751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c7166add4125e4b1a29de3b4974b13d469d8378efbd3c1a1aa6a22dcd8b04a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a3a141bfe5627b562a870ad931fe1cdc50d3dbf733a0568d089499010c9116cb`  
		Last Modified: Fri, 13 Jun 2025 17:05:27 GMT  
		Size: 64.8 MB (64790746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43964a7b36c19d8d08d18253a187b8d9786e92144f40e02ae62a91f72c8c9f73`  
		Last Modified: Fri, 13 Jun 2025 21:49:08 GMT  
		Size: 162.9 MB (162923005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:365d9f5001cfcbe5bb3413d794831fb0279b9f303f89db53e400da3b59925ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a053cfb5af02ef7a13cf183ae2fbd72ff7ee66b0a4abceb405b8cd76b0905ab`

```dockerfile
```

-	Layers:
	-	`sha256:d3b95eecf0fe1969729c1f9a91aa82c1fdc6f4a6b73fe818214fec605ce4b6da`  
		Last Modified: Fri, 13 Jun 2025 21:48:43 GMT  
		Size: 5.5 MB (5531053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ad0f3cbc7a47bfe69ab442ed3fc52cad1f7165a16e399680b0c21e6bdcb75c`  
		Last Modified: Fri, 13 Jun 2025 21:48:44 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
