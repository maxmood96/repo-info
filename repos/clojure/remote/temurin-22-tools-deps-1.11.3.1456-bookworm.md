## `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:338262fe73d9e165ed703b79dec6d8ce7194979d3ae5546f22f388595fafb001
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a62a2170cc573cb3d32c2875550f1bf0e6d5ee103ec974d9a0d02e176bd363c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286784754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c729b20876de3ff55dac80d03f4cd603fe6af4927818e27aebe9e6716b31e59c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ca994ce711f660090f8c9c14d9b14d6b5740ffe0739f7fd73d4ec693a12988`  
		Last Modified: Tue, 23 Jul 2024 07:14:18 GMT  
		Size: 156.7 MB (156715517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857a5d682765d318881d697560e56befe91276b7b4b09118eac488c077b73e4e`  
		Last Modified: Tue, 23 Jul 2024 07:14:21 GMT  
		Size: 80.5 MB (80514122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a40c228088b57c01e3e55e41aaa5e2bc8452a5f1a70b6de7c22f886d43eba52`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad6b3b945a93a5b46a130156c74633549e1dc561255ef15c5a3dcd79fbb0fcd`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:af25ba55625b0ebce5b16dc9ecfe6481f888c37ee5943bfc2261300f8d55d480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439765d1a5edd72971dd017561d6188ce9c66a1fdf543060d962a03c88f133b2`

```dockerfile
```

-	Layers:
	-	`sha256:51ae15c045fd8eb0a483f411d85f85b3fe47d611e63435a3518113c419d58aff`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 7.0 MB (7000764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3080be4b7282e34dad4ed40460b2b32959c95d81ad569ce60f2d7ae616e8c5f1`  
		Last Modified: Tue, 23 Jul 2024 07:14:20 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f7259b0a2fb600e89e28713e6a11fd94170588ef8cc034c982a5a39accab5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284589551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba296e5b10db6f8a2950dc26ba54a9cbd29b106585dce5180e24a01e78df41e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9254cd7885a46cc591cf9840aabe35758607f7cbcb4c312e42de17c9d452823`  
		Last Modified: Tue, 02 Jul 2024 09:43:32 GMT  
		Size: 154.7 MB (154737984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719cab993bc935472d0623b365be6e2ec9314f2ed52c8f3a033f2715c95aef5`  
		Last Modified: Tue, 02 Jul 2024 09:47:44 GMT  
		Size: 80.3 MB (80262078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63e74d0584d95006eebac5d07872e4d98107e2215364e09d5a9ef1fee33f38a`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de9aff301618aac1970e3a3af271b07170b6b62d31b99974d87ecac735e1a83`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:460bf55bd8a577602fb71ef57e96cec40f6ddcd84b35f7ef369a03ac726a3cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6983733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8186959b6e396230607f2f4f357204f89c74d0a22d6b78e85b9afcec48b138`

```dockerfile
```

-	Layers:
	-	`sha256:f14422122cb0d0b117e3216f5257eeae14280b79227577f619feb3f86ce5fa07`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 7.0 MB (6967050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0afb5aeef062c5d3319118fe66be6f78d1c9f99edc71445a59d97e2e931773`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 16.7 KB (16683 bytes)  
		MIME: application/vnd.in-toto+json
