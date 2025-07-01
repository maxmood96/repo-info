## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:801a142426d8229f1bf33db89d7386898b116badda21b4b43ecf49addb68f012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6bc04a539402a0c6914930e5d7083a2beb4030f1ab68752397f90fdf3507db25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179214869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979393893d26c237cd4f5f167b6eb84b02326d227085b1695ef8132c6185cefb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48348d2867466dc769c153a1acec279d1b9a0d6b9dad8d405d0f14294143782f`  
		Last Modified: Tue, 01 Jul 2025 02:40:46 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9daaaa241b8ef64abfe24cdd4c37e21601e65ea966a35c2fa632c3e23f4386`  
		Last Modified: Tue, 01 Jul 2025 12:55:50 GMT  
		Size: 59.0 MB (59005783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa900d844629288fbead9d6920f99279db2dc247b06bef58eacc75c54a7e73b7`  
		Last Modified: Tue, 01 Jul 2025 12:55:46 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa336eac294ad0d0c3feb8426cd6af52a19b350a44e23d0d2be4c3c86c7545a`  
		Last Modified: Tue, 01 Jul 2025 12:55:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6437c37d28aae8b6a4b65292c52ac74dd31b6ec56c4432c85abf3c3582d4d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830d534ea0d1118220951ce3e0fa82d223af0be0ba53fcc0b58a07577923f129`

```dockerfile
```

-	Layers:
	-	`sha256:869525adb4dcf13509dd8eeb63cde4c55edf351f9e71dc901267ed465a2de432`  
		Last Modified: Tue, 01 Jul 2025 06:40:26 GMT  
		Size: 5.3 MB (5258684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4bf1a09bf77a32bff652aa4b9b58656736b70dc5a4d2775d6a7db18affae8e5`  
		Last Modified: Tue, 01 Jul 2025 06:40:27 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b203d57a96644b989132cceffe94935b46178cb5a492dc00aad07c31a2dfaa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176974144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69e9dd1a35ab58a2c25bf83de2283df23a95581f7ef8c7aac0093f27310a16e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d483855ee265b40a7a56a2fb85f6b6b96648be553f96cfe9ba7c84939144ab81`  
		Last Modified: Tue, 01 Jul 2025 12:39:31 GMT  
		Size: 89.1 MB (89091269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75a863efcf22e68dfd7accc3dd6309178fb1bf7206863a5aba0041e0ddb11a2`  
		Last Modified: Tue, 01 Jul 2025 12:43:57 GMT  
		Size: 59.1 MB (59137696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6d0adf0afd3e636b7a2c2fe78c2bcdec6a09a403137f9d9027ed9ee5f9ffea`  
		Last Modified: Tue, 01 Jul 2025 12:44:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60ed3ee8bd0492f9f2642bf2b6febfbb25362f1c4ab686a3299e45e7273b032`  
		Last Modified: Tue, 01 Jul 2025 12:44:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b71a18774592dafea44e688eb23823ba59323f2612aa50ee891529ff134c7c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c3cc4606479ac68a217481f48283fa4f9857fc803c1d61d276961556799309`

```dockerfile
```

-	Layers:
	-	`sha256:bcb7c7684954f98dabc344cfd7cdb3a9f39e3300c4f26f210db4837e1f4d8e67`  
		Last Modified: Tue, 01 Jul 2025 15:40:02 GMT  
		Size: 5.3 MB (5264413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d81773d73772943c44a67c2eb56aae058245c0706a27de92932579670ebe4db`  
		Last Modified: Tue, 01 Jul 2025 15:40:03 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
