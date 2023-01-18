## `amazoncorretto:19-al2-full`

```console
$ docker pull amazoncorretto@sha256:848e933cdc4cf2311141de0c303379a425164e985b34af9ed5b16d5ad9a393b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:19-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:484106e8c9705bcc8e7b5e2f6520c292d874582054704c2dc523ff3d11c865b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221737381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0859e8f7f359e9d129ccc4925733c72c0c6230525a174fde4dd36726346679`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:27:55 GMT
ARG version=19.0.2.7-1
# Wed, 18 Jan 2023 20:28:18 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:28:19 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:28:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36c65bc78102a904e3a35faa408837a12013ea25492442f420688b775b754dc`  
		Last Modified: Wed, 18 Jan 2023 20:42:06 GMT  
		Size: 159.4 MB (159408756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:19-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a1c7eacfe4cf86f2be663aa16c59691848a0e4a6de578a095b9e2481c73d68e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221813435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d634aea444c49d2a8c48026830d678a5b927da645c497df83e052c7445d25f69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:42:22 GMT
ARG version=19.0.2.7-1
# Wed, 18 Jan 2023 20:42:40 GMT
# ARGS: version=19.0.2.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-19-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-19-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:42:42 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:42:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-19-amazon-corretto
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c2588cc46ed421f6a34ad9de2a03fee31c823d0d6d6bf3a6be37acdc2b9cf6`  
		Last Modified: Wed, 18 Jan 2023 20:47:06 GMT  
		Size: 157.8 MB (157849221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
