## `clojure:temurin-24-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:dcc4032318e53875d4d0017df7b9a8fc4d6886412746c255ab2e9473bdeed0b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:57ae138f85b698245b82fbd3c7f3a8a570cc15ac13baa90b5238ca735a26c3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212880595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2cc1b505a3dc345a861d770166320dc698b99f3ca6fcf58773ba96a6ba136c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931ad01a871aec2959139c81470045172028e38c81c93221323c9787e348c593`  
		Last Modified: Thu, 27 Mar 2025 17:53:38 GMT  
		Size: 89.9 MB (89949034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ff134734b118a60d041acc9e411ce84d9b0046ac971323cfab2b0b5d48599`  
		Last Modified: Thu, 27 Mar 2025 17:53:38 GMT  
		Size: 69.2 MB (69189246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8399f7536c4cfe86de23ed3026a426a0135bb1b5c1bca6e19609a5d8eb90d223`  
		Last Modified: Thu, 27 Mar 2025 17:53:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d853647818acea64b84b647fc36a65a447caf8c35411b228341565d046cf61b3`  
		Last Modified: Thu, 27 Mar 2025 17:53:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:53a066a3b4a2c0fd4d7e7724a975216731b5f164797607b7032e010addfbe083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7171000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b40f49db230080404bc9f98df7d284b467ad3b7340c7aab3ca07e976f5ffb4`

```dockerfile
```

-	Layers:
	-	`sha256:4f1343c2cb56e2963c56e3c35bcb48e89a30bdb27c9dcab57adb39fec8558c95`  
		Last Modified: Thu, 27 Mar 2025 17:53:37 GMT  
		Size: 7.2 MB (7155187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c5ece7be041ba689e2759733cb6aa95955240f9e0f81f75f94a9a7f7d80ee45`  
		Last Modified: Thu, 27 Mar 2025 17:53:37 GMT  
		Size: 15.8 KB (15813 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3dbc5a5728945491a1317d19b79567a2b9b9392d88e782da37bd1b8a0d8887b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.7 MB (210666630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cb2ff78c25a91cb5a1167cc9a10abbed3590894042fba6c3d9416b8dbd2ebf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cff61800d77fea8ceca86197d0088a545723471fc54b8d8f0c4585f35410dd`  
		Last Modified: Thu, 27 Mar 2025 17:55:17 GMT  
		Size: 89.1 MB (89092706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f12c4fe3996f585212279472c4932a72c8f0445af43b72391e61e4616f5a53`  
		Last Modified: Thu, 27 Mar 2025 18:00:17 GMT  
		Size: 69.3 MB (69324491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee96c4dd30698f263f5a2e145c1ce8845223f09f2ba1241d2480432fd168779`  
		Last Modified: Thu, 27 Mar 2025 18:00:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce0e8e187e9966521202f8e09f822719b18b1f778e7d30bac5723cf992d4698`  
		Last Modified: Thu, 27 Mar 2025 18:00:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:debda77c57f5f7b3952305ad3a5eb23a1188a67b3abc41ae7b5636ddceeb9ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad947b762e777059a7aa9b2df2e2c7a8946f928632d0c17a6803f7981255760e`

```dockerfile
```

-	Layers:
	-	`sha256:34cdd44bfe00f1d62decd7c70ef30e048724de318fd26df29f32dcc855b014fc`  
		Last Modified: Thu, 27 Mar 2025 18:00:15 GMT  
		Size: 7.2 MB (7160283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81402ce84e9fa14efdd8cefa74340bf7017a8d6e50d9bb11c522b88c7558cdfc`  
		Last Modified: Thu, 27 Mar 2025 18:00:14 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
