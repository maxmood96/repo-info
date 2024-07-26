## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:a13cddea4e1d62393b553ee212b027d6a3baac4864e59cf535e01ccbf8a5caa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:974d699e837fd1c331c8aaa1fbdf4d1c018bbdfb92fc520cdea71880de40f40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248632961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50625edabd7bc7a5020bde6ce77fab4725e8e553c34270f56dd6e1f0e637d376`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bad5124545812483359d2b92003e7c1fd36036bff0227300c4ce65035490bb`  
		Last Modified: Thu, 25 Jul 2024 19:05:27 GMT  
		Size: 158.6 MB (158579312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2488395d337a97b7882df3360c7eb6dd714cd3d45e2a93dff06d654dbb720596`  
		Last Modified: Thu, 25 Jul 2024 19:05:26 GMT  
		Size: 58.6 MB (58624275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002f551bf407787ebee85b6aebf42960f07860683bf33bac18ce624af541087c`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd25162512537eabededa7520dd5ecb29ac8b5dead137407ec52899063f77f46`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2187e1a04856a133a3d9d493f234c99c3239c9e9ce5f274fd0ee3c3a214f4722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a710be33e72b6b5732267798b367ffed5895c289a0a97f020ddd5de15eb3c7`

```dockerfile
```

-	Layers:
	-	`sha256:b8b24232564777f7201510f4791247ebc7d4174d9e40734bc8fab0b16fbc6445`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 5.0 MB (4950532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de9e7be9933e27f04fa5fc7a1560159ca232ab1effffef4bbb60ad4c9fcc5729`  
		Last Modified: Thu, 25 Jul 2024 19:05:25 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2537c2c3566b7c0c2aadd9b7022459b4d617a2b4d4bbb1c4a5c4ec275cc0e2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245567190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2a7553ef495dccd7b7448f22c0fc0a8835dc8f152ff8b53b438fdc30739407`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1809c9c43cb8a5d38ddcdceca82616c1c0ce8b228c7a20f60893aa6dad9b1104`  
		Last Modified: Thu, 25 Jul 2024 21:19:59 GMT  
		Size: 156.7 MB (156746183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291158d88d64767bd0386948d5f02b3755d0a835c4b35908a988755d66a9aa0a`  
		Last Modified: Thu, 25 Jul 2024 21:24:34 GMT  
		Size: 58.7 MB (58743880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f64fe9a5aecf5ac616973a4748d48aa06293a648ccb089bb07e145bf8dd1945`  
		Last Modified: Thu, 25 Jul 2024 21:24:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667c8077f132abc9ad4898e8f77dbb8e70fa94e9d29104b84703c3208d28275c`  
		Last Modified: Thu, 25 Jul 2024 21:24:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22dbb293945ea6cc3d979a412a538cc74af0fecee0b3aefd05e98c508ce52a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d27e7c47bb1a6bcf680061a1f9a6911d25646b745294be6f3b85d98eaf9d746`

```dockerfile
```

-	Layers:
	-	`sha256:355852fbff6525da0f5a8e0888a0a3db652202a49456419a7147c3007580ac74`  
		Last Modified: Thu, 25 Jul 2024 21:24:33 GMT  
		Size: 5.0 MB (4956912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc666c9c3b17e53615f33de52d1edde13e2c59f884a17e7764cc7b2d5683575`  
		Last Modified: Thu, 25 Jul 2024 21:24:32 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
