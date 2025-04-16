## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:674d24b818b8e889fb530a98c250f8638f14116f34eddbe0191f74e4dbc12aa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3599fc366ce27adc8a3992b6fee9ac48f1185f07caa8a2843308c354f82a4071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227607826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855ee6e72975185d79b9b0b0abcf9c3999e37975de0f0aaa83d8653bb38856d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc3ea053a6b64757030a1eb438d698be6e81c92b804f2376d0c7cfe353f8856`  
		Last Modified: Tue, 15 Apr 2025 23:56:02 GMT  
		Size: 164.9 MB (164854937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5dac7aa121b4e1dfca99283bbcbf4ae602af34b250d9dee3416fe0f9e6320eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee90feca150549ee807f4f1c73a2c2de7077af804974dec5fd49494776547d82`

```dockerfile
```

-	Layers:
	-	`sha256:9393dababb37a0f9bc0410063da2d488f273b049211c5f659bc702d6644cd8f5`  
		Last Modified: Tue, 15 Apr 2025 23:55:59 GMT  
		Size: 5.5 MB (5517025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b318041fd7eb29246126afb7ca93d47dff1d2e557206208d1962ffb60893452a`  
		Last Modified: Tue, 15 Apr 2025 23:55:59 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d4646f143c066da2da90bb660d57ba56777ec07300503066a68d3a3f49104c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227488378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30cb6a1d4456d02e6e5ce0bab3aba0a523b5a269b2aa3bfaac8e15a3008c08a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801f2d4c03ced6f3dd698c83d22a792997c6774ac7b281f577007cfc68d4b0d9`  
		Last Modified: Wed, 16 Apr 2025 00:15:56 GMT  
		Size: 162.9 MB (162922556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb1fbfbd209f89bfdc8c1285606cac711792132c1a045af3b0d4f89a3d24b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6a3a39a5c11975f1c6ccbc142c9cb3f35e5d1efd4c0ec071294473f4f31260`

```dockerfile
```

-	Layers:
	-	`sha256:19ae7dc6a140d9125fe1628e723e3f5caf2ac867a7c41d1a580f2d8934bc6557`  
		Last Modified: Wed, 16 Apr 2025 00:15:51 GMT  
		Size: 5.5 MB (5515714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30f2c42519668d4354e365af0af82dcfa2595f1fbb8796818396ff2029ecdca`  
		Last Modified: Wed, 16 Apr 2025 00:15:50 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
