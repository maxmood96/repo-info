## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:8ebc8b6d026b7fb2132bf1ef43713d98711a510ad44a2aee39ec2c24ca53d038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ca83695b26e05524a6651d127778fe0417ad22b1b8494bbd2af78b48c971f7e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214267650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da93272f1edc2b39472d4de7d14c5acb730f8b5d848700c1872d9d1db0a7a939`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 01:19:49 GMT
ADD file:a69ca7a5499bcd9d6e4317fdbd7256e93be44364bb746f5da10b4268c090bda0 in / 
# Fri, 16 Dec 2022 01:19:50 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:25:51 GMT
ARG version=17.0.6.10-1
# Wed, 18 Jan 2023 20:26:15 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:26:16 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:26:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5b4a36b5b78f93a5f470cf722b313bb32cddb0f8e0fa0db348059b5c0881b04f`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 62.3 MB (62328625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ee8a6c9205e9f9a894c9378a38b037be0ecaa9b9ea1f6f7617b9d77deb36d7`  
		Last Modified: Wed, 18 Jan 2023 20:38:36 GMT  
		Size: 151.9 MB (151939025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:64e63be1a38e166862098baf72bcc94c9191c1ce45ab62145cf47e03e2fcdbe9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214444719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d0072f56922dde9c2dc8bbf950e9d05c5c150de99f3f4562714943a3180ac5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:05 GMT
ADD file:26a6bf75c84c408d289e5569f13b1c65206966f875cdfc53ded0670cb85e35bf in / 
# Fri, 16 Dec 2022 00:41:07 GMT
CMD ["/bin/bash"]
# Wed, 18 Jan 2023 20:41:07 GMT
ARG version=17.0.6.10-1
# Wed, 18 Jan 2023 20:41:26 GMT
# ARGS: version=17.0.6.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 18 Jan 2023 20:41:28 GMT
ENV LANG=C.UTF-8
# Wed, 18 Jan 2023 20:41:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6cbfee25f0741b3d3f4d2474d904a200cd8404a01aa17813bf3fc3d4ebb551a4`  
		Last Modified: Thu, 15 Dec 2022 23:08:20 GMT  
		Size: 64.0 MB (63964214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9771c806ef58fff9dc805fc6ce87c7fd26ed16072fc9ba0f38c907d32e2ed9`  
		Last Modified: Wed, 18 Jan 2023 20:45:45 GMT  
		Size: 150.5 MB (150480505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
