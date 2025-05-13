## `clojure:temurin-24-trixie`

```console
$ docker pull clojure@sha256:c6e595bf7d27c8d8ac8495d89f05bfe785af1233187cf5587e31aa78955c83e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:5e1dfad9f9f4c4af0c1bef43e0b37d683de8198ed1db41833164913dae9627e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224461590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd021eb3f8df5dca3eb1fb1a80b142678d315a04793f35242f5493adad27f70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Mon, 28 Apr 2025 21:08:35 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543a4cc9777670296712f6a9872398e4d4ea99fbbc7cd6c8fc0c4b43902d72ce`  
		Last Modified: Tue, 13 May 2025 17:53:57 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4c43acec6a5a14bcf292c352792edda204cbfef0daed639326286a116e4b6c`  
		Last Modified: Tue, 13 May 2025 17:53:57 GMT  
		Size: 85.3 MB (85260312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7270013e05b5cac053745640ed655b033f02261e8fa2683f2b006c91f73eb18e`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be32e4c36379a1cb8bd32c0dc6565db5837d4835e62a64254753212717467358`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:124a9e901c879b014e8e544344ee9fedd861c76ceaeea49c8c2787fe4e45ddc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543dc3ec3d785bc375b366a22d221de94520ac328dbdab1d9b4e3daa81d9bca2`

```dockerfile
```

-	Layers:
	-	`sha256:e3bf3a8cedabe4cdb2dd07ca0297c94f776df1fb955757263d3b99e3d9d0f8a2`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 7.2 MB (7219815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa1f860a64e37173d89d6174d6a6ad1de31ea82b335412e8d94356c7f907a646`  
		Last Modified: Tue, 13 May 2025 17:53:55 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6f9283832c1d61df310cffec350f24396a16a2001d2b859c65d955a03c2231e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223888708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c33f1ad1a9b21769d2871bf35907f5736ae050ce7a0ec6eb0d352435c5874db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
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
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd3f46f8509be2e8269dbababafabf79f4ab8c9edb9b2e5e44756fabe24b705`  
		Last Modified: Tue, 13 May 2025 18:08:31 GMT  
		Size: 89.1 MB (89091184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423c8aa892fe9ff225a339615390a338b2061d7647d02f39c6e49756f80f9627`  
		Last Modified: Tue, 13 May 2025 18:10:41 GMT  
		Size: 85.2 MB (85172361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9235a887f968cf63713413b1d005ec7402acab31935306531d5172504b16193c`  
		Last Modified: Tue, 13 May 2025 18:10:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8f23d04e9cefce7666521476d866892cd38837a9bb30f867bd6975481ae525`  
		Last Modified: Tue, 13 May 2025 18:10:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f149abd302d7c820443711f36987af4a10745fb734940db576f6771100094e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7242750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39319440ce21fbe0e698569477489300418fadaa8e2470d528ea52776857c184`

```dockerfile
```

-	Layers:
	-	`sha256:d5cad05005a40077865a1314d75ae147a5030a8e78f9cb20a8419e2b76e72ad2`  
		Last Modified: Tue, 13 May 2025 18:10:39 GMT  
		Size: 7.2 MB (7226842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b168cbf6f6afdcecd2277de5d15dacbcae1a14020a5422e2d02e378dd0bae6`  
		Last Modified: Tue, 13 May 2025 18:10:38 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
