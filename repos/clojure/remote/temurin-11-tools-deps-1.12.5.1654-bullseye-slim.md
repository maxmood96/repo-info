## `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:13b8d4597f6f0b3129b34b1b6b4a8294a0f56ccca6d9cfa58f8a5501ab90fdc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:071cdb06e74afc44ae4a8e3d63804205a213e4dc62bdc126af61dc442b1a32a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232247233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c36e8fb9389d8bddfe4ac8e7f78465a066990194d88d26c39b26d8365774f0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:18:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:18:03 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d46573f32216931b92c2dfa694378edc914e8faeedfd2b2a082788043529a1`  
		Last Modified: Thu, 11 Jun 2026 01:18:38 GMT  
		Size: 145.9 MB (145886219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be64934ccbb1da67b94ec4c682535a10e2f3db695181e5f3af4e3ca2905bb4e7`  
		Last Modified: Thu, 11 Jun 2026 01:18:34 GMT  
		Size: 56.1 MB (56100113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a83d20086aa49b5f17c9c27582c604253baafe0f67b134f30f0c74bb0654cf`  
		Last Modified: Thu, 11 Jun 2026 01:18:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c3c58b9d66ba6510ced6143fb960a231f375bbd031b97813acc9c2ee77be0757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c15b573f4669572b1f817eb40324dd9a2d8e294965f9da1c45c8e05afac29a`

```dockerfile
```

-	Layers:
	-	`sha256:095bcf73733f886727b17bb396e858862d5b6f05e3d0587bfbc3cbb085d7e4c9`  
		Last Modified: Thu, 11 Jun 2026 01:18:31 GMT  
		Size: 5.3 MB (5337365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d82edc52f9c530be502c081cdab92d67ebc980bfd8628ed088b791484ebfccce`  
		Last Modified: Thu, 11 Jun 2026 01:18:31 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:facf339d85c403fa54ca400f83e2b6aeb4fc842e3dd9c72d4c0196273656d0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227596523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7205d8a3ecebf40c54e6a22d3cd4623d06321b3bff391cf6a01a822e474eb84e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 00:47:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 00:47:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:47:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:13 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72e6892d5213c368aee6116d4bdc0001aeedce6cb5be69e135100b8ffc53098`  
		Last Modified: Thu, 11 Jun 2026 00:47:52 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9874a8ef41a5657e5f07d9539e26251d4d7a2d4fd5997f9fd4afe7c444ed355f`  
		Last Modified: Thu, 11 Jun 2026 01:22:18 GMT  
		Size: 56.3 MB (56267497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7212bc370455a2d1e99b045e97c20a7b94a2877e59a65fd1a8ef775c5049a4`  
		Last Modified: Thu, 11 Jun 2026 01:22:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:455dae5da344c723cbee990c445af14370bbd9da6403d176657e3f818ea5e901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5357298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2ac78639963c415050cb18600a3aee44e79ca75324192435940be835784492`

```dockerfile
```

-	Layers:
	-	`sha256:2eb5ae44dbbf0ab51d9cf94d696b2cac3b297ee847543c224d4e421dfe261ff8`  
		Last Modified: Thu, 11 Jun 2026 01:22:17 GMT  
		Size: 5.3 MB (5343715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93345b9351cfd05a623a2c62a93760a3b86dc04fcea8e64b114fb53d944f92cb`  
		Last Modified: Thu, 11 Jun 2026 01:22:16 GMT  
		Size: 13.6 KB (13583 bytes)  
		MIME: application/vnd.in-toto+json
