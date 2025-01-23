## `amazoncorretto:8u442-al2-generic`

```console
$ docker pull amazoncorretto@sha256:cd5edc4ccab8300c7a079e7deefa2f2b2dcf16a71aa5244221ed5e4140f4014e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-generic` - linux; arm64 variant v8

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

### `amazoncorretto:8u442-al2-generic` - unknown; unknown

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
