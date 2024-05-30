## `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:b88c073a933e92cba2500651259bc548812086b46433ebb6b47453f1810e041b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dcda4c442a563e9ad55eb052db1b9cc6ad0d430e5b5fe4d793f76df8ffa21682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274966388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09174165ee62a4c5b1574039801687c3ea23d03924029fe9074e6d55f6400ede`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5603cd52c814a5d4b4a42bc9f33dbed8a99689d7f6efb1f402ef4272f2020b75`  
		Last Modified: Wed, 29 May 2024 19:57:15 GMT  
		Size: 145.1 MB (145095078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6f1ced0707a45db84ea611d9d465d03a76af00f4ec36490fb86c22fe753778`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 80.3 MB (80293871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff58d053538d7962b27c9b26788f7691ce4398a1da493a7667ebbbb1c6b214ba`  
		Last Modified: Wed, 29 May 2024 19:57:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa0200b67c3faa7155c0c0c24d801bc065935bb04a9d9434613581de923f19e`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:51b6d79ef569a747033800cf769d32579bf4535b117dc60b65e53c32e0f05c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6976057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1341f554569070e3f8231d971fe98a3410bae78d6601a307cfe5e8c5081cf`

```dockerfile
```

-	Layers:
	-	`sha256:a917e2a32cd621788f1147e3243b8f054879d7667a6d19ba3e22031a5bd64db6`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 7.0 MB (6960667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07815bf87cad64c927c00902d8c8ffed46ac3725c28daaf30e7d68ab59a200e9`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 15.4 KB (15390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d8870156de157966ddeafdd1f89c08c4896ac97c46378b2f401480915ad39e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273552293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a305e23ed40dd11ecf984edf1f91a93f5e303c93aaaa5f0436782f86fb4e9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbee6316dd5a09d22ef8a73e7805e971c35f28682e238f1ab33ffbb4ead1df2`  
		Last Modified: Wed, 29 May 2024 21:38:43 GMT  
		Size: 143.9 MB (143892768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cea9f22482255391b0ab25d86530ad2613fbda8dec630b3a6b754cac0f2cd89`  
		Last Modified: Wed, 29 May 2024 21:43:50 GMT  
		Size: 80.0 MB (80045092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf6c79228b30a2d12f2bd3c31fc87c2f11c26e839718dcd0e3f4b3a7224349c`  
		Last Modified: Wed, 29 May 2024 21:43:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2f5e3c547a26b965d011b5e25bddc5f1fd13c02c28601acacc667f768753cd`  
		Last Modified: Wed, 29 May 2024 21:43:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c627c72154b94c4fde402e7085d8be4183c1c91e0dd5ea76a44685ec3d9deb2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6982980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf7884cfb03557094e7161bfbf4d7bc0a3d39e92cbbfe2b60fde7c2d6512a2c`

```dockerfile
```

-	Layers:
	-	`sha256:3852eeed80ef96b84dcc94cb2cb55a72f07fc27fa37b20c771588543124480e5`  
		Last Modified: Wed, 29 May 2024 21:43:49 GMT  
		Size: 7.0 MB (6967054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f734f414922a6e85f99ee219264c4b31b0b24bba823e6e282b39059e2f267b4`  
		Last Modified: Wed, 29 May 2024 21:43:47 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json
