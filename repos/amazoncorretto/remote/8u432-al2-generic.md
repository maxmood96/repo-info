## `amazoncorretto:8u432-al2-generic`

```console
$ docker pull amazoncorretto@sha256:3718cf143b7aaec37742a61f49aba0ac9d67508e32cd98aaca0d6af422c05a31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e8caa22723e13254a6a40d951396e489bb2443952f1c0a5ec552f966dd0025d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138255104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96390a0466fdbe50720b3d944e00f90c5642f0c5f2be936fdac2798f166e377`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d383ff42fc6ca37ceface79227ca1c17139e26fe0fd6c3ac2bff18bc2fe26ac`  
		Last Modified: Wed, 08 Jan 2025 06:29:17 GMT  
		Size: 75.6 MB (75577665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2ab775e3fb3a12fe12be0dfcac4966f34fda108fb23ec5597b5f98dcf1ccc4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df1b423ae617d7f8fa7dc4d7656ab318753de12dd4cff5bb9d3648359e57282`

```dockerfile
```

-	Layers:
	-	`sha256:66d13644c04076b688dad4f9f5d1d12b4369d69c54e60ec48a0802942393c711`  
		Last Modified: Fri, 20 Dec 2024 22:30:40 GMT  
		Size: 5.4 MB (5359564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814369374e6e6f59c60fb5e45ea9dcba60975c37e4b9ee2b7c5f1240ea9cd109`  
		Last Modified: Fri, 20 Dec 2024 22:30:40 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:59d37a5dd05799ec42b81bb508f238e2cbcdac61eaf641f3b4e7765b08583a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124251016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8bbd04c59b24e684e10368aea92cf9e7a610834ae2674fd4dfffbb46c61007`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fc4c085a3225a682f95007088f4322b8190bb2f0ec35ad4f24aebebdfb1bc4`  
		Last Modified: Sat, 21 Dec 2024 01:34:40 GMT  
		Size: 59.7 MB (59669129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dca3ed3dc7e9558c96fd3d52eb1b7cee1d1b409288437cf7c175dd333ae7f247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a68787b04e46db1302836cc16d15bf1c95639ec40b1f252c262d4f42068341b`

```dockerfile
```

-	Layers:
	-	`sha256:15f7b474b43c9a85babee92cabc0b95dde777a9bc4362db918bc34463e8d54ae`  
		Size: 5.3 MB (5338063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7547ec7a25afe750b0e59d3170a051ef2138b203cfd304f9cd5bc2825d30fffd`  
		Last Modified: Sat, 21 Dec 2024 01:34:38 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
