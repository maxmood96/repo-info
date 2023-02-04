## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:08a35d0059f3325e14bfa22ee4df118ed2bd10de2ad7028684dbd64140e18b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cc00020433e8a08bc9875e42819cc339609483d4b2c41f381524b93a9b2474b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285319199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4be0278e4e01efc399e0c44b6061afb6c5c581c5768eaa2023cc0fe42d375d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:06:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:12:04 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:12:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:14:00 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 14:14:00 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:14:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 14:14:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 14:14:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 14:14:18 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 14:14:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87fb4ccb46beb33988288373afc1f2c97de5052711ef02009468a1bea691666`  
		Last Modified: Sat, 04 Feb 2023 14:24:01 GMT  
		Size: 192.4 MB (192438215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d1290f746a7faa4146af41768a004320044fba79d7360d9153ee5b4d9f6631`  
		Last Modified: Sat, 04 Feb 2023 14:25:08 GMT  
		Size: 61.5 MB (61483050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d0807e8fcd6d0a0c8c0d5f598b59c9b53f9ff4e861efde03cc8ee9ccfa4d41`  
		Last Modified: Sat, 04 Feb 2023 14:25:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deadb51a92294c3f39215dc3f30e894b63eba2351e08c67a31f82d694723a7d1`  
		Last Modified: Sat, 04 Feb 2023 14:25:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f691eada2c35dff4ee7b5875596af24d62459cf32640f76f70f4b69dfb582a34
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282903513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff815d3b11ab28221d03fce117f58bd35bbbcd647a0cf71007972197670d574`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:44:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 08:44:47 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:08:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:09:55 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 17:09:55 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:10:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 17:10:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 17:10:10 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 17:10:10 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 17:10:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3e25b707e39161f4cf1a28cf3bd4a0ec84bd0f2c93f699a34dc6dd1715cd62`  
		Last Modified: Sat, 04 Feb 2023 08:46:51 GMT  
		Size: 191.3 MB (191260441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282990698842fdd62deef9914955581272178b7f02d6d65f76953302c7a098e1`  
		Last Modified: Sat, 04 Feb 2023 17:19:37 GMT  
		Size: 61.6 MB (61597263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa125d814986ea54cccf74a8ad155c3666e45a755ddbe0eb10011cb888a1cc38`  
		Last Modified: Sat, 04 Feb 2023 17:19:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b314af79a5f1e4b5001807e08504d35e34e4a734773804b7eb3ac1195f69bfc6`  
		Last Modified: Sat, 04 Feb 2023 17:19:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
