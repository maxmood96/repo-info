## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:16e68d610eed4c8dbd28896bc6e1549539d3dc344df52254dd77c0aca5e75465
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:11f82d39e810354586759195d7345e0362cdafa1c8898181ad33cf270ab6660e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211054451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4e9815e8bc8e1a6b84e17daa57594c500a2dec493e711d2e412d39aae1a6c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:50 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:50 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 18:59:50 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed1a9e1b256f77b245cef53688fad9937d1eccfd8fb70e9215c3d4d265e596`  
		Last Modified: Wed, 21 Jan 2026 19:00:11 GMT  
		Size: 148.1 MB (148114295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ad24cf0482066a187f258427ad3cf66ffc13007f5e15628f03c7f008fe739dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4379817eb4e1e25e5f04d4e7fa86aa73ff6f4e03bf9cad7bf465d9cb7d5b21e9`

```dockerfile
```

-	Layers:
	-	`sha256:caeae42d587bd2d5dfe43367cf77dadae0183c8747f1212ea6de3e7fcdd381f6`  
		Last Modified: Wed, 21 Jan 2026 19:00:09 GMT  
		Size: 5.5 MB (5543009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a684606c4faeb398bfbc94f152a3300ce80d43bfc7d69dd470df46d334069d2`  
		Last Modified: Wed, 21 Jan 2026 19:00:10 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f4687ef4095090ca1ea7f05c046cd10b29259354561c31295fa74824bd5210aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (209991816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd12fd1590afb3a00043206a9fc87f93553937a47608e168fe29e8174f70133`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:49 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:49 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 18:59:49 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760c51bcf12611f308e2ab69755b82d7eaa8af9d7efaf8dfeb319eaf5ad770e7`  
		Last Modified: Wed, 21 Jan 2026 19:00:12 GMT  
		Size: 145.2 MB (145221382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bf1bc5ce978954baf26858e7c9a44733cc6f30410892a25574f20d4ed423ad6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e3f7acf6ed8b37273b322b1977b024f0541ba456fdf5cb0c806633cc281f36`

```dockerfile
```

-	Layers:
	-	`sha256:20e56c153537fce3a70b8dd35c5740dba6117471915d36028d485e48ee265152`  
		Last Modified: Wed, 21 Jan 2026 19:00:08 GMT  
		Size: 5.5 MB (5542503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55ac9585601e5b79452603e71fd126db6cd03e72fc88301e17d224ed68e1c31`  
		Last Modified: Wed, 21 Jan 2026 19:00:08 GMT  
		Size: 11.4 KB (11363 bytes)  
		MIME: application/vnd.in-toto+json
