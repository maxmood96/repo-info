## `amazoncorretto:17-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:f82e3cccef6ffa7db1ecb67ca35e622a823237fd3fc4a2de1239b4e0d646aef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9d5b8d97371cf127f35a2545041bc4cc524948e0431cf8a8eca3378265a4d808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214440191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b7a3eba646a4172f659d16c1991ddf7138e02881963bf11ce754c58150f964`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20ea6810da602f5c914128478327d94321883aee9b0c8a02cc20b8a8282c9c4`  
		Last Modified: Thu, 27 Mar 2025 23:58:41 GMT  
		Size: 151.7 MB (151687302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e76d3f23c80c0490e2e463844f53244ff77031e72b444f4bfb81d7f11ae6ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998b4c8687b3434f1dfa422731dc5eb4505a91c86f2d3a109328d9b64bb0cf18`

```dockerfile
```

-	Layers:
	-	`sha256:f1ebe4b4d2250cf01662119d0812fff78d16c6717694358163c61f32f3f05812`  
		Last Modified: Thu, 27 Mar 2025 23:58:38 GMT  
		Size: 5.5 MB (5517110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ad2aebe3f1a96410969266183c4681466a2e3f6cf7ec666c509bc120d921d3`  
		Last Modified: Thu, 27 Mar 2025 23:58:38 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b404aedb04e70d2d5da3ec1f42c1c3759bdde89dddd6a0cde10c50c0c4dd7522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214868886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d159ae66a99840b063cd8d45fbaa187cc01c703145f66af5eff4b916fc0ab91`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cb0a04e32045bea8a36477ff07d28428a7ae7e142505376782ccaa20b05e7b`  
		Last Modified: Fri, 28 Mar 2025 00:13:29 GMT  
		Size: 150.3 MB (150303064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:220bd51a75ffd418ebc908edd6665bc8ebb63f3f899816e83a189c0e5eb0affb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00a055ca60d63013fb655f3ba2b52ca40534dcab3b515163653a14b489541b7`

```dockerfile
```

-	Layers:
	-	`sha256:45716f41320eaa947673d669dd4f451f9634409ee4a6b019835d9cd0155ef7bd`  
		Last Modified: Fri, 28 Mar 2025 00:13:26 GMT  
		Size: 5.5 MB (5515799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f5536d307c684c99a6659fe24174bf58c3371e2919892a3d6ccee2428b7875`  
		Last Modified: Fri, 28 Mar 2025 00:13:25 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
