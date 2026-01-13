## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:3dc51f9dd1a1dc3c46bba4e85d75144fa673abe29cfdc3014fcc2e890042ca5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c61ce379b28a339a6d449af0e7000d95ba2a751a8e983d7786c372881984436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c9043c4b79be72266d843fd5ce60b4683fd3229edcdf0ae36fc867cf9f0001`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:28:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:28:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:28:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:28:11 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:32:17 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:32:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:32:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:32:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:32:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:32:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8362581ec721b649ef56b4c0eac8fcd6f1c674076d0048e3a8c91af545dfe7b5`  
		Last Modified: Tue, 13 Jan 2026 02:29:23 GMT  
		Size: 144.8 MB (144847890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7457a35f77d757654916be4fe2e289f5a365aca58beabe8e5ec62e08c2afde9c`  
		Last Modified: Tue, 13 Jan 2026 03:32:57 GMT  
		Size: 59.1 MB (59149814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaaa44c403a7a8c8d56076a7e36633ca9b3a95c17fc4e5fdf33750fd37b7af2`  
		Last Modified: Tue, 13 Jan 2026 03:32:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6208d05e28f5d2d457fb2a9e05b55678e25c627242cbd48bf7a6940401998e5a`  
		Last Modified: Tue, 13 Jan 2026 03:32:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c01eaa53e76ea6337b6cd0b972c1e323e944a6e03be45eba67ef26ea757dbdad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8289abfd147cd1c5c2632d05c742432c2447ffe468fe8b407d8122ad1e46ecb4`

```dockerfile
```

-	Layers:
	-	`sha256:6dae676d772a6d9dbb114ebcf71d23d976998b2910caa75853f378b4a2070735`  
		Last Modified: Tue, 13 Jan 2026 07:39:44 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a375af358ddc7f5b3f12e713804f4d4e2e5952d225ef77dbb0a597e652ed3a10`  
		Last Modified: Tue, 13 Jan 2026 07:39:45 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f74d1105c7d8f46600836c4f8d317063728ad1e2855c59d43e2ebafb22d9506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231713570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2a403fac52260d27abba171cd251e74c1a4daa42c087a3f61a4281d26a01c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:32:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:32:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:32:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:32:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:36:02 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:36:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:36:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:36:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:36:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:36:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4963b13a3a2bfc94413072ea575989a217e29d963bf274b19eb915056c541034`  
		Last Modified: Tue, 13 Jan 2026 02:33:58 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5488f9d03c9a45836ada004985f7ef72e45d362467f5a11aa9f9f415ee3fe92`  
		Last Modified: Tue, 13 Jan 2026 03:36:47 GMT  
		Size: 59.3 MB (59284092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439bc4e4d6ab0c3481566050acd9cb5d6594add376809be2c4cb95dcca2133a`  
		Last Modified: Tue, 13 Jan 2026 03:36:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ec18c3dfd5423fdd2a1a9bff058035bbb86c40cbd05eb16ea169cbe7d43df`  
		Last Modified: Tue, 13 Jan 2026 03:36:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c31cb8426baa9dc340105ae9d0ff9e2ddf3b6572d456ee981882754a47a54273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ff3a824974b8ff39390e1cc2f0f99298734a188eafe23bf6ba38503e818213`

```dockerfile
```

-	Layers:
	-	`sha256:5fb82a6e688b869b290b030bcd74e8e7491d13f3aff21903f051acf932d4cc18`  
		Last Modified: Tue, 13 Jan 2026 07:39:49 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a77b63e6ecb24d9aaf9a92cd14248a7dfc31fbad334618631882f21afed3a57e`  
		Last Modified: Tue, 13 Jan 2026 07:39:50 GMT  
		Size: 15.2 KB (15153 bytes)  
		MIME: application/vnd.in-toto+json
