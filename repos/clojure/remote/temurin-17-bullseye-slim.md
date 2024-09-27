## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:778c81d506441ada8c0b5bca3cbd6feca6f4568d10bc7ff202ee09975bedcd4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f30f72380fc9decb7eceb478f29cd27b237140d44dfa731035ff3bf07ff03e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235536332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60258a961991984326afb8da17bc04afa569652f98149ba2bf40e4661a46cfc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3f8098417d4e58edb1d793501c273179d6a66ae1f757913927a37037046fe2`  
		Last Modified: Fri, 27 Sep 2024 06:01:20 GMT  
		Size: 145.2 MB (145166532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605212cf615d3d44f8e6585bdafb79867521ba17bf8a6d100caf77be7cc0930c`  
		Last Modified: Fri, 27 Sep 2024 06:01:18 GMT  
		Size: 58.9 MB (58940164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f74762e1fdb213f4303ad47c295165f81d9e9ebd0027a0448943e8f13850cf`  
		Last Modified: Fri, 27 Sep 2024 06:01:17 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1fd34dbed73be1d8fb7a2e6f87e0ef071b6eb180e73ee8402dbcaabb60d3e`  
		Last Modified: Fri, 27 Sep 2024 06:01:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab8a00f3640c6a990d2402cd2e24e1057455b8df5bd36bbc0fda73b935aa7603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5114322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7178cb3c145ba0ee34f53ee9f6357aa56897c68cbbc590402dbaf973171b87cd`

```dockerfile
```

-	Layers:
	-	`sha256:808086fd30a496e9a3ed4986bdbda530b6a4304f1d2d0f3f28c3263a7c4f013e`  
		Last Modified: Fri, 27 Sep 2024 06:01:17 GMT  
		Size: 5.1 MB (5098809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a8d8d3d3ecf92a811c40de0fecdb3f89d2ee07849ecb0978ae544ebe2f4224`  
		Last Modified: Fri, 27 Sep 2024 06:01:17 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fff623afa0052fa2f05a2bc1b3473ee82900f2c2f032456161736120ba5211a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233106681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f6fa523eec4f45b43ac465bbed52557bb64cfdb03419b40b5d42b23ddca704`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef65a68f4c97f7ff7a0f9db0bea71f2058e85f0e6f0aab1a2de311ee49382ab`  
		Last Modified: Tue, 17 Sep 2024 04:33:50 GMT  
		Size: 144.0 MB (143959494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6c86fa66cac8e7ec56395777a6022a575a1d906b2840d711bf90c64a9a5c62`  
		Last Modified: Tue, 17 Sep 2024 04:39:00 GMT  
		Size: 59.1 MB (59071775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9f1bf16c9cec8db523339afbee545cfae683eb73b842bde8722d60cfb42b78`  
		Last Modified: Tue, 17 Sep 2024 04:38:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc618a6ca0cd86bdd5c65d388220566cd7f4dabed30c17b718e1242ae35aeb79`  
		Last Modified: Tue, 17 Sep 2024 04:38:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af66447594ffd5543da42f1ade6bc0420fbd2d9d8e93e05d4d6b3a3b86e8fdf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e357c2aeb80203507dd3ee4f04ea11bb0080cf1cf9ed6fd36b9764d996c2da28`

```dockerfile
```

-	Layers:
	-	`sha256:2a81078803b7cebc519d8da5144d1d209737215e6f0342c5713670eca3ec7891`  
		Last Modified: Tue, 17 Sep 2024 04:38:59 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13f43333fa50ff9fa82d58c3de7a2302db3f09d979dd71a63e5996aecc668c2`  
		Last Modified: Tue, 17 Sep 2024 04:38:58 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
