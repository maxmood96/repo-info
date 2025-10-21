## `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:747a73dbe75e08ae18dba7979c680096a10d2dc93b0f5a8f5eedf535f2f910fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4776f626cadb7ee6e20b61d3de6f20cc41dbbb8c83b855bea3a44aad3b12dc91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234103677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ef219a394c875beea8d968a13c0fa4aacaf529b4f721b802880f503c818135`
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
	-	`sha256:152c8c75acf05c2851cc23c10bd4fb9ca3cfaa0dea296dd2bea1471bfaae9959`  
		Last Modified: Tue, 21 Oct 2025 11:44:56 GMT  
		Size: 144.7 MB (144693292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36922efef9b74660e8281088c898f99d8d737605292a65133405c4e101b45bc3`  
		Last Modified: Tue, 21 Oct 2025 02:22:23 GMT  
		Size: 59.2 MB (59150979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f6d6de7397d45cc181bea3bec888fbf5c876c2ab9032cf118ab8ab0ba97eec`  
		Last Modified: Tue, 21 Oct 2025 02:22:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa14b711b9a6d90a940da3ebddcf5da58522dc1494f99e8afffd9bd23839546`  
		Last Modified: Tue, 21 Oct 2025 02:22:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43aacea7ac717b709cb89b6da95644c3f41ef706bedc0891b98d0265861e60a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927d331d6f6413a5452e1243d3934f1e27451012f6470d38037c9f7d65769ad3`

```dockerfile
```

-	Layers:
	-	`sha256:b5b3f82e378b54fc7d87e6e138b93d410022563aefbadbb78b7b71f876c99510`  
		Last Modified: Tue, 21 Oct 2025 09:38:42 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ae2066036d61ff627b7b6ad20371661aae2e920448525dde108d7771ea7f1c`  
		Last Modified: Tue, 21 Oct 2025 09:38:43 GMT  
		Size: 15.1 KB (15078 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f0567fd3a344587d5f848036a287507675b34847facb19e68c0b73ccece7400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231579113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc408c231d89f74a3a9c3149a76eae4698cfe2935c3f615c1fc47127f9d78f1f`
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
	-	`sha256:c3b3f234d4ffc37eb503c6ba834c3953f931772e7e63ccde1559493b034be564`  
		Last Modified: Tue, 21 Oct 2025 08:47:56 GMT  
		Size: 143.5 MB (143542158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf76a61c6bc3be755ffb4ebf80a8723100d7d94304b829eba2ecfb4e68eceff2`  
		Last Modified: Tue, 21 Oct 2025 02:28:00 GMT  
		Size: 59.3 MB (59287512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a90467513a6cf0f7db16901db3f4c59e9e175548d16a8c435bd2c3bfa2e371`  
		Last Modified: Tue, 21 Oct 2025 02:27:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641e6a0793c844ac70e8cf7fbd3c0e63e9c0f7ab873d65aac7afe88a8b5de5`  
		Last Modified: Tue, 21 Oct 2025 02:27:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b316c06ad5ceaf63cf06b15ea2e4da51f3800167399865a5a8a97acb3b5d923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf16927c3853816ea558f7d03597f9b476800a2b90e13eeaabe1cb3398c359e`

```dockerfile
```

-	Layers:
	-	`sha256:bda2335b18f6e55b72370e71519c9264a7242575f36274b66ea0beef37fe4d42`  
		Last Modified: Tue, 21 Oct 2025 09:38:47 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58e05b6dde8185c46fb895cadca3e7f80ce784f5f65ab177660e12a5d773c009`  
		Last Modified: Tue, 21 Oct 2025 09:38:48 GMT  
		Size: 15.2 KB (15196 bytes)  
		MIME: application/vnd.in-toto+json
