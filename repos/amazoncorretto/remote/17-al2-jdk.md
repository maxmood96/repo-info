## `amazoncorretto:17-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:0d440c2d3d00279a74863f39e5b161658180612f5d4d370177b10b24501c25b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fb5eb70c01cb01962b3b76e53f1ec7a517e8bb66db3aedbd95a8b2c504ba2d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.2 MB (214240208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95552f8bce0d27be51529f084a84d193f9f181f71a778015bd42c55e78ddb53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ff001010b923a0181362a7f37e350a3085467a2b774e124a0214de57212325`  
		Last Modified: Sat, 11 Jan 2025 02:29:35 GMT  
		Size: 151.6 MB (151604378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d87cdf605cf501f037485021214b16f7b4996488ef73a7485e5da847e1c7bf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ffc648cfcc064c41ce3d955060de683ccfa4250e0fb9a76d1be4aeb7477c07`

```dockerfile
```

-	Layers:
	-	`sha256:099131f683bd7dcc1c88ae7b16f73a8f1d9df1d28f7aaf9c25b3946a9e6f0d28`  
		Last Modified: Sat, 11 Jan 2025 02:29:31 GMT  
		Size: 5.5 MB (5517110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:427cbd192d8a0369742bfe5b872067a9573ca876f3de8a4d7c93833ca9743091`  
		Last Modified: Sat, 11 Jan 2025 02:29:31 GMT  
		Size: 11.3 KB (11256 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a72df4e6791618b75b3e5f06097401a687ea5e1ad069ddbd9a735379317f72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214905497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4e9f9debf69ce8fdbdeccf39556b779556877bb2ded0f438a2c22f4c5276`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b396860cb9f9c27bdb6b1b3bf0882bcb2815907fe44d9d85f398239e98a1602`  
		Last Modified: Thu, 23 Jan 2025 18:41:53 GMT  
		Size: 150.3 MB (150315192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c5ab719f28b8f9cdeab138832cc58f85daa57d06946986a2bc295f0ea4d9867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a905cacbfb408b7becf73e270b6e2d0a0832928e4ab2c4104144f7f5c83e9a3`

```dockerfile
```

-	Layers:
	-	`sha256:c67d8d5f13ab8bcc981ca1fff736627c73374ea738682019da1b0f93ca53f8c4`  
		Last Modified: Thu, 23 Jan 2025 18:41:49 GMT  
		Size: 5.5 MB (5515795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf91283e0932dab026b0163a27b8ab21a8356052394040e90a9390e752264b9`  
		Last Modified: Thu, 23 Jan 2025 18:41:49 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
