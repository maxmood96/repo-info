## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:a02ee655918650ebcb9580cc84ac6a40b73e550dde659ecac792b5fb06b6f56d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:35fb2ba5cc0fd0971c0119f52f6305cfd856dcb2e442d4d248288865ecc86ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214834231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5b3ee9b0145a66645e6a67bdcc4d386b95084aecf6d04967dfb833366c9e7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:dcefe03e9009da4739e237894f3fe49af6782d53d9e2202e46127bd568617855`  
		Last Modified: Sat, 09 Aug 2025 04:15:21 GMT  
		Size: 63.0 MB (62959372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0609072df14ca55d332f8e3c224846b0b7eead95460c9ece0cfefd122f064`  
		Last Modified: Wed, 13 Aug 2025 23:11:17 GMT  
		Size: 151.9 MB (151874859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4078c265b57d406658829e3cc3d94ae1ea0a7300096b90ed6d894f9b8e5c0f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5543728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c37597809d812b007c73fffa0a3deea655418a8b5b233382dc9f5efcb89a8fb`

```dockerfile
```

-	Layers:
	-	`sha256:dbc6e9cf703f8c21c7080807911dd7a3f2e4ab0bdb0038043210500b0b19cc89`  
		Last Modified: Thu, 14 Aug 2025 00:48:02 GMT  
		Size: 5.5 MB (5532473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf90095971b1d3750fd33aa377af790a48b1b03be11ee1326285820eec80853`  
		Last Modified: Thu, 14 Aug 2025 00:48:03 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:65edbfb6c35ee94ea9470aa8556b9155e194117e1e4a6bc4761794076b1f8fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215192203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0615caa5cdd2f849af599ef45d3bdb3cd6b9a78728964e8223c25d61c78b4e7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cd4aced99c35e8bc24c9f8f76de4c6384d08e38ee655cb9bdcb8b655f87e74`  
		Last Modified: Thu, 14 Aug 2025 09:14:46 GMT  
		Size: 150.4 MB (150397839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:971e723004b0c39ea48c950355aa82121d3820e859ae2333973fcfaa9dd5488d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d56ad2bef51c8c5c3c04e4e6e816c4ab94890f150d7da8c9d96442a8711dc7`

```dockerfile
```

-	Layers:
	-	`sha256:7caaa99bb21bbc66a0b5655172051c4ecaa4d1c18587bd29de24a2cf01745316`  
		Last Modified: Thu, 14 Aug 2025 09:48:04 GMT  
		Size: 5.5 MB (5531162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21bd8226845bf0e8dc60c213aabe5c992aa8a6dfbd3c380eec0f7bb7f7c2d27b`  
		Last Modified: Thu, 14 Aug 2025 09:48:05 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
