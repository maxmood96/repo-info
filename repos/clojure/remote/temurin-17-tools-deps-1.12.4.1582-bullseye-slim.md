## `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye-slim`

```console
$ docker pull clojure@sha256:f10316e8951a012a9b886fcb7c03923a5c3f51b62380686140fc56a0eee1c972
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9a6f93f60d59e97e11f40192983fa62f4b5af8df68e9e1d18a587400a820db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be59e5f4a10b20439d967d32b3a4aedcfce10bb3169bc2698d48de2f879c48f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:38:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:30 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:38:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:38:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d64da4c392abad4a99093a64e66e8581b257455a88c6938061a4783adaf472c`  
		Last Modified: Fri, 12 Dec 2025 19:23:28 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e9e337a721b1ae8b5cee1c2fbd299ccc42887236822cd30958b52aa6fa7aa0`  
		Last Modified: Thu, 11 Dec 2025 22:39:18 GMT  
		Size: 59.2 MB (59150079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cebf9e82532512bbe26c2d6a6455bf045b91361722dbe9867d2198d90882de`  
		Last Modified: Thu, 11 Dec 2025 22:39:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214b3e9a9bd32d2366dc99d15051a0ac99dd5393afa06d9149abcd92afae5684`  
		Last Modified: Thu, 11 Dec 2025 22:39:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0012bd4b0f12448b5c370c603ece46800b271833d31dad9b243802e88137a679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5c2cbd2c0d4fc3dbd2427d95ef4a008dadcca8a6cc5d756745a5b7b839e4cb`

```dockerfile
```

-	Layers:
	-	`sha256:7ca8ab82c6b6d7999bfe8005091443d6d008c1c67a64502fa7719cfa79243c0f`  
		Last Modified: Fri, 12 Dec 2025 01:38:12 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870a189cea3059f18eb76b27ef5d9e331a9894077ee99e938b485adfd10c0e38`  
		Last Modified: Fri, 12 Dec 2025 01:38:13 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d5aab0fd3cbd8ddb91e7ff298f713cc3e15f87c3db69bf93cc8def6db147ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231714063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4ccfd3b4fca0b8de7a0e8ba259d15a6fdeab45ed7bfaf673efb4a7367f0ebf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:39:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:15 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4beb495072dee11f669b03f7ac5ee81150ef9cfb6322073504562cf0dda18401`  
		Last Modified: Fri, 12 Dec 2025 19:24:16 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661b1b7f0b5788f39b3c9a77e1c6f54fab8bff466edc365ae138c9920b671234`  
		Last Modified: Thu, 11 Dec 2025 22:40:02 GMT  
		Size: 59.3 MB (59284624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4037e91e8a7fb402f601b0e3bd1012eba70fa187bc8afd47977b03da88973b5`  
		Last Modified: Thu, 11 Dec 2025 22:39:55 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da42e31f32df7dfeab27e1088a8df80562904eb16a08eaad81330c0cd97a2819`  
		Last Modified: Thu, 11 Dec 2025 22:39:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1afca12ce38b1a3c60c29dccf31e646a4f975333c7c0082c9698b0ee92950b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807faeb7e4e5cad78f2770dcef87aa11d141e6748cc2c83937320026c75a9a09`

```dockerfile
```

-	Layers:
	-	`sha256:99ea255453fc1f6022b8cbafa1df15ce4d990791ce212c7f34b3d2e38d4ceda7`  
		Last Modified: Fri, 12 Dec 2025 01:38:18 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4af9a5bc6d952d68f8242a036ea97e1cb21ee1122f32623615847ec69f98dfc7`  
		Last Modified: Fri, 12 Dec 2025 01:38:18 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
