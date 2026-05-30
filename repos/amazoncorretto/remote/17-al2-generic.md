## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:823513044539880b2ffadffd48fb59b1670beb7cb0da6f15ce08a92928be1dd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3efde5fe5faa9037a07dfcdbbb25471ac3b0bedf5a1a289a8a3b466c98d86563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215620164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604bc236c96165b83a1ebefae1b7bd1254bead16a09c5eb197652204b51c5a7b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:34 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:34 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:34 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a8a7978ba0ff58ed98a62aa94453f0163b3b048a2891c3f00e0f937576d6f6`  
		Last Modified: Sat, 30 May 2026 01:11:54 GMT  
		Size: 152.7 MB (152678214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f0ae4bb4c5a81482250788fb272e8601573975dc327cbd3ab1a6d807a61a669e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79636f44bd81273bd30cb5f4ab6e9ac3540a647725425e15e0f376ff2ad2ff9f`

```dockerfile
```

-	Layers:
	-	`sha256:cdacbccf73c520c1601e0eb59a7d5bf884082a40c03fe83988fa9343a6ec798e`  
		Last Modified: Sat, 30 May 2026 01:11:51 GMT  
		Size: 5.5 MB (5536617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4c10fa02289a4bc65e475689e2a1136ecb63a8840f957f327327e1d2edb535`  
		Last Modified: Sat, 30 May 2026 01:11:50 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:04302d30a43f4911489e50113c16273a2492a2d3793278f13a5ce4afca4d516a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216109541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4094169e22e85effaf5b3b74424a17a0b2ad2a1bc034053d44d9a917cc0b585c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:36 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:36 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:36 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeed7018fa6b115148f6bea5857f5dcf0cebdc10077dc033be3c7b430dc97a5`  
		Last Modified: Sat, 30 May 2026 01:11:57 GMT  
		Size: 151.3 MB (151318832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c19c118d76e3be82ca6b099cbbc4b33bfa8f7a6ad96e49f013d5bca3a44985a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d50cbe351f84fa106aad234c36c88c12ab5d7626a180583cebd9f8a820f5a9`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e0256f5362ca3baf7df528252b0e11696ad4503d4edf87d9ffb48f1614f96`  
		Last Modified: Sat, 30 May 2026 01:11:54 GMT  
		Size: 5.5 MB (5535306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3b67f9a5027c35b3c2c29b108ef5a33ab74f152d701d1e61b4e3c1996cbfa8`  
		Last Modified: Sat, 30 May 2026 01:11:54 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
