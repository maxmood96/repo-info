## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:dcd3cf72ebc9bec59a3c8bf5b5538c7bacf84f50b45054a43eee41ed6c1fcca5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61c010eb2c9b2ad7c91023ae0ca7b6e1e570a187ee69bef6e8c6684984b4c835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179214679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:683b3708fb6664412b62b43589119b28827259bbe370fdd38b0091e8607e08c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ade5661204e6e829a6794399fe4630b1684e2a39ad112a2ad314b87b267e6e2`  
		Last Modified: Tue, 10 Jun 2025 23:53:30 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a70e0ee4ec10249b7a098ba46e4d2620ecbe082379b9a6430002ee6755bad`  
		Last Modified: Tue, 10 Jun 2025 23:53:25 GMT  
		Size: 59.0 MB (59005572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6b58653c1ae356bc714e2ff5e05444df1beeeade6799c94fd3487065b4f120`  
		Last Modified: Tue, 10 Jun 2025 23:53:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7a58fe448d023f73a9731fa54a930b43ccca1000f01a6373341ce04123b32c`  
		Last Modified: Tue, 10 Jun 2025 23:53:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af8a8c9c1dec625e48bba13acf9567986dda91413cce88403080a9548dd76cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee16c7a4849013fafaa6594c3b73886430bfdf7e9e593cd5186f85c5d0f3092`

```dockerfile
```

-	Layers:
	-	`sha256:9094269d32f82f65b0873e4a34f69e205322237d54264d229cfd77408f2cb87d`  
		Last Modified: Wed, 11 Jun 2025 03:39:49 GMT  
		Size: 5.3 MB (5258684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a0d364bb1f5a4af3d75bbdefb520eb2de90af55ff9261073f6d2f848d5e6d1`  
		Last Modified: Wed, 11 Jun 2025 03:39:50 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bd716daeafe985922e4081d2bb209dc5ed154f5671a67cf1ba072e889b6c8e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176976075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0216ac96b6c3b5ebe691b59226896e8432c2db0c89c103afb31824a704aca6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bded46ee81e89e59e64c533c353440bea9d4be7e5e0f2def77398507b60fd0f`  
		Last Modified: Tue, 03 Jun 2025 21:26:27 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617d2e941b5a8d336ac455a6b57a614452e6b6d2e2a8a44e92b612bb7c859cc`  
		Last Modified: Mon, 09 Jun 2025 18:00:55 GMT  
		Size: 59.1 MB (59137504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb517819ae0717c399f95861e79d0d9718d44befa3a1c42487816a529690d0`  
		Last Modified: Mon, 09 Jun 2025 18:00:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa15176a19901889642d201788d71e55b80944b6a96a2004d3ecbe4bc37d2a4e`  
		Last Modified: Mon, 09 Jun 2025 18:00:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc6a321e96938203a906d1601a1c155fc3b4fa2edc652ef3b11ecb7c0ac699e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2dddb2d2d38dbcf3795841f399e94108c95f77b5c32c3d3ac7245fd2295259`

```dockerfile
```

-	Layers:
	-	`sha256:354bef7d04b7905b5093ecd45206c69dffd63d1ea63b6c6f9541bf5c58545fd6`  
		Last Modified: Mon, 09 Jun 2025 18:41:23 GMT  
		Size: 5.3 MB (5266037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c33ec242b4c1761c1dcbc612332152f8059eb45cb676cb19f2e649d7ae77aa`  
		Last Modified: Mon, 09 Jun 2025 18:41:24 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
