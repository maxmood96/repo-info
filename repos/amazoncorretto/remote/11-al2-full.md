## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:e619a14fa2b423e99559a3e266f500110b42b890374e47a5336b59f90949bd7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:01710340d47460ef1cc6a64940b502fb2c14a57dcf5738457a1fb7010fb01dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d740f60eb71a4f540ee3b81a59b3ad8477cb47f4f0b21526b9ce5e6d4d592c74`
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
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66d3d6094d4cd397049fc185148528c5f88b7930cf9c66ee49252ee8239250c`  
		Last Modified: Thu, 27 Feb 2025 21:08:11 GMT  
		Size: 148.3 MB (148280392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2b2bf4c3d19b9e3fc0d43fb42b3e027f976084dd61ddf9092ab197e796918d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5754ca9b91b9363f72a1e7883122f0a8dfdc4b0a1ae1c846b0548007f446643a`

```dockerfile
```

-	Layers:
	-	`sha256:bd0cb815e1b33f06d2f3a04610de751e95584c7c36d21f22977f5d76aae4c9fd`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 5.5 MB (5524415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f09bf3b98d6b1ac0672554c3828ec935ee57bbc93b3541260d4210764fc075`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

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

### `amazoncorretto:11-al2-full` - unknown; unknown

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
