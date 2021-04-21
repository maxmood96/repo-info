## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:7f4379378c791fd02a5c93bd0e8f0694612d782c3665823413f1c5191d6f1262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:00aee242da8f1dc4212eb0fbf63a1a8d405f3ad7ced4f37d8c47d21d5c7b8b7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.2 MB (137238262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaef49ef26491ebd020a02bb485e98c5c6bb9766427900580ae9c41e6e12524`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:20 GMT
ADD file:3b750ce7e7425c1cb02261d65b1e301d5818cda51a80dc8ab3b915ee5ca37d4e in / 
# Tue, 30 Mar 2021 21:59:21 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 23:19:20 GMT
ARG version=1.8.0_292.b10-1
# Tue, 20 Apr 2021 23:19:40 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Apr 2021 23:19:41 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:19:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:99a21848b482c10fd4b103b7ab95e1446142e76e3dfa673efd0a23fb264ec5e5`  
		Last Modified: Tue, 30 Mar 2021 13:54:37 GMT  
		Size: 61.9 MB (61946585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ece89ed8d5944dabfaaa536301db77053bc6a2a996a272109b639f20b9cfca`  
		Last Modified: Tue, 20 Apr 2021 23:21:24 GMT  
		Size: 75.3 MB (75291677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:63b87dc056c11913fd13a02a6cd6a2d15e881b17021be3cd76bb452d7d09932c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123049888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7684c1b0eb2a94a3e457a5cc240c76ab7140b4d211a6927a2e712480350a8e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:59:58 GMT
ADD file:540e42c4903b87925bc490b00820f555e531041d1b1fcea6ee56f4cc3bbc895d in / 
# Tue, 30 Mar 2021 22:00:02 GMT
CMD ["/bin/bash"]
# Tue, 20 Apr 2021 23:43:19 GMT
ARG version=1.8.0_292.b10-1
# Tue, 20 Apr 2021 23:43:53 GMT
# ARGS: version=1.8.0_292.b10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 20 Apr 2021 23:43:55 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:43:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7d8296f22a3c3f786ce15fb5be7dce44af09932e617f9a981183619985014031`  
		Last Modified: Tue, 30 Mar 2021 22:01:09 GMT  
		Size: 63.7 MB (63660038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19674c905fc4a155e31837e0f8b91c7a503bd185ffae72d35ce7877265d63dae`  
		Last Modified: Tue, 20 Apr 2021 23:45:24 GMT  
		Size: 59.4 MB (59389850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
