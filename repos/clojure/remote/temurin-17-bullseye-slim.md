## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:3395aa22c9e0ef4fc5d6975a642e5d357a4f029b3c910676c0a8ecae76771068
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:66af64766e7cc22a6792f52316c9832ba904e3f8bb123aa614e5939a917ed26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639682a76f2650d5cfe8b7a564186f9b48b0fce94b07aaa746f1a5e79f4bcefe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:00:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:00:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:00:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:00:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:00:26 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf73e9da6b8b4321b6d5293c69535afcfc7e64e3e386926a12ca3161d37df87`  
		Last Modified: Tue, 30 Dec 2025 01:01:21 GMT  
		Size: 144.8 MB (144847979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083789e80846f3256d71512b96f0342ad9f0026c004330c93ce0fc7d741f4f94`  
		Last Modified: Tue, 30 Dec 2025 01:01:16 GMT  
		Size: 59.1 MB (59149911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a1bed5af49e458e913141a67612d0518b9de6aea2057e1fed62145071602c`  
		Last Modified: Tue, 30 Dec 2025 01:01:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464179c3537a2e1e12fd3cf8f81b12ad73752940fde9d8c84fa99ec387d7ed1e`  
		Last Modified: Tue, 30 Dec 2025 01:01:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b34f52651bcf46de87abb73077d1bf380ef7eb91f9de09ff21ba3dc3be91b9dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a420b1246ced407c25cc6ce55e0b834bd9e38ede16026bb2095e58d60f0439c`

```dockerfile
```

-	Layers:
	-	`sha256:b034355492fd84348c5a256044838f03f819274c956e7c719b36f87a8614800a`  
		Last Modified: Tue, 30 Dec 2025 01:36:02 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56fdda78326e4c0428de84bdba31a894acbe334c533697e4b707d5a5c217d6ca`  
		Last Modified: Tue, 30 Dec 2025 01:36:03 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

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
