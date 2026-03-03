## `amazoncorretto:8-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:b5938740f9fcc555af7bf3e37881e0064ec9dab286d77db464a81b2b4e77344d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e83de4cbc3ad474aca4a4aed69bd45b526b40a15f923df8e3e6b33ce6a4ccb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139096995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d5704495bdc9814d17cd06d97a09ea2ae7692ea9f99b6392fd0492d3f1a778`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:08:53 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:08:53 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:08:53 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:08:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8671a46cd97cb565ae682f62b0c2f1c346eb6aa7a6c1b32d27ef14bee0510a9`  
		Last Modified: Mon, 02 Mar 2026 23:09:08 GMT  
		Size: 76.1 MB (76136766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:91ee5d08c521a1c0108b6c6a7d368b70a4c25aab35f4a4c9a01f13fdc14ba5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa6e3fd12a20d92e94774e659e061d6aed849250d5b4d9e767cd7b9de4581c0`

```dockerfile
```

-	Layers:
	-	`sha256:7550d221444f211e288c72f33d00d4a9a2eb3b45cfecb77f2f9115c002016acd`  
		Last Modified: Mon, 02 Mar 2026 23:09:06 GMT  
		Size: 5.4 MB (5377358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d74d67a62025536b6c1d95d863b32df9ef4db33a8b26b0eab53967bedc892dc`  
		Last Modified: Mon, 02 Mar 2026 23:09:05 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3239cdc42d424eb38bdec5b7537e03c52f5deadf08d1243923c03ab484b324b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124736616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6124dc80081b6e2a46bb7675dfa7eaabe6931a4520ce59adda3e9efd5d80b6e3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:09:16 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:09:16 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:09:16 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:09:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb8ebfe61a3b23e04e4a22e0eed5f6ba1100ebbc43ae35b9af41c612940a6d5`  
		Last Modified: Mon, 02 Mar 2026 23:09:30 GMT  
		Size: 59.9 MB (59925205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bc6ff17183fe94fc1731194500f728824af40d7ba6f9a92cca039689cc3fe7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deac5ed4c6236cfb524be4dafe123d7e9bb3970393166c9fac43eaae285a4aaa`

```dockerfile
```

-	Layers:
	-	`sha256:f038c8ae2533478df63407bf4c60b21bf9835350fc17f785e092c1d6030b3bce`  
		Last Modified: Mon, 02 Mar 2026 23:09:29 GMT  
		Size: 5.4 MB (5355857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54bf667ae33dd700797b28bdd4bdff8097ab2c4d8205c4b254a1045164773f80`  
		Last Modified: Mon, 02 Mar 2026 23:09:28 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
