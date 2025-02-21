## `amazoncorretto:11-al2-generic`

```console
$ docker pull amazoncorretto@sha256:ad62c0f683aed0af8a92f1a0b5847b21675d26aeff15f9177857fbcc8cfb27f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:801ca07d96ac7066c2278a36046a7853d2ca60a2c4354051e8085b2176557d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210849159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d6110d52eb47f45ddb375f90a3aec7e6ce554dfbe9ec6887c827c9af31914c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:43fdf45428917f1f386fbfe0eba1ccfdadae7696a4cce30a96cca587ab25ab90`  
		Last Modified: Wed, 05 Feb 2025 10:24:14 GMT  
		Size: 62.7 MB (62665244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e230daff1413643d46aeceb69e8d26b360770a5e9b6cca15ca9ed2e89e2ec0b`  
		Last Modified: Mon, 10 Feb 2025 20:08:31 GMT  
		Size: 148.2 MB (148183915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:613b986277f2cb98571123597fe8f9ab36cbbd36c7b32b2f0d7aa85ce1475dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79eccba5f2c81b202626b1212fe23e5f1a9c1899eccae4a102eb9e4f20150f3`

```dockerfile
```

-	Layers:
	-	`sha256:27a2a882a791ac531c0ee3d01e5a267ecb9b44e55a958be9de5646be15b25819`  
		Last Modified: Mon, 10 Feb 2025 20:08:29 GMT  
		Size: 5.5 MB (5524415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82d5fca58dca3ea7dbf37b2e8bd73d6de20b905bf0d56f1a3204b18a3e0e2fd`  
		Last Modified: Mon, 10 Feb 2025 20:08:29 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2f26ec551ffddc7973557cdabd9df6cd65a73c0c650315495b13cc389afeb8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209866711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761c4d6760d1e9380d3d5afc5fcdc4d4412d177303aedbbce89756f2430a67f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4381a8d213612cc45236cab51e94b7db9295fff0e1cbb949ff7f98b361421988`  
		Last Modified: Mon, 10 Feb 2025 20:15:11 GMT  
		Size: 145.3 MB (145288489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:96b1528a1fd6ff7fcd8a99eefb634acbd62bdd9c113422d79270aabb147b17ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13b39991d7ffb0f39c780a46787a472385b8c33f5cbb5afea10813540449011`

```dockerfile
```

-	Layers:
	-	`sha256:51c8130100d1444d079c9f133e542ecf5042bfd7743f582b42c291c50cd69efe`  
		Last Modified: Mon, 10 Feb 2025 20:15:07 GMT  
		Size: 5.5 MB (5523909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c43046bb9cc8372d32cb5684a5af6c07a2cad76639b552d6007baf684c82d17`  
		Last Modified: Mon, 10 Feb 2025 20:15:07 GMT  
		Size: 11.4 KB (11406 bytes)  
		MIME: application/vnd.in-toto+json
