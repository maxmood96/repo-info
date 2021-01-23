## `amazoncorretto:15-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:5d44cf594cd4e4de912bc559e5f13b1c36d4b83521216598dbb9e44a4367d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:15-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c1e48b8f4425b79d9362dce8c60a88b176dfa21f56376eae85dc35c6749b482
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.7 MB (217674174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a27ac94a60e769b27d4855d5e2323483542468f10499edf1a85ae070366d35`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:20:01 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:20:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:20:20 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75963262766311d0a7d40f30c07fffa202b9e5b32f35d6cfb70ad51ce630e0f6`  
		Last Modified: Fri, 22 Jan 2021 23:21:25 GMT  
		Size: 155.7 MB (155666746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:15-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6402bb83f45546a8ba0f4b7ed67c1bdb0b179d8ba3a6e22ef168aa345e47537
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219246874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e086e2e140090c710c358ccc49358023e86b0e1f23f38e7a00b15862d7afba7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 19:39:59 GMT
ADD file:d991483ad4376be5e4327b3789511ab9266db8b87fc4b5327f0cabd1016ba00a in / 
# Wed, 23 Dec 2020 19:40:02 GMT
CMD ["/bin/bash"]
# Fri, 22 Jan 2021 23:39:43 GMT
ARG version=15.0.2.7-1
# Fri, 22 Jan 2021 23:40:19 GMT
# ARGS: version=15.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-15-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-15-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 22 Jan 2021 23:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:40:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-15-amazon-corretto
```

-	Layers:
	-	`sha256:3307d2ab2034125075f0b058dcc32d6bf3e2c0595f1306de08d9e4a0287ddd76`  
		Last Modified: Wed, 23 Dec 2020 19:40:59 GMT  
		Size: 63.7 MB (63707914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97903ed68d862654dd466114bfa7e540200c8cdced49a5d6dc002e7cdd346f38`  
		Last Modified: Fri, 22 Jan 2021 23:41:13 GMT  
		Size: 155.5 MB (155538960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
