## `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:20933d21f68016a4d29062a56411ae0e75e3d3914fba8e5be6e1b0d356bd6469
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cc46462067d4740730dc91208f9289f8a84dd962f592afb0edbedf8d012998d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254304959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a2776bbfa5b9d06bdab9d1d3d8ee1d8b6fe4a8bd0662c3ad6d6e5dac0b2a5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ed10d0647783c33ead6a3ebda02b1e5bfebadafc4da9ca50b866c2c4635bbc`  
		Size: 165.3 MB (165295092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bc1995721921f774e14f1acdb846e02771819c38e8f2078afeb6c8e565ca1a`  
		Last Modified: Tue, 24 Dec 2024 22:39:21 GMT  
		Size: 58.8 MB (58756181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fe46dd2e4bdbb1a4c457f37c475a362356923662548af20614108c278c987e`  
		Last Modified: Tue, 24 Dec 2024 22:39:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2cee38f6f8b14862819fef59ca9e705103ec84f9370d812b6adbaa95cb3af4`  
		Last Modified: Tue, 24 Dec 2024 22:39:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c461f1c8eb8164724736fe09dcee61306ced6cfe4e2423966e2073bcbf418c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a2349601ec967927a37b119637f3112bd01ca2b88b36e7b4573c3673597b99`

```dockerfile
```

-	Layers:
	-	`sha256:4c3542db63608bf2f12bf37ff845b16bfe8c94b89d3b4c94192e725a40814484`  
		Last Modified: Tue, 24 Dec 2024 22:39:20 GMT  
		Size: 5.1 MB (5122012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b1d4db5a94a52a4ffa072abce45749b32bc568f92c10055c129cdb08b8a49f`  
		Last Modified: Tue, 24 Dec 2024 22:39:19 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3d93cd6df49f5b39b4cca48c38eb8d20e9e3e5f376837959940995f6d7c6d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250908076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed76453d8a884400256312c9eeacd1bf6654623abc0a1e384a58df944d19c75b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b4fb805b80b71c3e0694a62a0807be3fbcc30b4f67cf6fa8370c3421f0982`  
		Last Modified: Wed, 25 Dec 2024 07:39:53 GMT  
		Size: 163.3 MB (163281786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9902af53b04bf7cc99ca0c3bb745814f2bf48c411b1df5d7e3f4f326ecfb132`  
		Last Modified: Wed, 25 Dec 2024 07:42:44 GMT  
		Size: 58.9 MB (58880399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9203937e686b5e7dd93e48bc4cb1e9a0fe4ef38edbd8cbfd3fc75d398373af85`  
		Last Modified: Wed, 25 Dec 2024 07:42:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43655f12ace35e655666e6f65c087e50cc15ad2e6e53b860f0abb9120261901c`  
		Last Modified: Wed, 25 Dec 2024 07:42:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f9ab47675b5faea01984ae3c962d0a54cc2d494d0f035f930f77a1e0800689f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb50f82ea85151597d9dd87713a3e3a4f7cc3caf1d024715530ab6e973a79d5`

```dockerfile
```

-	Layers:
	-	`sha256:0d4c4e857ca59a3596f7ea496663a4d830e0015063393a652e5b33b19951418e`  
		Last Modified: Wed, 25 Dec 2024 07:42:42 GMT  
		Size: 5.1 MB (5127123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06d89b9845cc6ba5c71805ef55f4ec889e9f40364fa5b2a9b2b4c9310c3b34e4`  
		Last Modified: Wed, 25 Dec 2024 07:42:42 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json
