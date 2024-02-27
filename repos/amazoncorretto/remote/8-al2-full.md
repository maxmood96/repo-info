## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:a07ee8b023bbd2110daede9bf18a3700f81ff1f5b3aa10ae9b6034c0c4960fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:417a271a4d8a475920f939e86ced3c452585f27adc7067c7d71d8bed23e59a90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138247759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd162b71c8440d2350b9fb7521ed841e1d5e959fcd18febe0ae483acc44086d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:52:13 GMT
COPY dir:54de4a09e8ed7b6d891ffc8d82bcabfb18706cd08eadb7193bbf9e8397ee4d73 in / 
# Mon, 26 Feb 2024 22:52:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:08:34 GMT
ARG version=1.8.0_402.b08-1
# Mon, 26 Feb 2024 23:08:55 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Feb 2024 23:08:56 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:08:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e24f20ed38d851720ffd5b15a06dad772c10fa9feea0e462fb5065d997fcb0bb`  
		Last Modified: Sat, 24 Feb 2024 04:13:54 GMT  
		Size: 62.6 MB (62646731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1e711ade82ff110dfe45616e36c0b9e7e23053ea07ba5b82ecc5b52d4c28b6`  
		Last Modified: Mon, 26 Feb 2024 23:22:44 GMT  
		Size: 75.6 MB (75601028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a7eddf765ccc0cf7cffecd93831cee5bac4434395fd0b8ca95facf944c5f5baf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124055013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f547aea4ebce9b801d5097df44bf477b0bf12bf0af0a966497a5589e66c641d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:29 GMT
COPY dir:ed6a811a4137d0b4591f2c9dabfdd849cb878c3501af91aa79c89a2e9f4479d5 in / 
# Mon, 26 Feb 2024 23:06:30 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:35:47 GMT
ARG version=1.8.0_402.b08-1
# Mon, 26 Feb 2024 23:36:04 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Mon, 26 Feb 2024 23:36:05 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:36:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:53f483bd5fa48049d6551a641e547b302df82b17493915161f3f62020b3648fa`  
		Last Modified: Mon, 26 Feb 2024 23:07:06 GMT  
		Size: 64.4 MB (64445079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c52acaf1eaf6846aaef9af2e579861236cf57491edcecedcda4eca68485f59`  
		Last Modified: Mon, 26 Feb 2024 23:46:19 GMT  
		Size: 59.6 MB (59609934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
