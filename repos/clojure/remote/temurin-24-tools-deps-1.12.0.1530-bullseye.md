## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:68303b9a3d0b4afbf32ea4d1a60b9ef5b88d57663dc9988d32fc9bb03b96a360
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:604932363a810bde8009533b50b70826024bc2f8a9cabb01bebe8175b6b94967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213101492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d43ea5de887f49c1cffd3253586e12483ad1a80f997cb2162be2b50fceca6f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30fcc19a67f7c23934d4a55148b82ba9143aa778f81d154eaed249b614c1116`  
		Last Modified: Tue, 03 Jun 2025 05:17:00 GMT  
		Size: 90.0 MB (89952002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4cc8937861d21162cdae93e7dad1f66c8961ec395353acbf957ee181d638e6`  
		Last Modified: Tue, 03 Jun 2025 05:17:00 GMT  
		Size: 69.4 MB (69398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e5915d6d84be2d7e923db732c42376f9bc4cf1dc08611d904d819afaaf4524`  
		Last Modified: Tue, 03 Jun 2025 05:16:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55093a0f991f40d56a7da4e780840f4282539463be476bd3eca3e23882bba8ea`  
		Last Modified: Tue, 03 Jun 2025 05:16:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4dbed1dc5dd1c1c1f93cdd38f3034ed8e2971ee151a1fb988440bc1c7f1735e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e997156d17e32096cb67e8f36f690278ad15a2e2f35260326d568de2aa93cd75`

```dockerfile
```

-	Layers:
	-	`sha256:c062656e2dd4e7c7ee07c26be4b5f609d4ecfb7ee2d22b7a689fe9c3b52b775b`  
		Last Modified: Tue, 03 Jun 2025 05:16:58 GMT  
		Size: 7.2 MB (7206832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2789a0be32c9aa7d111aa2f664a1c0f844fc0c99c1fb682c8278004d2c04e57`  
		Last Modified: Tue, 03 Jun 2025 05:16:57 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d5068ccb5ee1d57be31d7efde327516b6a127965f47c4836abbf53c4c467fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210870633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f3bf0a55daef4ada020a0742774ecbc919a26a86caed5000d67723af1cb359`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4d6f57ce17d9b1e545949e47ffb51eaaf6c23a96fe74a72056817227fcab22`  
		Last Modified: Thu, 22 May 2025 08:40:27 GMT  
		Size: 89.1 MB (89091270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750cdf9d6a9b431dafb25a25f6b93f903a23621c6981172e751fdbeaecb5e64`  
		Last Modified: Thu, 22 May 2025 08:45:25 GMT  
		Size: 69.5 MB (69530568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15b9792c5a80a2e5a9583213132dd3ac7e463f9d1ab319900db46c6ddad17dd`  
		Last Modified: Thu, 22 May 2025 08:45:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e3b03b288cdd376eb7c3562ab7b112a3c00b087a0836ac18497900d0cabd65`  
		Last Modified: Thu, 22 May 2025 08:45:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b2d1a05cb24fc2be87ab31ce1edc5ee22e94a35725f9b70bc11a29e3c52d0036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7226263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7e61dfb6458f163a75318c42ec3fb3378b76bc34c290e78cf2cd9df6ac9d3a`

```dockerfile
```

-	Layers:
	-	`sha256:fc4e362e5178ed29edfedde90b5d4c2c3fe06e8d51f7b5f33095a5bf488823f5`  
		Last Modified: Thu, 22 May 2025 08:45:23 GMT  
		Size: 7.2 MB (7210332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0aaa53533dfb4160ae792ab371d95f8be333de051f961d2429b28dddc2142a8`  
		Last Modified: Thu, 22 May 2025 08:45:22 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json
