## `amazoncorretto:11-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:132d295e2e1d1a273563bac24a6b080d88f5982b91b403a30d7c190e4352ffc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fcbba2d8a629d0f35085ea4e23616b85e6047561230def6ee24fec34106119fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210850794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90696178eb6e7f70e98003be81432da0ba7ef4199107d516d03298b82c70678e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b6252bf1f0f9b41e2a8f6374a8a252f1ae25a67239bcc02d43af3b859d1b4c3d`  
		Last Modified: Sat, 25 Jan 2025 04:14:29 GMT  
		Size: 62.7 MB (62669455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a915f6a9013dcc7d789628238b94f837415410b738bac0f918a7f1dfa8e86be`  
		Last Modified: Sat, 01 Feb 2025 01:08:39 GMT  
		Size: 148.2 MB (148181339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:99e751a4dab5b981841cfe2287e4aed1d40d6f9e825c9e7dcff630a3ba5f3fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99f3bcb38fc4d0c0492165b8431634fdd4179366577bfca6580c4aa1c1cd29f`

```dockerfile
```

-	Layers:
	-	`sha256:1b4e036192163cb765934340c1f4af3524e54457e0fa3ee343b15a2d455f7cd3`  
		Last Modified: Sat, 01 Feb 2025 01:08:36 GMT  
		Size: 5.5 MB (5524411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20b1f86aa9390202c1634d1929c4f094552df7900d94fec570c3a99bf3fddc9`  
		Last Modified: Sat, 01 Feb 2025 01:08:36 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d608a0ec9e4d92a310bea20f359068dde26560623244fed0a8e63397fdbb4725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209866879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522a0b302b388978bb6667c5f9555d92cef7ce7c24e4d0ef6a2434f08eea8040`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:e694aca9e8d5c223f3e2469e032276879ab4b403abc21549d4277f4463b2974b`  
		Last Modified: Mon, 27 Jan 2025 15:17:25 GMT  
		Size: 64.6 MB (64578423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e8904a985d69287eab1fab568d78d1bb01a93fa4abef3da47a0d9d5d2d39b6`  
		Last Modified: Sat, 01 Feb 2025 02:11:11 GMT  
		Size: 145.3 MB (145288456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:541f9b503326d653b057c5e41248eac269f142c4ef30b47ba5f6d3608c42eff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c3fd87bab53a8cbae52c6f1d47c4ad98225c7dcc9eaa4ddaf8d49493d17dc9`

```dockerfile
```

-	Layers:
	-	`sha256:0a5e1d26c69b33d09a7eed5acea5d09e664d0bf65733fec78c1b8c2dd8013748`  
		Last Modified: Sat, 01 Feb 2025 02:11:07 GMT  
		Size: 5.5 MB (5523905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0319f2af3bcac0e22b36856d748f9dd2c63d2053ec326bb61e30da2c9c34b0`  
		Last Modified: Sat, 01 Feb 2025 02:11:06 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
