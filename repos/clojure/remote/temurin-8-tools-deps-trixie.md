## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:843be2682f2dc3b174af9095e5d2e0eef69465a9a58cb87f8519f764b62c6f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e14520a70418df3a52b020aee8a31df41dfb6a7f8a5d398d594b33832a2bbae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189557722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b294e7e99abaf2def4ad8b0fa6483d94711119643799cc9a1cbb7cfb2944a21`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:29:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:29:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:29:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:29:58 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:29:58 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:30:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:30:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:30:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83451a89c64b14e75322f691f6056a80a5cf375e95e456fe2d70d8c7b202a02e`  
		Last Modified: Tue, 04 Nov 2025 04:30:47 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31954aeea07a175af8c2ec530092cc7e761fbc2e4e7c86681d23d1a5ac83724`  
		Last Modified: Tue, 04 Nov 2025 04:30:45 GMT  
		Size: 85.5 MB (85540158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfd4cb917783fcb67f55514a9920462d5b6f2de93da5e91fc2ae0dc8e2cb9f3`  
		Last Modified: Tue, 04 Nov 2025 04:30:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d65d42bf8f629e7b029e652ada9feac56f8b7edf839384af0a2e695b7186222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d177114a564ebfe59694b92b1e1420a20ed1b13000b22754841337ae5fbb51d5`

```dockerfile
```

-	Layers:
	-	`sha256:865c27abc3e35ceb6c99c2763f1d4768cfed36bcb3671065d7d4be6887d94199`  
		Last Modified: Tue, 04 Nov 2025 10:49:28 GMT  
		Size: 7.6 MB (7588509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d445f56b6ca8341f7167b27642a75e8d561a6775ce40fa0aba4bad5ecb019f01`  
		Last Modified: Tue, 04 Nov 2025 10:49:28 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a9546d50fba44892d2a6ee68b93f0110e1df6563a0f7c44c1725d2ca2101550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188850032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb51239120d662a40832868de1b8e2ea5ba6997cb9e2d57ee623562fe1db1dc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:43:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:43:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:43:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:43:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:43:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012cfff097586e0e345ff08545d54aad49cc1b7405c28acf74e13ba2aaef1ae4`  
		Last Modified: Tue, 04 Nov 2025 01:44:30 GMT  
		Size: 53.8 MB (53835630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962512242c36d05b976e7935ee3b00d7c13cecae688d52a1cb2a2782620b7bf8`  
		Last Modified: Tue, 04 Nov 2025 01:44:37 GMT  
		Size: 85.4 MB (85363328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fd133bdd3678529d87d6a792f4bc5e963808d20e45bff3b5559a209bde056a`  
		Last Modified: Tue, 04 Nov 2025 01:44:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dfba9379c0c33d6d3ded3d5c255d214319b8b73edb57ca48fb6fbc274688111a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c4b26e34b89c4b1e4aaab838263cb47da95178529a6cd16ca14f3db6a7f170`

```dockerfile
```

-	Layers:
	-	`sha256:98404a2ac06423d2185f9b199a7a732e2c31342e18bbc9e7a3c2ce22965014e4`  
		Last Modified: Tue, 04 Nov 2025 10:49:34 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db03c94b2430d7dd10647320724b3ad679de0efec9a56bf822389c5040bca8d8`  
		Last Modified: Tue, 04 Nov 2025 10:49:35 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:08f8dc124d683296a768fc81d8bcfb13be1305a9a474f04f0a975f38e9ed6e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196225728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e35e7a77b7458247e244838a47e78982b3910621cf04b140a9b6af754834a09`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:02:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:02:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:02:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:02:16 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:07:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:07:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:07:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431f20163584da71198702546386fbb961546d955c4c1930a7d523c1e219f1cd`  
		Last Modified: Tue, 04 Nov 2025 13:03:55 GMT  
		Size: 52.2 MB (52165358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dffe9164d90ff58e4fc614f3fe2a78b70f166009b7de0cb9407c02343826ac`  
		Last Modified: Tue, 04 Nov 2025 13:09:03 GMT  
		Size: 90.9 MB (90949596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b185f0385f706cb3b0ab7d5ca0ccc14cdcec42428c059d5d9a09057a52690418`  
		Last Modified: Tue, 04 Nov 2025 13:08:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa85284725bfddc2c9f8a44de813c93acac07a337c174303ff1e95e4e1add5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316a93df6f1800ce3054f855d6200463e340ce5def06cd96f0ed7e03fe585fee`

```dockerfile
```

-	Layers:
	-	`sha256:0673543f1db6803d8aade18bba77d277b7ade16f25690d59f00c301020c56620`  
		Last Modified: Tue, 04 Nov 2025 16:41:16 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06a54f56d87d73b267b427371bf522adce171e905f772aa9329a2edffcc9b806`  
		Last Modified: Tue, 04 Nov 2025 16:41:17 GMT  
		Size: 13.4 KB (13418 bytes)  
		MIME: application/vnd.in-toto+json
