## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:f49527a15afd2bf5a225e08e271a4e9db2c34eaf38906aeb1a4dc5d50e7a7c14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ae7982981a935d710ec244d62e0c26243a962e40e87e115c4af1ca49a86e5767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214284844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc70812038791acf5318949bcd63d38ba6041a5dcf55df77575867090a21546d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce47bbf12c856f2c3827f5733bc33beb2ba86473a4817f4f8c1b87f1990cd6d`  
		Last Modified: Sat, 16 Nov 2024 00:48:47 GMT  
		Size: 151.6 MB (151607405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6f20a02af3d6dca1d24b1913cd6a4355105e648a6c04b45d226f88a2d969210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5539035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f727c35b884c4a3930fd9b7db450e95f4921523a7b1679f30c77371abcce5053`

```dockerfile
```

-	Layers:
	-	`sha256:507997736adc85759b2f6b05191f36744c9f6fbceec9c38c1b02387efe142e73`  
		Last Modified: Sat, 16 Nov 2024 00:48:45 GMT  
		Size: 5.5 MB (5527779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc83591e32619dd8d67995d14ec1a0e0ada7cd5c9aa1c6e8e53bac98c90b561a`  
		Last Modified: Sat, 16 Nov 2024 00:48:45 GMT  
		Size: 11.3 KB (11256 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:327387519e49a92b80a98d8e227079bbbdd4558e774220ab22aa075b63573f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214820830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc26db83521dfa2ef0997ba52dc4cb64cf63a8905cdd056b8f8ee4e2413eca7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737939e85848b34826899ab042c8aad6fc1fba8f7f661936f213981c4b20421e`  
		Last Modified: Sat, 16 Nov 2024 00:58:26 GMT  
		Size: 150.2 MB (150238943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0cf8cdac74db508d3a7c149bda4dd28f77f67305a49137ba7efef1f5945c1fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb087a9fcb2f2e0923be9d8f24b434397d2f8e07cd1d417b7b2b398995173a4`

```dockerfile
```

-	Layers:
	-	`sha256:2963a141d6328480f776c5ca1531595cabf168c048eae6e124d50a21c60b2332`  
		Last Modified: Sat, 16 Nov 2024 00:58:17 GMT  
		Size: 5.5 MB (5526466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e9662f3a77ae4fd35e764e0041fd7235986ce388548bb441c20756e834c31eb`  
		Last Modified: Sat, 16 Nov 2024 00:58:17 GMT  
		Size: 11.4 KB (11408 bytes)  
		MIME: application/vnd.in-toto+json
