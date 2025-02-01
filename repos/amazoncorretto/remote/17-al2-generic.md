## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:9331187e449b3ec4751da063e70dc8b29ab4211f23c32a1de63759179f066b10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1c8528435e542cc2720b5cb4e4cfac5b4e1436bda80d4843019a54a31c8d2071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214284043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd42b620ed9da3b2ad5fb8336cf1c3e01575c555312c4370e266e26f4c1aad73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b6252bf1f0f9b41e2a8f6374a8a252f1ae25a67239bcc02d43af3b859d1b4c3d`  
		Last Modified: Sat, 25 Jan 2025 04:14:29 GMT  
		Size: 62.7 MB (62669455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61332b9a39ac021cbc46e61e8f0e39d4ac7120cfb8713a57729b61388819ff92`  
		Last Modified: Sat, 01 Feb 2025 01:08:43 GMT  
		Size: 151.6 MB (151614588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3140b02327edca3e233e210a767c2165850d63517fc075a88ff2b09744f917cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760e8c39f65abf0c2f360128b219b5d751f5d5df9911cc96c3fead2566e813c2`

```dockerfile
```

-	Layers:
	-	`sha256:f9e0201adef8fd3a213f0da5ea341a7cb560cc4a39d3b6a8d21bf7c98e624b3f`  
		Last Modified: Sat, 01 Feb 2025 01:08:42 GMT  
		Size: 5.5 MB (5517106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b34f6f690e51a240908ec158a4e7fa4811179fe3491b95a319ca17ccd5696ad`  
		Last Modified: Sat, 01 Feb 2025 01:08:42 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2ea01437eee766a2e38c7a99e534732819f27cf6bc1631a0c03777aa47dfc3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214880499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0a39bdc7a1bc7b8d352a07cb2a3b907cec3db2bb4c45d1872bdfea07fb7918`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:e694aca9e8d5c223f3e2469e032276879ab4b403abc21549d4277f4463b2974b`  
		Last Modified: Mon, 27 Jan 2025 15:17:25 GMT  
		Size: 64.6 MB (64578423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b7ffd61ef03152a91781f0d57549b116d8dd777b501e80802b8e8700708d0e`  
		Last Modified: Sat, 01 Feb 2025 02:16:24 GMT  
		Size: 150.3 MB (150302076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3063f282e29f687331d5dd819ab66551fc2b914f9aa6030db00368634e7f9522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0355d42d93ac653b42f0e8b16bd905a0968e01f55f58db36ab95c521af78f6`

```dockerfile
```

-	Layers:
	-	`sha256:0b1417911f3479dd8987da850da72a92587eacb293556bbff61516dea735f832`  
		Last Modified: Sat, 01 Feb 2025 02:16:21 GMT  
		Size: 5.5 MB (5515795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16788dab62186b298478ee29e0b1e7079a3caf1fbe0c0787a5f3bc3d2ca5a2c`  
		Last Modified: Sat, 01 Feb 2025 02:16:20 GMT  
		Size: 11.4 KB (11405 bytes)  
		MIME: application/vnd.in-toto+json
