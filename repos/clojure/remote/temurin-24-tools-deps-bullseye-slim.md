## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9f301280279984a91037b488dbdcd30538b74387dc849342390e3985cd46cee3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f943b4d4070746894eb766a7e78ec1129e4737b0068db4786e2f229122129fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179214288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6326ab3e7967477193d575eb43fb58300a616f18adea7498af3b82e686b7b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7940a8a0e27cb1719340841c1644ad5988e40de50a0966af7bc28d087ea034b`  
		Last Modified: Mon, 09 Jun 2025 19:19:41 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c010e11a30790a1e2bbf26edae7ee72933c0e7372ffc72941b323041544c0cca`  
		Last Modified: Mon, 09 Jun 2025 19:19:40 GMT  
		Size: 59.0 MB (59005305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d9146f8cc9205160618412db44c43279c21b0e0b1ffa7aeab30d8ddcc45806`  
		Last Modified: Mon, 09 Jun 2025 19:19:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1c4209aee449c4a219a714ef88ac6bf4267dbf9ecca16ad253dcbd38f67a26`  
		Last Modified: Mon, 09 Jun 2025 19:19:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e35a0e4cc7049b4b18851336b073da87760d0d776234bed04b1eff5fcde3aa82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3d259424fda02fb96c8a933ba0afac51c30150e5509d65a0c0d0d32f23806c`

```dockerfile
```

-	Layers:
	-	`sha256:9476d392a3cb54e03bce5890df70195ce588ed78aafeabd97d2658930d6e687a`  
		Last Modified: Mon, 09 Jun 2025 18:41:16 GMT  
		Size: 5.3 MB (5260308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3282c3bf5b389ce8d6fab6240d8bc41f4c86f317235a20d1f0696ea1d237c1`  
		Last Modified: Mon, 09 Jun 2025 18:41:18 GMT  
		Size: 15.9 KB (15872 bytes)  
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
