## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:0a41b7d696943c251ed6bf29e09f47273f189078bc7e783bba63da0eb4a1e758
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7525dc2b7bf3980f7c04c4df568cb274a18c69b7c86f13b0882c279f08ca43f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247215265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c37a7b269fea4e83d2c09f2a3abd280a8f6ace9e0d976ca2aa696d41057d04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051b084dffcc32737f3f7f01122fd6d83128ae86aa6165aa99896da9c5066521`  
		Last Modified: Tue, 21 Oct 2025 10:51:35 GMT  
		Size: 157.8 MB (157804769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359832a7559cebbbe7e73dfa4d1f2f5951833e8aac41af74bb4b107c12c295de`  
		Last Modified: Tue, 21 Oct 2025 02:23:43 GMT  
		Size: 59.2 MB (59151090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6775683dda89ee03d7069f85aeb7a4bcb3f5ec477182fbe666c06af54c46d`  
		Last Modified: Tue, 21 Oct 2025 02:23:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe83654cc7f1662f86977be93e70590fde6bc2c5912f3b4cca89406a01a2f2a`  
		Last Modified: Tue, 21 Oct 2025 02:23:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:953d27bdbad542a54b3304707281772dc2850c76da4624f0152250f54b6865b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c29b5d6f33ba65ea52a82e52b8a859add0a6995458eb788529475d7598bee2`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f91f7f93e91b9bae7d356665da0387c2450577055ded52bac74cd334a3192`  
		Last Modified: Tue, 21 Oct 2025 09:41:28 GMT  
		Size: 5.3 MB (5311169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:879a5aace326d6367088df81619269622de9454e35ae91a1ed9f2d2360bc08ba`  
		Last Modified: Tue, 21 Oct 2025 09:41:29 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7a007e0044ec8c94204e774b4e08b752214c3c4a13667bfaa264d0d8d4c1ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244118073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd99547f77d069c3182c8ba5e42dc3fd06d25f1ce3ef84a2c26f03e887bb098`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c58427f0e485063420619bb5b5890b8de24bc0ca9e1890b5614e50166d3173`  
		Last Modified: Tue, 21 Oct 2025 08:45:48 GMT  
		Size: 156.1 MB (156081199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980867f0311b137517566df32f272a2383d813141dce16472aab3348df7bb351`  
		Last Modified: Tue, 21 Oct 2025 08:39:27 GMT  
		Size: 59.3 MB (59287431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72c42fdfa32716c92ce7a62f071d409a022189e73f65b7ebc0042dde19a3794`  
		Last Modified: Tue, 21 Oct 2025 08:39:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0da91e12b848108f767f624e086a16ce86ff0631a7bb66aa1e160a6b5ed5b1`  
		Last Modified: Tue, 21 Oct 2025 08:39:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b995b738ce34f5bad7a734fc3d14d316b2d3faa9bcbe95276251c570553b8b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60df0224bfc66861005481e387191be47472d276bb806c17959d2a2beb0f218f`

```dockerfile
```

-	Layers:
	-	`sha256:94391b4f6eef6f69030b8f6285651f159b9f6d76b652152e098ccb2522e0559e`  
		Last Modified: Tue, 21 Oct 2025 09:41:34 GMT  
		Size: 5.3 MB (5316901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4541fc0908587496d23333181e7ac479660d47896e69d6ca5b2a9f5d924f97`  
		Last Modified: Tue, 21 Oct 2025 09:41:35 GMT  
		Size: 15.2 KB (15195 bytes)  
		MIME: application/vnd.in-toto+json
