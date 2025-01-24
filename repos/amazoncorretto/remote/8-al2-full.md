## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:09974004d7076a1851d417825c47a959f158cf0902ee7c491e86d8acac9eb090
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:09dc85879250512b13a54fb2460fb2aeed5ed47dac4cebd23658dfe449a19065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138207870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f242aaf9401bc3aa00876cbe052a995bb7c90246608e1a94c830271155da1e3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:24 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ff49cdf0051001697eb997ff2a321133bbf5d184ed54b92c88e3d268844908`  
		Last Modified: Thu, 23 Jan 2025 18:27:10 GMT  
		Size: 75.6 MB (75572040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:55d4793ca5d79d3be790544ae7b8d9175c32179ef522790ba6bd064665e4a29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691421c9fa92a61566c1ef8e8f3e59cc3c054c0f5908ff78aa4a92e4023d420a`

```dockerfile
```

-	Layers:
	-	`sha256:73936311b843192ebf25f1c5579ff47a9c0d6a3c835810672059d877bc458b14`  
		Last Modified: Thu, 23 Jan 2025 18:27:09 GMT  
		Size: 5.4 MB (5359564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80fe089e30b4346c4b5c67f24bd041b7640ad1833259babd4405d4b335e6b4e2`  
		Last Modified: Thu, 23 Jan 2025 18:27:09 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ce95b9903afa01eb591f8e20820c6025d13d16df3252a3eaf22a65f0d8ce1352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124261455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14e18af4e528ff530d538673012d299e24d62665881c033196a0b453b5c209c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a40fc02393a849ecb556016054b90c4bb62c50d5ac13a9617e59cc0d2b432b8`  
		Last Modified: Thu, 23 Jan 2025 18:28:55 GMT  
		Size: 59.7 MB (59671150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ad406d0d187950ae63878ffebe4735f387065216a606180c908314fa5944b4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669c139484c6db7cd0a8069f01e583621cc26ca1d829cb4164afa711938b294f`

```dockerfile
```

-	Layers:
	-	`sha256:9627f50dbd597f8782925e839cdbe4c79ef459fd71ac606cd88b422490350803`  
		Last Modified: Thu, 23 Jan 2025 18:28:53 GMT  
		Size: 5.3 MB (5338063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d9cb9e8c8b8e87638c61a5ce0e9bdf1d1b35eb9122aa6e3654b220843ffea8`  
		Last Modified: Thu, 23 Jan 2025 18:28:52 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
