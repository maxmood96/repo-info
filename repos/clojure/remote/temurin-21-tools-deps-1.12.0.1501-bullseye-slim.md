## `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim`

```console
$ docker pull clojure@sha256:d236a1b2a588871719ce97ee1f8aa77abd4e0dd2abf9e7ecb8f3887e2c73e509
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:634f2cafe88c6677d96509bba098b47d205570c86e7fbb602555af6b5757b857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246610247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4373f3e63e4d5df3dffca72f93a3e7e8f8f85fa9e672f0faaeb60ecba098a35`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da7e899f12f36f8979c739dd84b9112e24612f0411521d1257b8c497beb5f2`  
		Last Modified: Wed, 29 Jan 2025 20:27:53 GMT  
		Size: 157.6 MB (157568696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8deaa2af65db15ffb7922f890e4fe0dfa6a8e1b46945bbf498770d38d6c2c2`  
		Last Modified: Wed, 29 Jan 2025 20:27:52 GMT  
		Size: 58.8 MB (58787844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9753910450a57011124303246be6d46686c28505964c854be34dd9f9b2212057`  
		Last Modified: Wed, 29 Jan 2025 20:27:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b1996fcdd329fb475f21a12bd15f1ad599e2275557f6bc47dc7e4d9e0c86be`  
		Last Modified: Wed, 29 Jan 2025 20:27:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0afbf842eead83997f7142e76dba96ed7c524bc7c4b59e87603c25b3da9974b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3675638620d1bcd4a32ba9e1baddc4036f8fe11bd031239cd2c0a70fcb71934`

```dockerfile
```

-	Layers:
	-	`sha256:e2a63fcb49e1375e0c519eeab85b13790c865e71fdc25c4b223cd31332d68d76`  
		Last Modified: Wed, 29 Jan 2025 20:27:51 GMT  
		Size: 5.1 MB (5120867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88c766783010c9cd21363e24f79d5c8d33c70b9b2e511409a19c461fa85ee078`  
		Last Modified: Wed, 29 Jan 2025 20:27:51 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65f2773f13ba1eba1c4af7b34c065a200447100646eba3f00c200060895b88a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243448105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad28ccace4e238f996ee2bf436862e7c374b5f9f2909bf9944575f5efc93db2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55539c7f273509ebef282fa1d891a4509c722ccc8a21bfa5ea9e1bac67e688f`  
		Last Modified: Thu, 23 Jan 2025 02:56:29 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0a2396ea90a4bb8b117ff60adadc658c602349905217d870f4c0ef0ce788b`  
		Last Modified: Wed, 29 Jan 2025 20:55:15 GMT  
		Size: 58.9 MB (58909081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa0a3ca81613a6ecf40e5c9361cc92e45f5bc60df23528c7dad2fcc26c6dba`  
		Last Modified: Wed, 29 Jan 2025 20:55:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0102ae2ab78f49340fa0b1a987f8840094c907198d2e9dcbcbe5fb057f383c20`  
		Last Modified: Wed, 29 Jan 2025 20:55:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1321c5775579c9ce166abe13703497945065edaef7ee50fcef131bbf70d4e252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae6eb19c26eb0a7f82968d5ba0b6f9dad507d4a9895f645035eb17fff010444`

```dockerfile
```

-	Layers:
	-	`sha256:447cd1f8d2a383a6abe7fa960a329e3eb6c4551408b9e9559b759f50f22341fa`  
		Last Modified: Wed, 29 Jan 2025 20:55:13 GMT  
		Size: 5.1 MB (5126623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fa3a1a8c03c3c6fe4d0a6fd8b86e8692b92d41c11cdd82afd47d63aecec3d9`  
		Last Modified: Wed, 29 Jan 2025 20:55:13 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
