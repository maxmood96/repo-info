## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:a6aca0f4f9597a9adc88ff5ffefb16c86e19f9cef1ce2360ee87a9eaca1930cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d373a186ef88cb4d4a8abd0cf8b06f0938ffc336bc02354335d6b0844961fb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214503532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9695d38d562126fe80e4e398ec55d017450cbf421221abc404bf20d537bbc1f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3b5771a528b1220f7f687181fc0cec216aed88a7fd109a223e795a33dcb1dd`  
		Last Modified: Tue, 15 Apr 2025 23:55:59 GMT  
		Size: 151.8 MB (151750643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dd05b7c11715eb347f8739ce35e289d4cc297e81480d7042285bea26122fe176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f52fe08a420f4299735ec280a16ed2c42c5edf2c115e5b19a70cbdc8072b7ca`

```dockerfile
```

-	Layers:
	-	`sha256:e291ebd6943e51ea09e4528b6abde45de54c134a7e34c3ad85f471b9b4e2496e`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 5.5 MB (5517134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a120124ab1053355f84f4aeafd99d1dd3c1568173a1dc9081dc3ad619f3b6b83`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

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
