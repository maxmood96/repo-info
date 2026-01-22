## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:6b9ed043d8b5b5fadc69abfd56672ea8fa68bb6f8671f1d8c5f93fec397ffc4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8e1941c5835280ff063a80dbbbb7c2adf19e38e5ab673ebdd28b259da6955c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139059752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac4cba82921cc6884535f7fc124ff61fd00d4595500089cf1fa33729a7ec53e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:58:02 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:58:02 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 18:58:02 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2cf296d047513764ffd5d8eb73bd7e7516a94e3a350ef1d2cde26a84ada185`  
		Last Modified: Wed, 21 Jan 2026 18:58:18 GMT  
		Size: 76.1 MB (76119596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8139c5b5b8da2c99af68c8101cfeec45ec254091ae3e97038a21338552145e7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a9b18293aed3c6cc02dee26a7abdd250de7e87bd0075bafcb86c7ab92c1aa8`

```dockerfile
```

-	Layers:
	-	`sha256:b64665c0c4350ac51a1af6f9c63b757bac79b6afbc5e67c38a1549bcc79e1ef6`  
		Last Modified: Wed, 21 Jan 2026 18:58:15 GMT  
		Size: 5.4 MB (5377358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4369146720e73dfb3a1ad6486e1f2895bff9df0ee7982c20843eb8453a2d4d5d`  
		Last Modified: Wed, 21 Jan 2026 18:58:15 GMT  
		Size: 11.5 KB (11526 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:72f8ecff18ca5c09c5d13e241812f1b537b20decd8e73bb1e41032511247dd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124708972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b01976c62f0325ff7c255a3c4369a6455cb22a7ee0cc07bbc83f06f3479d5f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:58:32 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:58:32 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 18:58:32 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 07:47:55 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef0c3a8367555fd665644b39150b785e2d0486976224b943fc47236f954e820`  
		Last Modified: Wed, 21 Jan 2026 18:58:47 GMT  
		Size: 59.9 MB (59938538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4db70ff5941d2a044dd487d6dbc42e37a24f47871b813927a15db54690dbc119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaaad45122b99483d6576f2aa464206e288d0a30e5f495529e43c0081edfe08`

```dockerfile
```

-	Layers:
	-	`sha256:d981c27b4c880d7710833fef718da2723c45cda38d33efa2910395edfaf7f64e`  
		Last Modified: Wed, 21 Jan 2026 18:58:46 GMT  
		Size: 5.4 MB (5355857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67251f92da9533274e07a4952ef40e867149423fd7932080d485b65d0f43ef25`  
		Last Modified: Wed, 21 Jan 2026 18:58:46 GMT  
		Size: 11.7 KB (11689 bytes)  
		MIME: application/vnd.in-toto+json
